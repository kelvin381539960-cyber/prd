# Agent A｜RedotPay / KAST 对照（截至 2026-08-29）

> 状态：Agent A 最终落盘（2026-08-29）。
> 类型：Step 3 evidence / mode-level 落位，不是最终竞争战略结论。
> 证据边界：只使用 `/tmp/redotpay-kast-evidence/` 已缓存官方页面与本地 Step 2 文件；不联网、不检索、不补抓。

---

## 0. Evidence policy

1. 只使用 `/tmp/redotpay-kast-evidence/` 目录中已采集的官方页面文本（`.txt` 提取自 `.html` 缓存），以及 `03-agent-f-aix-anchor.md` 和 `research/aix-market-positioning/02-ecosystem-map.md`。
2. 每条判断必须能回溯到具体官方 URL 缓存或上述两个本地锚点文件。
3. Job（J1/J2/J3）是分析推断，必须标 `analysis inference`，不得写成 AIX 或竞品 confirmed fact。
4. Starting money pool 只指用户进入产品前已持有的资产类型与来源，不得写产品内部余额容器。
5. Merchant acceptance / Visa worldwide acceptance 不作为 region / issuance 依据。
6. "170+ countries" / "100+ countries" / "150M merchants" 不作为逐国 issuance/service eligibility 依据。
7. 四项 AND gate 沿用 Step 2：`same region AND same core Job AND same starting money pool AND substitutable final real-world payment outcome`。任何一项 Unknown 或 No → Overall Unknown 或 No。
8. X/Y/Strategy Cluster 沿用 `02-ecosystem-map.md` 的定义。Account Role 沿用 Step 2 overlay。
9. 所有日期均为 2026-08-29 access date；各页面 official dateModified 见 URL index。

---

## 1. RedotPay

### 1.1 Current facts

| 维度 | 官方事实 | 证据来源 |
|---|---|---|
| **Product type** | "RedotPay is a stablecoin-based payment app that lets you use your cryptocurrency just like traditional currency." | redotpay-services.txt |
| **All-in-one Wallet** | "Securely hold and manage multiple types of digital and local currency in a single app." | redotpay-services.txt |
| **Crypto deposit** | 用户从外部 wallet 或 exchange 发起 withdrawal，复制 RedotPay deposit address 并确认；示例为 USDT-TRC20。 | redotpay-deposit.txt |
| **Supported assets** | "RedotPay supports multiple cryptocurrencies for payments and deposits, including: BTC, ETH, BNB, SOL, S, SUI, TRX, XRP, USDT, USDC." | redotpay-services.txt |
| **Spend mechanism** | "Spend instantly: No need to manually sell your crypto; we convert it to local currency the moment you pay." | redotpay-services.txt |
| **Card product** | Stablecoin-based card; virtual and physical; online, in-store, ATM。 | redotpay-card-type.txt; redotpay-payments.txt; redotpay-where-use.txt |
| **Card issuance restrictions** | 列出约 49 个 region 不可开 virtual/physical card；**列表不含 Philippines**。 | redotpay-restrictions.txt |
| **KYC** | 需 personal details + ID photo + face scan + residential address + questionnaire；18+；one account per person。 | redotpay-kyc-req.txt |
| **Card fees** | Virtual card issuance 10 USD；physical card 100 USD；均从 account balance 扣。 | redotpay-card-fees.txt |
| **Withdraw crypto** | 支持向外部 wallet/platform withdraw crypto。 | redotpay-deposit.txt related links |
| **International Transfer** | Send crypto，receive local currency；转到 bank account or e-wallet。 | redotpay-transfer.txt; redotpay-intl-common.txt |
| **Internal Transfer** | RedotPay 用户之间 email/phone/UID 发送。 | redotpay-internal-transfer.txt |
| **Crypto Gift** | 用户之间 send/receive crypto gift。 | redotpay-crypto-gift.txt |
| **USDs** | In-app reward token；不能外部 withdraw；仅用于 card spend / fees / statements / 内部 send。 | redotpay-usds.txt |

### 1.2 Job inference（analysis inference）

| Job | 判定 | 理由 |
|---|---|---|
| **J1**（稳定、可跨境的钱） | Not primary / plausible | 有 multi-currency wallet + international transfer，但缺 unified/same-balance closure；不构成 Money Account 主定位。 |
| **J2**（已持有 Crypto，转换为现实购买力） | **Primary** | 核心机制是：已持有 BTC/ETH/BNB/SOL/USDT/USDC 等 crypto，从外部 wallet/exchange deposit 后用 card 直接消费，无需手动卖币。 |
| **J3**（不卖 Crypto、保持敞口） | Secondary / separate mode | RedotPay Credit 提供 crypto-backed credit line（spend without selling），但这是独立 credit mode，不是 generic card auto-convert mode 的 primary。 |

**本报告的 four-AND 判定限定在 generic crypto auto-convert card mode，不含 RedotPay Credit。**

### 1.3 Starting money pool

用户进入产品前已持有的资产，从外部 wallet 或 exchange 经 on-chain deposit 进入 RedotPay。支持的起点包括：

- **稳定币**：USDT、USDC（与 AIX 起点直接交集）。
- **波动币**：BTC、ETH、BNB、SOL 等（超出 AIX 当前 stablecoin-only 范围）。

**本报告的 four-AND 判定限定在 stablecoin-starting segment（用户已持有 USDT 或 USDC 并从外部 wallet/exchange 进入）。**

### 1.4 X / Y / Strategy Cluster

| 维度 | 结论 | 官方依据 |
|---|---|---|
| **X** | **X2** Provider-custodied Wallet/Account Balance | "All-in-one Wallet: Securely hold and manage multiple types of digital and local currency in a single app." 消费时从 platform wallet/account 扣减，未观察到独立 Dedicated Card Balance 证据。 |
| **Y** | **B** At-payment asset sell/convert | "No need to manually sell your crypto; we convert it to local currency the moment you pay." 资产留在 wallet，到 payment 时自动转换。 |
| **Strategy Cluster** | **S2** | X2×B 完全匹配 Step 2 定义的 S2 "托管 Crypto 余额，付款时再卖"。 |

**不做 X1 假设。不做 S3 假设。**

### 1.5 Account Role

**Spend Feature / Account-adjacent（不得升级 Money Account）。**

理由：有 crypto deposit / withdraw / international transfer / internal transfer / crypto gift 等 rail 证据，但当前官方页面未出现 "unified balance" 或等价表述。Step 2 要求 Money Account 必须同时证明 receive + hold + send + spend + unified/same-balance。RedotPay "All-in-one Wallet" 是产品叙事，不足以替代 "unified balance" 官方术语。

### 1.6 Card

| 维度 | 官方事实 |
|---|---|
| **Card type** | "Stablecoin-based card that lets you spend crypto like a regular card." |
| **Card variants** | Virtual + Physical。 |
| **Usage** | Online / in-store / ATM (physical card)。 |
| **Acceptance** | Major card networks；"over 130 million merchants worldwide"。 |
| **Fees** | Virtual 10 USD；Physical 100 USD。 |
| **Issuance restrictions** | 约 49 regions 不可开卡；PH 不在列表中。 |

**PH current service/issuance gate：Yes。** 依据 `Card Issuance Restrictions` 页定义（"Residents of these areas are ineligible for both virtual and physical cards"）， Philippines 不在 restricted list，可判 PH 当前未被 issuance-restriction 阻挡。**Merchant acceptance 不作为依据。**

### 1.7 Fees / KYC（proven only）

| 项 | 已证明 | 未证明 |
|---|---|---|
| **Card issuance** | Virtual 10 USD; Physical 100 USD; 从 account balance 扣 | 完整 FX / ATM / inactivity / replacement fee 表 |
| **KYC** | personal details + ID + face scan + address + questionnaire; 18+; one account | KYC provider / KYC tier / KYC-to-card sequencing |
| **Crypto deposit** | on-chain deposit from wallet/exchange; network selection | deposit limits / network fees |
| **International Transfer** | send crypto receive local currency; fees shown before confirm | 完整 FX schedule / per-country limits |

### 1.8 Four-AND gate vs AIX

| Gate | 结论 | 依据 |
|---|---|---|
| **Same region** | **Yes（PH full journey）** | AIX Wallet Crypto Deposit = PH 且 Card Phase 1 含 PH（`03-agent-f-aix-anchor.md` §1）。RedotPay `Card Issuance Restrictions` 列表不含 PH → PH current issuance/service gate = Yes（redotpay-restrictions.txt）。完整 `stablecoin → RedotPay → card spend` journey 在 PH 成立。 |
| **Same core Job** | **Yes（stablecoin-starting J2 segment）** | RedotPay generic card auto-convert mode 的 primary Job = J2（analysis inference）；AIX 对 stablecoin-starting J2 segment 也是 strong/plausible（`03-agent-f-aix-anchor.md` §4）。该 segment 内 overlap 成立。 |
| **Same starting money pool** | **Yes** | RedotPay 支持从外部 wallet/exchange deposit USDT/USDC；AIX 起点是已持有 USDT/USDC/WUSD/FDUSD 从外部 wallet/exchange 充值。stablecoin-starting segment 起点重合。 |
| **Substitutable final outcome** | **Yes** | 都是 card real-world spend（online / in-store / ATM）。 |
| **Overall** | **Yes / direct（限定 PH stablecoin-starting J2 segment）** | 四项 AND 同时满足。 |

**此判定不改变 AIX `X1 / Y Unknown / Species Unknown` 的事实锚点，也不要求 X/Y 相同。**

### 1.9 Unknown / limitations

1. RedotPay 是否有 separate Dedicated Card Balance（X1）未证明；当前 X2 判定基于 "All-in-one Wallet" + "convert at payment" 描述，不排除内部结构变化。
2. RedotPay Credit 是独立 crypto-backed credit mode，不在本 four-AND 判定范围内。
3. RedotPay `Card Issuance Restrictions` 未提供 PH 正面白名单；判定基于 restricted-list 定义 + PH 不在列表的 absence-of-restriction 推理。不视为逐国 issuer 终表。
4. 完整 fee table / ATM fees / FX pricing / deposit limits / withdrawal limits 未证明。
5. RedotPay "All-in-one Wallet" 不升级 Money Account；不引入 unified balance 假设。
6. 130M merchant acceptance 不作为 issuance 依据。

### 1.10 URL index（accessed 2026-08-29）

| # | URL | 支持点 | Cache file / official dateModified |
|---|---|---|---|
| R1 | https://helpcenter.redotpay.com/en/articles/11070044-redotpay-services-and-features | Product type, All-in-one Wallet, spend instantly, supported assets, merchant acceptance, 100+ countries | redotpay-services.html; 2026-07-24 |
| R2 | https://helpcenter.redotpay.com/en/articles/10339284-how-do-i-deposit-crypto-to-my-redotpay-account | Crypto deposit from wallet/exchange, on-chain address flow | redotpay-deposit.html; 2026-07-28 |
| R3 | https://helpcenter.redotpay.com/en/articles/10566205-what-type-of-card-is-the-redotpay-card | Card type, stablecoin-based, crypto spend | redotpay-card-type.html; 2026-07-21 |
| R4 | https://helpcenter.redotpay.com/en/articles/11027588-how-do-i-use-my-redotpay-card-for-payments | Virtual/physical card usage, ATM | redotpay-payments.html; 2026-07-21 |
| R5 | https://helpcenter.redotpay.com/en/articles/11027583-where-can-i-use-my-redotpay-card | 130M merchants, online/in-store/ATM, sanctioned-country exclusion | redotpay-where-use.html; 2026-07-26 |
| R6 | https://helpcenter.redotpay.com/en/articles/14254838-card-issuance-restrictions | Card issuance restricted list; PH absent | redotpay-restrictions.html; 2026-08-28 |
| R7 | https://helpcenter.redotpay.com/en/articles/10920717-identity-verification-requirements | KYC: ID + face scan + address + questionnaire; 18+ | redotpay-kyc-req.html; 2026-07-21 |
| R8 | https://helpcenter.redotpay.com/en/articles/10566200-are-there-any-fees-for-getting-a-card | Virtual 10 USD / Physical 100 USD issuance fee | redotpay-card-fees.html; 2026-07-27 |
| R9 | https://helpcenter.redotpay.com/en/articles/11008771-how-to-get-a-redotpay-card | Card acquisition flow: app → sign up → verify → add crypto → card | redotpay-how-get-card.html; 2026-07-21 |
| R10 | https://helpcenter.redotpay.com/en/articles/10721182-how-do-i-get-a-virtual-card | Virtual card flow + billing address + 10 USD fee | redotpay-virtual-card.html; 2026-07-29 |
| R11 | https://helpcenter.redotpay.com/en/articles/10721338-how-do-i-get-a-physical-card | Physical card flow + shipping address + 100 USD fee | redotpay-physical-card.html; 2026-07-30 |
| R12 | https://helpcenter.redotpay.com/en/articles/11388117-how-to-send-crypto-and-receive-local-currency | International Transfer: send crypto receive local currency | redotpay-transfer.html; 2026-07-22 |
| R13 | https://helpcenter.redotpay.com/en/articles/11325255-common-questions-about-international-transfer | Intl Transfer mechanics: crypto→local currency→bank/e-wallet | redotpay-intl-common.html; 2026-07-21 |
| R14 | https://helpcenter.redotpay.com/en/articles/13868119-what-is-usds | USDs: in-app reward token, no external withdraw, card spend/fees/internal send only | redotpay-usds.html; 2026-02-26 |
| R15 | https://helpcenter.redotpay.com/en/articles/10339293-how-to-make-an-internal-transfer | Internal transfer: email/phone/UID between RedotPay users | redotpay-internal-transfer.html; 2026-07-22 |

---

## 2. KAST

### 2.1 Current facts

| 维度 | 官方事实 | 证据来源 |
|---|---|---|
| **Product type** | "The global money app powered by stablecoins." "The financial platform to store, earn, move, and spend stablecoins." | kast-home.txt |
| **Global Account** | "One account. Everywhere you need it. A US account number. An EU IBAN. Receive salary, invoices, and transfers directly into KAST." | kast-global-accounts.txt |
| **ACH/SWIFT/Fedwire** | "ACH, SWIFT and Fedwire transfers"; "US dollar deposits via ACH and Wire"; "Deposit over US banking rails (ACH, Fedwire)"; "Deposit over SWIFT"。 | kast-global-accounts.txt |
| **Receive / Send / Spend** | "Unified Balance Spend, send, and receive from one account"; "Receive salary, invoices, and transfers directly into KAST"; "Send local fiat"; "Send stablecoins"; "Spend via card or pay bills globally"。 | kast-global-accounts.txt |
| **Stablecoin deposit** | "Deposit from any supported network (ETH, Tron, Arbitrum)"; "Instant conversion to USD inside KAST"; "Deposit from Exchanges & Wallets: Simple wallet-to-wallet transfers"。 | kast-global-accounts.txt |
| **Crypto deposit** | "Deposit crypto: Convert instantly into USD"; "Send out as USD or crypto again"。 | kast-global-accounts.txt |
| **Supported stablecoins** | USDT (Ethereum/TRON/Solana/Polygon/BNB Chain 等), USDC (Ethereum/Solana/Polygon 等), PYUSD, RLUSD。 | kast-stablecoins-v2.txt; kast-supported-tokens-v2.txt |
| **Supported crypto (receive)** | BTC, ETH, SOL, XRP, BNB 及其他。Non-stablecoin auto-converted to stablecoins。 | kast-supported-tokens-v2.txt |
| **Card** | Virtual + physical; Visa; "money comes straight from your wallet"; "deducted right away"。 | kast-card-use-v2.txt |
| **Card availability** | "You can check if KAST is available in your country during the sign-up process. If you don't see your country in the dropdown menu, we haven't launched there yet." 无逐国 issuance/service 列表。 | kast-card-availability.txt |
| **Card pricing** | Standard: annual $0; virtual free (first 2); physical free ($40 shipping)。Premium: $1,000/yr。Private: $10,000/yr。 | kast-cards-fees-v2.txt |
| **Fees** | Top-up 0%; FX 0.5–1.75%; Card spend USD 0%; ATM $3+2%; stablecoin deposit 0% (1:1 to USD, 0% spread); crypto deposit 2–5% auto-conversion。 | kast-cards-fees-v2.txt |
| **Card class** | ⚠️ 两个 2026-08-09 官方 Help Center 页面冲突：`kast-debit-or-credit.txt` 说 "All KAST cards are credit cards" 并描述 credit line secured by deposited balance；`kast-card-use-v2.txt` 说 "deducted right away - so you're always spending your own funds, not credit"。同日同级来源，无法按日期裁决，本报告不裁决 classification。 | kast-debit-or-credit.txt vs kast-card-use-v2.txt |

### 2.2 Job inference（analysis inference）

| Job | 判定 | 理由 |
|---|---|---|
| **J1**（稳定、可跨境的钱） | **Plausible / at least J1 overlap** | Global Account / Unified Balance / ACH/SWIFT/Fedwire / receive/send/spend strongly support J1; independent of card mechanism conflict. |
| **J2**（已持有 Crypto，转换为现实购买力） | **Secondary inference** | 支持从外部 wallet/exchange deposit stablecoin/crypto，然后 card spend。对 stablecoin-starting 用户可推断 J2 也被覆盖，但官方页面定位偏 J1 global account。 |
| **J3**（不卖 Crypto、保持敞口） | **Unproven** | Secured-credit wording conflicts with own-funds/no-interest wording and does not prove Step1 J3. |

**本报告 four-AND 的 same-core-Job 判定至少是 J1 overlap；stablecoin-starting J2 可作为 secondary inference 但不强写 primary。**

### 2.3 Starting money pool

用户进入产品前已持有的资产，从外部 wallet/exchange 经 on-chain deposit 或 fiat rail 进入 KAST。

**Stablecoin-starting segment**：用户已持有 USDT 或 USDC，从外部 wallet/exchange deposit 进入 KAST（instant conversion to USD, 1:1, 0% spread）。这与 AIX 起点直接重合。

**Non-stablecoin-starting segment**：用户已持有 BTC/ETH/SOL 等，deposit 后 auto-convert to stablecoin。此 segment 不在本报告 four-AND 判定内（AIX 无 volatile crypto 起点）。

**Fiat-starting segment**：ACH/SWIFT/Fedwire/SEPA 入金。此 segment 起点是法币，不与 AIX stablecoin 起点重合。

### 2.4 X / Y / Strategy Cluster

| 维度 | 结论 | 官方依据 |
|---|---|---|
| **X** | **X2 confirmed** | "money comes straight from your wallet"; "deducted right away"; "Account Deposit Limit / Account Balance Limit"。消费从 KAST platform wallet/account 扣。 |
| **Y** | **Unknown — Source Conflict** | C-like evidence: "Can I spend stablecoins directly without converting? Yes."; "money comes straight from your wallet"; "deducted right away"。Credit-line evidence: "deposited balance secures credit line"; "purchase charged to credit line"; "repay within billing cycle"。All are current 2026-08-09; the credit article itself also says amounts pull directly from balance, no interest, and no monthly bill。 |
| **Strategy Cluster** | **Unknown pending vendor clarification** | Y cannot be fixed while the official card-purchase-power mechanism documents conflict; no cluster is assigned until vendor clarification。 |

### 2.4.1 Source Conflict：KAST Card 购买力机制

三份 2026-08-09 官方文档对 card 购买力机制给出不一致描述：

- `kast-stablecoins-v2.txt` 说可以 "spend stablecoins directly"。
- `kast-card-use-v2.txt` 说 "money comes straight from your wallet" 且 "deducted right away"。
- `kast-debit-or-credit.txt` 说 deposited balance secures a credit line、purchase charged to a credit line、repay within billing cycle；但同一篇也说金额直接从 balance 扣、no interest、no monthly bill。

同日同级来源无法按日期或层级裁决。X2 stays confirmed; Y and Cluster remain Unknown; Account Role Money Account and four-AND are unaffected.

### 2.5 Account Role

**Money Account。**

依据：`kast-global-accounts.txt` 明确 "Unified Balance Spend, send, and receive from one account"，加上 "ACH, SWIFT and Fedwire transfers" / "US account number / EU IBAN" / "Receive salary" / "Send stablecoins" / "Spend via card"。满足 Step 2 Money Account 全部四项要求：receive + hold + send/spend + unified/same-balance。

### 2.6 Card

| 维度 | 官方事实 |
|---|---|
| **Card variants** | Virtual + physical；Apple Pay / Google Pay 支持。 |
| **Network** | Visa。 |
| **Usage** | Online / in-store / ATM (physical)。 |
| **Mechanism** | Source conflict, do not pick one: `kast-card-use-v2.txt` describes money coming straight from the wallet / deducted right away; `kast-debit-or-credit.txt` describes a deposited balance securing a credit line / purchase charged to a credit line / repay within billing cycle。 |
| **Fees** | Standard virtual free / physical free + $40 shipping; FX 0.5–1.75%; ATM $3+2%。 |
| **Limits** | Card transactions unlimited (balance-based); ATM $250/withdrawal, max $750/day。 |

### 2.7 PH card availability / issuance eligibility

**官方 `Is the KAST Card Available in My Country?` 页面（kast-card-availability.txt）只说：**

> "You can check if KAST is available in your country during the sign-up process. If you don't see your country in the dropdown menu, we haven't launched there yet."

**该页面未提供逐国 issuance/service eligibility 列表，也未提及 Philippines。**

**以下推断链均不可用：**

- ❌ "150M merchants / Visa worldwide acceptance" → 不能推断 PH issuance。
- ❌ "PHP – Philippine Peso payout" → 不能推断 PH card issuance eligibility。
- ❌ "170+ countries / global account" → 不能推断 PH card issuance。
- ❌ Testimonials（Argentina / Vietnam / Toronto）→ 不构成 eligibility 证据。

**结论：KAST 当前 PH card issuance/service eligibility = Unknown。**

### 2.8 Four-AND gate vs AIX

| Gate | 结论 | 依据 |
|---|---|---|
| **Same region** | **Unknown** | AIX 完整 journey 锚点 = PH（`03-agent-f-aix-anchor.md` §1）。KAST card availability 页无 PH 明确正面资格；merchant acceptance / PHP payout / global account 均不作为 issuance 依据。→ region gate 不能证 Yes。 |
| **Same core Job** | **至少 J1 overlap（analysis inference）**；stablecoin-starting J2 可作 secondary inference 但不强写 primary。 | KAST Money Account/global-money evidence 覆盖 J1；AIX 对 stablecoin-starting J2 segment strong/plausible。J1 overlap 本身不等于 same core Job 的 primary match。 |
| **Same starting money pool** | **Yes（stablecoin users）** | KAST 支持从外部 wallet/exchange deposit USDT/USDC；AIX 起点是已持有 USDT/USDC 从外部 wallet/exchange 充值。stablecoin-starting segment 起点重合。 |
| **Substitutable final outcome** | **Yes** | 都是 card real-world spend。 |
| **Overall** | **Unknown due region** | Region gate Unknown → 四项 AND 不能同时证 Yes。 |

### 2.9 Unknown / limitations

1. PH card issuance/service eligibility 未证明；官方页面只提供 signup-time country dropdown check，无公开逐国列表。
2. `kast-debit-or-credit.txt` 与 `kast-card-use-v2.txt` 对 card classification 存在冲突（两页均 2026-08-09 official dateModified）；本报告记录冲突，不裁决 classification，也不裁决 credit-line 语义。该冲突 DOES affect Y/Cluster，因此两者均保持 Unknown。
3. KAST Global Account 服务由 Bridge/Lead Bank 支持（Footer disclosure）；这不改变产品侧 Money Account 判定，但表示底层 banking partner 结构需后续核验。
4. 逐国 issuer / KYC tier / exact KYC-to-card sequencing 未证明。
5. "170+ countries" 不作为逐国 issuance 依据。
6. Merchant acceptance / PHP payout 不作为 issuance 依据。

### 2.10 URL index（accessed 2026-08-29）

| # | URL | 支持点 | Cache file / official dateModified |
|---|---|---|---|
| K1 | https://www.kast.xyz | Product type, store/earn/move/spend stablecoins, 170+ countries, 150M merchants, global account, receive/send/spend | kast-home.html |
| K2 | https://www.kast.xyz/global-accounts | Global Account, ACH/SWIFT/Fedwire, unified balance, deposit stablecoins/crypto/exchange, send stablecoins/fiat, spend via card | kast-global-accounts.html |
| K3 | https://concierge.kast.xyz/hc/en-us/articles/13939999566095-Is-the-KAST-Card-Available-in-My-Country | Card availability check via signup dropdown; no country list; no PH mention | kast-card-availability.html; 2026-08-09 |
| K4 | https://concierge.kast.xyz/hc/en-us/articles/14237170585999-Where-Can-I-Use-My-KAST-Card | Visa acceptance, money from wallet, deducted right away, not credit, ATM | kast-card-use-v2.html; 2026-08-09 |
| K5 | https://concierge.kast.xyz/hc/en-us/articles/9850062738703-What-Are-the-Fees-and-Conditions-for-KAST-Cards-and-Accounts | Card pricing, FX, ATM, stablecoin deposit 0% 1:1, crypto deposit 2–5% auto-convert, limits, PHP payout | kast-cards-fees-v2.html; 2026-07-13 |
| K6 | https://concierge.kast.xyz/hc/en-us/articles/13980432315535-Why-Is-My-Country-Restricted-from-Accessing-KAST | Restricted country logic: KYC dropdown; no country list; no PH mention | kast-restricted-country.html; 2026-08-09 |
| K7 | https://concierge.kast.xyz/hc/en-us/articles/11784729022863-Which-Stablecoins-Are-Supported-on-the-KAST-App | USDT/USDC/PYUSD/RLUSD networks; deposit/send stablecoins; spend directly without converting | kast-stablecoins-v2.html; 2026-08-09 |
| K8 | https://concierge.kast.xyz/hc/en-us/articles/13973209755663-What-Tokens-and-Blockchains-Does-KAST-Support | Send/receive USDT/USDC; receive BTC/ETH/SOL/XRP/BNB; network details | kast-supported-tokens-v2.html; 2026-08-09 |
| K9 | https://concierge.kast.xyz/hc/en-us/articles/15043176480143-Is-My-KAST-Card-a-Debit-or-Credit-Card | Card class conflict: says credit card but no interest/no credit check/repay own funds | kast-debit-or-credit.html; 2026-08-09 |
| K10 | https://concierge.kast.xyz/hc/en-us/articles/11290428597647-What-Are-the-Daily-Spending-and-ATM-Withdrawal-Limits-on-My-KAST-Card | Card transactions unlimited (balance-based); ATM $250/$750/day | kast-daily-limits.html; 2026-08-09 |

**未采信的缓存文件：**

- `fetch-13971393267087-How-Do-I-Create-A-USD-Account-on-KAST`（Cloudflare challenge page；无文章内容）
- `fetch-15113303577231-Do-I-Need-to-Already-Own-Crypto-to-Use-KAST`（Cloudflare challenge page；无文章内容）
- `kast-fund-account.txt`（404 page not found）
- `kast-card-use.html` / `kast-cards-fees.html` / `kast-k-vs-solana.html` / `kast-limits.html` / `kast-send-usd.html` / `kast-stablecoins.html` / `kast-transfer-duration.html`（旧版或冗余版本；以 `-v2` / `-dom` 版本为准）

---

## 3. 总结

| 维度 | RedotPay | KAST |
|---|---|---|
| **Product type** | Stablecoin-based payment app; crypto card | Global money app powered by stablecoins |
| **X × Y / Cluster** | X2 × B / **S2 primary** | X2 confirmed / Y Unknown / Cluster Unknown (official mechanism conflict) |
| **Account Role** | Spend Feature / Account-adjacent | **Money Account** |
| **Card** | Virtual + Physical; stablecoin-based card | Virtual + Physical; Visa |
| **PH issuance/service** | **Yes**（restricted list 不含 PH） | **Unknown**（signup dropdown check only，无 PH 正面资格） |
| **Same region (vs AIX)** | **Yes（PH full journey）** | **Unknown** |
| **Same core Job (vs AIX)** | **Yes（stablecoin-starting J2 segment; analysis inference）** | **至少 J1 overlap; stablecoin J2 secondary inference** |
| **Same starting pool (vs AIX)** | **Yes**（USDT/USDC from wallet/exchange） | **Yes**（USDT/USDC from wallet/exchange） |
| **Final outcome (vs AIX)** | **Yes**（card real-world spend） | **Yes**（card real-world spend） |
| **Overall four-AND** | **Yes / direct（限定 PH stablecoin-starting J2 segment）** | **Unknown due region** |

**判定边界：**

1. RedotPay direct 判定限定在 generic crypto auto-convert card mode + PH + stablecoin-starting J2 segment。RedotPay Credit / International Transfer / P2P 不在同一判定范围内。
2. KAST 的 Unknown 不表示"No"，只表示当前官方证据不足以确认 PH card issuance eligibility。
3. 两个判定均不改变 AIX `X1 / Y Unknown / Species Unknown` 的事实锚点。
4. 两个判定均基于 evidence-level four-AND gate，不替代 Step 4 竞争关系分析。
