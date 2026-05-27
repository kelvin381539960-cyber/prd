# Deposit Address 充值体验优化 PRD

## 1. 项目背景与前置条件

### 1.1 背景

当前 AIX 存在两类主要充值方式：

- Binance Exchange / GTR
- Connect Wallet

其中：

- Connect Wallet 不提供复制充值地址能力。
- 大量用户仍保持行业通用习惯：复制充值地址后，在外部 App 发起转账。
- 用户因此会进入 Binance Exchange / GTR 路径复制地址。
- 但 GTR 当前仅支持 Binance 来源。
- 当用户从非 Binance App 发起充值时，可能导致 DTC 不支持、拒绝或进入异常状态。

当前问题的核心不是“缺少 Wallet 入口”，而是：

> 用户将 Binance-only 地址误认为通用充值地址。

本需求目标是降低该误用行为导致的失败率与异常率。

---

### 1.2 目标

本需求目标：

- 降低用户复制 Binance-only 地址到非 Binance App 充值导致失败或异常的概率。
- 保留 Binance Exchange / GTR 路径的复制地址能力。
- 为灰度用户提供添加发送钱包地址白名单能力。
- 保留 Connect Wallet 路径，不新增复制地址能力。
- 优化充值入口结构，降低用户对 Wallet / WalletConnect 的认知混淆。

---

### 1.3 非目标（Out of Scope）

以下内容不在本 PRD 范围内：

- Under Review 交易详情模块。
- DTC 风控中资金处理逻辑。
- 客服话术。
- 非 Binance 交易所充值支持。
- 交易所地址自动识别。
- Connect Wallet 主流程改造。

---

### 1.4 依赖与前置条件

- DTC 提供白名单添加接口。
- 白名单添加后立即生效。
- AIX 支持灰度配置能力。
- AIX 支持根据灰度开关展示白名单入口。
- DTC 当前不能识别交易所来源地址。

---

## 2. 全局规则（合规 / 风控 / 限制）

### 2.1 充值方式规则

| 充值方式 | 用户动作 | 是否可复制地址 | 来源限制 |
|---|---|---|---|
| Binance Exchange / GTR | 从 Binance 转账 | 是 | 仅支持 Binance |
| Deposit Address（暂定命名） | 复制地址后从外部 App 转账 | 是 | 仅支持已加白名单的个人钱包 |
| Connect Wallet | 连接钱包并确认转账 | 否 | WalletConnect 支持钱包 |

说明：

- `Deposit Address` 为暂定命名，最终命名待产品确认。
- 不使用 `Personal Wallet` 作为正式入口名，避免与 `Connect Wallet` 认知混淆。

---

### 2.2 白名单规则

- 白名单对象为用户外部发送钱包地址。
- 白名单仅适用于个人钱包地址。
- 非 Binance 交易所不支持。
- 用户未添加白名单时，仍允许复制充值地址。
- 白名单添加成功后立即生效。
- 白名单启用依赖 DTC 接口。

---

### 2.3 灰度规则

| 用户类型 | 白名单入口 |
|---|---|
| 正式用户 | 不展示 |
| 灰度用户 | 展示 |

说明：

- 正式用户不暴露白名单能力。
- 灰度用户可添加发送钱包地址。

---

### 2.4 风控边界

- 本需求不改变现有 KYC、AML、制裁、限额规则。
- 本需求不改变 DTC 风控逻辑。
- 本需求重点是降低错误充值路径选择。
- DTC 无法自动识别交易所来源地址，因此不能承诺自动拦截。

---

## 3. 核心业务流程（主流程）

### 3.1 流程总览

```text
┌──────────────────────────────┐
│ User enters Deposit           │
└───────────────┬──────────────┘
                │
                ▼
┌──────────────────────────────┐
│ Select deposit method         │
│ - Deposit Address             │
│ - Connect Wallet              │
└───────────────┬──────────────┘
                │
        ┌───────┴────────┐
        │                │
        ▼                ▼
┌────────────────┐  ┌──────────────────┐
│ Deposit Address│  │ Connect Wallet    │
│ path            │  │ existing path     │
└───────┬────────┘  └──────────────────┘
        │
        ▼
┌──────────────────────────────┐
│ Select asset / network        │
└───────────────┬──────────────┘
                │
                ▼
┌──────────────────────────────┐
│ Receive address page          │
│ - Show deposit address        │
│ - Show whitelist entry        │
│ - Allow copy address          │
└───────────────┬──────────────┘
                │
        ┌───────┴────────┐
        │                │
        ▼                ▼
┌──────────────────┐  ┌──────────────────┐
│ Add sending       │  │ Copy deposit      │
│ wallet address    │  │ address           │
└─────────┬────────┘  └──────────────────┘
          │
          ▼
┌──────────────────────────────┐
│ DTC whitelist API             │
│ Success: effective immediately│
└──────────────────────────────┘
```

---

### 3.2 充值入口结构

页面仅展示两个核心入口：

| 入口 | 用户理解 |
|---|---|
| Deposit Address（暂定） | 获取充值地址后，从外部 App 手动转账 |
| Connect Wallet | 连接钱包并直接确认转账 |

设计原则：

- 避免同时出现多个 Wallet 名称导致用户混淆。
- 不使用 `Personal Wallet` 命名。
- Connect Wallet 必须明确“不需要复制地址”。

---

### 3.3 Deposit Address 主流程

#### 触发条件

用户选择 Deposit Address。

#### 系统动作

- 用户选择币种。
- 用户选择网络。
- AIX 获取充值地址。
- 灰度用户展示白名单入口。
- 所有用户允许复制充值地址。

#### 页面行为

页面展示：

- Deposit Address
- Copy 按钮
- 灰度用户白名单入口
- 非 Binance 交易所不支持提示

#### 白名单行为

灰度用户可：

- 添加发送钱包地址。
- 添加成功后立即生效。
- 继续复制充值地址。

#### 限制说明

- 不支持非 Binance 交易所。
- 不承诺自动识别交易所地址。
- 用户仍可能误用交易所充值。

---

### 3.4 Binance Exchange / GTR 路径

#### 规则

- 保留当前复制地址能力。
- 保留现有 GTR 流程。
- 必须强化 Binance-only 提示。

#### 页面要求

页面需明确：

- 该地址仅支持 Binance 来源。
- 非 Binance App 充值可能失败。

#### 风险提示

首次 Copy 可增加风险确认。

具体 UI 方案待 UI / Product 确认。

---

### 3.5 Connect Wallet 路径

#### 规则

- 保持现有流程。
- 不提供复制地址能力。
- 不增加白名单流程。

#### 页面要求

需要明确：

- 不需要复制地址。
- 用户将在钱包中确认交易。

---

## 4. 页面与交互说明

### 4.1 入口页

页面目标：

- 让用户优先按“操作方式”理解充值。
- 避免 Wallet / WalletConnect 认知混淆。

页面结构：

| 入口 | 描述方向 |
|---|---|
| Deposit Address | 从外部 App 手动转账 |
| Connect Wallet | 连接钱包并确认交易 |

---

### 4.2 Deposit Address 页面

页面需包含：

- Deposit Address
- Copy 按钮
- 灰度用户白名单入口
- 来源限制提示

页面重点：

- 不支持非 Binance 交易所。
- 推荐先添加发送钱包地址。
- 不阻断用户复制地址。

---

### 4.3 白名单入口

仅灰度用户展示。

用户输入：

- 发送钱包地址
- 地址标签（待确认是否需要）

成功后：

- 立即生效。
- 页面状态更新。

---

## 5. 异常与失败流程

### 5.1 白名单添加失败

#### 触发条件

DTC 白名单接口返回失败。

#### 前端表现

- 展示失败提示。
- 保留用户输入。
- 支持用户重试。

#### 状态记录

记录：

- whitelist_status
- error_code
- request_id
- wallet_address

---

### 5.2 非 Binance 交易所充值

#### 风险

用户可能仍从 OKX / Bybit / Coinbase 等非 Binance 交易所充值。

#### 当前限制

- DTC 无法识别交易所来源地址。
- 前端无法自动阻断。

#### 当前处理

- 页面显性提示。
- Binance-only 提示。
- 用户风险确认。

---

### 5.3 未添加白名单直接复制

#### 规则

允许复制。

#### 风险

用户后续充值可能失败。

#### 当前处理

通过页面提示降低风险。

---

## 6. 状态机与状态映射

### 6.1 白名单状态

| 状态 | 含义 |
|---|---|
| not_added | 未添加 |
| submitting | 提交中 |
| active | 已生效 |
| failed | 添加失败 |

---

### 6.2 状态流转

```text
┌────────────┐
│ not_added  │
└─────┬──────┘
      │ submit
      ▼
┌────────────┐
│ submitting │
└─────┬──────┘
      │
  ┌───┴────────────┐
  │                │
  ▼                ▼
┌────────┐    ┌────────┐
│ active │    │ failed │
└────────┘    └───┬────┘
                  │ retry
                  ▼
             ┌────────────┐
             │ submitting │
             └────────────┘
```

---

## 7. 接口与系统依赖

### 7.1 依赖系统

| 系统 | 用途 |
|---|---|
| AIX App | 页面与交互 |
| AIX Backend | 灰度与白名单转发 |
| DTC | 白名单接口 |
| GTR | Binance Exchange 地址能力 |

---

### 7.2 接口依赖

#### 获取充值配置

用途：

- 获取充值入口。
- 获取币种与网络。

待确认：

- 是否新增 method。
- 是否复用现有 method + mode。

---

#### 获取充值地址

用途：

- 获取 deposit address。

待确认：

- Deposit Address 与 GTR 是否复用地址接口。

---

#### 添加白名单

用途：

- 添加发送钱包地址。

字段待确认：

- wallet_address
- network
- asset
- address_label
- request_id

---

## 8. 埋点与指标

建议埋点：

- Deposit method exposure
- Deposit method click
- Deposit Address exposure
- Connect Wallet exposure
- Copy address click
- Binance-only warning exposure
- Add whitelist click
- Add whitelist success
- Add whitelist failed

关键指标：

- Binance-only 地址误用率
- Deposit Address 使用率
- 白名单添加成功率
- 非 Binance 来源失败率

---

## 9. 验收标准

### 9.1 功能验收

- 正式用户不展示白名单入口。
- 灰度用户展示白名单入口。
- 用户可复制 Deposit Address。
- 用户未加白名单时仍可复制地址。
- 白名单添加成功后立即生效。
- Connect Wallet 不展示复制地址。
- Binance Exchange / GTR 保留复制地址能力。

---

### 9.2 风险控制验收

- 页面明确提示 Binance-only 限制。
- 页面明确提示非 Binance 交易所不支持。
- 页面避免 Wallet / WalletConnect 混淆。
- 用户能够区分：
  - 手动地址充值
  - Connect Wallet

---

## 10. 风险点与待确认事项

### 10.1 风险点

| 风险 | 影响 |
|---|---|
| 用户仍从非 Binance 交易所充值 | 仍可能失败 |
| DTC 无法识别交易所来源 | 无法自动阻断 |
| Deposit Address 命名不清晰 | 用户理解错误 |
| 用户跳过白名单直接充值 | 仍可能失败 |

---

### 10.2 待确认事项

| 编号 | 问题 |
|---|---|
| Q1 | Deposit Address 最终命名 |
| Q2 | 白名单是否按 network 生效 |
| Q3 | 是否支持多个钱包地址 |
| Q4 | 是否支持删除白名单 |
| Q5 | 灰度维度 |
| Q6 | Binance-only 风险确认是否上线 |

---

## 11. 落地评审摘要

### Product

- 本需求核心是降低充值路径误用，而不是新增 Wallet。
- 入口结构按“操作方式”组织，而不是按 Wallet 类型组织。

### Engineering

- 白名单能力依赖 DTC 接口。
- 不新增交易所自动识别逻辑。
- 需支持灰度配置。

### Risk / Compliance

- 不改变现有 KYC / AML / 制裁逻辑。
- 不改变 DTC 风控逻辑。
- 重点是用户侧路径风险控制。

---

## 12. 来源引用

- AIX 当前充值逻辑分析
- DTC 白名单能力说明
- 用户体验评审结论
- 《PRD 编写规范》
