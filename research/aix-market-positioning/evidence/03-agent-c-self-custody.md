# Agent C｜Self-custody / stable-spend 重点玩家收口（截至 2026-08-29）

> 用途：为 Step 3 提供本组五个玩家的 mode-level 定位证据底稿。
> 范围：**仅 MetaMask Card、Plasma One、Bleap、Karta、OKX Pay/Card SG**。未新增玩家。
> 时点：官方页面 access/verification 均按 **2026-08-29** 记录。OKX 直连当前页超时，使用 Step 2 curated 2026-08-29 evidence + Wayback snapshot 作为补充来源。
> 纪律：current / future 分开；region issuance 不用 merchant acceptance 或全球覆盖推断；self-custody 不自动等于 Money Account；品牌自家材料只证明该品牌自身，不作为对其他品牌的一手比较证据。

## 0. 结论速览

| 玩家 / mode | Current service / issuance region | Job inference | Starting money pool | X×Y / Cluster | Account Role | Card role | 四项 AND gate vs AIX current |
|---|---|---|---|---|---|---|---|
| **MetaMask Card** | 多国 list；US / UK signup temporarily closed；外区为 waitlist | J2 primary；stablecoin mode 可承接 J1-like spend | 用户自托管钱包中的 crypto / stablecoin（mUSD、wETH、EURe、GBPe、USDC、aUSDC、USDT） | **X3 confirmed；Y=B confirmed；stablecoin-funded X3×C candidate / S5 primary，S4 candidate** | Spend Feature（Card mode）；页面另有 Money Account mode，但不得套用到 Card mode | 将自托管钱包资产接到 Mastercard 的现实消费 rail | **No**（current list 与 AIX Phase 1 PH/VN/AU 无重合） |
| **Plasma One** | Current live 处理；issuance/service country list Unknown；页面称 Visa acceptance 180+ countries，但明确 geographic eligibility limits apply | J1 primary（stablecoin 当日常钱）；J2 secondary | 用户自有 stablecoin / USD-backed balance | **X3×C / S4** | Money Account-leaning；unified/same-balance 细节未钉死 | Stablecoin balance backing card 的 Visa spend rail | **Unknown**（region issuance Unknown） |
| **Bleap** | Europe current；Mexico / Brazil current；更多 countries coming soon；具体 country list 另查 Help Center | J1 primary；J2 secondary | bank transfer 或 crypto/stablecoin，稳定为 EUR/USD stablecoin spendable balance | **X3×C / S4** | Money Account-leaning；unified/same-balance 细节未钉死 | Self-custodial wallet 关联的 Mastercard spend rail | **No**（Europe/MX/BR 与 AIX Phase 1 无重合） |
| **Karta** | Current live card / crypto top-up / crypto send；service country list Unknown，仅称 products may not be available to all customers | J1-leaning，但 current 闭环不足 | Crypto top-up：USDT / USDC 多链 | **X Unknown；Y=A confirmed；S4 direction，S1-candidate boundary** | Account-adjacent；Money Account 不成立 | Crypto top-up 后启用的 Visa Signature spend rail | **Unknown**（region Unknown） |
| **OKX Pay/Card SG** | **仅 SG mode**；不推广全 OKX | J1 primary；secondary J2 | OKX Pay 中的 USDT / USDC | **X3×C / S4**（沿用 Step 2 落位） | Spend Feature / Account-adjacent | SG 场景下的 stablecoin direct spend / Visa spend rail | **No**（SG 与 AIX Phase 1 无重合） |

> 四项 AND gate 的比较基准来自 `evidence/02-agent-f-aix-current-position.md`：AIX Card Phase 1 = PH / VN / AU；AIX 起始资金池为稳定币；核心 outcome 为稳定币余额转为现实消费。四项条件必须同时成立，任一未证即 Unknown，任一确定不成立即 No。

## 1. MetaMask Card

### Current service / issuance region

- Current FAQ 明确列出 current available countries：Andorra, Argentina, Austria, Belgium, Brazil, Bulgaria, Canada, Chile, Colombia, Costa Rica, Croatia, Cyprus, Denmark, Dominican Republic, El Salvador, Finland, France, Germany, Gibraltar, Greece, Guatemala, Guernsey, Hungary, Iceland, Ireland, Isle of Man, Italy, Jersey, Liechtenstein, Luxembourg, Malta, Mexico, Monaco, Netherlands, Norway, Panama, Poland, Portugal, Romania, Slovakia, Slovenia, Spain, Sweden, Switzerland, Uruguay。
- 同一 FAQ 写明：**US 与 UK signup temporarily closed**；支持区外用户加入 waitlist。
- 页面另有“Metal Card is now available in the US”与“available in ... the US, and the UK”的旧/新表述并存。因此按更明确的 issuance FAQ 处理：US/UK current signup closed；不把 Metal Card 文案覆盖为 full card issuance。

### Job inference

- Primary：**J2**。官方核心表述为“spend crypto IRL / instant spending direct from your crypto wallet / spend crypto anywhere”，用户从已持有 crypto 获得日常购买力。
- Secondary：页面当前也支持 mUSD / USDC / USDT 等 stablecoin source，可承接持有稳定币用户的现实支付需求，但不应抹掉其 crypto instant-convert 主定位。

### Starting money pool

- 用户钱包中自托管的 crypto / stablecoin。页面列举 token：**mUSD、wETH、EURe、GBPe、USDC、aUSDC、USDT**；网络为 Linea、Solana、Monad、Base，并注明 US 不支持 Solana、NY/TX 不支持 Base 等例外。

### X / Y / Cluster

- **X3 confirmed**：官方明确 funds stay in wallet / maintain self-custody until payment。
- **Y=B confirmed**：支付时将 crypto converted to local currency。
- **Stablecoin-funded mode 为 X3×C candidate**：mUSD / USDC / USDT 支持 stable-value source，但页面没有逐 token 的 spend mechanics 足以把它独立确认成与 crypto convert 完全等价的 C mode。
- **Cluster**：S5 primary；S4 candidate（仅限 stablecoin-funded mode）。

### Account Role

- **Card mode = Spend Feature**。
- 页面另有 **Money Account** 模式，支持 add funds、convert to mUSD、earn、spend 等。这是 MetaMask 体系内的另一个 mode，不能反向把 Card 自动升级为 Money Account。

### Card role

- Mastercard 实体/虚拟消费 rail；核心是把 MetaMask wallet 的资产直接连到现实支付，而非独立长期资金账户本身。

### Fees / KYC

- Fees：页面同时出现 “no additional MetaMask fees / minimized network costs” 与 “charged a minimal fee for each transaction” 的表述；未在本页确认完整费用表，因此不写具体费率。
- KYC：本页未见可确认的完整 KYC/identity 阶梯，标 Unknown。

### Direct four-AND gate

| 条件 | 判断 |
|---|---|
| Same region | **No**：current list 与 AIX Phase 1 PH/VN/AU 无重合；US/UK closed 不改变判断 |
| Same core Job | Yes / partially confirmed：J2 与稳定币 spend 均与 AIX 核心问题相邻 |
| Same starting money pool | Partially：MetaMask 起点含 volatile crypto；stablecoin source 支持但非唯一 |
| Substitutable final outcome | Yes：现实卡消费 |
| **Overall** | **No**（region 已确定不重合） |

### Current vs future

- Current：card issuance list、wallet-until-payment spend、crypto conversion、stablecoin token support。
- Future / boundary：外区 waitlist；“more countries rolling out soon”不能写入 current；Money Account 与 Card mode 必须分开。

### Unknown / limitations

- 各 mode 与 token 的扣款细节、issuer/program manager、US/UK 状态矛盾、完整 fees/KYC 未核。

### Official URLs

- https://metamask.io/card — accessed/verified 2026-08-29。

## 2. Plasma One

### Current service / issuance region

- 按 Step 2 final review 与用户硬约束，**Plasma One 按 current live 处理，不得降级为 early access**。
- Current 页面同时包含 app download / App Store 与 Google Play 路径、issuance 说明和“Join Plasma One now / Download”类 CTA；但也残留 hero CTA “Sign up to the waitlist” 与 analytics id `one_wallet_get_early_access`。这是页面口径不一致，本稿按 current live 处理并保留矛盾提示。
- **具体 issuance/service country list Unknown**。页面称 Visa card 可在 180+ countries 的商户处使用，同时明确 “Geographic, regulatory, and other eligibility limits apply”。因此 180+ 只是 acceptance/营销口径，不是 issuance eligibility。

### Job inference

- Primary：**J1**。定位为 stablecoin card / everyday money：deposit stablecoins、access USD、send instantly、spend globally。
- Secondary：Earn vault 与 bank off-ramp 使其覆盖稳定币持有、转账和法币出金，但主要仍是 stablecoin as money。

### Starting money pool

- 用户自有 stablecoin / USD-backed balance。官方 FAQ：“Plasma One does not custody your assets. The stablecoin balance backing your Plasma One card is owned and custodied by you.”

### X / Y / Cluster

- **X3×C**：self-custody / user-owned stablecoin balance 直接 backing card。
- **Cluster：S4**。Step 2 final review 已提示：X3×C 确认度高于 “candidate”，后续不应把 Plasma One 仅当弱 candidate。

### Account Role

- **Money Account-leaning / Money Account evidence strong**：current 页面支持 stablecoin deposit、send、receive、card spend、Earn、bank off-ramp，并称 virtual account details 可用于 receive salary / pay bills / move fiat in and out。
- 仍不能只凭营销语句断言 **unified/same-balance** 技术结构；该细节待产品级核验。

### Card role

- Visa card 是 stablecoin balance 的现实消费 rail；card issued by Rain, a Visa Principal Member；global account services powered by Bridge。Bridge 实体按 US / EEA / other residents 分开，但这不等于具体可服务国家清单。

### Fees / KYC

- Fees（proven only）：Plasma One does not charge any Plasma One fees；bank withdrawals 等场景存在 partner fees 且 app confirm 前展示；zero-fee USDT transfers 限 Plasma routes。
- KYC：本页未确认完整 KYC/identity 流程，标 Unknown。

### Direct four-AND gate

| 条件 | 判断 |
|---|---|
| Same region | Unknown：AIX PH/VN/AU 与 Plasma current issuance overlap 未证 |
| Same core Job | Yes：J1 stablecoin as money 与 AIX 高度相邻 |
| Same starting money pool | Yes：均为 stablecoin |
| Substitutable final outcome | Yes：现实卡消费/资金使用 |
| **Overall** | **Unknown**（region Unknown） |

### Current vs future

- Current：self-custody stablecoin balance、send/receive/spend、Visa card、Earn、bank off-ramp、Bridge-powered account services。
- Future / boundary：waitlist/early-access 残留文案不得当作 current；180+ countries 不得转写为 issuance list；Bridge 各实体可用范围不能外推为具体国家。

### Unknown / limitations

- Unified/same-balance 语义、具体 country matrix、Google/Apple Pay per-region availability、完整 KYC 与 fee table 未核。

### Official URLs

- https://www.plasma.to/one/ — accessed/verified 2026-08-29。

## 3. Bleap

### Current service / issuance region

- Current FAQ 明确：**available across Europe**；LATAM expansion 中 **Mexico and Brazil already available**；more countries coming soon。具体 supported countries / accepted documents 需查 Help Center。
- Europe 是当前核心服务范围；MiCA CASP 由 Latvijas Banka 授权，Bleap SIA 为主体。

### Job inference

- Primary：**J1**。官方称 self-custodial money app，可 hold/send/spend/save without a bank in between；EUR/USD stablecoin spendable balance 直接用于现实消费。
- Secondary：**J2**。用户可从外部 crypto wallet 转入其他 token，再 convert 成 EUR/USD，但这一步是显式 convert，不是消费时自动卖币。

### Starting money pool

- Bank transfer 或 crypto/stablecoin 存入。EUR / USD 稳定为 **EURA / USDC 等 stablecoin equivalents**；页面称 stablecoins sent via supported networks automatically become USD/EUR spendable balance。

### X / Y / Cluster

- **X3×C**：官方明确 “spend stablecoins directly from a self-custodial wallet”、self-custodial MPC wallet、card uses the EUR/USD balance you hold。
- **Cluster：S4**。Step 2 曾保留 candidate；本轮 current 页面已提供 direct stable-value deduction 的较强证据。

### Account Role

- **Money Account-leaning**：current 页面明确 hold/send/spend/save、bank transfer/crypto deposit、send money、spend。
- 但 unified/same-balance 技术细节与 wallet/spendable balance 的法律控制关系未独立核验，不能直接写成完全成立的 Money Account。

### Card role

- Mastercard 是 self-custodial wallet / spendable balance 的现实消费 rail。

### Fees / KYC

- KYC（proven）：sign-up 后需 email/phone 与 identity verification；KYC status 会影响 SEPA withdrawals 等能力。
- Fees（proven only）：adding money、converting、spending free；card issuance free；无 monthly/annual fee；cashback in USDC，最高 20%。MiCA 覆盖范围与 Savings/Trading 等非 MiCA 服务分开。

### Direct four-AND gate

| 条件 | 判断 |
|---|---|
| Same region | **No**：Europe/MX/BR 与 AIX Phase 1 PH/VN/AU 无重合 |
| Same core Job | Yes：J1/J1-like stablecoin spend |
| Same starting money pool | Yes/partially：stablecoin 与 bank onramp 均有 |
| Substitutable final outcome | Yes：现实卡消费 |
| **Overall** | **No**（region 已确定不重合） |

### Current vs future

- Current：Europe、Mexico、Brazil、self-custodial wallet、EUR/USD spendable balance、card、identity verification、cashback。
- Future / boundary：“expanding into Latin America / more countries coming soon”不得当 current；Savings/Trading 的监管覆盖不能外推到 card 模式。

### Unknown / limitations

- 具体 country list、issuer/BIN、unified balance 细节、MiCA 服务与 card spend 的边界关系未核。

### Official URLs

- https://www.bleap.finance/ — accessed/verified 2026-08-29。

## 4. Karta

### Current service / issuance region

- Current live：Telegram bot / app、quick verification、stablecoin top-up、activate virtual Visa card、card payments、send to external crypto wallet。
- Receive from / Get Paid Your Way、Sent Payments（global payouts）页面明确标 **Coming Q3 2026**；bank transfer 也写 coming soon；bank withdrawals 写 coming soon。这些一律是 future。
- **Service/issuance country list Unknown**；页面仅称 “Karta products may not be available to all customers”。不得用 “spend at 150M merchants worldwide” 或 Visa acceptance 推导 issuance region。

### Job inference

- Current 证据更接近 **J1-leaning**：USDT/USDC 余额变成 Visa 消费力。
- 但 receive/get paid/global payouts/bank rails 仍是 future，因此不能证明完整 stablecoin money account 闭环；Job 定级只能保守。

### Starting money pool

- Crypto top-up：**USDT 或 USDC**，网络为 TRON(TRC-20)、Ethereum、BNB Smart Chain、Polygon、Arbitrum、Optimism、Base、Solana。
- Bank transfer 为 coming soon，不得当 current starting pool。

### X / Y / Cluster

- **Y=A confirmed**：FAQ 明确 top up your balance to activate virtual card；存在 pre-fund / top-up 行为。
- **X Unknown**：页面自称 only you control your wallet / self-custody，但同时要求 top up 到 balance 并刷卡；现有页面不足以证明 top-up 后资产仍保持在 X3 用户控制 wallet，也不足以证明其落入 X1 dedicated balance。不能凭 self-custody 文案直接写 X3。
- **Cluster：S4 direction，S1-candidate boundary**。不硬归 S4，也不硬归 S1。

### Account Role

- **Account-adjacent**。current 只有 crypto top-up、card spend、send to crypto wallet；receive/get paid/send payouts 与 bank withdrawal future，因此 **Money Account 不成立**。

### Card role

- Visa Signature virtual/physical card 是当前核心现实消费 rail；Apple Pay/Google Pay/ATM 为页面宣称能力，但本稿不把它们外推为所有 region 可用。

### Fees / KYC

- KYC（proven）：Telegram bot / app 内 quick verification，页面称 takes up to 5 minutes；完整 KYC 等级未核。
- Fees（proven only）：Visa Virtual activation 5 USDT（页面显示从 30 USDT 降价）；Visa Physical from 100 USDT；Virtual Accounts free；Crypto Top-Up network fee only；card payments 1.5%；ATM withdrawal 1.5% + 1 USDT；页面另列 SEPA/SWIFT 发送费率，但这些 bank rails 与 Receive/Send payouts 的 current 状态冲突，必须按 future/未生效处理，不能当 current fee。

### Direct four-AND gate

| 条件 | 判断 |
|---|---|
| Same region | Unknown：issuance/service region Unknown |
| Same core Job | Yes/partially：stablecoin spend 方向相邻，但 current 闭环不足 |
| Same starting money pool | Yes：USDT/USDC |
| Substitutable final outcome | Yes/partially：card spend 已见，但 broader money usage future |
| **Overall** | **Unknown**（region Unknown，且 current 完整性不足） |

### Current vs future

- Current：crypto top-up、quick verification、activate virtual Visa、card spend、send to external crypto wallet、cashback claims。
- Future：Receive / Get Paid Your Way、Sent Payments / global payouts、bank transfer、bank withdrawals。

### Unknown / limitations

- Custody/top-up 后的 X、issuer、country matrix、self-custody 与 card balance 的技术关系、完整费用生效范围未核。

### Official URLs

- https://karta.io/ — accessed/verified 2026-08-29。

## 5. OKX Pay/Card SG

### Current service / issuance region

- **只使用 SG mode**，不得推广为全 OKX。
- Step 2 curated 2026-08-29 evidence 记录：smart wallet until pay、stablecoin direct spend、SG Visa program。本轮 2026-08-29 直连 `https://www.okx.com/en-sg/pay` 超时，未新增 live 抓取；使用该 curated evidence，并用 Wayback 2026-03-11 snapshot 复核 SG 页面当时存在的 stablecoin top-up、GrabPay merchant spend、pay friends、self-custody/custody-free-fees 营销表述。Wayback snapshot 仅作 fallback，不替换 Step 2 2026-08-29 curated source。

### Job inference

- Primary：**J1**。SG 页面定位 money app：USDT/USDC into OKX Pay，之后 stablecoin direct spend / pay stores / pay friends。
- Secondary：若用户来自 exchange 持仓或用 crypto 支付，可覆盖 J2，但当前证据主轴是 stablecoin payment。

### Starting money pool

- **USDT / USDC** in OKX Pay。

### X / Y / Cluster

- **X3×C / S4**，沿用 Step 2 final 落位：smart wallet until pay；stablecoin direct spend。

### Account Role

- **Spend Feature / Account-adjacent**。页面显示 send/receive/pay 能力，但 Step 2 未确认 unified/same-balance 的完整 Money Account 结构，不能升级。

### Card role

- SG 场景下的 stablecoin direct spend / Visa spend rail；具体 card issuance eligibility 与 program 细节不得从 Pay 页面外推。

### Fees / KYC

- Fees（proven in snapshot only）：no fees, no gas for send/pay 营销表述。完整 fee table 与 exceptions 未核。
- KYC：本组证据未确认，标 Unknown。

### Direct four-AND gate

| 条件 | 判断 |
|---|---|
| Same region | **No**：SG mode 与 AIX Phase 1 PH/VN/AU 无重合 |
| Same core Job | Yes：stablecoin direct spend |
| Same starting money pool | Yes：USDT/USDC |
| Substitutable final outcome | Yes：现实支付/转账 |
| **Overall** | **No**（region 已确定不重合） |

### Current vs future

- Current：SG Pay/Card mode、USDT/USDC、stablecoin direct spend、pay stores/friends。
- Future / boundary：页面 disclaimer “may not be available in all jurisdictions”；任何 non-SG OKX 落位都必须另证。

### Unknown / limitations

- 2026-08-29 direct fetch 失败；issuer、SG issuance eligibility、unified balance、KYC、完整 fee table 未核。

### Official URLs

- https://www.okx.com/en-sg/pay — Step 2 curated accessed/verified 2026-08-29；本轮直连超时。
- http://web.archive.org/web/20260311190453/https://www.okx.com/en-sg/pay — Wayback fallback snapshot 2026-03-11，检索于 2026-08-29。

## 6. 横向 Unknown 与下一步核验问题

1. **Region matrix**：Plasma One 与 Karta 的 issuance/service country list 是最大 gap；不能用 global/acceptance 数字补。
2. **Custody / balance transition**：Karta self-custody 文案与 top-up balance 的关系；Bleap spendable balance 的链上控制关系；Plasma One unified/same-balance 细节。
3. **Stablecoin mode vs crypto mode**：MetaMask 已同时具备 crypto 与 stablecoin source，需按 mode 拆开，不能只用 S5 覆盖全部。
4. **Future 不得升级**：Karta Q3 2026 receive/payments、Bleap “more countries coming soon”、MetaMask waitlist、Plasma One 残留 waitlist 文案都不得当 current。
5. **直接竞品判定**：本组没有一家能凭现有证据对 AIX current Phase 1 组成四项 AND 的 direct competitor；region 是主要阻断点，Plasma/Karta 因 region Unknown 只能保留 Unknown。

## 7. Evidence sources

| Source | Date | Role |
|---|---|---|
| MetaMask official Card page | accessed/verified 2026-08-29 | Primary official evidence |
| Plasma One official page | accessed/verified 2026-08-29 | Primary official evidence |
| Bleap official homepage/FAQ bundle | accessed/verified 2026-08-29 | Primary official evidence |
| Karta official homepage/FAQ bundle | accessed/verified 2026-08-29 | Primary official evidence |
| OKX SG Pay official page | Step 2 curated accessed/verified 2026-08-29 | Reused prior official evidence |
| OKX SG Pay Wayback snapshot | snapshot 2026-03-11；retrieved 2026-08-29 | Fallback corroboration only |
| `evidence/02-sources.md` | 2026-08-29 | Prior curated source index |
| `evidence/02-agent-f-aix-current-position.md` | 2026-08-29 | AIX internal comparison baseline |
