# Agent D｜Credit / Borrow 对照：ether.fi Cash Card 与 Nexo Card（截至 2026-08-29）

> 状态：Agent D 收口草稿 / 待评审。
> 时点：external current evidence 为 2026-08-29 采集；ether.fi 文章另有下文标注的 official dateModified。
> 范围：仅 ether.fi Cash Card 与 Nexo Card。不合并两个品牌，不合并同一品牌的不同 spend mode。

## 0. 方法与来源边界

- 外部现状只使用本轮 `/tmp/aix-credit-evidence/` 已采集官方页面；最多补抓每家 1 个官方页面的约束未突破：ether.fi 补抓 `304388-how-does-card-issuance-work`，Nexo 补抓 credit-mode article。ether.fi 请求被官方站点重定向回 `304388-how-does-collateral-and-borrowing-work`，Nexo 返回 generic Support Center shell；两者均不产生新增产品事实。
- ether.fi official dateModified：Borrow vs Direct Pay `2026-08-20`；available countries `2026-08-02`;restricted `2026-08-23`；collateral & borrowing `2026-06-19`。Nexo card page 无可见 dateModified，按 accessed `2026-08-29` 处理。
- Nexo current areaServed 保持 **EEA + UK**，不从 merchant acceptance、App availability 或站点可见的其他 Nexo product page 推广。
- Fees / KYC / thresholds 只写缓存官方页可直接支持的条目；未支持的写 Unknown。

## 1. ether.fi Cash Card

### Current service & issuance region

**Live status**：ether.fi 官方 Personal 页把 Cash card 放入当前 Spend 能力（virtual / physical card），并把 Borrow 作为当前产品叙事；未发现 Cash card 本身 Coming Soon / early-access 限定。页面另有 protection program 标注 not yet live，本报告不把它当 current card fact。

**Issuance / service eligibility**：official available-countries article 说 Cash card 在列出的 supported jurisdictions 可用，适用于 Personal 与 Corporate members，且需 KYC / compliance；official restricted article 说 Cash and fiat services 对 listed unsupported countries / U.S. states 不可用，并列出 card spending unsupported countries。两页 2026-08-29 均可访问，本报告不裁决个别国家的局部差异。

**与 AIX current overlap 的直接重合**：AIX Card Phase 1 为 PH / VN / AU。ether.fi available page 列出 Philippines、Australia，但 listed unsupported countries 列出 Vietnam；available 与 restricted 页面存在局部冲突，且该判断是 membership/eligibility overlap，不是 direct conclusion。

### Starting money pool

**官方确认的资产驻留**：Cash card spending 由用户 ether.fi Vault 内资产驱动。official non-custodial statement 描述整个 app 为 all-in-one **non-custodial**、用户 retain full ownership and control；issuance disclosure 说明 Card 由独立 Issuer 单独条款发行。

**官方已确认的 spend assets**：

- Direct Pay：purchase 时 immediately deducted from Vault 的 **USDC or LiquidUSD** balance；USDC 优先，LiquidUSD 次之；其他 Vault assets 在当前 Direct Pay 不 eligible。
- Borrow Mode：可用 Vault 全部 assets 作为 collateral / spending base；不卖 crypto。
- Collateral page 当前列出 wETH / wHYPE / USDC / EURC / USDT / frxUSD / OP、platform tokens 与 Liquid Vaults tokens，并给出各自 LTV 与 liquidation threshold。

**与 AIX 对齐 / 分歧点（不是定位结论）**：AIX 起点是 DTC-custodied stablecoin balance（USDC / USDT / WUSD / FDUSD）且 Card Balance 分离；ether.fi 起点是 non-custodial Vault 资产。即使部分 asset symbols 重合（如 USDC / USDT），custody 与消费容器不同。

### Job inference

**J3**：primary。Borrow Mode 官方机制是 crypto 作 collateral、spend without selling；匹配 J3“不卖 Crypto、保持敞口、获得消费流动性”。

**J2**：secondary。Direct Pay 直接从 Vault USDC / LiquidUSD balance 扣款；对已经把 stable value 放入 Vault 的用户，这是“把已持有的 crypto/stable value 直接用于消费”，非借贷。

**J1**：不判定。现有页面没有支持“J1 是 primary job”的 stable-cross-border money account statement；Account Role 只能记 Unknown / Account-adjacent candidate，不能升级。

### X / Y / cluster by mode

| Product mode | X | Y | Strategy cluster | Evidence boundary |
|---|---|---|---|---|
| Direct Pay Mode | X3 | C | S4 candidate / strong-adjacent | 官方说直接从 Vault 的 USDC/LiquidUSD 扣款；但 official pages 未定义该 Vault 的完整 user-control boundary、receive/hold/send/spend closure 或 unified balance，因此 S4 不能升级为 confirmed。 |
| Borrow Mode | X3 candidate | D | S6 Onchain/Self-custody variant candidate | Borrowing / collateral / liquidation mechanics confirmed；但 custody/control boundary of Vault during credit lifecycle is not fully defined by cached official pages. |

### Direct Pay vs Borrow：不能合成一种机制

| Dimension | Direct Pay Mode | Borrow Mode |
|---|---|---|
| Purchasing-power mechanism | 直接扣 Vault USDC/LiquidUSD balance | Vault assets 作 collateral，形成 borrow balance / credit |
| Is it credit? | No | Yes |
| Debt / interest | 无 interest charges 或 fees beyond standard transaction costs | Interest immediately accrues; variable APY, via Aave v4; no grace period / billing cycles |
| Collateral / LTV risk | Not applicable from cached pages | LTV by asset (USDC/USDT/EURC/frxUSD 90%; LiquidUSD/eUSD/LiquidReserve 80%; wETH/weETH 55%; LiquidETH/LiquidBTC 50%; eBTC 52%; etc.); liquidation thresholds and bonus exist |
| Refunds | 官方未给出 mode-specific refund handling in cached pages | refund credited to vault main balance, does not automatically repay borrow; manual repayment required |
| J3 relation | Direct Pay 本身不是 J3 mechanism | Borrow Mode 是明确的 J3 mechanism |

The borrow-rate table is not a final fee schedule: it records collateral economics, not a complete consumer fee table.

### Card role / Account Role

**Card role**：Card / spend rail；virtual card for instant access, physical card for everyday spending。

**Account Role**：Unknown / at most Account-adjacent candidate。official non-custodial statement 有 hold / earn / borrow / spend / send narrative，但 cached pages 没有完整 receive + hold + send + spend + unified/same-balance closure。**不得升级 Money Account。**

### Fees / KYC / borrow thresholds（仅有证据）

| Item | Evidence-backed statement | Unknown / no claim |
|---|---|---|---|
| Fees | **Direct Pay** 无 interest charges beyond standard transaction costs；该说法针对 Direct Pay，不涵盖 Borrow Mode 的借贷利息，也不含完整 consumer fee schedule。 | issuance fee, monthly fee, FX pricing, ATM fees, premium membership pricing, complete fee table |
| KYC | available page 明确 subject to successful account verification (KYC) and applicable compliance；unsupported page 使用 residence / registration / resident tests。 | KYC provider, exact KYC doc list, KYC-to-card sequencing |
| Borrow thresholds | LTV 与 liquidation threshold 按资产列示（examples: USDC/USDT/EURC/frxUSD 90% LTV / 95% threshold；LiquidUSD/eUSD/LiquidReserve 80% / 90%；wETH/weETH 55% / 75%；LiquidETH/LiquidBTC 50% / 70%；ETHFI/sETHFI/OP 20% / 50%）。liquidation 时 Debt Manager 可处置 vault tokens。 | minimum borrowing amount, minimum vault balance, regional minimum deposit |

## 2. Nexo Card

### Current service & issuance region

**Live status**：official card page 将 Nexo Card 作为 current product：Credit/Debit Mode 可切换、virtual card 可 activate、physical card 有 shipping/eligibility 条件、Apple Pay / Google Pay 叙事存在。

**areaServed**：official FAQ explicitly says currently available only to citizens and residents of selected European countries, including **EEA and UK**；identity document must be issued in EEA / UK / other eligible Europe。card footer says issued by **DiPocket UAB**。这个 areaServed 结论保持，不推广到 merchant acceptance 或其他 Nexo services。

**与 AIX current overlap 的直接重合**：AIX Card Phase 1 为 PH / VN / AU。Nexo areaServed 保持 EEA+UK，因此 current card areaServed overlap = **None**。这是 overlap-to-direct gate 的 region 输入，不是 direct conclusion。

### Starting money pool

**官方确认的资金池**：Nexo Card 两个 mode 都 connect to user's **available Nexo balance**。Debit Mode spend stablecoins / crypto / FiatX assets (EURx, USDx, GBPx) 并 prioritise assets；Credit Mode 用 crypto-backed Credit Lines。官方 card page 提到 industry-grade custody，Card 由 DiPocket UAB issued。

**与 AIX 对齐 / 分歧点**：AIX 起点 DTC-custodied stablecoin wallet + separate Card Balance；Nexo 是 custodied Nexo platform balance。同 custody class 但 container 不同：AIX Card 消费扣 separate Card Balance（X1 confirmed），而 cached Nexo evidence 没有证明先转入 separate card balance，只 connect to available balance。

### Job inference

**J3**：primary，仅 Credit Mode。credit mode lets purchases without selling Bitcoin / other crypto, retaining upside potential；官方另有 “over 100,000 BTC stayed in clients’ portfolios” narrative。

**J2**：primary/secondary for Debit Mode。spend digital assets / stablecoins / crypto / FiatX；Nexo handles conversion。对 already stable-asset users 这也是 direct stable-value spend path，但 Nexo page 未证明它是专用 X1 card balance。

**J1**：不判定。cached official evidence 没有 stable, cross-border money account claim。

### X / Y / cluster by mode

| Product mode | X | Y | Strategy cluster | Evidence boundary |
|---|---|---|---|---|
| Debit Mode | X2 | Unknown | Unknown cluster, X2 confirmed | 官方 connect to available balance + handle conversion，但没有证明消费前进入专用卡余额（X1），也没有足够字段把它定为 B 或 C。因此不是 S2/S3 合并机制。 |
| Credit Mode | X2 | D | S6-Custodial | crypto-backed credit line / spend without selling / connect to available balance confirmed。 |

### Debit Mode vs Credit Mode：不能合成一种机制

| Dimension | Debit Mode | Credit Mode |
|---|---|---|
| Purchasing power | spend digital assets, including stablecoins / crypto / FiatX | crypto-backed Credit Lines |
| Is it credit? | No | Yes |
| Sale / conversion | Nexo handles conversion for you | 官方未写 at-payment sale；避免 B/C 猜测 |
| Debt / repayment | no borrowing / repayment from cached evidence | flexible repayment, no fixed schedule, no credit checks |
| Interest | 官方 marketing says earn interest on available balance / unspent balance；不把它写成借贷利率 | starting from 1.9% interest on crypto-backed credit lines |
| Cashback | 无 Debit cashback claim | up to 2% crypto cashback, loyalty-tier dependent, balance above $5,000 |

### Card role / Account Role

**Card role**：Card / spend rail；virtual + physical card；Apple Pay / Google Pay current narrative。

**Account Role**：Unknown / Spend Feature at most。available Nexo balance 支持 card 消费，但本轮 cached evidence 未证明 receive + hold + send + spend + unified/same-balance closure。不升级 Money Account。

### Fees / KYC / borrow thresholds（仅有证据）

| Item | Evidence-backed statement | Unknown / no claim |
|---|---|---|---|
| Activation / issuance | Virtual card activate once account has at least **$50**；physical card需要 account balance above **$5,000** worth of digital assets and at least Gold Loyalty Tier；physical card free shipping。 | delivery cost by region, card-management fees |
| Fees | FX fees weekday **EEA/UK/CH 0.2%**, ROW 2%; weekend EEA/UK/CH 0.7%, ROW 2.5%。ATM free withdrawals by loyalty tier up to €2,000 / £1,800 monthly, beyond 2% fee minimum 1.99 EUR/GBP。官方 says no monthly, annual, or inactivity card fees。 | full card fee schedule and any credit-specific fees |
| KYC | FAQ says eligible users must complete Identity Verification with supported identity document issued in EEA / UK / other eligible Europe。 | KYC provider, document list, KYC-to-card sequencing |
| Borrow thresholds | Official card page 没有给出 card-mode-specific minimum collateral amount, LTV, or borrowing minimum。 | card-mode-specific LTV / collateral minimums；不借用其他 Nexo credit pages。 |

## 3. Direct four-AND gate（同一消费任务的可替代性）

规则沿用 Step 2：**same region AND same core Job AND same starting money pool AND substitutable final real-world payment outcome**。四项必须同时成立；overlap 本身不是 direct。

### 3.1 AIX baseline

| Gate input | AIX current evidence |
|---|---|
| Region | Card Phase 1 **PH / VN / AU**，但完整 `stablecoin → AIX → card spend` journey 的最强 current 地域锚点是 **PH**；VN/AU 完整 journey Unknown。Wallet PH deposit 不替代 Card 口径。 |
| Core Job | Analysis inference：stablecoin-starting **J2 segment strong/plausible**（已持有 supported stablecoin，寻求卡消费）；J1 direction plausible but incomplete；**J3 unsupported**。 |
| Starting money pool | 用户进入产品前已持有 stablecoin（USDC / USDT / WUSD / FDUSD），经外部交易所或 self-custody wallet 充值进入 DTC-custodied stablecoin Wallet；另有 separate Card Balance，消费扣 Card Balance。Wallet→Card funding mechanism Unknown，但不改变“进入产品前的 stablecoin 起点”。 |
| Final real-world payment outcome | card real-world spending |

### 3.2 ether.fi vs AIX

| Gate input | Direct Pay | Borrow Mode | Gate result |
|---|---|---|---|
| Same region | PH yes；VN unsupported-on-restricted-page；AU full-journey Unknown；available-vs-restricted conflict noted | PH yes，但下一项已失败 | **Yes on PH segment** |
| Same core Job | J2-compatible on stablecoin-starting segment（AIX 侧 Job 标 analysis inference） | **J3 primary**; AIX J3 unsupported | **No** |
| Same starting money pool | stablecoin-starting segment yes（already-held USDC / USDT 与 AIX 起点直接交集）；custody/container difference 不属于第 3 项门槛 | Borrow collateral 列表含 USDC / USDT，事前 stablecoin 起点可 overlap；custody/container 差异不用于判 No | Not required for direct decision |
| Substitutable outcome | card real-world spend | card real-world spend，但需 preceding gates | **Yes** |
| **Overall** | **Yes / direct candidate for PH stablecoin-starting J2 segment** | **Not direct** | — |

ether.fi Direct Pay 对 AIX 的 PH stablecoin-starting J2 segment 是 **direct candidate**；这是 evidence-level four-AND 判定，不等于 X/Y/cluster 相同（S4 candidate vs AIX Species Unknown），也不自动处理 Step 4 的竞争强度。Borrow Mode 是 S6-onchain candidate，与 AIX 无同 mechanism overlap，可列 **indirect / reference competitor**。

### 3.3 Nexo vs AIX

| Gate input | Debit Mode | Credit Mode | Gate result |
|---|---|---|---|
| Same region | EEA+UK vs AIX complete-journey PH anchor；无 overlap | EEA+UK vs AIX complete-journey PH anchor；无 overlap | **No** |
| Same core Job | J2-compatible on stablecoin-starting segment（AIX 侧 Job 标 analysis inference） | J3 primary; AIX J3 unsupported | Not required for direct decision |
| Same starting money pool | stablecoin is among Debit spend assets，starting pool 可与 AIX stablecoin-starting segment 对齐；不用 platform container/custody mismatch 强判 | 同 Debit Mode；不用 container mismatch 强判 | Not required for direct decision |
| Substitutable outcome | card real-world spend，但 region gate 已失败 | card real-world spend，但 preceding gates 已失败 | Not required for direct decision |
| **Overall** | **Not direct** | **Not direct** | **Not direct** |

Nexo 是 **potential / adjacent competitor**。其 Credit Mode 属于 S6-Custodial；AIX 无 borrow/credit mode，不构成同 mechanism overlap。

## 4. Unknowns & limitations

1. ether.fi available vs restricted pages 在 VN 等个别国家存在局部冲突；本报告只记录冲突，不裁决国家资格。
2. ether.fi Direct Pay 的 X3 判断依赖官方 non-custodial claim + Vault direct deduction；Vault 内 user-control boundary、receive/hold/send/spend closure 未完全证明，因此 S4 只能是 candidate / strong-adjacent。
3. ether.fi Borrow Mode X3 candidate 的 custody/control lifecycle 未完全证明；不把 X3 写成 confirmed。
4. ether.fi Card issuance fee / complete consumer fee table / minimum borrow amount 未证明。
5. Nexo Debit Mode X 被确认为 X2（available balance），Y remains Unknown：无法从 cached page 区分 B vs C。不合并成一种机制。
6. Nexo card-mode-specific borrow LTV / collateral minimums 未证明；不借用其他 Nexo credit pages。
7. Nexo card page 无 dateModified，按 accessed 2026-08-29 处理；后续若页面变化，以 current page 为准。
8. 本报告没有把 merchant acceptance、membership benefit 或 portfolio marketing 当 areaServed。
9. Agent D 的 four-AND gate 只处理 ether.fi/Nexo vs AIX。它不决定 Step 3 全玩家矩阵或 Step 4 竞争图。
10. four-AND 中 ether.fi Direct Pay 的 PH direct 判定依赖 AIX 侧 Job analysis inference 与 PH full-journey anchor；VN/AU 完整 journey 保持 Unknown。该判定不把 S4 candidate 写成 confirmed，也不改变 AIX `X1 / Y Unknown / Species Unknown` 的事实锚点。

## 5. URL index（accessed 2026-08-29）

| # | URL | Scope | Official date / cache evidence |
|---|---|---|---|
| 1 | https://www.ether.fi/personal | Cash card current product narrative, virtual/physical, non-custodial claim, issuer disclosure, borrow FAQ | etherfi-cash.html, accessed 2026-08-29 |
| 2 | https://help.ether.fi/en/articles/326983-understanding-your-cash-card-borrow-mode-vs-direct-pay-mode | Direct Pay vs Borrow mechanism, interest via Aave v4, refund handling | dateModified 2026-08-20; etherfi-modes.html |
| 3 | https://help.ether.fi/en/articles/758780-in-which-countries-is-the-cash-card-available | available countries + KYC/compliance; PH/AU listed; physical-card availability flag | dateModified 2026-08-02; etherfi-countries.html |
| 4 | https://help.ether.fi/en/articles/262373-where-is-ether-fi-cash-currently-unavailable | unsupported countries / U.S. states; VN listed; card spending unsupported list | dateModified 2026-08-23; etherfi-restricted.html |
| 5 | https://help.ether.fi/en/articles/304388-how-does-collateral-and-borrowing-work | Borrow collateral/LTV/liquidation thresholds; issuance redirect noted | dateModified 2026-06-19; etherfi-collateral.html |
| 6 | https://nexo.com/crypto-card | Nexo Card current product, Debit/Credit modes, EEA+UK FAQ, fees, $50/$5,000 activation thresholds, DiPocket UAB | canonical URL confirmed; nexo-card.html, accessed 2026-08-29 |
| 7 | https://support.nexo.com/article/how-does-the-nexo-card-work-in-credit-mode | Official card page links to this article for Credit Mode detail | nexo-card.html internal link only; live fetch returned generic Nexo Support Center shell, content not extracted; no claims taken |
| 8 | https://support.nexo.com/article/how-does-the-nexo-card-work-in-debit-mode | Official card page links to this article for Debit Mode detail | nexo-card.html internal link only; live fetch returned generic Nexo Support Center shell, content not extracted; no claims taken |
| 9 | https://support.nexo.com/article/who-can-order-the-nexo-card | Listed by sitemap; not opened as an additional official fetch. No claims taken. | nexo-sitemap-webarticle-1.xml |
