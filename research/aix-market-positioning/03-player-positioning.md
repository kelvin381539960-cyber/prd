# Step 3：玩家定位（Player Positioning）

> 状态：Final（2026-08-29）。基于已评审 Step3 证据（Agent A–F）汇编，结论以本轮固定结论为准。
> 类型：阶段研究结论。`Direct candidate` 是证据级 four-AND 判定，不是 Step4 竞争关系最终分类，也不含 Step5 战略决策。

## 1. 核心结论

1. **AIX 当前最强用户/战场锚点 = PH + 用户已持有受支持稳定币 + 想要现实卡消费力。** 这是 J2 的 stablecoin-starting segment；稳定币属于 Crypto，J2 不限于波动资产。
2. 以 four-AND（same region + same core Job + same starting money pool + substitutable final outcome）在 PH stablecoin-starting J2 segment 上判定，仅 **3 个 evidence-level `Direct candidate`**：RedotPay generic auto-convert card、Bitget Wallet Card、ether.fi Direct Pay。
3. **KAST 机制结论按 Step3 证据降级**：X2 confirmed / Y Unknown / Strategy Cluster Unknown（官方文档冲突，待厂商澄清）；Money Account 结论保留。
4. `Direct candidate` 不等于 Step4 竞争分类，不代表最终竞争格局，也不构成 AIX 战略选择。

## 2. AIX 锚点（现状事实）

| 维度 | 当前结论 |
|---|---|
| 地区 | Wallet Crypto Deposit = PH；Card Phase 1 = PH/VN/AU；完整 stablecoin→card journey 仅 PH 已确认；VN/AU 完整 journey Unknown |
| 资金起点 | 用户进入产品前已持有 USDC/USDT/WUSD/FDUSD（外部交易所或自托管钱包充值）；当前无波动币资产产品 |
| 托管/消费容器 | DTC 外部托管（非 self-custody）；Card Balance 独立，消费扣 Card Balance → X1 confirmed |
| Y 轴 | Unknown（Wallet→Card funding 机制未证） |
| Species / Account Role | Species Unknown；Account Role 未证实，最多 Account-adjacent（缺 receive/send/withdraw 完整闭环） |
| Jobs（analysis inference） | J1 plausible/不完整；J2 对受支持稳定币起点 segment strong/plausible；J3 不支持 |

> 口径：`starting money pool` 只看用户**选择产品之前已拥有**的资产；产品内部 X/custody 差异（Card Balance、Funding Account、Vault 等）不阻止直接竞争判定。

## 3. 四类用户 segment

| Segment | 定义 | 当前覆盖玩家 |
|---|---|---|
| **A）存量稳定币 → 日常消费** | 用户已持有 USDT/USDC 等，换取现实卡消费力 | AIX、RedotPay、Bitget、ether.fi Direct Pay；KAST/Plasma/Karta 相邻（待地区证据） |
| **B）更宽波动币（BTC/ETH）→ 消费** | 用户持有 BTC/ETH 等，消费时卖出/转换 | RedotPay、Bybit、MetaMask；AIX 当前更窄（仅稳定币起点） |
| **C）稳定币作为长期资金 / Money Account** | 稳定币 = 长期持有与收付的"钱" | KAST 最强；Plasma、Bleap、OKX SG、Karta 为方向（完整闭环/地区未全部确认） |
| **D）抵押不卖币消费（J3）** | 用 crypto 作抵押获得消费流动性 | Nexo Credit、ether.fi Borrow、RedotPay Credit；AIX 不服务 |

## 4. 玩家矩阵（mode-level）

> 四项 AND 只在 PH stablecoin-starting J2 segment 上判定；`Direct candidate` 为证据级判定，不是 Step4 竞争分类。

| 玩家 / mode | X×Y / Cluster | Account Role | 起点资金池 | Job（analysis inference） | 地区 vs AIX | 四项 AND | 阻断点 |
|---|---|---|---|---|---|---|---|
| **RedotPay** generic auto-convert card | X2×B / S2 | Spend Feature / Account-adjacent | USDT/USDC（也含 BTC/ETH 等） | J2 primary | PH gate Yes（restricted list 不含 PH；受通用 onboarding/KYC 约束） | **Direct candidate**（PH stablecoin-starting J2） | 无（segment 限定） |
| **Bitget Wallet Card** | Y=A confirmed / X Unknown / S1 candidate only | Spend Feature | USDT/USDC（也含 ETH/SOL） | J2 primary | PH availability confirmed | **Direct candidate**（PH stablecoin-starting J2） | 无（segment 限定） |
| **ether.fi Direct Pay** | X3×C / S4 candidate/strong-adjacent | Unknown / Account-adjacent | 已持有 USDC/USDT 进 Vault | J2 secondary | PH listed available（available/restricted 页 VN 冲突已记录） | **Direct candidate**（PH stablecoin-starting J2） | 无（segment 限定） |
| **KAST** | X2 confirmed / Y Unknown / Cluster Unknown（Source Conflict） | **Money Account** | USDT/USDC | J1 primary；J2 secondary | Unknown（仅 signup dropdown 查询，无 PH 正面资格） | Unknown | PH issuance/service Unknown |
| **Bybit Card** | X2×B / S2 | Spend Feature | USDC（payment priority） | J2 primary | Unknown（只见 program names，无逐国资格） | Unknown | PH issuance Unknown |
| **Crypto.com Card** | X1×A / S1（SG/AU region modes） | Spend Feature | Unknown（stablecoin→card load 路径未证） | J2 primary | Unknown（无 PH 证据；AU 页面存在但 AIX AU full journey Unknown） | Unknown | PH 无证据 + 起点池未证 |
| **Plasma One** | X3×C / S4 | Money Account-leaning | 自有 stablecoin | J1 primary；J2 secondary | Unknown（issuance/service country list 未公布） | Unknown | 地区 Unknown |
| **Karta** | X Unknown × Y=A；S4 direction，S1-candidate boundary | Account-adjacent | USDT/USDC | J1-leaning（current 闭环不足） | Unknown（service country list 未公布） | Unknown | 地区 Unknown + 闭环不足 |
| **MetaMask Card** | X3×B / S5 primary；stablecoin mode S4 candidate | Spend Feature（Card mode） | 自托管 crypto/stablecoin | J2 primary | No（current list 无 PH/VN/AU） | **Not Direct current** | region No |
| **Bleap** | X3×C / S4 | Money Account-leaning | stablecoin / bank transfer | J1 primary；J2 secondary | No（Europe/MX/BR） | **Not Direct current** | region No |
| **OKX Pay/Card SG** | X3×C / S4 | Spend Feature / Account-adjacent | USDT/USDC | J1 primary；J2 secondary | No（仅 SG mode） | **Not Direct current** | region No |
| **Nexo Debit** | X2 / Y Unknown / Cluster Unknown | Spend Feature at most | stablecoin/crypto/FiatX available balance | J2-compatible | No（EEA+UK） | **Not Direct current** | region No |
| **Nexo Credit** | X2×D / S6-Custodial | Spend Feature at most | crypto available balance | J3 primary | No（EEA+UK） | **Not Direct current** | region No + J3 不匹配 |
| **ether.fi Borrow** | X3 candidate ×D / S6 onchain candidate | — | Vault 资产作 collateral | J3 primary | PH listed available | **Not Direct current** | J3 不匹配（AIX J3 不支持） |

## 5. 三个 Direct candidate（证据级）

### 5.1 RedotPay generic auto-convert card

- 机制：X2×B / S2——资产留在托管 wallet，支付时自动转换（"No need to manually sell"）。
- PH region gate：current Card Issuance Restrictions 列出约 49 个不可开卡地区，PH 不在列表 → Step3 gate 判 region Yes，仍受通用 onboarding/KYC 约束；**不作为 merchant acceptance 证据**。
- 匹配段：PH + stablecoin-starting J2 + USDT/USDC 起点 + 卡消费结果 → 四项 AND 全满足。
- 边界：判定仅限 generic auto-convert card mode；RedotPay Credit（J3）与 International Transfer 不在范围内；完整费表未证。

### 5.2 Bitget Wallet Card

- 机制：官方明确 Activate → top up → spend → **Y=A confirmed**；top-up 后是否形成独立 Dedicated Card Balance 未证 → **X Unknown / S1 candidate only**（不得写 X1/S1 confirmed）。
- PH：current availability 与 physical card 列表均含 PH → availability confirmed。
- 匹配段：PH + stablecoin-starting J2 + USDT/USDC 起点 + 卡消费结果 → 四项 AND 全满足。

### 5.3 ether.fi Direct Pay

- 机制：X3×C / S4 candidate/strong-adjacent——官方声明 non-custodial；Direct Pay 直接从 Vault 的 USDC/LiquidUSD 扣款；Vault 完整 user-control 边界未完全证明，不升 confirmed。
- PH：available countries 页列 PH；restricted 页列 VN 不支持（available vs restricted 局部冲突已记录，不裁决）。
- 匹配段：PH + stablecoin-starting J2 + 已持有 USDC/USDT 起点 + 卡消费结果 → 四项 AND 全满足。
- 边界：ether.fi Borrow 是 J3 机制（抵押不卖），AIX J3 不支持 → **Not Direct current**。

> 三个判定都是 evidence-level four-AND gate，不是 Step4 竞争关系分类；X/custody 差异（X1 vs X2 vs X3）不阻止 direct 判定。

## 6. KAST：来源冲突与 Step3 修正（重要更新）

**Step3 强制修正：KAST 当前机制结论 ≠ Step2 结论。**

2026-08-09 的三份 KAST 官方文档互相冲突：

| 来源 | 描述 |
|---|---|
| Card-use 页 | money comes straight from your wallet；deducted right away；spending own funds, not credit（C-like） |
| Debit-or-credit 页 | "All KAST cards are credit cards"；balance secures credit line；purchase charged to credit line；billing cycle——但同一页也说 no interest / no monthly bill / own funds（D-like 与 C-like 混杂） |
| Stablecoins 页 | 可直接 spend stablecoins（C-like） |

**Step3 superseding 结论（current mechanism）：**

- **X2 confirmed**（消费从 KAST 托管 wallet/account 扣款）
- **Y Unknown**（C-like vs D-like 冲突，不裁决）
- **Strategy Cluster Unknown**（不硬归 S3 或 S6，待厂商澄清）
- **Account Role：Money Account 保留**（unified balance + receive/send/spend 证据独立于 Y 判定）

历史说明：Step2 曾将 KAST 写为 X2×C / S3；Step3 新证据将机制确定性降级，这是对 current mechanism 的 superseding 结论，不是默默改写历史。KAST four-AND 仍因 PH issuance eligibility Unknown 而为 Unknown，机制冲突不影响 four-AND。

## 7. 五个竞争变量

1. **PH regional eligibility**：RedotPay / Bitget / ether.fi Direct Pay 已证可服务 PH；KAST / Bybit / Crypto.com / Plasma / Karta 的 PH issuance eligibility 未证。
2. **起点资金池宽度**：AIX 仅稳定币起点；RedotPay / MetaMask 等同时覆盖波动币起点，在非稳定币 segment 形成超集。
3. **Account Role**：KAST / Plasma 的 Money Account 定位带来更高切换成本与不同竞争边界。
4. **Custody / Container（X）**：AIX X1 vs RedotPay X2 vs ether.fi X3 vs Bitget X Unknown；影响信任与监管定位，但不影响 four-AND。
5. **发卡成本与费率**：RedotPay virtual 10 USD / physical 100 USD；Bitget 0 fee；KAST 免费+premium；ether.fi 完整费表未证。

## 8. 未解决 Unknown

1. KAST / Bybit / Crypto.com / Plasma One / Karta 的 PH issuance/service eligibility。
2. AIX Wallet→Card funding 机制（Y）→ Species 精确归类。
3. Bitget top-up 后的资金容器（X）。
4. KAST 机制冲突（C vs D）需厂商澄清。
5. Crypto.com stablecoin→card load 起点路径。
6. RedotPay / Bitget / ether.fi Direct Pay 完整费表。
7. AIX Send/Swap runtime、独立 Receive、余额币种一致性。
8. ether.fi available vs restricted 页的 VN 局部冲突。

## 9. Step3 结论

1. **三个 evidence-level `Direct candidate`**（PH stablecoin-starting J2 segment）：RedotPay generic auto-convert card、Bitget Wallet Card、ether.fi Direct Pay。
2. **AIX 锚点不变**：X1 confirmed / Y Unknown / Species Unknown / Account Role 最多 Account-adjacent；完整 journey 仅 PH 已确认。
3. **KAST 机制降级**：X2 confirmed / Y Unknown / Cluster Unknown（待厂商澄清）；Money Account 保留。
4. **Unknown rows**（KAST / Bybit / Crypto.com / Plasma / Karta）主要因地区/证据缺口；**Not Direct current**（MetaMask / Bleap / OKX SG / Nexo Debit / Nexo Credit / ether.fi Borrow）因地区和/或 J3 不匹配。
5. 本报告不构成 Step4 竞争关系最终分类，不做 Step5 战略决策。
