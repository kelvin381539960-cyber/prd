---
source_section: Security / 7 全局规则、8 需求描述、9 外部接口、10 错误码；Registration BIO / Password；Card Manage PIN / Sensitive operations；Wallet Send/Swap auth
source_doc: archive/legacy-prd/security/identity-verification/README.md；archive/legacy-prd/app/registration-login/README.md；archive/legacy-prd/card/manage/README.md；archive/legacy-prd/wallet/deposit-send-swap/README.md
module: security
feature: password-policy
version: "1.2"
last_updated: 2026-05-28
authors: [吴忆锋]
status: released
depends_on: []
---

# Password Policy 密码策略

> Code alignment note: 2026-05-28 按 AIX 前端代码 `src/data/set-pwd/SetPwdRepo.ts`、`src/data/set-pwd/SetPwdData.ts` 补充设置 / 找回 / 修改密码的运行时可确认接口与入参。本次只写入代码可直接证明的内容；本文档第 2 节的最小/最大长度、复杂度、校验时机、显示控制等均来自历史 PRD / UI 规范，当前前端代码无法确认，保持原文并在 0.1.3 标注为不可由代码推导。

## 0.1 代码可确认的运行时事实补充（2026-05-28）

以下内容来自 AIX 当前代码实现，仅作为运行时事实补充；若与下文历史 PRD 描述存在差异，以当前代码和后端业务事实复核为准。

### 0.1.1 密码相关接口

代码可确认 `SetPwdRepo` 接口：

- `registerStep2(payload)` → `Urls.registerStep2`
- `initForgetPwd(method)` → `Urls.forgetPwdStep1`
- `setForgetPwd(method, newPassword)` → `Urls.forgetPwdStep2`
- `initChangedPwd()` → `Urls.changePwdStep1`
- `setChangePwd(newPassword)` → `Urls.changePwdStep2`

### 0.1.2 入参结构

代码可确认：

- `RegisterStep2Request` 包含 `recommendTag`（可选）、`password`、`otpSessionId`、`dataConsent`（可选）。
- `ForgotPwdMethod` 为联合类型，支持 `{ email }`、`{ mobile, areaCode }`、`{ sessionId }` 三种形态；`setForgetPwd` 会把 `newPassword` 与 method 合并提交。
- `setChangePwd` 仅提交 `newPassword`。

### 0.1.3 不从代码推导的内容

以下内容本次不从代码补充（第 2 节相关规则来自历史 PRD / UI 规范，未经代码确认）：

- 密码最小 8 / 最大 32 字符限制。
- 大小写字母、数字、特殊符号复杂度要求。
- 失焦校验 / 实时校验等校验时机。
- 明文 / 密文显示控制与眼睛图标交互。
- 两次输入一致性校验文案。
- 后端对密码强度的实际校验规则。

## 1. 功能概述

AIX 全局统一的密码安全规范，适用于注册设置密码和重置密码场景。

## 2. 密码规则

### 2.1 基本要求

| 规则项 | 要求 |
|--------|------|
| 最小长度 | 8 字符 |
| 最大长度 | 32 字符 |
| 超出限制 | 前端禁止继续输入，Toast：`密码最长32个字符` |

### 2.2 复杂度要求（全部必须满足）

| 类型 | 范围 | 缺失提示 |
|------|------|----------|
| 小写字母 | a-z | `Password must include a lowercase letter` |
| 大写字母 | A-Z | `Password must include an uppercase letter` |
| 数字 | 0-9 | `Password must include a number` |
| 特殊符号 | `! @ # $ % ^ & * ( ) _ + - = { } [ ] \| \ : " ; ' < > ? , . /` 等 | `Password must include a supported symbol` |

### 2.3 显示控制

| 状态 | 说明 |
|------|------|
| 默认 | 密文显示（圆点•或星号*） |
| 眼睛图标-闭眼 | 密文 |
| 眼睛图标-睁眼 | 明文 |
| 切换 | 点击眼睛图标切换明文/密文 |

## 3. 校验时机

| 场景 | 校验时机 |
|------|----------|
| 注册 - Set Password Page | **失焦后校验**（blur event） |
| 注册 - Re-enter Password Page | **实时动态校验**（onChange） |
| 重置密码 | 同上两种页面规则 |

## 4. 确认密码（Re-enter）

| 规则项 | 说明 |
|--------|------|
| 一致性校验 | 与第一次输入对比 |
| 不一致提示 | `Passwords do not match. Please try again.` |

## Source alignment additions

| 规则 | 结论 | 来源 |
|---|---|---|
| 密码长度 | 8-32 字符；超过 32 位前端禁止继续输入 | Registration Set Password；Security Login Passcode |
| 复杂度 | 必须包含小写字母、大写字母、数字、符号 / supported symbol | Registration Set Password |
| 显示控制 | 点击眼睛图标明文显示，再次点击恢复密文 | Registration Set Password |
| 两次不一致 | 提示 Passwords do not match. Please try again. | Registration Re-enter Password |
| 文案边界 | Set Password 页使用 supported symbol，Re-enter 页使用 symbol；知识库统一为 supported symbol / symbol，不自行扩展允许字符集 | Registration |

## 5. 调用方

- `account/registration` — 设置密码 + 确认密码
- `account/password-reset` — 重设密码 + 确认密码
