# Step 2｜生态位地图

> 状态：Final / Reviewed（2026-08-29，经 Advance Codex CLI → ARouter → grok-4.6 → xhigh 最终复评 PASS）
> 类型：阶段研究结论；用于 Step 3 玩家定位与后续竞争关系判断，不代表 AIX 最终战略决策。

## 核心结论

Step 2 使用 **两条 Solution Axes** 建立产品模式坐标：

1. **消费前实际被扣款的钱放在哪里（Value Container Immediately Before Purchase）**；
2. **购买力如何形成（Purchasing-power Mechanism）**。

在这两个坐标之上，另加一个 **Account Role overlay** 判断产品只是“消费功能”，还是用户长期使用的“Money Account”。

> **重要修正**：Account Role 不是第三条 Solution Axis；生态物种也不再定义为“每一个 cell 就是一个物种”。物种是市场中已观察到的稳定策略簇；可以对应单一 cell，也可以像 Credit 一样跨不同 custody/container 形成同一 Job 下的机制簇。

---

## 一、两条 Solution Axes

### X 轴：Value Container Immediately Before Purchase

判断规则：**看一笔消费真正发生时，被扣减的用户价值余额在哪里**，不看公司出身，也不看资产最初从哪里转入。

| X | 定义 | 可观测判别 |
|---|---|---|
| **X1 Dedicated Spend / Card Balance** | 独立于主 Wallet/Account 的专用消费余额 | 消费扣 Card/Spend Balance；通常需先把资产转入该余额 |
| **X2 Provider-custodied Wallet / Account Balance** | 由产品方托管的通用 Wallet / Account 余额 | 消费直接从托管 Wallet/Account 的用户余额扣减，不先进入独立 Card Balance |
| **X3 Self-custody / User-controlled Wallet or Vault** | 资产在用户控制的链上 Wallet/Vault 中直到支付 | 消费前资产仍在用户控制的 onchain wallet/vault，不先转入平台托管消费余额 |

### Y 轴：Purchasing-power Mechanism

判断规则：**看用户消费能力在交易发生前/发生时是怎么产生的**。

| Y | 定义 | 可观测判别 |
|---|---|---|
| **A Manual pre-fund / pre-convert** | 用户先把资产转入/换成专用消费余额 | 明确存在 top-up / pre-fund / pre-convert 步骤 |
| **B At-payment asset sell / convert** | 支付时才把非稳定资产卖出/换成本地结算购买力 | 付款时自动出售/转换 BTC、ETH 等资产 |
| **C Stable-value balance deduction** | 用户以 Stablecoin / USD-equivalent 稳定余额作为消费来源 | 用户侧直接扣稳定价值余额；卡网络后端是否做 fiat settlement 不改变此分类 |
| **D Collateral-backed borrowing / credit** | 不出售抵押资产，通过借款/信用形成购买力 | 资产作为 collateral，产生 debt / credit balance |

### 分类操作规则

1. **按 product mode 分类，不按 brand 分类。** 同一品牌有两种消费模式时可跨多个 cell。
2. X 看“消费时被扣的余额”，不是资金最初来源。Self-custody 资产若先 top up 到独立 Card Balance，最终仍是 **X1**。
3. Y 看“购买力形成机制”。同一品牌若既能卖 BTC 支付、又能直接扣 Stablecoin，可分别占 **B / C**。
4. 证据不足时写 **Unknown**，不为了把品牌塞进地图而猜机制。
5. Card / QR / Transfer 是 **Rail**；Region / Issuer / Network / Regulation 是 **constraint layer**，均不参与 X/Y 定义。

---

## 二、Account Role Overlay（不是第三条轴）

Account Role 用于回答：**这个模式只是“让我花钱”，还是用户会把它当长期资金账户？**

| Overlay | 判别标准 | 用法 |
|---|---|---|
| **Spend Feature** | 证据主要证明 top-up / spend / card 等消费能力 | 不称“全球账户” |
| **Money Account** | 有明确证据证明同一用户资金体系支持 **receive + hold + send/transfer + spend**，并存在 unified/same-balance 或等价账户结构 | 才可称“Stablecoin Money Account / Global Account” |
| **Account-adjacent** | 已有部分 receive/send/pay 能力，但统一余额、完整闭环或 live 状态不够 | 只作为邻接，不升级为 Money Account |

**为什么需要 overlay：** X2×C 可以同时出现“托管 Stablecoin 直接消费卡”和“KAST 式长期 USD/Stablecoin 账户”。两者消费机制相同，但用户心智和产品角色不同；这个差异不能偷偷塞进 X 轴。

---

## 三、已观察到的 6 个策略簇

> “Species”在本研究中指 **已观察到、对用户 Job 和竞争关系有解释力的策略簇**，不是数学上每个 X×Y cell 都必须拥有一个物种。

### S1 `先充消费余额，再花` / Pre-funded Spend Balance

- **核心 Job**：J2。
- **坐标**：X1 × A。
- **人话定位**：Crypto 可以来自任何地方，但消费前必须先 top up / convert 到独立消费余额。
- **已确认样本**：Crypto.com traditional prepaid。Bitget Wallet Card current 仅确认 `Activate → top up → spend` 与 crypto top-up；其消费前是否形成独立 Dedicated Spend/Card Balance 尚未被当前证据证明，因此仅记为 **S1 candidate（Y=A confirmed / X=Unknown）**。
- **其他样本**：Crypto.com traditional prepaid；Gate Prepaid **待 current 产品级复核**。
- **Account Role**：通常为 Spend Feature。
- **为什么存在**：资金边界与 issuer 风险控制清楚；代价是多一步 top-up。

### S2 `托管 Crypto 余额，付款时再卖` / Custodial Crypto Instant-convert Spend

- **核心 Job**：J2。
- **坐标**：X2 × B。
- **人话定位**：Crypto 留在平台托管 Wallet/Account，刷卡时才自动卖/换成结算购买力。
- **强样本**：RedotPay generic crypto auto-convert mode、Bybit Card。
- **其他样本**：Gate Instant **待复核**；Wirex **boundary / 待产品模式核验**。
- **Account Role**：按产品另标，不因有 Wallet/Transfer 就自动升级为 Money Account。
- **为什么存在**：用户不想提前把资产锁到卡余额，希望持有资产到实际付款时。

### S3 `托管 Stablecoin 余额直接花` / Custodial Stable-value Spend

- **核心 Job**：主要 J1；也可承接持有 Stablecoin 的 J2 场景。
- **坐标**：X2 × C。
- **人话定位**：钱已经是托管的 Stablecoin / USD-equivalent 余额，消费直接扣这个稳定价值余额。
- **强样本**：KAST。当前官方明确 Global Account / Unified Balance，并支持 ACH、SWIFT、Fedwire 资金进入，以及 receive / send / spend。
- **Account Role**：
  - KAST = **S3 + Money Account**：当前官方明确 US/EU account、Unified Balance、ACH / SWIFT / Fedwire，以及 receive / send / spend。
  - 其他 X2×C 产品若只证明“Stablecoin 可以刷”，只能标 **S3 + Spend Feature / Account-adjacent**，不能直接叫“全球账户”。
- **为什么存在**：用户要的是稳定、跨境、随时可用的钱，而非等待 Crypto 上涨后再消费。

### S4 `自托管 Stablecoin 直接花` / Self-custody Stable-value Spend

- **核心 Job**：J1 或 Stablecoin 持有者的现实支付需求。
- **坐标**：X3 × C。
- **人话定位**：Stablecoin 在用户控制的链上 Wallet/Vault 中，直到支付时再直接扣稳定价值余额。
- **较强样本**：OKX Pay/Card **仅限 SG 已验证模式**；ether.fi Direct Pay（Vault USDC/LiquidUSD direct deduction，custody/control 程度仍需在 Step 3 产品级确认）。
- **候选 / 邻接**：Bleap、MiniPay、Gnosis Pay；**Plasma One 为 current live 的 S4 强邻接/候选**，官方已明确 self-custody、stablecoin balance backing card、global account services、send/receive/spend；Karta = direction，receive/payout future。
- **Account Role**：逐个验证；不能因为“self-custody + card”就称全球账户。
- **为什么存在**：用户既想用 Stablecoin 做现实支付，又不希望长期把资金放在中心化托管余额。

### S5 `自托管 Crypto，付款时再换` / Self-custody Crypto Instant-convert Spend

- **核心 Job**：J2。
- **坐标**：X3 × B。
- **人话定位**：BTC/ETH 等资产一直留在自己的钱包，到付款时才转换成商户可接受的购买力。
- **强样本**：MetaMask Card。
- **与 S1 的关键区别**：MetaMask 的核心证据是资产保持 self-custody until payment；Bitget current 虽明确先 top up 再 spend，但当前证据尚不足以证明 top-up 后一定形成独立 X1 Dedicated Spend/Card Balance，因此 Bitget 只保留为 S1 candidate。
- **为什么存在**：Web3-native 用户希望保留钱包控制权，同时获得现实支付能力。

### S6 `抵押 Crypto，不卖也能花` / Crypto-backed Credit Spend

- **核心 Job**：J3。
- **核心机制**：Y=D。
- **人话定位**：不卖 Crypto，用资产作抵押形成贷款/信用，再消费。
- **这是一个跨 X 的机制策略簇，不等于一个 cell**：
  - **S6-Custodial variant**：X2 × D，例如 Nexo Credit Mode。
  - **S6-Onchain/Self-custody variant**：X3 × D，例如 ether.fi Borrow Mode；其 custody/control 边界在 Step 3 继续核验。
- **为什么不硬拆两个物种**：两者解决的是同一个 J3，核心用户选择逻辑首先是“卖币 vs 抵押借款”；custody 是第二层差异。后续若竞争分析证明两类用户和替代关系显著不同，再拆分。

---

## 四、X × Y Occupancy Map

> 这张表是 **坐标占用图**，不是“16 个 cell = 16 个物种”。空格可以一直为空；出现新模式时也可以新增策略簇，而不是强塞 S1–S6。

| Value Container ↓ / Mechanism → | A Pre-fund | B At-payment convert | C Stable-value deduction | D Collateral credit |
|---|---|---|---|---|
| **X1 Dedicated Spend/Card Balance** | **S1** | 未观察到稳定主簇 / 不强填 | 未观察到稳定主簇 / 不强填 | 未观察到稳定主簇 / 不强填 |
| **X2 Provider-custodied Wallet/Account** | 暂空 | **S2** | **S3** | **S6-Custodial** |
| **X3 Self-custody / User-controlled Wallet/Vault** | 通常 pre-fund 后会转成 X1；不在此强造物种 | **S5** | **S4** | **S6-Onchain/Self-custody** |

### 地图读法

- 一个 **product mode** 先落 X/Y 坐标，再标 Job、Account Role、Rail、Region。
- 一个品牌可以有多个 mode，因此可以跨多个 cell；例如 Nexo Debit/Credit、ether.fi Direct Pay/Borrow。
- **Account Role 是 overlay**：例如 KAST = `X2×C / S3 / Money Account`；一个只有 Stablecoin card spend 的产品可以是 `X2×C / S3 / Spend Feature`。
- 暂空 cell 不自动产生新物种，也不得把新产品强塞进已有物种。

---

## 五、玩家当前落位

| 玩家 / 模式 | X×Y / 策略簇 | Account Role | 证据边界 |
|---|---|---|---|
| **RedotPay generic crypto auto-convert** | X2×B / **S2 primary** | Spend Feature / Account-adjacent | current 官方明确 all-in-one wallet + crypto auto-convert；International Transfer 不足以证明 Unified Money Account |
| **KAST** | X2×C / **S3** | **Money Account** | current 官方明确 Global Account + Unified Balance + ACH / SWIFT / Fedwire + receive / send / spend |
| **Bybit Card** | X2×B / **S2** | Spend Feature | Funding Account + payment conversion；地区另核 |
| **Bitget Wallet Card current** | **X=Unknown × Y=A confirmed / S1 candidate** | Spend Feature | current 官方只足以证明 activate → top up → spend 与 crypto top-up；“top up”本身不足以证明消费前形成独立 Dedicated Spend/Card Balance，因此不得确认 X1 / S1 |
| **Gate Prepaid / Instant** | S1 / S2 **candidate** | Unknown | current 直连 403；Step 3 前需重新验证 live 模式 |
| **Crypto.com traditional prepaid** | X1×A / **S1** | Spend Feature | 作为传统 prepaid 参考；Step 3 若纳入重点玩家再复核 current product mode |
| **OKX Pay/Card SG** | X3×C / **S4** | 先标 Spend Feature / Account-adjacent | 仅 SG 模式；不得推广全 OKX；Money Account 资格需另证 |
| **MetaMask Card** | X3×B / **S5** | Spend Feature | self-custody until payment |
| **ether.fi Direct Pay** | X3×C / **S4 candidate/strong-adjacent** | Account-adjacent | USDC/LiquidUSD 直接从 Vault 扣；Vault custody/control 在 Step 3 继续核验 |
| **ether.fi Borrow** | Y=D / **S6 Onchain variant candidate** | — | Borrow mechanism 已确认；X3 custody/control 继续核验 |
| **Nexo Credit** | X2×D / **S6 Custodial** | — | current 官方明确 crypto-backed Credit Line / spend without selling |
| **Nexo Debit** | X2 spend mode，具体 B/C 需产品级核验 | Spend Feature | 不再直接写 S2-like，避免把 Debit 机制猜成 instant-convert |
| **Bleap / MiniPay / Gnosis Pay** | **S4 candidates** | 待验证 | self-custody / stablecoin 方向存在，但 Step 3 逐个验证 live direct-deduction 与 account role |
| **Plasma One** | X3×C / **S4 current live candidate** | **Money Account / strong account-like evidence** | current 官方已明确 self-custody、stablecoin balance backing card、global account services、send / receive / spend；具体 region eligibility 仍需按 current 页面逐区验证 |
| **Karta** | **S4 direction candidate** | 待验证 | receive/payout Coming Q3 2026，不当 current capability |
| **Wirex** | X2 mode，B/C **Unknown** | Account-adjacent / Unknown | 不强塞 S2/S3，Step 3 产品级验证 |

---

## 六、Region / Issuer / Network Constraint

Step 2 只建立纪律；真正的 player×region eligibility matrix 在竞争阶段逐产品维护。

### 原则

1. **App availability ≠ Card issuance eligibility**。
2. **Merchant acceptance ≠ issuance eligibility**。
3. **“100+ / 200+ countries” ≠ 具体 issuance country list**。
4. 同一品牌不同 region / issuer / mode 必须分开。
5. 没有确凿 current evidence 就写 **Unknown**。

### 当前高置信例子

- **Bitget Wallet Card**：current official page 给出 EEA+UK、LATAM、APAC、South Africa、Pakistan/Bangladesh 等明确可用范围；不同 help 版本细节需 Step 3 按日期复核。
- **RedotPay**：current Card Issuance Restrictions 明确 US、Singapore、Indonesia、India、Türkiye、Morocco、mainland China 等不可开卡；不能从“100+ countries”反推具体国家可开。
- **KAST**：“200+ transfer / 150M merchant acceptance”不等于 Card issuance eligibility。
- **OKX**：本轮只使用 **SG Pay/Card** 证据，不推广到其它市场。
- **ether.fi**：supported/restricted 页面存在局部冲突，Step 3 必须按最新资格页复核。

---

## 七、AIX 当前落位：只写事实，不提前做战略选择

> 依据：`evidence/02-agent-f-aix-current-position.md`。External competitor facts 与 AIX internal facts 分开。

### 7.1 Current Facts

- AIX Wallet 当前确认资产为 **USDC / USDT / WUSD / FDUSD**。
- 资金由外部 **DTC account/sub-account** 托管，**不是 self-custody**。
- **Wallet Balance 与 Card Balance 分离**。
- Card 消费已确认 **扣 Card Balance**。
- 普通用户 **Wallet → Card funding / purchase-time funding mechanism = Unknown**。
- 独立 Receive = Unknown；Send / Swap runtime 仍需核验；Withdraw unsupported/hidden。
- 无已确认 volatile crypto balance 产品。
- 地区口径存在版本冲突，不能直接做竞争地区重合结论。

### 7.2 Current Coordinate

| 维度 | AIX 当前结论 |
|---|---|
| **X** | 对 Card purchase 而言，**X1 Dedicated Card Balance 已确认**（实际消费扣 Card Balance） |
| **Y** | **Unknown**。不知道用户是否必须手动 Wallet→Card pre-fund，也不知道是否存在 purchase-time 自动 funding/转换 |
| **Account Role** | **Unproven / Account-adjacent at most**。Receive Unknown、Send/Swap runtime pending、Withdraw unavailable，不能称 Money Account |
| **Species** | **Unknown**。只有当 Y=A 被证实时才能归 S1；当前不得归 S3，也不得写 S1↔S3 boundary |

### 7.3 明确不能下的结论

- 不能因为 Card Balance 与 Wallet Balance 分离，就推断 **S1**；分离只证明 X1，不证明 Y=A。
- 不能因为 Wallet 有稳定币余额，就推断 **S3 / Money Account**；当前缺 Unified Balance + 完整 receive/hold/send/spend 证据。
- 不能把“未来做统一 Stablecoin 全球账户”写成当前生态位。
- **S1→S3 是 Step 5 的战略选项，不是 Step 2 的事实结论。**

### 7.4 进入 Step 3 前最重要的 AIX 核验

1. Card purchase 前，Card Balance 是如何获得资金：手动 top-up、自动 transfer、实时 conversion，还是其它机制？
2. Wallet→Card 是否有用户可见/自动资金路径？触发时点是什么？
3. Send / Swap 的真实 runtime 状态。
4. Receive 是否有独立 live 能力。

这些 Unknown 不阻止建立市场地图，但**阻止当前把 AIX 硬归 S1/S3**。

---

## 八、Step 3 的统一落位模板

后续每个产品**按 mode**记录以下字段，避免再按品牌印象分类：

| 字段 | 必填内容 |
|---|---|
| User Job | J1 / J2 / J3，可多选但标 primary |
| X | X1 / X2 / X3 / Unknown |
| Y | A / B / C / D / Unknown |
| Strategy Cluster | S1–S6 / Candidate / Unknown |
| Account Role | Spend Feature / Money Account / Account-adjacent / Unknown |
| Rail | Card / QR / Transfer / P2P 等 |
| Region Eligibility | 具体 current issuance/service eligibility；Unknown 不补 |
| Live Status | Live / Pilot / Early access / Future / Unknown |
| Evidence | 官方事实 / internal fact / inference / unknown |

**直接竞品判定不只看“同一 S”**。生态位只做第一层筛选；后续必须同时满足 **same region + same core Job + same starting money pool + substitutable final real-world payment outcome**，四项缺一不可。

---

## 九、Step 2 修订后结论

1. **真正的两条坐标轴**是 `消费时价值容器 × 购买力形成机制`；两者负责描述“钱在哪里、怎么变成购买力”。
2. **Money Account 是 overlay，不是隐藏第三轴**；只有明确 receive/hold/send/spend + unified/same-balance 证据才能打该标签。
3. **Species 是观察到的策略簇，不等于每个 cell**；S6 明确是 Y=D 的跨 custody credit cluster，并保留 X2 / X3 variants。
4. **品牌不是物种**；同一品牌不同 mode 可以跨 cell，产品必须 mode-level 落位。
5. **AIX 当前只确认 X1、Y Unknown、Species Unknown**；S1/S3 都要等事实，Step 2 不提前做战略选择。
6. 这张地图的用途是给 Step 3 提供稳定、可复现的落位方法，而不是在 Step 2 直接宣布谁是 AIX 的最终直接竞品。
