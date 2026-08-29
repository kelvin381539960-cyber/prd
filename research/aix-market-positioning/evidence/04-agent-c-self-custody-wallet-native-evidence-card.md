# Step 4 Agent C｜Self-custody / Wallet-native J2 市场证据卡（Closeout）

> 状态：Step 4 Agent C closeout（2026-08-30）。**只收口，不再浏览**。
> 证据基础：已采集官方页面缓存 `/tmp/agentc4.EgHRFp/`（2026-08-29 访问）+ Step 1–3 已评审定义（`01-market-overview-and-user-jobs.md`、`02-ecosystem-map.md`、`03-player-positioning.md`、`evidence/03-agent-c-self-custody.md`、`evidence/03-agent-e-crosscheck.md`、`evidence/02-agent-f-aix-current-position.md`）。
> 纪律：AIX 仅是未来进入者；当前 AIX 事实（X1 / Y Unknown / Species Unknown / Account Role 最多 Account-adjacent）**不定义市场**。本卡只把「玩家官方页面 + Step 1–3 定义」整理成证据卡，不新增市场事实、不重新联网、不改结论。
> 校验：本卡全部官方摘录已逐条在缓存文本中做 verbatim 匹配校验（2026-08-30，本地离线脚本，全部通过）。

---

## 1. Y 轴校验表（自托管 / Wallet-native J2 维度）

> 作用：本组是"消费时扣哪个余额 + 购买力怎么形成"的 Wallet-native 证据层；**不是 AIX 的 current 事实层**。AIX 只在文末以 future-entrant 对照出现。

| 玩家 / 官方页面 | 消费容器 (X) | 购买力机制 (Y) | Step 1–3 结论 | 关键证据（缓存官方原文摘录） |
|---|---|---|---|---|
| MetaMask Card（官方站点页面） | X3（self-custody until payment，S5 primary） | B（结算点转换）；stablecoin mode 为 S4 candidate | X3×B / S5 primary；区域 = No（current list 不含 PH/VN/AU） | "…anywhere Mastercard is accepted"；"You control your funds until the moment of payment"；"maintain custody of tokens until you pay"；"…converted to the local currency at checkout"；"One tap funding / Easily deposit and manage your card funds directly on the MetaMask mobile app" |
| Plasma One（官方站点） | X3 self-custody（S4 强邻接/候选） | C（stablecoin direct deduction） | X3×C / S4；region Unknown（未公布 country list） | "The stablecoin balance backing your Plasma One card is owned and custodied by you."；"Plasma One does not custody your assets."；"…Visa card in 180+ countries"（acceptance marketing，不作 issuance）；"Geographic, regulatory, and other eligibility limits apply." |
| Bleap（官方站点 + Helper 中心） | X3 self-custody MPC（S4 候选） | C（EUR/USD stablecoin spendable balance） | X3×C / S4；region No（Europe/MX/BR current） | "A self-custodial money app where you can hold, send, spend and save without a bank in between."；"…spend stablecoins directly from a self-custodial wallet"；"The Bleap card spends directly from your euro or dollar balance, anywhere Mastercard is accepted…" |
| Karta（官方站点） | X Unknown（self-custody 文案 vs top-up 后容器未证） | A（top-up → activate → spend） | Y=A confirmed / X Unknown / S4 direction–S1 candidate boundary；region Unknown | "Only you control your wallet."；"…top up your balance to activate your virtual card — that's all!"；"Bank transfer: Coming soon."；"Receive from Get Paid Your Way Coming Q3 2026" |
| OKX Pay/Card SG（官方 SG 页面） | X3（smart wallet until payment，S4） | C（stablecoin direct spend） | X3×C / S4；region No（仅 SG mode） | "Your crypto remains in your smart wallet until the point of payment, without moving funds into a separate custodial wallet in advance."；"Once your OKX Pay wallet is funded with stablecoins, you can tap and pay directly." |
| ether.fi Direct Pay（官方 Helper） | X3（Vault direct deduction，S4 candidate） | C（USDC/LiquidUSD、结算点转换） | X3×C / S4 candidate；region 依据 available 页 PH Yes / restricted 页 VN 冲突 / AU Yes | "…immediately deducted from your ether.fi Vault from your USDC or LiquidUSD balance"；"Any USDC balance…used first, then LiquidUSD…"；"Your crypto is converted to the required currency at the point of sale." |
| Gnosis Pay / Gnosis Card（官方站点 + 开发者文档） | X3（Safe Smart Account / self-custodial） | C（stablecoin Visa debit） | Step 2 S4 candidate/infrastructure reference；非 Step 3 玩家表成员 | "Take control of your money through your SAFE account. You own your keys, you own your crypto."；"Gnosis Pay’s first product is Gnosis Card: a stablecoin based visa debit card…"；"…80+ million Visa merchants"；"Card issued by Monavate Limited pursuant to licence by VISA Europe Limited" |

---

## 2. 逐玩家官方证据卡（自托管 / Wallet-native）

### 2.1 MetaMask Card（官方页面方式；原 support URL 为重定向 stub）

- 缓存文件：`metamask-card-wayback-20260806.html`（官方站点快照，2026-08-06 页面版本；support URL `https___support.metamask.io_manage-crypto_metamask-card_what-is-metamask-card_.html` 仅含 meta refresh 重定向，无可提取正文）。
- 机制：X3×B / S5 primary；stablecoin mode 为 S4 candidate（mUSD/USDC/USDT 支持）。
- 地区：current countries 明确列表；**US/UK signup temporarily closed**；外区 waitlist；PH/VN/AU 不在列表。
- 关键证据（2026-08-06 快照 verbatim）：
  - "Instant spending directly from your crypto wallet, anywhere Mastercard is accepted."
  - "You control your funds until the moment of payment, all managed directly in your MetaMask wallet."
  - "You maintain self-custody of your funds until the second you pay."
  - "Your crypto is converted to the local currency at checkout, eliminating the need for centralized exchanges or third party platforms."
  - "MetaMask Card currently supports nine tokens: mUSD , wETH , EURe , GBPe, USDC , USDT ."（HTML 文本抽取含空格；页面实际仅列六种）
  - "Where can I use my MetaMask Card? Globally! MetaMask Card functions like a crypto debit card that lets you spend your money IRL anywhere Mastercard is accepted, at over 150 million merchants worldwide."（acceptance marketing, 不作 issuance）
  - "Signups for MetaMask Card in the US and the UK are temporarily closed."
- Unchanged Step 3 结论：**Not Direct current**（region No）；market Y 轴贡献 = S5；stablecoin-mode S4 candidate 不得合并为 S4 confirmed。
- 本卡新证据标记：除原 URL 外，support URL 为 redirect stub；官方页面快照可复现此结论。

### 2.2 Plasma One（官方站点 + footnotes）

- 缓存文件：`plasma-one.html` / `https___www.plasma.to_one_.html`（同一内容 duplicate，2026-08-29 访问）。
- 机制：self-custody stablecoin balance → Visa card；X3×C / S4 strong-adjacent（Step 2 final；Step 3 保留 "X3×C / S4"、Money Account-leaning）。
- 地区：具体 country list **Unknown**；"180+ countries" 是 Visa acceptance 营销口径；footnote 9 "Geographic, regulatory, and other eligibility limits apply, and are subject to change." 明确限定。
- 关键证据（verbatim）：
  - "Who custodies my money? You do. Plasma One does not custody your assets. The stablecoin balance backing your Plasma One card is owned and custodied by you."
  - "One account for global money"；"Your Stablecoin Card for Everyday Money"。
  - "Anywhere Visa cards are accepted, online and in store, in over 180 countries."
  - "Global account services for Plasma One are powered by Bridge. Services to US residents are provided by Bridge Building Inc.; EEA residents by Bridge Building Sp. Z.o.o.; and all other residents by Bridge Building Limited."
  - "The Plasma One Card is issued by Rain, a Visa Principal Member, pursuant to a license from Visa."
  - "Plasma One does not charge any additional fees. Some transactions, such as foreign exchange and bank withdrawals, include partner fees, which are shown in the app before you confirm."
  - "Can I withdraw from Plasma One to my bank account? Yes. Send funds to your bank using off-ramps directly inside the app. The rails available to you depend on your region."
  - "Send and receive stablecoins across borders in seconds with zero fees"；footnote 7: "Zero-fee USD₮ transfers refer to Plasma routes; third-party fees may apply"。
  - "PCI DSS v4.0.1 Level 1 Service Provider - SAQ D"（page claims audit/compliance; 不作为业务事实）。
- 边界：unified/same-balance 细节未钉死；不能因 "global account services" 自动升级 Money Account confirmed（Step 3 保留 Money Account-leaning）。

### 2.3 Bleap（官方站点 + Helper Center）

- 缓存文件：`bleap.html` / `https___www.bleap.finance_.html`（duplicate）；`https___help.bleap.finance_en_articles_11088792-am-i-eligible-for-card.html`（eligibility，2026-07-03 written）。
- 机制：MPC self-custody + EURA/USDC spendable balance → Mastercard；X3×C / S4。
- 地区：current = Europe + Mexico + Brazil；**PH/VN/AU 不在**；eligibility page 还证明 PH、Viet Nam 在 restricted nationalities 列表（不得作 current coverage）。
- 关键证据（verbatim）：
  - "A self-custodial money app where you can hold, send, spend and save without a bank in between. That's Bleap."
  - "Bleap is a crypto card built for the European market, issued under a MiCA license, that lets you spend stablecoins directly from a self-custodial wallet."
  - "The Bleap card spends directly from your euro or dollar balance, anywhere Mastercard is accepted, online or in-store. You can spend in both currencies: the card automatically uses the balance you hold, so there is nothing to top up and you never need to convert between euros and dollars."
  - "Euros are held as EURe and dollars as USDC, the digital version of each currency, always at a 1:1 rate."
  - "Bleap wallets use MPC (multi-party computation) technology, a form of self-custody where your private key is split into separate shares instead of being stored in one place. No single party, including Bleap, ever holds your complete key."
  - "Bleap is available across Europe and is expanding into Latin America, where it is already available in Mexico and Brazil, with more countries coming soon."
  - "Card issuance: Free"; "Monthly or annual fee: None".
  - "You can spend any token available on Solana, Base, or Arbitrum with the Bleap card"；"Euro (EURe) and dollar (USDC) balances are spent directly."；"Any other token... is converted to euros or dollars in one tap, in seconds, with no fees, and then spent with the card."
  - Eligibility page: "…unable to issue cards to users who either: Reside outside of the EEA or Switzerland…"; "Hold nationality from any of the countries listed below… Philippines (the)… Viet Nam…"
  - Regulator: "Bleap SIA holds CASP license No. 27-55/2026/14, granted by Latvijas Banka (the central bank of Latvia) on 25 June 2026…"
- 边界：Europe+MX/BR 是 current；"more countries coming soon" 是 future，不升级；同一页面把 MiCA CASP 与 Savings/Trading 非 MiCA 服务分开，卡模式不得外推。

### 2.4 Karta（官方站点 + FAQ）

- 缓存文件：`karta.html` / `https___karta.io_.html`（duplicate，2026-08-29 访问）。
- 机制：top-up（USDT/USDC 多链）→ activate virtual Visa → spend；**Y=A confirmed / X Unknown**；receive/payouts 是 future（Coming Q3 2026）。
- 地区：具体 service country list **Unknown**；"150M merchants" 是 merchant acceptance 营销口径；"Karta products may not be available to all customers."
- 关键证据（verbatim）：
  - "Your Money is Always Yours"（标题）；"Only you control your wallet. Secure by design — send, receive, and manage your crypto."
  - "Receive from Get Paid Your Way Coming Q3 2026"; "Sent Payments Coming Q3 2026"; "Bank transfer: Coming soon"; "Bank withdrawals are coming soon — stay tuned!"
  - "Just start the Karta Telegram bot , open the app within Telegram, complete a quick verification (it takes up to 5 minutes). After that, top up your balance to activate your virtual card — that's all!"（HTML 文本抽取含空格）
  - "Stablecoins: USDT or USDC on Tron (TRC-20), Ethereum, BNB Smart Chain, Polygon, Arbitrum, Optimism, Base, Solana."
  - "Use Karta Visa Signature® worldwide. Instant virtual and physical cards. Compatible with Apple Pay, Google Pay, and global ATM cash access."
  - "Karta works anywhere Visa is accepted — online, in-store, and at ATMs. Availability depends on local regulations and partner coverage."（对应 "Karta products may not be available to all customers."）
  - Fees current（页内可见）："Visa Virtual 5.00 USDT"; "Visa Physical from 100.00 USDT"; "Card payments 1.5%"; "ATM Withdrawal 1.5% + 1 USDT"; "SEPA (EUR) 1,5% + €2"; "SWIFT (USD) 1,4% + $2"（SEPA/SWIFT 与 bank rails future 状态冲突，不得当 current usable fee）。
  - FAQ 中 "There's a one-time fee of 30 USDT 5 USDT" 是页面不同位置的同一 activation fee 表述（30→5 促销态）；本卡保留该表面冲突。
- 边界：current = top-up / card / crypto send；receive / payouts / bank rails = future；不可因 "Self-Custody wallet" 文案直接证明 top-up 后仍 X3。

### 2.5 OKX Pay/Card SG（官方 SG 页面）

- 缓存文件：`okx-sg-pay.html` / `https___www.okx.com_en-sg_pay.html`（duplicate，2026-08-29 访问）。
- 机制：smart wallet until payment；USDC stablecoin direct spend；X3×C / S4（沿用 Step 2）。
- 地区：**仅 SG mode**；页面 disclaimer "Products or services shown on this page may not be available in all jurisdictions."
- 关键证据（verbatim）：
  - "Pay directly with USD stablecoins everywhere Visa® is accepted."
  - "Once your OKX Pay wallet is funded with stablecoins, you can tap and pay directly."
  - "Your crypto remains in your smart wallet until the point of payment, without moving funds into a separate custodial wallet in advance."
  - "We don't add fees when you spend your own money"；"Zero transaction or FX fees, at home and abroad. A transparent, market-based spread applies only when conversion is required."（营销费率 claim；完整 fee table 未在本页证明）
  - "Made for Singapore. Built for everyday."
  - "OKX SG Pte Ltd is a Major Payment Institution licensed by the Monetary Authority of Singapore."
  - "Earn up to 10% cashback on all eligible purchases, in-store and online. Cashback paid in USDG."（rewards 非本卡直接机制证据）
- 边界：不推广到全 OKX；issuer / unified balance / KYC / 完整费表仍 Unknown。

### 2.6 ether.fi Cash Card Direct Pay / Borrow（官方 Helper，2026-08-20 dateModified）

- 缓存文件：`etherfi-directpay.html`（官方文章，dateModified 2026-08-20）；`etherfi-countries.html`（2026-08-02）；`etherfi-restricted.html`（2026-08-23）；`etherfi-personal.html`（官方站点）。
- 机制（mode 级分开）：
  - Direct Pay：X3×C candidate（Vault USDC/LiquidUSD direct deduction；结算点转换）。
  - Borrow：X3 candidate × D / S6-candidate（不卖币、抵押借款）。
- 地区：available 页列出 **Philippines**、Australia；restricted 页列出 **Vietnam** 为 unsupported；局部冲突记录，不裁决。
- 关键证据（verbatim）：
  - Direct Pay: "When you make a purchase with the Cash card, the funds are immediately deducted from your ether.fi Vault from your USDC or LiquidUSD balance."；"Any USDC balance in your Vault will be used first, then LiquidUSD as a secondary spend asset if there isn't any USDC available."；"Transactions are processed instantly from your available balance"；"No interest charges or fees beyond standard transaction costs"；"Your crypto is converted to the required currency at the point of sale"
  - Borrow: "Instead of selling your crypto, you use it as collateral to borrow funds for your purchase."；"You can spend without selling your crypto assets"；interest accrues immediately via Aave v4, variable APY, no grace period/billing cycle（interest mechanics evidence）。
  - Personal page: "Fully non-custodial, you retain full ownership and control of your funds while accessing everything ether.fi has to offer."；"Top up your ether.fi Cash card with the assets you hold and use it for everyday purchases."；"Hold, earn, borrow, spend, trade, and send from one account that works the way you do."（non-custodial claim + account narrative；Account Role 仍 Unknown / Account-adjacent candidate，不升级 Money Account）。
- 边界：Direct Pay 与 Borrow 是两个 mode；非质押/非稳定币资产不得混入 Direct Pay 结论；full consumer fee table 未证明。

### 2.7 Gnosis Pay / Gnosis Card（官方站点 + 开发者文档，补充参考）

- 缓存文件：`https___gnosispay.com_.html`（官方站点）；`https___docs.gnosispay.com_.html`（官方开发文档）。
- 机制：Safe Smart Account self-custody；stablecoin Visa debit；X3×C direction（Gnosis Chain 生态示例）。
- 关键证据（verbatim）：
  - Docs: "Gnosis Pay’s first product is Gnosis Card: a stablecoin based visa debit card, enabling users to spend their digital assets in the traditional economy using the Gnosis Pay network."；"Take control of your money through your SAFE account. You own your keys, you own your crypto."；"Accepted at 80+ million Visa merchants worldwide."；"Earn up to 5% cashback on eligible transactions based on the amount of GNO you hold in your wallet."
  - Site: "Your users control their funds via Safe Smart Accounts"；"Ship stablecoin card programs in minutes"（B2B infra）；"The Gnosis Pay Debit Card issued by Monavate Limited pursuant to licence by VISA Europe Limited"（issuer disclosure）。
- 边界：早期 Step 2 将其列为 S4 candidate / infrastructure reference，不作为 Step 3 玩家表成员；本卡仅作为 Wallet-native 机制补充证据。

---

## 3. 与 Step 1–3 的引用对账（本卡只搬运，不改判）

| 引用来源 | 本卡使用方式 | 一致性 |
|---|---|---|
| `01-market-overview-and-user-jobs.md` | J2 = 已持有 Crypto → 现实购买力；stablecoin 属于 J2；three-job family | 原样引用 |
| `02-ecosystem-map.md` | X1/X2/X3 定义、Y=A/B/C/D、S1–S6、Account Role overlay、region 纪律 | 原样引用 |
| `03-player-positioning.md` | 14 mode matrix、3 个 Direct candidate、5 个竞争变量 | 原样引用 |
| `evidence/03-agent-c-self-custody.md` | MetaMask/Plasma/Bleap/Karta/OKX SG 的 Step 3 落位（X/Y/Cluster/Account Role/region） | 原样引用 |
| `evidence/03-agent-e-crosscheck.md` | 独立 four-AND 重算（3 Direct / 5 Unknown / 6 Not Direct） | 原样引用 |
| `evidence/02-agent-f-aix-current-position.md` | AIX 只作为 future-entrant 对照锚（PH region、X1/YS Unknown） | 原样引用 |
| 缓存官方页面 | 本节逐条 verbatim 证据；不新增 URL | 已逐条离线校验 |

---

## 4. 区域 Gate 三态复核（本组）

> 规则：issuance/service eligibility 使用官方明确列表或明确限制；"180+ countries / 150M merchants / 80M+" 仅 acceptance marketing；Unknown ≠ No。

| 玩家 | PH | VN | AU | 依据（Step 1–3 已评审 + 本卡缓存） |
|---|---|---|---|---|
| MetaMask Card | **No** | **No** | **No** | current list 明确无 PH/VN/AU；US/UK closed；外区 waitlist |
| Plasma One | **Unknown** | **Unknown** | **Unknown** | country list 未公布；180+ 为 acceptance；Bridge US/EEA/other 不逐国 |
| Bleap | **No** | **No** | **No** | Europe/MX/BR current；eligibility 页 PH、Viet Nam 在 restricted nationalities |
| Karta | **Unknown** | **Unknown** | **Unknown** | "products may not be available to all customers"；150M 为 acceptance |
| OKX Pay/Card SG | **No** | **No** | **No** | 仅 SG mode |
| ether.fi Direct Pay | **Yes**（available 页） | **Conflict**（available vs restricted） | **Yes**（available 页） | available/restricted 局部冲突不裁决 |
| Gnosis | **Unknown**（本组未作玩家表判定） | Unknown | Unknown | B2B site + docs；issuer EEA framing；不作 PH/VN/AU 断言 |

---

## 5. 横向 Unknown 与下阶段核验清单（承接 Step 3 §6）

1. Plasma One / Karta 具体 issuance country matrix（PH 是否可服务）——最大 gap。
2. Karta top-up 后资产容器（X Unknown：self-custody 文案 vs balance/top-up 后的实际扣款位置）。
3. Bleap spendable balance 与 MPC wallet 的技术控制关系（unified/same-balance 是否成立）。
4. Plasma unified/same-balance 是否成立（global account services 不自动等于 Money Account confirmed）。
5. OKX SG issuer / unified balance / KYC / 完整 fee table。
6. MetaMask 的 stablecoin-mode spend mechanics 逐 token 核验（S4 candidate 不升级）。
7. ether.fi Direct Pay 的 Vault 完整 user-control boundary；available vs restricted 的 VN 冲突。
8. 费率完整性：OKX "zero fee" 营销声明、Plasma partner fees、Karta SEPA/SWIFT 与 bank rails future 冲突、MetaMask minimal fee 与 "no additional MetaMask fees" 并存。

---

## 6. 结论（Closeout）

1. **本组市场证据支持 Step 2/3 已固定的自托管簇（S4/S5）**：MetaMask（X3×B / S5）、Plasma One（X3×C / S4 strong）、Bleap（X3×C / S4）、Karta（Y=A / X Unknown / S4 direction–S1 boundary）、OKX SG（X3×C / S4）、ether.fi Direct Pay（X3×C / S4 candidate）、Gnosis（X3×C direction）。
2. **区域 Gate 三态不变**：MetaMask / Bleap / OKX SG 是 No；Plasma / Karta 是 Unknown；ether.fi Direct Pay 仅 PH 有正面 available 页证据（VN 冲突不裁决）。
3. **无新增玩家、无新增 URL、无改写历史结论**：本卡仅把 Step 1–3 已评审定义 + 官方缓存整合为 evidence card；AIX 不参与市场级关系定义。
4. **AIX（future entrant）对照（不定义市场）**：AIX current = X1 / Y Unknown / Species Unknown / Account Role 最多 Account-adjacent；若未来确认 Y/Species，再在 Step 5 更新 AIX 与 S4/S5 簇的相对关系。
5. **下阶段输入**：PH issuance eligibility（Plasma/Karta）、Karta X、Bleap/Plasma unified balance、ether.fi Vault control、费率表；这些 Unknown 不得被本卡升级为确认。
