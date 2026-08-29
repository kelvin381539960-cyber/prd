# AIX Current Anchor（Step 3 直接比较用事实锚点）

> 状态：Completed（2026-08-29）。只读取以下三个已确认文件汇编，不联网、不扫描全仓、不引入新的历史探索。
> 来源：`evidence/02-agent-f-aix-current-position.md`；`research/aix-market-positioning/01-market-overview-and-user-jobs.md`；`research/aix-market-positioning/02-ecosystem-map.md`。
> 用途：为 Step 3 玩家与 AIX 的直接比较提供稳定的 AIX 侧口径。本文件只写当前事实与明确 Unknown，不做战略结论，不做竞品判断。

---

## 1. 地区准入：Wallet 与 Card 必须分开

| 维度 | AIX 当前事实 | 状态 | 禁止 |
|---|---|---|---|
| **Wallet Crypto Deposit 支持国家** | Philippines（PH）only | Current Implementation（用户确认 2026-05-29） | 不得扩展为 Card 支持国家，不得反推 KYC 全量白名单 |
| **Card Application Phase 1 支持地区** | Philippines、Vietnam、Australia（PH / VN / AU） | Current Implementation | 不得反推 Wallet Deposit 支持国家，不得反推 KYC 全量白名单 |
| **KYC 居住国白名单** | 版本口径存在冲突（archive 显示 VN/PH/AU ✅；330 版本 PH+SG；内测临时 PH/AU/VN/SG），未在当前 KB 收口 | Unknown / conflict noted | 不得从 Wallet 或 Card 任一口径推导 KYC 国家线 |

**硬约束：Wallet Crypto Deposit current = PH；Card Phase 1 = PH/VN/AU。两者不可互推。** 竞品地区比较必须按 rail 分别对齐，不得用任一口径替代另一口径。完整 `stablecoin → AIX → card spend` current journey 的地域锚点，当前最强确认是 PH：Wallet Crypto Deposit = PH 且 Card = PH/VN/AU。不得把 PH/VN/AU 都当作已确认完整 journey region；VN/AU 的完整 Wallet→Card journey 应标 Unknown。

---

## 2. Starting money pool 与资产类型

| 层面 | AIX 当前事实 | 状态 |
|---|---|---|
| **Wallet 资产范围** | 仅稳定币：USDC、USDT、WUSD、FDUSD | Current Implementation |
| **无波动币资产** | 当前无已确认的 volatile crypto balance 产品 | Current Implementation |
| **资产托管位置** | DTC 外部供应商托管（Master Account / Sub Account 模型）；非 self-custody | Current Implementation |
| **资金进入方式** | 外部稳定币充值：GTR / Exchange 地址充值，或 WalletConnect / Self-custodial Wallet 充值 | Current Implementation |
| **法币入金** | DTC 有 `FIAT_DEPOSIT=6` 分类，但 AIX 用户路径未见确认 | Unknown |
| **Card Balance** | 独立于 Wallet Balance 的卡余额；消费扣 Card Balance | Current Implementation |
| **Wallet → Card 用户充值路径** | KB 未确认普通用户可主动将 Wallet 余额转入 Card；仅确认退款/冲正/入账事件触发 Card → Wallet 自动归集 | Unknown |
| **Card 余额币种** | 与 Wallet balance 币种是否一致未确认 | Unknown |

**AIX 侧 starting money pool 判定：** 用户在进入 AIX 前，资金起点是外部交易所或自托管钱包中已持有的稳定币（USDC/USDT/WUSD/FDUSD），进入 AIX 后驻留于 DTC 托管的稳定币 Wallet。不是波动币起点，不是法币起点。Card Balance 是消费侧独立资金池，其常规充值机制 Unknown。

---

## 3. 生态位坐标（X / Y / Species / Account Role）

| 维度 | AIX 当前结论 | 依据 |
|---|---|---|
| **X（Value Container Immediately Before Purchase）** | **X1 = Dedicated Card Balance，已确认**。卡消费扣 Card Balance，Card Balance 独立于 Wallet Balance | Agent F §4/§5；Step 2 §7 |
| **Y（Purchasing-power Mechanism）** | **Unknown**。不知道用户是否必须手动 Wallet→Card pre-fund，也不知道是否存在购买时自动 funding/转换 | Step 2 §7 |
| **Species** | **Unknown**。只有当 Y=A 被证实时才可归 S1；当前不得归 S3，也不得写 S1↔S3 边界 | Step 2 §7 |
| **Account Role** | **Unproven / Account-adjacent at most**。Receive Unknown、Send/Swap runtime pending、Withdraw 不可用，缺完整 receive/hold/send/spend + unified balance 证据，不能称 Money Account | Step 2 §7 |

**禁止推论：**

- Card Balance 与 Wallet Balance 分离只证明 X1，不证明 Y=A，不证明 S1。
- Wallet 有稳定币余额不证明 S3 / Money Account。
- X1 确认不自动推导 Species；Y 未知则 Species 必须保持 Unknown。

---

## 4. User Job：只能作为 analysis inference

| Job Family | AIX 侧分析推断 | 状态 |
|---|---|---|
| **J1**（稳定、可跨境的钱） | **Plausible / incomplete**：AIX 的 stable-value money + card spend 覆盖该 Job 的核心方向，但 Receive/Send/Withdraw 闭环不完整；PH 已确认完整 stablecoin→card journey，VN/AU 仅 Card 支持已确认，完整 journey Unknown | Analysis inference only；非 AIX 文档事实 |
| **J2**（已持有 Crypto，转换为现实购买力） | **Strong / plausible for the supported stablecoin-starting segment**：适用于已从交易所或自托管钱包持有受支持稳定币并寻求卡消费能力的用户。AIX 当前无 volatile-crypto balance 只表示当前覆盖范围不包含 confirmed BTC/ETH/volatile balance，不代表 J2 不适用 | Analysis inference only；非 AIX 文档事实 |
| **J3**（不卖 Crypto，保持敞口获得消费流动性） | **Unsupported**：无 collateral / credit / borrow 能力证据 | Analysis inference only；非 AIX 文档事实 |

**硬约束：J1/J2/J3 是 Step 1 市场分析概念，不是 AIX 文档内事实。** 在 Step 3 直接比较中使用 Job 时，必须标注 `analysis inference`，不得写成 AIX confirmed fact，也不得用于 Species 归类。

---

## 5. Rail 当前状态清单

| Rail | 当前状态 | 关键事实 |
|---|---|---|
| **Deposit** | Current Implementation | GTR / Exchange 与 WalletConnect / Self-custodial 两条稳定币入金子路径；仅支持稳定币；Wallet Crypto Deposit 国家 = PH |
| **Hold** | Current Implementation | Wallet 托管稳定币（USDC/USDT/WUSD/FDUSD）；Card Balance 独立托管；无波动币 |
| **Receive** | **Unknown** | 独立 Receive 是否存在、与 Deposit 关系、页面与支持范围均未确认；交易历史有 Receive 类型但无独立入口路由（ALL-GAP-052/059/060/061/062） |
| **Send** | Current Implementation / **runtime confirmation pending** | KB 把 Send 拆分为 active 主事实（向 AIX 平台存量用户发送同一币种稳定币），但 KB 索引仍保留"当前是否上线待确认"，运行态需产品/后端核验 |
| **Swap** | Current Implementation / **runtime confirmation pending** | KB 把 Swap 拆分为 active 主事实（同一用户不同稳定币之间兑换），但 KB 索引仍保留"当前是否上线待确认"，运行态需产品/后端核验 |
| **Spend** | Current Implementation | Card 消费扣 Card Balance；Virtual / Physical Card 可用；Card Phase 1 = PH/VN/AU |
| **Withdraw** | **不支持 / 入口隐藏** | 当前暂不支持，后续开放；App 隐藏 Withdraw 入口（ALL-GAP-071 resolved-by-user） |
| **Fiat Deposit** | Unknown | DTC 有 `FIAT_DEPOSIT=6` 分类，但 AIX 用户路径未见确认，不得写成已上线能力 |

---

## 6. 直接比较 four-AND：AIX 侧口径

Step 2 要求直接竞品判定必须同时满足以下四项（AND），缺一不可。以下逐项给出 AIX 侧对标口径：

| AND 条件 | AIX 侧口径 | 当前可用性 |
|---|---|---|
| **1. Same region** | 按 rail 分别对齐：Wallet Crypto Deposit 比较 = PH only；Card 比较 = PH/VN/AU。不得用任一口径替代另一口径，不得合并为"AIX 支持国家"。完整 `stablecoin → AIX → card spend` current journey 的最强地域锚点是 PH；VN/AU 完整 journey = Unknown | 可用，但必须分 rail；完整 journey 只能锚定 PH |
| **2. Same core Job** | AIX 侧 Job 只能标 `analysis inference`。AIX 最接近 J1 方向，但闭环 incomplete；AIX 对 stablecoin-starting J2 segment 为 strong / plausible，但 confirmed BTC/ETH/volatile balance segment 不适用；J3 unsupported。Same core Job 允许按用户 segment 比较：例如 AIX stablecoin-starting J2 segment 可与竞品对应 J2 segment 判断 overlap。与竞品 Job 比较时，必须显式说明这是分析推断而非 AIX 文档事实 | 部分可用，需标 inference 且按 segment 对齐 |
| **3. Same starting money pool** | 只比较用户进入产品前的 starting money pool。AIX 侧 = 用户已持有稳定币（USDC/USDT/WUSD/FDUSD），从外部交易所或自托管钱包充值进入 DTC 托管稳定币 Wallet。若竞品典型起点是波动币（BTC/ETH）或法币，则 starting money pool 不同，不得直接判为同一起点。Wallet→Card 内部 funding 机制不是第 3 项的必要条件 | 可用 |
| **4. Substitutable final real-world payment outcome** | AIX 侧 = 通过 Card（Virtual/Physical）完成现实世界消费，扣 Card Balance。竞品必须提供可替代的最终现实支付结果，不只是链上转账、充值或资产查看 | 可用 |

**四项 AND 同时满足才可判为 direct competitor。任何一项 Unknown 或不匹配 → 不得判 direct。**

---

## 7. 阻止确定结论的 Unknown

以下 Unknown 会限制 Species/Account Role/部分地区或依赖 rail 的竞争判断；不自动阻止在 PH 上依据 four-AND 判断 direct。必须作为核验问题带入后续步骤：

| Unknown | 阻止什么 |
|---|---|
| Wallet → Card 用户充值 / purchase-time funding 机制 | Y 轴判定；Species/S1/S3 精确归类。不自动阻止 direct-competitor four-AND；four-AND 本身不要求 X/Y 相同，第 3 项也只看进入产品前的 starting money pool |
| Send / Swap 真实 runtime 状态 | Account Role 升级；four-AND 第 4 项可替代性 |
| 独立 Receive 是否存在 | Money Account 判定；four-AND 第 4 项可替代性 |
| Wallet 与 Card 余额币种是否一致 | Starting money pool 精确对齐 |
| AIX user ↔ DTC Sub Account 映射 | 账户结构判断 |
| WalletAccount.status 与能力准入映射 | 资产/入金可用性判断 |
| KYC 与 Deposit / Card 前置关系 | 用户旅程入口判断 |
| 完整费用表（FX、ATM、跨境、Swap 价差、Send gas 等） | 成本结构对比 |
| KYC 国家线版本冲突 | 地区准入精确对齐（不得用 Wallet/Card 口径替代） |

这些 Unknown 不阻止建立市场地图，也不自动阻止 direct-competitor four-AND。Step 3 仍可在 PH + confirmed starting pool / Job / final payment outcome 的四项 AND 满足时判 direct；涉及 VN/AU 完整 Wallet→Card journey，或依赖未确认 rail（如 Receive、Send/Swap runtime）的结论保持 Unknown。Y Unknown 仍阻止 Species/S1/S3 精确归类，但不自动阻止 direct competitor。Step 3 应将上述 Unknown 转为核验问题，不得用推测填补。
