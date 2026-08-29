# Agent B｜Custodial Cards Step 3 收口（Bitget Wallet Card / Bybit Card / Crypto.com Card）

> 状态：Step 3 Agent B 收口稿（2026-08-29）
> 类型：evidence / mode-level 落位，不是最终竞争战略结论。
> 证据边界：只使用 Step 1/Step 2、AIX prior evidence 与 `/tmp/aix-evidence-03/` 已缓存官方页面；官方 URL 最多补抓 3 个，本轮实际补抓 1 个（Bybit Card Requirements 刷新，当前站点仍显示 unsupported，因此不作为事实源）。不做进一步开放检索。
> 结论纪律：Bitget 仍受硬约束限制——没有新的官方证据明确独立 Dedicated Card Balance 前，只能写 `Y=A confirmed / X Unknown / S1 candidate`。Crypto.com 按当前具体区域产品模式记录，不做品牌泛化。

## 0. 判定口径

- **J1**：获得并持续使用稳定、可跨境的钱。
- **J2**：已持有 Crypto，低摩擦转化为现实购买力。
- **J3**：不卖 Crypto、保持敞口获得消费流动性。
- **X/Y/Strategy Cluster**：沿用 `02-ecosystem-map.md` 的 `X=Value Container`、`Y=Purchasing-power Mechanism`、`S1–S6`。
- **Account Role**：沿用 Step 2 overlay。没有 receive + hold + send/spend + unified/same balance 证据时，不得称 Money Account。
- **Direct four-AND gate**：`same region + same core Job + same starting money pool + substitutable final real-world payment outcome`。四项均有证据才是 Yes；任何一项被证明为 No，则整体 No；证据不足时保留 Unknown。本表只做 Step 3 证据级判定，不替代 Step 4 竞争关系分析。

## 1. Bitget Wallet Card

### Current service/issuance region

官方 current 产品页写明卡片“currently available”于以下范围：

- Europe: EEA + UK。
- Latin America: Argentina, Brazil, Chile, Colombia, Ecuador, El Salvador, Guatemala, Mexico, Panama, Peru。
- Asia-Pacific: Singapore, South Korea, Japan, Vietnam, Malaysia, mainland China, Taiwan, Australia, Thailand, Philippines。
- Africa: South Africa。
- South Asia: Pakistan, Bangladesh。

页面同时说明 “Card issuing partners vary by region. Availability depends on local support.”，所以这是 current service availability 证据，不是逐国 issuer/发卡资格终表。Physical card 当前列出的地区为 Singapore, South Korea, Japan, Vietnam, Malaysia, Taiwan, Australia, Thailand, Philippines。

### Job inference

- **Primary：J2**。官方路径是持有/使用 crypto，先 verify identity，activate card、top up、spend；页面示例支持 USDT、USDC、ETH、SOL top-up。
- J1 “稳定可跨境的钱”不被当前证据证明为产品主定位；不能把 card 营销语升格为 Money Account。

### Starting money pool

推断：用户先持有 Bitget Wallet 侧 crypto，再把 USDT/USDC/ETH/SOL 等 crypto top-up 到卡内消费路径。

证据强度：

- crypto top-up 明确。
- 页面有 “If you lose control of your wallet...you won't be able to top up or withdraw from the card” 的表述，支持 card 与 wallet 资金路径相关。
- 但当前页面没有明确说 top-up 后形成独立 Dedicated Card Balance，也没有完整 custody 表述。

### X/Y/cluster

| 维度 | 结论 |
|---|---|
| X | **Unknown**。官方只证明 top-up 后 spend，未明确 independent Dedicated Card Balance。 |
| Y | **A confirmed**。官方明确 `Activate your card, top up, and spend`。 |
| Strategy Cluster | **S1 candidate only**。不得升级为 confirmed S1。 |

### Account Role

**Spend Feature**。没有 receive + hold + send/spend + unified balance 证据，不能称 Money Account。

### Card role

Visa/Mastercard acceptance 的 everyday spending card；支持 Apple Pay、Google Pay、WeChat Pay、Alipay 等 third-party payment platforms。Card 是消费 rail，不是已证明的全球资金账户。

### Current fees/KYC if proven

已证明：

- `0 opening fee & annual fee`。
- `No interest markup, no monthly card fee, no hidden charges`。
- Reward typically covers most top-up and currency conversion fees；超过月度 assetback allowance 后 standard fees apply。
- Apply flow 明确要求 `Apply online and verify your identity`。

未证明：

- 完整 top-up / FX / ATM / replace 等费用表。
- KYC tier、身份核验后的账户结构。

### Direct four-AND gate

| Gate | 结论 | 依据 |
|---|---|---|
| Same region | Yes | AIX 已确认完整 stablecoin→card journey 的 region 为 Philippines；Bitget current availability 与 physical card 均含 Philippines。Vietnam / Australia 不作为 AIX 完整 journey 证据。 |
| Same core Job | Yes（stablecoin-starting J2 segment） | 该 segment 内，J2 判断为 analysis inference：把已有 crypto/stablecoin 转为现实消费；不写成 AIX 事实。 |
| Same starting money pool | Yes | Bitget 官方明确支持 USDT、USDC top-up；AIX 当前也是 stablecoin 资金进入。 |
| Substitutable final outcome | Yes | 都是 card real-world spending。 |
| **Overall** | **Yes** | 当前证据下，Bitget Wallet Card 对 AIX 的 stablecoin 起点 segment 满足四项 AND。 |

### Unknown/limitations

- X 仍 Unknown；不得写成 confirmed X1/S1。
- 当前页面未证明 Wallet → Card 的手动/自动细节与 custody 边界。
- 逐国 issuer、limit、full fee schedule、KYC tier 未证明。
- Direct gate 只针对 stablecoin-starting segment；不表示 Bitget 全产品与 AIX 完全重合。

### Official URL index + 2026-08-29

| # | URL | 支持点 |
|---|---|---|
| B1 | https://web3.bitget.com/card | current availability、apply/verify/top-up/spend、fees、physical card、crypto top-up examples。 |

## 2. Bybit Card

### Current service/issuance region

当前缓存官方页面不能证明逐国 issuance list。Bybit Card Management 页面可见 card programs 为 Argentina、Brazil、AIFC、Asia Pacific、Mexico；同一官方页面的相关文章分类还出现 Australian Users 等 program 标题。

“Where is Bybit Card available” 当前页面显示 unsupported；“Bybit Card Requirements” 刷新后仍 unsupported。因此 country-level current issuance eligibility 为 **Unknown**，不得从 program 名称反推具体国家。

### Job inference

- **Primary：J2**。用户可选择 payment crypto asset，系统按 priority 在交易时转换；transaction detail 明确可查 `Crypto Sold`。
- 若 Funding Account 中是 base currency/fiat/stable balance，则可能服务更偏 J1 的用户，但当前证据不足以把它升为主 Job。

### Starting money pool

明确：**Bybit Funding Account**。

官方解释 Spending Power 由 Funding Account 的 base currency available balance 加上 selected payment crypto asset converted to base currency 计算。Transaction 成功后金额从 Funding Account 扣减；crypto-funded transaction 可查看 `Crypto Sold`。

### X/Y/cluster

| 维度 | 结论 |
|---|---|
| X | **X2 confirmed**。消费扣减/冻结发生在 provider-custodied Funding Account。 |
| Y | **B confirmed**。payment crypto asset 在交易时 converted/sold。 |
| Strategy Cluster | **S2**。 |

### Account Role

**Spend Feature**。Funding Account 支撑 card spending，但当前证据不足以证明 receive + hold + send/spend + unified balance 的 Money Account 结构。

### Card role

Card 是消费 rail；官方管理页可见 Mastercard 或 Visa program，支付页明确 online sites accepting Mastercard。支持 Apple Pay / Google Pay / Samsung Pay，但按 program 和添加方式有差异。

### Current fees/KYC if proven

已证明：

- Spending Power / Funding Account / payment crypto priority / `Crypto Sold` 机制。
- Payment authorization 会先冻结 Funding Account 金额，完成后扣减。

未证明：

- 当前 fee schedule。
- KYC/申卡 prerequisites 的具体条款。

### Direct four-AND gate

| Gate | 结论 | 依据 |
|---|---|---|
| Same region | Unknown | 只证明 program names；country-level issuance eligibility 未证明。 |
| Same core Job | Yes | J2：crypto at payment convert/sell 后消费。 |
| Same starting money pool | Yes | USDC 明确出现在 Bybit payment priority；与 AIX 的 stablecoin 起点有直接交集。 |
| Substitutable final outcome | Yes | 都是 card real-world spending。 |
| **Overall** | **Unknown** | Region gate 未证明，不能完成四项 AND。 |

### Unknown/limitations

- 具体国家 eligibility、issuer、full fees、limits、KYC tier 未证明。
- 不能从 “Asia Pacific” 推断 Philippines / Vietnam / Australia。
- 不能因有 Funding Account 就称 global money account。

### Official URL index + 2026-08-29

| # | URL | 支持点 |
|---|---|---|
| By1 | https://www.bybit.com/en/help-center/article/How-to-Consult-Your-Bybit-Card-and-Spending-Information | Funding Account、Spending Power、payment priority、deduction、Crypto Sold。 |
| By2 | https://www.bybit.com/en/help-center/article/How-to-Make-Payments-with-Bybit-Card | payment flow、frozen amount、Mastercard acceptance。 |
| By3 | https://www.bybit.com/en/help-center/article/Bybit-Card-Management-Settings-Guidelines | card programs、card type、pay wallets。 |

## 3. Crypto.com Card

> 结论按当前 region-specific product mode 记录，不做品牌泛化。

### Current service/issuance region

当前缓存官方页面可见 SG 与 AU 两个 region-specific card product 页。Official Help Center 的 Fees & Limits collection 列出多个地区文档：United States、Singapore residential / non-residential、Europe residential / Europe non-residential users in Brazil and select LATAM markets、United Kingdom、Canada、Australia including New Zealand residents holding Australia-issued cards、Bahrain & select GCC markets。

这些证据支持地区化产品族存在，但不构成完整逐国 issuance eligibility 表。Country-level issuance list 仍为 **Unknown**。

### Job inference

- **Primary：J2**。官方 FAQ 明确 cardholders cannot load cryptocurrency onto the card；crypto 必须先 converted to respective market's currency，再 load 到卡。
- Cash Account / debit / credit card top-up 用户可能有更偏 fiat funding 的用法，但当前证据不足以升为主 Job。

### Starting money pool

明确：Crypto.com App 内 **Crypto Wallet**、**Cash Account**，或其他 credit/debit cards，经 Card tab 的 Top up 进入卡余额。

关键限制：crypto cannot be loaded directly；必须 converted to respective market's currency before card load。

### X/Y/cluster

| 维度 | 结论 |
|---|---|
| X | **X1 confirmed**。官方明确 prepaid card 需 top up，消费前有独立 card balance。 |
| Y | **A confirmed**。先 top-up / pre-convert，再 spend。 |
| Strategy Cluster | **S1**。 |

### Account Role

**Spend Feature**。Prepaid card + top-up 模式不构成 Money Account。

### Card role

Visa prepaid card，用于 purchases 与 ATM withdrawals；region-specific fee/limit/tier 结构。SG/AU 页面均为 Visa Prepaid Card/Level Up 语境。

### Current fees/KYC if proven

Singapore residential-address product mode 已证明的示例：

- ATM withdrawal above monthly free limit：2%。
- Debit card top-up 0%；credit card top-up 1%；Apple Pay debit/credit top-up 2%。
- Close account S$50。
- Card replacement Midnight S$45.01，其他 tiers S$50。
- Foreign transaction fee 按tier区分，且有 2026-09-01 起更新条款。
- Inactivity：12 个月无 cardholder-initiated financial activity 后 S$5/month，2026-09-01 起更新为 S$6。

AU product page 已证明 tier/subscription/lockup、CRO rewards、ATM/top-up limits 等 AUD 口径。

未证明：

- 逐国 issuance eligibility。
- KYC tier 与身份核验条款；缓存页只可见 App account / Level Up / apply flow，不能推导完整 KYC 规则。

### Direct four-AND gate

| Gate | 结论 | 依据 |
|---|---|---|
| Same region | Unknown | Crypto.com 有 AU product page，但 AIX 在 AU 只确认 Card；AIX 完整 Wallet→Card journey 仍 Unknown，因此不能写 AU-level Yes。 |
| Same core Job | Yes | J2：crypto 先 convert，再 prepaid card spend。 |
| Same starting money pool | Unknown | 官方页明确 Crypto Wallet / Cash Account / cards，但未在缓存页证明 USDT/USDC 等 stablecoin pool 与 AIX 完全同构。 |
| Substitutable final outcome | Yes | 都是 card real-world spending。 |
| **Overall** | **Unknown** | Region 与 starting money pool gate 均未证明，不能完成四项 AND。 |

### Unknown/limitations

- 不能把 SG/AU fees、tier、limits 推广到其他地区。
- 不能把 Help Center collection 的地区文档名直接当作完整 issuance country list。
- Cash Account 与 Crypto Wallet 的 custody 边界、可支持币种、stablecoin-specific 路径未证明。
- KYC/申卡前置未证明。

### Official URL index + 2026-08-29

| # | URL | 支持点 |
|---|---|---|
| C1 | https://crypto.com/sg/cards | SG region-specific product mode、tier/fees/limits、FAQ、top-up、crypto conversion rule。 |
| C2 | https://crypto.com/au/cards | AU region-specific product mode、tier/fees/limits、FAQ、top-up、crypto conversion rule。 |
| C3 | https://help.crypto.com/en/articles/6043620-crypto-com-prepaid-visa-card-fees-and-limits-singapore-applicable-to-singapore-residential-address-users-only | SG residential-address product mode 的详细 fees/limits。 |
| C4 | https://help.crypto.com/en/collections/3374054-crypto-com-card-fees-limits | current region-specific fees/limits 文档族。 |

## 4. 收口摘要

| Product | X/Y/Cluster | Account Role | Direct four-AND gate |
|---|---|---|---|
| Bitget Wallet Card | `X Unknown × Y A / S1 candidate` | Spend Feature | **Yes**（stablecoin-starting segment） |
| Bybit Card | `X2 × B / S2` | Spend Feature | **Unknown**（region gate 未证明） |
| Crypto.com Card | `X1 × A / S1`（SG/AU current modes） | Spend Feature | **Unknown**（region 与 starting money pool 未证明） |

Step 3 Agent B 到此收口；不做开放研究，不做品牌级泛化，不把候选写成 confirmed。
