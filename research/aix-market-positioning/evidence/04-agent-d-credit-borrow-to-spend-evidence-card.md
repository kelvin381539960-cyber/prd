# Step 4 Agent D 收口｜J3 Crypto-Backed Credit / Borrow-to-Spend 最终证据卡

> 状态：Step 4 Agent D CLOSEOUT（2026-08-30）。只收口，不再浏览。
> 类型：Step 4 输入证据卡 / mode-level 固定稿；「J3 不卖 Crypto、保持敞口获得消费流动性」簇的证据固化。不替代 Step 4 主文档 `04-competition-map.md` 的 R1–R5 分类。
> 数据边界：只使用 `/tmp/aix-j3-evidence-04/` 已采集官方页面缓存（2026-08-30 访问）与 Step 1–3 已评审定义/结论（`01-market-overview-and-user-jobs.md`、`02-ecosystem-map.md`、`03-player-positioning.md`、`evidence/03-agent-d-credit.md`、`evidence/03-agent-a-redotpay-kast.md`、`evidence/03-agent-f-aix-anchor.md`、`evidence/03-sources.md`）。**未联网、未补抓、未新增 URL。**
> AIX 纪律：AIX 仅是未来进入者。本卡不以 AIX 为比较锚点；AIX 当前事实（X1 confirmed / Y Unknown / Species Unknown / J3 unsupported）不参与任何市场级判断，也不得过滤、升级或降级任何玩家行。

---

## 0. 范围与不纳入

**纳入本卡（J3 mode 级）**：

- **Nexo Card Credit Mode**（`nexo-card.html/.txt`）与 **Nexo Credit Line / Borrow**（`nexo-lending.html/.txt`，canonical https://nexo.com/borrow）。
- **ether.fi Cash Card Borrow Mode**（`etherfi-personal.html/.txt`，canonical https://www.ether.fi/personal；Step 3 Agent D 已固定的 Borrow 机制沿用）。
- **RedotPay Credit**（5 篇官方 Help Center 缓存：credit-account-guide / balance-interest / getting-started / credit-limit / credit-risk）。

**纳入「J3 相邻 / 方向」但不作 borrow-to-spend 卡证据**：

- **Ledn**（`ledn-home.html/.txt`）：Bitcoin-backed loans，出款到 USD/USDC/本地货币，**无卡消费 rail 缓存证据**。
- **YouHodler**（`youhodler-getcash.html/.txt`、`youhodler-card.html/.txt`）：Get Cash 抵押借款可到账钱包/银行；**Crypto Card 为 "almost here" / Pre-order，非 current**。
- **Wirex**（`wirex-home.html/.txt`）：仅首页 "save, borrow, spend" 营销语句，卡页/借页面均 404，**仅 directional**。
- **Baanx**（`baanx-home.html/.txt`）：B2B OpenFi 叙事（self-custody / buy / spend / borrow），消费者产品页 404，**仅 directional B2B 技术叙事**。

**缓存存在但无效 / 不纳入落位**：

- **Binance Card / Loans**（`binance-card.html/.txt`、`binance-loans.html/.txt`、`binance-help-loan.html`）：空文件，无内容。
- **Bybit Loans**（`bybit-loan.html/.txt`）：canonical 重定向到 https://www.bybit.com/en/ 首页壳，无借款产品正文。
- **OKX Loan / Credit**（`okx-credit.html/.txt`、`okx-loan.html/.txt`）：SG/全局壳页，canonical 指向 help URL 但正文未提取；无产品事实。
- **Coinbase Card**（`coinbase-card.html/.txt`）：Cloudflare challenge（"Just a moment..."），无正文。
- **Coins.ph Loans**（`coinsph-loans.html/.txt`）：canonical 为 https://www.coins.ph/en-ph/loans 但页面 404；**不构成 Coins.ph 借款产品证据**。Coins.ph 首页仅证明其为 PH e-wallet / crypto 应用。
- **Arch Finance**（`arch-home.html/.txt`）：投资顾问/理财平台（锁定金额、最低投资、收益叙事），无卡消费 / 借款消费证据；不纳入 J3 战场。
- **Aave**（`aave-home.html/.txt`）：协议首页（onchain savings / lending / borrowing），无消费者现实支付卡 rail 证据；不纳入 consumer J3 card 战场。

---

## 1. 缓存证据清单（/tmp/aix-j3-evidence-04，2026-08-30 访问）

| 缓存文件 | 官方 URL / canonical（缓存内提取） | 内容状态 | 有效性 |
|---|---|---|---|
| `nexo-card.html/.txt` | https://nexo.com/crypto-card | 完整：Credit / Debit 双 mode、spend without selling、EEA+UK FAQ、费用、DiPocket UAB、100M merchants、100,000 BTC 叙事 | ✅ 有效（J3 主证据） |
| `nexo-lending.html/.txt` | https://nexo.com/borrow | 完整：crypto-backed Credit Line、1.9% 起、$50–$2M、BTC/ETH 50% LTV、USDT/USDC 90% LTV、NEXO 15%、无 credit check、灵活还款 | ✅ 有效（J3 主证据，非卡专属参数） |
| `nexo-credit-line.html/.txt`、`nexo-credit.html/.txt` | 无 canonical（站点壳） | 导航壳 + "Page not found" | ❌ 无效；不取事实 |
| `etherfi-personal.html/.txt` | https://www.ether.fi/personal | 完整：Cash card、Borrow "access cash without selling"、credit card 问答、non-custodial 声明、issuer 声明 | ✅ 有效（J3 主证据） |
| `redotpay-credit-account-guide.html/.txt` | https://helpcenter.redotpay.com/en/articles/11093458-guide-to-using-the-credit-account | 完整：Credit Account vs Funding Account、pledge、credit limit spend、LTV 0.9 buffer（dateModified 2026-07-21） | ✅ 有效（J3 主证据） |
| `redotpay-credit-balance-interest.html/.txt` | https://helpcenter.redotpay.com/en/articles/11093493-understanding-your-credit-balance-and-interest | 完整：credit balance、no selling、pledged assets、0.05%/day simple interest（2026-07-21） | ✅ 有效（J3 主证据） |
| `redotpay-credit-getting-started.html/.txt` | https://helpcenter.redotpay.com/en/articles/13224754-getting-started-with-redotpay-credit | 完整：v3.0.0+、自动 credit limit、非稳定币 collateral、card/checkout 使用（2026-04-10） | ✅ 有效（J3 主证据） |
| `redotpay-credit-limit.html/.txt` | https://helpcenter.redotpay.com/en/articles/13224793-understanding-your-credit-limit | 完整：公式、支持资产（BTC/BNB/ETH/GRAM/S/SOL/TON/TRX/XRP）、稳定币不计入（2026-08-25） | ✅ 有效（J3 主证据） |
| `redotpay-credit-risk.html/.txt` | https://helpcenter.redotpay.com/en/articles/13224824-managing-your-credit-risk | 完整：risk index 0–0.6–0.8–0.9、liquidation、0.05%/day、还款方式（2026-08-06） | ✅ 有效（J3 主证据） |
| `ledn-home.html/.txt` | 缓存页无 canonical 标签；本地 URL 记录 https://ledn.io | 完整：BTC-backed loans、APR 9.25–11.49%、50% LTV、$500 起、出款 USD/USDC/本地货币 | ✅ 有效（J3 相邻，borrow-to-cash） |
| `youhodler-getcash.html/.txt`、`youhodler-card.html/.txt`、`youhodler-home.html/.txt` | 缓存页无 canonical；本地 URL 记录 https://www.youhodler.com | 完整：Get Cash（借贷到钱包/银行）、Crypto Card "almost here" / Pre-order | ✅ 有效（J3 相邻 / 卡非 current） |
| `wirex-home.html/.txt` | https://www.wirexapp.com | 首页营销："Save, borrow, spend, and trade"；无 mode 级借款/卡参数 | ⚠️ 仅 directional |
| `wirex-card.html/.txt`、`wirex-credit*.html/.txt` | — | 404 Error | ❌ 无效 |
| `baanx-home.html/.txt` | 缓存页无 canonical；本地 URL 记录 https://www.baanx.com | B2B OpenFi 营销 + 合作伙伴引语；消费者产品页 404 | ⚠️ 仅 directional |
| `baanx-card.html/.txt`、`baanx-digital-credit.html/.txt`、`baanx-lend.html/.txt`、`baanx-products.html/.txt` | — | "Not Found" | ❌ 无效 |
| `arch-home.html/.txt` | https://arch.finance | 投资平台：金额锁定、最低投资、顾问分层；无借款消费卡 | ❌ 不属 J3 card 战场 |
| `coinsph-home.html/.txt` | https://www.coins.ph/en-ph | PH e-wallet / crypto 应用首页 | ⚠️ 仅区域背景 |
| `coinsph-loans.html/.txt` | https://www.coins.ph/en-ph/loans（页面 404） | 404 | ❌ 无借款证据 |
| `aave-home.html/.txt` | https://aave.com/ | 协议首页：onchain savings / lending / borrowing | ❌ 无消费者卡 rail |
| `binance-card.html/.txt`、`binance-loans.html/.txt`、`binance-help-loan.html` | — | 空 / 无正文 | ❌ 无效 |
| `bybit-loan.html/.txt` | canonical 重定向 https://www.bybit.com/en/ | 首页壳 | ❌ 无借款正文 |
| `okx-credit.html/.txt`、`okx-loan.html/.txt` | canonical 指向 help/loans URL | 壳页，无提取正文 | ❌ 无效 |
| `coinbase-card.html/.txt` | — | Cloudflare challenge（"Just a moment..."） | ❌ 无效 |

---

## 2. J3 判定口径（沿用 Step 1–3，不重算）

- **J3**：不卖 Crypto、保持敞口的同时获得消费流动性（`01-market-overview-and-user-jobs.md`）。
- **Y=D Collateral-backed borrowing / credit**：资产作为 collateral，产生 debt / credit balance（`02-ecosystem-map.md`）。
- **S6 是跨 X 的机制策略簇**：S6-Custodial（X2×D，Nexo Credit Mode）与 S6-Onchain/Self-custody variant（X3×D，ether.fi Borrow Mode）为同一 Job 下的两个 variant；不硬拆两个物种。
- **Region 纪律**：merchant acceptance / 100+ / 150M / 170+ / 180+ 等营销数字不进入 issuance 判定；Unknown ≠ No。
- **Current / Future**：coming soon / pre-order / "almost here" 一律不升级为 current。
- **本卡不做 four-AND / R1–R5 判定**：只固定 mode 级证据；RedotPay Credit 是否独立成 four-AND row 留给 Step 4 主文档 / Step 5 决定。

---

## 3. Mode 证据卡

### 3.1 Nexo Card Credit Mode + Nexo Credit Line（J3 主样本：S6-Custodial）

**缓存依据**：`nexo-card.html/.txt`（canonical https://nexo.com/crypto-card）、`nexo-lending.html/.txt`（canonical https://nexo.com/borrow）。

已固化事实（逐一对应缓存原文）：

- 卡页明确双 mode："Switch between Credit and Debit Mode with one tap. Spend without selling your crypto"；Credit Mode 使用 crypto-backed Credit Lines；"Access capital without selling your crypto"、"flexible repayment with no fixed schedule or credit checks"。
- 官方 FAQ："Credit Mode allows you to make purchases without having to sell your Bitcoin or other crypto. It also helps you retain the upside potential of your crypto"。
- 品牌级叙事：超过 100,000 BTC "stayed in clients' portfolios while they spent with the Nexo Card"（营销叙事，不作为机制事实之外的 issuance/目录依据）。
- Borrow 页："Don't sell your crypto, borrow against it."；rates "start at 1.9% per year"；"Receive between $50 and $2M with instant approval and no credit checks"；"Spend without selling" 场景；"The more you top up your Nexo account, the more you can borrow and spend"。
- LTV（Borrow 页 calculator 可见）：BTC 50%、ETH 50%、NEXO 15%、USDT 90%、USDC 90%；"Combine BTC, ETH, and 100+ supported assets as collateral"。
- 还款：部分/全额随时还款、无固定日期、无最低分期、可用 crypto 或 stablecoin 还款；自动还款（LTV 上升时部分 collateral 自动偿还）机制存在。
- 地区：卡 FAQ 明确 "currently available only to citizens and residents of selected European countries, including the European Economic Area (EEA) and the United Kingdom"；issued by DiPocket UAB。**PH/VN/AU = No。**
- 费用/门槛（卡页）：virtual card 激活需至少 $50；physical card 需 balance > $5,000 + Gold tier；FX 周中 EEA/UK/CH 0.2% / ROW 2%，周末 0.7% / 2.5%；ATM 免费额度按 tier（至 €2,000 / £1,800/月）；无月费/年费/不活跃费（卡页口径）。

坐标（沿用 Step 3，且 Borrow 页证据支持）：

| 维度 | 结论 |
|---|---|
| X | X2（平台托管 available balance / Nexo account） |
| Y | **D confirmed**（crypto-backed Credit Line / collateral） |
| Strategy Cluster | **S6-Custodial** |
| Account Role | Spend Feature at most（卡页未证明 receive/hold/send/spend + unified balance closure） |
| Region vs PH | **No（EEA+UK）** |

### 3.2 ether.fi Cash Card Borrow Mode（J3 主样本：S6-Onchain/Self-custody candidate）

**缓存依据**：`etherfi-personal.html/.txt`（canonical https://www.ether.fi/personal）；Borrow 机制沿用 Step 3 Agent D 已评审证据（`evidence/03-agent-d-credit.md`），本卡不重抓。

已固化事实（缓存原文 + Step 3 固定结论）：

- Personal 页叙事："Hold, earn, borrow, spend, trade, and send"；"Access cash without selling — Borrow against the assets you hold and access cash when you need it."。
- Cash card FAQ："How often do I need to pay off my credit card balance? You are able to spend without selling your assets by taking out a loan against your entire portfolio. There is no repayment schedule, you can repay whenever you like."。
- 官方披露：ether.fi 是 non-custodial 应用；Cash card 由独立 Issuer 按单独条款发行。
- Step 3 Agent D 已固定：Borrow Mode = Vault 资产作 collateral / spending base，不卖 crypto；interest 立即 accrues、variable APY（经 Aave v4）；无 grace period / billing cycles；refund 回 Vault main balance，不自动还款；LTV 按资产（USDC/USDT/EURC/frxUSD 90%；LiquidUSD/eUSD/LiquidReserve 80%；wETH/weETH 55%；LiquidETH/LiquidBTC 50%；eBTC 52% 等）。
- 地区：available-countries 页列 PH/AU；restricted 页列 VN（available vs restricted 局部冲突保持不裁决）。

坐标（沿用 Step 3）：

| 维度 | 结论 |
|---|---|
| X | X3 candidate（Vault user-control 边界未完全证明） |
| Y | **D confirmed**（collateral-backed borrow / credit） |
| Strategy Cluster | **S6-Onchain / Self-custody candidate** |
| Account Role | —（无独立账户角色判定） |
| Region vs PH | PH available 页 Yes；VN conflict；AU available 页 Yes |

### 3.3 RedotPay Credit（J3 live 样本；Step 3 仅列为 J3 segment 示例，未作独立 four-AND row）

**缓存依据**：5 篇官方 Help Center 文章（见 §1；2 篇 2026-07-21、1 篇 2026-04-10、1 篇 2026-08-25、1 篇 2026-08-06 dateModified；均 v3.0.0+ 或 pre-v3.0.0 兼容说明）。

已固化事实（逐一对应缓存原文）：

- 定位："spend without selling your crypto"；"By using your assets as a safety collateral, you get an instant credit line for your daily purchases"。
- 账户结构：Funding Account（主钱包，deposits 到达）与 Credit Account（pledged assets）分离；转入 Credit Account 的资产作 collateral，存在未偿余额时不可 withdraw。
- 消费机制：card transaction "deducted from your credit limit rather than your wallet balance"；每次交易产生 credit balance；pledged collateral 锁定至还款。
- Credit limit 公式：`Available credit limit = Asset value × LTV − Outstanding balance`（缓存原文）。
- 支持 collateral 资产：**BTC、BNB、ETH、GRAM、S、SOL、TON、TRX、XRP**；**稳定币 USDT/USDC 不计入 credit limit**（缓存原文明确）。
- 利率：0.05%/day simple interest（principal-only，不复合）；无固定还款日 / pay-as-you-go；无 lock-in；无隐瞒费用（官方声明口径）。
- 风险机制：risk index = outstanding / collateral value；<0.6 Safe；0.6–0.8 Moderate；0.8–0.9 Margin Call；≥0.9 liquidation triggered；支持 Auto-Collateral；LTV safety buffer 0.9（90%）。
- 还款：Repay via Balance 或 Repay via Collateral；全额还款（via balance）默认自动释放全部 pledged assets。
- 地区：**PH/VN/AU 逐国 Credit 资格未证**（缓存无资格列表）；Help 文章含 Money Lender's Licence No. [1715/2025]（香港放债人牌照，仅主体资格背景，不作 PH 可用性）。

坐标与边界：

| 维度 | 结论 |
|---|---|
| X | 信用卡支付不扣 wallet balance；扣 credit limit，pledged assets 位于 Credit Account。Step 3 未给 RedotPay Credit 分配正式 X 坐标；本卡保留 **X unassigned（Credit-Account-anchored）**，不强行套 X2 |
| Y | **D confirmed（crypto-backed credit line / collateral）** |
| Strategy Cluster | **S6（custodial variant candidate）**；Step 3 仅作为 J3 segment 示例，不升级 four-AND row |
| Account Role | Spend Feature / Credit mode；不涉及 Money Account 判定 |
| Region vs PH | **Unknown**（无逐国资格证据；不可用 PH/VN/AU restricted 推理代替） |

### 3.4 J3 相邻 / 方向样本（borrow-to-cash，无卡消费 rail 证明）

| 玩家 | 缓存证据 | J3 关系 | Region vs PH |
|---|---|---|---|
| **Ledn** | BTC-backed loans：APR 9.25–11.49%（B2X 计算器 9.25–10.99% 区间）；起始 50% LTV；margin call 70% LTV / liquidation 80%；$500 min；出款 USD/USDC/本地货币；无卡、无消费 rail 证据 | **J3 相邻（borrow-to-cash）**；满足"不卖 BTC"但最终结果是现金/稳定币，不是 borrow-to-spend card | Unknown（"100+ / 120 countries" 为营销口径；eligibility 链接未缓存） |
| **YouHodler** | Get Cash：crypto/stablecoin 作 security，获得 USD/EUR/GBP/CHF/BTC/stablecoin，资金进入 Wallet，可银行/交易所/Apple Pay 等还款；Crypto Card 页面为 "Your Crypto Card is almost here" + Pre-order | **J3 相邻（borrow-to-cash）**；有 Card 路线但 **非 current** | Unknown / 站点按司法辖区屏蔽页；无 PH 资格证据 |
| **Wirex** | 首页 "Save, borrow, spend, and trade — all from one dashboard"；无借款/卡参数页（404） | **Directional only**；无 mode 级事实 | Unknown（无资格证据） |
| **Baanx** | B2B OpenFi 叙事："self-custody transactions, allowing users to buy, spend, and borrow directly against digital assets"；消费者产品页 404 | **Directional only（B2B 技术叙事）**；无消费者 J3 卡事实 | Unknown |

**不纳入**：Arch（投资平台）、Coins.ph（/loans 404）、Aave（协议，无卡 rail）、Bybit Loan / OKX Loan / Binance Loan / Coinbase Card（壳页/空缓存）。

---

## 4. J3 borrow-to-spend 战场读数（AIX-independent）

1. **已观察 J3 borrow-to-spend 样本**：Nexo Card Credit Mode（S6-Custodial，地区 EEA+UK）与 ether.fi Cash Card Borrow Mode（S6-Onchain candidate，地区证据 PH Yes / VN conflict / AU available 页 Yes）；RedotPay Credit 为 live 的第三方官方样本（地区 Unknown，Step 3 未独立 four-AND）。
2. **J3 与 J2 消费簇的边界**：J3 的核心购买力形成是 collateral-backed credit（Y=D），不是直接扣 stable balance（Y=C）或卖出（Y=B）。RedotPay Credit 明确排除 stablecoin 计入 credit limit，进一步说明该簇面向"持 crypto 不卖"用户；J2 stablecoin-starting 消费段不在同一 mechanism。
3. **PH J3 密度（证据级）**：confirmed = 1（ether.fi Borrow，available-page 级别，受资格页冲突/逐国 issuer 细节限制）；Unknown = RedotPay Credit、Ledn、YouHodler；No = Nexo（EEA+UK）。Nexo 因此是 J3 机制成熟样本但不出现在 PH。
4. **borrow-to-cash vs borrow-to-spend 不合并**：Ledn / YouHodler 提供"借款→现金/稳定币到账"而不是"借款额直接在卡上消费闭环"；两者不可合成一种机制（同 Step 3"不能合成一种机制"纪律）。
5. **当前无任何 J3 pair 达到 R1-confirmed**：Nexo Credit 与 ether.fi Borrow 为 S6 同簇（D 同、X 不同、地区不同，Step 4 主文档按 R4 处理）；RedotPay Credit 的 X 与地区未证。本卡不重判 R1–R5。

---

## 5. AIX 未入市对照（仅 future-entrant 输入，不改市场级关系）

- AIX current anchor（`03-agent-f-aix-anchor.md`）：J3 unsupported——无 collateral / credit / borrow 能力证据；X1 confirmed / Y Unknown / Species Unknown；Account Role 最多 Account-adjacent。
- 本卡所有玩家落位与 AIX 是否存在无关；**不得用 AIX 的 PH 锚点反向改写 Ledn / YouHodler / RedotPay Credit 的 Unknown 行**。
- 若 AIX 未来进入 J3，需新的 borrow/credit 能力；该方向属于 Step 5 战略选项，本卡不评估。

---

## 6. 未解决 Unknown（Step 4 主文档 / Step 5 输入）

1. RedotPay Credit 的逐国 eligibility（PH/VN/AU）与 pre-v3.0.0 / v3.0.0+ 版本口径差异（guide 文章注 pre-v3.0.0，其余注明 v3.0.0+）。
2. ether.fi available vs restricted 页在 VN 的冲突；Borrow Mode 的逐国 issuer 终表。
3. Nexo 卡 Credit Mode 是否有独立的卡专属 LTV / collateral minimum（Borrow 页 LTV 为 Credit Line 通用参数，未证明逐卡适用）。
4. Ledn / YouHodler 的 PH 资格（营销人口数不进入判定；Ledn eligibility 帮助链接未缓存）。
5. YouHodler Crypto Card 上线状态（"almost here" / Pre-order 到 current 的时点）。
6. Wirex / Baanx 的 directional 声明是否代表 current consumer 产品（当前仅首页/B2B 声明）。
7. Coins.ph 借款产品是否存在（/loans 404 不是否定证据，只是当前缓存不可用）。
8. Aave 等 onchain 借贷协议是否应作为 infra reference 进入 Step 5 J3 图谱（本卡不判）。

---

## 7. 约束自检

- ✅ 未联网、未补抓、未新增 URL；所有缓存 canonical 均从 `/tmp/aix-j3-evidence-04/` 本地 HTML 提取。
- ✅ AIX 只作为 future-entrant 出现；未用 AIX PH / X1 / Y Unknown 定义任何玩家行。
- ✅ J3 / Y=D / S6 判定沿用 Step 1–3；RedotPay Credit、Nexo、ether.fi 坐标未越权升级。
- ✅ Unknown ≠ No：RedotPay Credit、Ledn、YouHodler PH 行保持 Unknown；Nexo EEA+UK 保持 No。
- ✅ Future 未当 current：YouHodler Crypto Card "almost here" 不视为已上线；Wirex / Baanx 仅 directional。
- ✅ merchant acceptance / 100+ / 120 / 150M / 170+ / 180+ / $10B loans 等营销数字未进入 issuance 判定。
- ✅ borrow-to-cash（Ledn / YouHodler）与 borrow-to-spend（Nexo / ether.fi / RedotPay Credit）未合并。
- ✅ 无效缓存（Coinbase、Binance、Bybit Loan、OKX Loan、Coins.ph Loans、Baanx/Wirex 404）明确排除，不产生事实缺口。
- ✅ 本卡不替代 `04-competition-map.md` 的 R1–R5 分类。

---

## 8. 来源映射（仅本地证据文件 / 缓存，无新 URL）

| 本卡内容 | 来源 |
|---|---|
| Nexo Card Credit Mode 全部条目 | `nexo-card.html/.txt`（canonical https://nexo.com/crypto-card，2026-08-30 缓存） |
| Nexo Credit Line / LTV / 利率 / $50–$2M | `nexo-lending.html/.txt`（canonical https://nexo.com/borrow，2026-08-30 缓存） |
| ether.fi Personal / Borrow 叙事 | `etherfi-personal.html/.txt`（canonical https://www.ether.fi/personal，2026-08-30 缓存） |
| ether.fi Borrow 机制 / LTV / Aave v4 | `evidence/03-agent-d-credit.md`（Step 3 已评审）；`evidence/03-sources.md` E2/E5 |
| RedotPay Credit 5 篇 | `redotpay-credit-*.html/.txt`（dateModified 见 §1） |
| Ledn / YouHodler / Wirex / Baanx / Arch / Coins.ph / Aave / Bybit / Binance / OKX / Coinbase | `/tmp/aix-j3-evidence-04/` 对应缓存（见 §1） |
| J3 / Y=D / S6 / Account Role 定义 | `01-market-overview-and-user-jobs.md`、`02-ecosystem-map.md` |
| Step 3 落位与 four-AND 边界 | `03-player-positioning.md`、`evidence/03-agent-a-redotpay-kast.md`、`evidence/03-agent-e-crosscheck.md` |
| AIX future-entrant 锚点 | `evidence/03-agent-f-aix-anchor.md`、`evidence/02-agent-f-aix-current-position.md` |

---

## 9. 输出 JSON

```json
{
  "outcome": "PASS",
  "summary": "Step 4 Agent D closeout materialized the final J3 crypto-backed credit / borrow-to-spend evidence card from /tmp/aix-j3-evidence-04 caches plus Step 1-3 definitions only (no browsing, no new URLs). Fixed facts: Nexo Card Credit Mode = X2 x D / S6-Custodial / EEA+UK only / borrow page confirms 1.9% starting rate, 50-2M USD range, BTC/ETH 50% LTV, USDT/USDC 90% LTV, no credit checks, flexible repayment; ether.fi Borrow Mode = X3 candidate x D / S6-Onchain candidate / PH available-page Yes with VN conflict and AU available-page Yes / non-custodial claim retained; RedotPay Credit = live official v3.0.0+ feature, credit-limit formula, 9 supported non-stable collateral assets (BTC/BNB/ETH/GRAM/S/SOL/TON/TRX/XRP), stablecoins excluded, 0.05% daily simple interest, risk-index thresholds 0.6/0.8/0.9, PH eligibility Unknown; Ledn and YouHodler kept as J3-adjacent borrow-to-cash (no spend-card rail; YouHodler Crypto Card pre-order/non-current); Wirex/Baanx directional-only; invalid caches (Coinbase, Binance, Bybit Loan, OKX Loan, Coins.ph Loans, Baanx/Wirex 404s) excluded from placement; Arch/Aave/Coins.ph not J3 card players per cache. AIX kept strictly future-entrant; no AIX capability or geography row filtered, upgraded, or downgraded any competitor; J3 vs J2 borrow-to-spend vs borrow-to-cash distinctions preserved. No R1-R5 reclassification attempted.",
  "changedFiles": [
    "research/aix-market-positioning/evidence/04-agent-d-credit-borrow-to-spend-evidence-card.md"
  ],
  "tests": [
    "every cited cache file exists under /tmp/aix-j3-evidence-04 and its extracted text supports the quoted fact (spot-checked nexo-card, nexo-lending, etherfi-personal, all five redotpay-credit articles, ledn-home, youhodler-getcash, youhodler-card)",
    "canonical/dateModified extraction from cached HTML (nexo-card=nexo.com/crypto-card; nexo-lending=nexo.com/borrow; etherfi-personal=www.ether.fi/personal; RedotPay articles have JSON-LD dateModified 2026-04-10/07-21/08-06/08-25)",
    "invalid cache audit: coinbase-card (Cloudflare challenge), binance card/loans (empty), bybit-loan (homepage redirect), okx credit/loan (shell), coinsph-loans (404), baanx/wirex credit pages (404) marked non-evidence",
    "J3 mechanism discipline check: Y=D only for collateral-backed credit; direct stable-value deduction (Y=C) and at-payment conversion (Y=B) not merged into J3",
    "borrow-to-cash vs borrow-to-spend check: Ledn and YouHodler not listed as borrow-to-spend card providers",
    "current/future check: YouHodler Crypto Card 'almost here'/pre-order and Wirex/Baanx directional claims not treated as current",
    "region discipline check: PH rows for RedotPay Credit/Ledn/YouHodler stay Unknown; Nexo stays No (EEA+UK); merchant/marketing numbers not used as issuance evidence",
    "AIX guardrail scan: AIX appears only in future-entrant discipline; no AIX fact changed any competitor row",
    "R1-R5 scope check: card performs no Step 4 competition-map classification"
  ],
  "commands": [
    "ls -la /tmp/aix-j3-evidence-04 to inventory 21 cache files (html+txt)",
    "python3 canonical/dateModified extraction over /tmp/aix-j3-evidence-04/*.html to verify local source URLs",
    "rg -n -i 'spend without selling|credit line|collateral|0.05|LTV' /tmp/aix-j3-evidence-04/*.txt to verify every cited fact against cache text",
    "git status --short to confirm only the new evidence card was added"
  ],
  "decisionsRequired": [
    "Decide whether RedotPay Credit becomes an independent J3 four-AND row / Step 4 mode (currently only a Step 3 J3 segment example) and resolve its PH/VN/AU eligibility plus pre-v3.0.0 vs v3.0.0+ article mismatch",
    "Resolve ether.fi available-vs-restricted page conflict for Vietnam and confirm PH country-level issuance for Borrow Mode",
    "Confirm whether Nexo card Credit Mode uses the Borrow-page LTV parameters (BTC/ETH 50%, USDT/USDC 90%) or has separate card-specific collateral minimums",
    "Determine whether Ledn / YouHodler borrow-to-cash products should enter J3 competition density as adjacent alternatives despite having no card-spend rail",
    "Re-check YouHodler Crypto Card launch status once it moves beyond pre-order before treating it as current J3 spend rail",
    "Decide whether Wirex/Baanx directional 'borrow' claims and Aave onchain lending warrant a Step 5 verification list or are out of scope",
    "Decide whether Coins.ph PH loans (current cache 404) should be re-collected for the PH J3 density picture"
  ],
  "requiresGptReview": true
}
```
