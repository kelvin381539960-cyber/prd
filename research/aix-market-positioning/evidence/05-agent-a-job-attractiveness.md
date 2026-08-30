# Step 5 Agent A 收口｜J1 / J2 / J3 市场吸引力比较（Job Attractiveness Evidence Card）

> 状态：Step 5 Agent A CLOSEOUT（2026-08-30）。只收口，不再浏览。
> 类型：Step 5 输入证据卡；比较三个 Job Family 的市场吸引力；**不选择 AIX 目标方向**。最终目标生态位与 AIX 战略决策由 Step 5 主流程决策层完成。
> 数据边界：只使用 Step 1–4 正式文档（`01`–`04`）、Step 4 已评审 evidence cards（`evidence/04-*.md`）与 Agent A 本地缓存（`/private/tmp/aix-step4-agent-a/`、`/private/tmp/aix-evidence-04/`、`/private/tmp/a16z-card-spend.html`、`/private/tmp/defillama-stablecoins.json`）。**未联网、未新增 URL、未补抓。**
> 纪律：AIX 当前能力与地理（X1 / Y Unknown / PH/VN/AU / stablecoin-only / J3 unsupported）**不进入市场吸引力排名**；AIX 仅作为 future-entrant 背景。每条判断标 Fact / Inference / Unknown，并保留来源可追溯性。

---

## 0. 术语与比较框架

- **J1 Global Money**：获得并持续使用一种稳定、可跨境、能收 / 存 / 转 / 花的钱（`01-market-overview-and-user-jobs.md` §4）。
- **J2 Crypto → Spend**：已持有 Crypto（Stablecoin 属于 Crypto），愿意卖 / 换一部分，低摩擦变成现实购买力（同源）。
- **J3 Keep Crypto → Liquidity**：不卖 Crypto、保持敞口的同时获得消费流动性（同源）。
- 比较维度：**pain strength / frequency / value creation / retention potential / monetization / competition intensity / structural trend/catalyst / structural risk**。
- 证据纪律：Unknown ≠ No；merchant acceptance ≠ issuance eligibility；future ≠ current；样本缺失 ≠ 市场空白；营销覆盖数字不进入逐国判定（`04-competition-map.md` §2.2、§7；`04-sources.md`）。
- 本卡不重算 four-AND，不替代 Step 4 主文档分类。

---

## 1. 可信证据基线（仅采用有效本地缓存 / 已评审文档）

### 1.1 Agent A J1 缓存（`/private/tmp/aix-step4-agent-a/`，2026-08-30 采集）

| 缓存文件 | 对应官方页面 | 有效性 | 本卡用途 |
|---|---|---|---|
| `kast-global-accounts.html` | https://www.kast.xyz/global-accounts | ✅ 完整可用 | J1 账户结构 / KAST 规模 / 跨境 rails |
| `kast-home.html` | https://www.kast.xyz | ✅ 完整可用 | KAST 产品定位 / rewards / 营销数字（不进入 eligibility） |
| `kast-series-a.html` | KAST Blog（$80M Series A） | ✅ 完整可用 | 1M+ users、~$5B annualized volume、营收翻倍、扩张方向 |
| `kast-card-availability.html` / `kast-debit-credit.html` / `kast-stablecoins.html` / `kast-limits-article.html` | KAST Help Center 文章 | ❌ Cloudflare challenge，无正文 | 不采信；KAST 机制冲突与 PH Unknown 沿用 Step 3 结论 |
| `plasma-one.html` | https://www.plasma.org/personal | ✅ 完整可用 | S4 / J1-leaning 样本 |
| `bleap.html` / `bleap-eligibility.html` / `bleap-pricing.html` | Bleap 官网 / Help Center | ✅ 可用（eligibility 页为 2026-07-03 written） | J1 样本；PH/VN 国籍限制 No |
| `karta.html` | https://karta.io | ✅ 完整可用 | J1 闭环不足；receive/payouts Q3 2026 future |
| `okx-pay-sg.html` | https://www.okx.com/en-sg/pay | ✅ 完整可用 | J1（SG 限定）样本 |
| `okx-card-fees-help.html` / `okx-card-get-help.html` | OKX SG 帮助页 | ❌ 404 | 费用表 Unknown |
| `karta-help.html` / `karta-pricing.html` / Bleap funding/spending collection | — | ❌ 404 / 集合页无正文 | 不采信 |

**明确排除（challenge / 404 / 空 / 搜索噪声）**：KAST 5 篇 Help Center 缓存（Cloudflare）、OKX SG 两张费用/获取帮助页（404）、Karta Help/Pricing（404）、Bleap funding/spending collection（404）、以及 `/private/tmp/aix-evidence-04/` 中 `binance-*.html/.txt`（空或仅 Wayback 参考）、`coinbase-card*`、`wirex-card*` 等 challenge/壳页。**本卡不使用这些文件产生任何事实。**

### 1.2 a16z 2026-08-07 文章（`/private/tmp/a16z-card-spend.html`，✅ 完整正文）

- 标题：*5 charts: How crypto cards are driving stablecoin spend*（Robert Hackett & Ryan Holloway，2026-08-07）。
- 关键事实（原文字句）：
  - "Crypto payment cards have gone from a novelty to more than $750 million in monthly spend."
  - "Monthly crypto payment card volume reached $759 million in July, up (roughly 2.5x) from $306 million a year earlier — and up from less than $1 million when tracking began in Oct. 2023."
  - "Nearly 9 million purchases were made using crypto payment cards during July, up from about 5.2 million a year ago."
  - "That puts the average amount spent per transaction at around $86."
  - "As of July, Optimism carries about 29% of crypto card spend volume, Solana about 19%, and Base about 19%. Gnosis has dropped to about 2%."
  - "USDC handles about 58% of card spending and USDT about 26%, up from roughly 48% and 7% a year ago, respectively."
  - "Crypto payment cards remain a small market next to traditional card networks, which process trillions of dollars per month."
  - "For the tracked programs, this is happening almost entirely through Visa."
- 口径注明：Paymentscan tracked onchain activity；RedotPay（最大项目）为 issuer self-reported，非 onchain observed。**本卡不把该数字当成全市场 TAM，只作 J2 相关轨迹证据。**

### 1.3 DefiLlama stablecoins API（`/private/tmp/defillama-stablecoins.json`，2026-08-30 本地缓存）

- 总稳定币供应（peggedUSD 口径，422 个 pegged asset 条目，334 条有 current 数值）：**≈ $310.7B**。
- 趋势：日 +$0.57B（+0.18%）、周 +$1.47B（+0.48%）、月 +$3.38B（+1.10%）；近月持续净增长。
- USD-pegged 占比：**100%（$310.7B / $310.7B）**——与 a16z State of Crypto 2025 "over 99% USD-denominated" 方向一致（该报告属 Step 1 权威背景，非本卡新增）。
- 前五大：USDT ≈ $183.4B、USDC ≈ $74.2B、USDS ≈ $6.7B、DAI ≈ $4.8B、USD1 ≈ $4.2B（排序依据同缓存）。
- 备注：DefiLlama 是汇总第三方数据源，供应数字为 Fact（以此缓存为准）；不推断其与消费支出的因果关系。

### 1.4 已评审 Step 4 evidence cards（作为事实 / inference 基线）

- `04-agent-a-j1-global-money-card.md`（PARTIAL PASS）：KAST / Plasma / Bleap / Karta / OKX SG 玩家事实采用；AIX 对照段不采用。
- `04-agent-b-custodial-exchange-prefunded-card.md`（PASS）：J2 托管 / 预充值样本（Bitget / Bybit / Crypto.com）采用。
- `04-agent-c-self-custody-wallet-native-evidence-card.md`（PARTIAL PASS）：J2 / J1 自托管样本（MetaMask / Plasma / Bleap / Karta / OKX / ether.fi / Gnosis）采用。
- `04-agent-d-credit-borrow-to-spend-evidence-card.md`（PARTIAL PASS）：J3 样本（Nexo / ether.fi Borrow / RedotPay Credit / Ledn / YouHodler）采用。
- `04-agent-e-regional-maturity-density.md`（PASS AFTER REVISION）：市场级密度数据采用；AIX baseline 段不采用。
- `04-sources.md`：证据纪律与采用范围。
- Step 1 三层规模：L1 ≈ $390B run-rate（含大量 B2B）、L2 ≈ $153B consumer-related flow、L3 card spend 2025 ≈ $4.5–5.2B / 2026-07 ≈ $759M 月、~9M 笔（`01-market-overview-and-user-jobs.md` §2/§9）。

---

## 2. 比较矩阵（市场级，AIX-independent）

> 评分刻度：High / Medium / Low / Unknown；每格标注 Fact / Inference / Unknown。J1 密度仅在“已证实可服务/发卡的组合”口径下判读；营销覆盖数不参与。

| 维度 | J1 Global Money | J2 Crypto → Spend | J3 Keep Crypto → Liquidity |
|---|---|---|---|
| **Pain strength** | **Medium–High（Inference）**：跨境收/存/转/花多重摩擦（KAST 叙事：跨 border 慢、贵、多步；Step 1 Money Friction）。凭据：KAST global-accounts 文案 + Series A 定位 | **High（Inference，有可观察行为佐证）**：存量 Stablecoin 用户要低摩擦变现实购买力；2026-07 卡消费 $759M/月、9M 笔为已发生行为，非仅问卷 | **Medium（Inference）**：明确受众 =“不想卖 Crypto 但仍要流动性”；对非持币用户无痛点；J2 的“愿意卖一部分”用户不构成 J3 痛点 |
| **Frequency** | **High（Inference）**：收工资/汇款/日常收付是重复性资金行为；KAST 定位“every move / one account” | **Medium–High（Inference）**：月 9M 笔、均额 ~$86 指向高频小额；但从存量资产池转为消费的触发频次低于日常账户收付 | **Low–Medium（Inference）**：borrow-to-spend 是资金结构决策 + 消费事件组合；频率天然低于直接 spend，且“借款余额”非每笔都发生 |
| **Value creation** | **High（Inference）**：替换传统跨境银行/汇款链条；KAST 证据：US/EU 账户、ACH/SEPA/SWIFT/Fedwire、Unified Balance receive/send/spend、无 US residency 要求。价值上限高，但依赖 region 落地 | **High but bounded（Inference）**：解决“卖币→法币→消费”的转换摩擦；a16z 数据显示机制已被规模化采用，但单笔价值上限受均额/卡渗透限制 | **Medium–High（Inference）**：为“不愿卖币”用户解锁消费流动性，保留资产敞口（Nexo/ether.fi/RedotPay Credit 叙事）；价值真实但受众窄、机制复杂 |
| **Retention potential** | **Highest（Inference）**：Money Account 心智 + receive/send/spend 闭环 => 主账户切换成本高（Step 4 §4.1；KAST 账户结构）；测试题：“用户是否说这是我账户/我的钱” | **Medium（Inference）**：Spend-first 用户按“消费入口”使用，更易因价格/新增竞品切换；Step 4 §3 竞争变量中成本/体验直接可比较 | **Medium–High（Inference）**：抵押借款余额 + 自动补抵押/还款机制形成资金关系；但若无持续消费或借款需求，可长期休眠 |
| **Monetization** | **High（Inference）**：FX/conversion spread、Premium 订阅（KAST $1,000/$10,000/年）、card fees、ATM/FX 费、沉淀资金相关收益；KAST revenue doubled since Sep 2025（品牌自述） | **Medium（Inference）**：发卡费（RedotPay $10/$100、Bitget 0）、FX/ATM 费、可能的 interchange；L3 基数 $759M/月，但竞争使价差压缩；更依赖消费流水 | **Medium–High（Inference）**：利息（Nexo 1.9% 起、RedotPay 0.05%/day、Ledn 9.25–11.49% APR）+ 清算/费用结构可产生收入；但风险成本与合规成本高 |
| **Competition intensity** | **Medium（Inference，区域差异大）**：KAST 强账户样本，Plasma/Bleap/Karta/OKX SG 在途；**0 个“Money Account confirmed × region confirmed”组合（Fact，Step 4）**；PH J1 密度 = 0 confirmed / 5 unknown / 2 No（`04-agent-e`）→ 证据空白不是蓝海 | **Highest（Fact/Inference 混合）**：Step 3/4 样本覆盖 14 个 product modes，J2 机制簇最多（已观察 4 类机制簇，Step 4 §3）；PH/AU/SG/MX-BR/EEA+UK confirmed ≥3（`04-agent-e` §4.1）；a16z 显示多链/多程序扩张 | **Low–Medium（Inference，含 Unknown）**：confirmed 样本少：Nexo Credit（EEA+UK）、ether.fi Borrow（PH/AU available-page）、RedotPay Credit（live，region Unknown）；borrow-to-cash（Ledn/YouHodler）相邻不合并。**逐国资格 Unknown 巨大，不能写“蓝海”** |
| **Structural trend / catalyst** | **High（Inference，慢变量）**：稳定币供应 $310.7B 创新高（Fact）、稳定币成“全球美元层”（Step 1）；KAST $80M Series A + 1M users（品牌 fact）；制度/合规/银行关系决定加速度 | **Highest（Fact）**：a16z 2026-08-07：$759M/月、2.5x YoY、< $1M→$759M（Oct 2023→Jul 2026）、9M 笔、USDC 58%/USDT 26%、Visa 为主；稳定币供应 +$3.38B/月（DefiLlama Fact）作为上游池扩展 | **Medium（Inference，尚无独立动量证据）**：RedotPay Credit 上线（live + 文档 2026-04~08）、ether.fi Borrow PH/AU、Nexo 成熟但 region No；**无 J3 专属月度/增速事实** |
| **Structural risk** | **Medium–High（Inference）**：逐国牌照与银行/托管关系；KAST “not a bank/fintech powered by partners” 与 “crypto-equivalent obligation, not USD bank deposit” 披露（Fact）；合规/储备/脱锚/监管重压 | **Medium（Inference）**：监管与 issuer 依赖；卡网络规则（如 stablecoin settlement）；RedotPay restricted list、KAST availability challenge 显示地区窗口化；市场仍小（对比传统卡 trillion 规模） | **High（Inference）**：信用/清算风险、抵押品波动、利率敏感性；RedotPay Credit risk index（0.6/0.8/0.9 阈值）、liquidation、稳定币不计入 collateral（Fact）；需要牌照与风控能力；J3 机制最复杂 |

---

## 3. 逐维度来源映射（可追溯性）

| 内容 | 标记 | 来源 |
|---|---|---|
| J1/J2/J3 定义与市场边界 | Fact（本仓定义） | `01-market-overview-and-user-jobs.md` §4 |
| L1/L2/L3 三层规模 | Fact（采用口径） | `01-market-overview-and-user-jobs.md` §2/§9 |
| KAST Global Account / Unified Balance / US+EU / ACH/SEPA/SWIFT/Fedwire / receive/send/spend / “not a bank” 披露 | Fact（一手） | `kast-global-accounts.html`（`/private/tmp/aix-step4-agent-a/`） |
| KAST 1M+ users、~$5B annualized volume、revenue doubled、$80M Series A、扩张方向 | Fact（品牌自述） | `kast-series-a.html` |
| KAST 170+ countries / 150M merchants / cashback / membership 价格 | Fact（营销口径，不作 eligibility） | `kast-home.html` |
| KAST 机制冲突（C vs D）、PH Unknown | Fact（沿用 Step 3 未裁决） | `03-agent-a-redotpay-kast.md`；`03-sources.md` K3–K10 |
| Plasma / Bleap / Karta / OKX SG 事实与 region 状态 | Fact（一手） | `04-agent-a-j1-global-money-card.md`；`04-agent-c-*` |
| J2 $759M/月、2.5x YoY、9M 笔、~$86/笔、链与稳定币占比、Visa 为主、Paymentscan 口径 | Fact（第三方统计，a16z 转引） | `/private/tmp/a16z-card-spend.html`（2026-08-07） |
| 稳定币总供应 $310.7B、日/周/月增量、USD-pegged 100%、前五大 | Fact（DefiLlama API 缓存） | `/private/tmp/defillama-stablecoins.json` |
| J2 机制簇最多（Step 3/4 样本 14 个 product modes）、PH/AU/SG/MX-BR/EEA+UK confirmed ≥3、J1 0 confirmed 组合、J3 confirmed 少 | Fact（Step 4 评审后的样本读数） | `04-agent-e-regional-maturity-density.md`；`04-competition-map.md` |
| J3 机制事实（Nexo Credit/ether.fi Borrow/RedotPay Credit/Ledn/YouHodler） | Fact（已评审缓存） | `04-agent-d-credit-borrow-to-spend-evidence-card.md` |
| 各维度痛点/频率/价值/留存/变现/风险判断 | **Inference**（由上述证据推导；不写成事实） | 本卡比较框架 |
| 逐国 J1/J3 资格、J3 增速、真实留存率、货币化单位经济 | **Unknown** | Step 3/4 Unknown 清单 + 本卡 |
| 无效/被排除缓存 | Fact（排除记录） | §1.1 排除清单 |

---

## 4. 每个 Job 的 Attractiveness + Confidence + 关键 Unknown（不选方向）

> 以下为 **市场级吸引力判断**，非 AIX 建议；AIX 能力与地区不参与加权。

### 4.1 J1 Global Money

- **Attractiveness：High–Medium（按“能落地”折算为 Medium–High）**
  - 结构性价值与留存上限最高：Money Account 闭环（收/存/转/花 + unified balance）换的是主账户心智和切换成本；KAST 是目前唯一完整账户样本，并已用 $80M Series A、1M+ users、~$5B annualized volume、营收翻倍验证方向（Fact）。
  - 但**竞争密度无法确认**：0 个“Money Account × region”confirmed 组合；KAST/Plasma/Karta 的 PH 资格 Unknown；这是证据空白而非蓝海。
  - 估值折让风险：账户重资产（牌照、银行/托管关系、合规），若逐国落地慢，吸引力打折。
- **Confidence：Medium**（账户价值方向证据强；落地与地区证据弱）。
- **关键 Unknown**：KAST/Plasma/Karta 逐国（尤其 PH）服务资格；KAST 机制冲突（Y=C vs D）是否影响账户叙事；J1 用户留存/主账户心智的真实转化率；监管把稳定币账户定义为 e-money/money transmission 后的单位经济。

### 4.2 J2 Crypto → Spend

- **Attractiveness：High（有已发生行为支撑）**
  - 三项硬数据（a16z/Paymentscan）给出**可观测的“已存在需求”**：$759M/月、2.5x YoY、9M 笔、~$86/笔；加上稳定币供应 $310.7B 且持续增长（Fact），供给池大且扩张。
  - 但**竞争强度最高**：机制最多（Step 3/4 样本 14 个 product modes、4 类机制簇）、同一 segment 多个市场 confirmed ≥3；产品趋于同质（卡/QR/接受范围/返现已成为入场券，`05-agent-c`）。
  - 价值创造明确但 **bounded**：单笔均额 $86、基数 $759M/月，相对传统卡万亿市场仍小；变现空间受价格竞争挤压。
- **Confidence：High**（需求存在性与趋势为 Fact；竞争强度为已评审样本 Fact）。
- **关键 Unknown**：真实活跃用户数与留存（9M 笔 ≠ 9M 用户）；各 provider 盈亏与单位经济；逐国 eligibility 上限（KAST/Bybit/Plasma/Karta 等 0 国或局部 confirmed）；稳定币卡支出是否只是“存量 crypto 换现”转移而非净新增消费。

### 4.3 J3 Keep Crypto → Liquidity

- **Attractiveness：Medium（真实但窄、证据稀、风险高）**
  - 需求真实（不愿卖币仍要流动性），机制已存在：Nexo Credit（EEA+UK，成熟）、ether.fi Borrow（PH/AU available-page）、RedotPay Credit（live，region Unknown）；borrow-to-cash 相邻样本（Ledn/YouHodler）。
  - 但无 J3 专属市场体量/增速事实（Unknown），逐国资格 Unknown 巨大；机制复杂度与结构风险最高（信用、清算、抵押品波动、牌照）。
  - 不能因“confirmed 样本少”写蓝海：Unknown ≠ 无人。
- **Confidence：Low–Medium**（机制存在性 Fact；吸引力判断主要靠 Inference + Unknown）。
- **关键 Unknown**：J3 真实用户规模与增速；RedotPay Credit 逐国资格（PH/VN/AU）；ether.fi VN available-vs-restricted 冲突裁定；稳定币是否应计入 collateral（RedotPay 明确不计入，Fact）；J2 用户中“不愿卖币”约束的渗透率。

---

## 5. 横向结论（市场级，不选 AIX 方向）

1. **需求证据强度**：J2 > J1 > J3。J2 有月度消费/笔数/增速事实；J1 有账户结构与规模事实但无逐国落地证据；J3 只有机制样本、无体量事实。
2. **价值与留存上限**：J1 > J3 > J2。主账户心智的切换成本最高；J3 的资金关系中等；J2 消费入口切换成本最低。
3. **竞争强度**：J2 > J1（已有样本）> J3；但 J1/J3 的“低密度”主要是证据缺口（Unknown），不得读成低竞争。
4. **结构趋势**：J2 有最快可观测增长（Fact）；J1 有稳定币供应/机构化/合规催化剂（慢变量）；J3 缺少独立动量证据。
5. **结构风险**：J3 > J1 > J2（当前证据面）。
6. 三个 Job 均存在决定吸引力的关键 Unknown；本卡**不推荐、不排序**，只为 Step 5 决策层提供证据输入。

---

## 6. 约束自检

- ✅ 未联网、未新增 URL、未补抓；所有新引用均来自 Step 1–4 正式文档、Step 4 已评审 evidence cards 或 Agent A 本地缓存。
- ✅ 无效缓存（Cloudflare challenge / 404 / 空壳 / 搜索噪声）明确排除并留痕，未产生事实。
- ✅ 每条判断标记 Fact / Inference / Unknown，且提供来源映射。
- ✅ AIX 当前能力与地理未参与吸引力排名；只保留“AIX 为未来进入者”背景。
- ✅ 未选择 AIX 目标方向。
- ✅ 营销覆盖数字（170+ / 150M / 180+ 等）未进入 eligibility 或竞争密度判定；a16z 转引 Paymentscan 口径分段使用，未混入 L1/L2。
- ✅ Unknown ≠ No：J1/J3 密度低 ≠ 蓝海；J2 基数小 ≠ 无机会。

---

## 7. 来源列表（仅缓存 / 已评审文件）

| 类别 | 来源 |
|---|---|
| Step 1–4 正式文档 | `research/aix-market-positioning/01-market-overview-and-user-jobs.md`、`02-ecosystem-map.md`、`03-player-positioning.md`、`04-competition-map.md` |
| Step 4 已评审 evidence cards | `evidence/04-agent-a-j1-global-money-card.md`、`04-agent-b-custodial-exchange-prefunded-card.md`、`04-agent-c-self-custody-wallet-native-evidence-card.md`、`04-agent-d-credit-borrow-to-spend-evidence-card.md`、`04-agent-e-regional-maturity-density.md`、`04-sources.md` |
| Step 3 已评审证据（KAST conflict / AIX anchor） | `evidence/03-agent-a-redotpay-kast.md`、`evidence/03-agent-f-aix-anchor.md`、`evidence/03-sources.md` |
| Agent A J1 缓存（有效） | `/private/tmp/aix-step4-agent-a/kast-global-accounts.html`、`kast-home.html`、`kast-series-a.html`、`plasma-one.html`、`bleap*.html`、`karta.html`、`okx-pay-sg.html`（2026-08-30） |
| Agent A J1 缓存（无效/排除） | `kast-card-availability.html`、`kast-debit-credit.html`、`kast-stablecoins.html`、`kast-limits-article.html`（Cloudflare）；`okx-card-fees-help.html`、`okx-card-get-help.html`、`karta-help.html`、`karta-pricing.html`、Bleap collections（404）；`aix-evidence-04/` 中 binance/coinbase/wirex 等空壳页 |
| a16z 2026-08-07 文章 | `/private/tmp/a16z-card-spend.html`（canonical https://a16zcrypto.com/posts/article/charts-payment-card-stablecoin-spend/） |
| DefiLlama stablecoins API | `/private/tmp/defillama-stablecoins.json`（2026-08-30 缓存；422 pegged-asset 条目；aggregate 为本地计算） |
