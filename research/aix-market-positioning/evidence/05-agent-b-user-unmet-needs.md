# Step 5 Agent B 证据卡｜按用户 Job / Trigger 拆分的未满足需求（User Unmet Needs by Job / Trigger）

> 状态：Step 5 Agent B MATERIALIZE ONLY（2026-08-30）。只物化，不研究、不浏览、不补抓、不改其它文件。
> 类型：Step 5 输入证据卡；说明「哪些用户、在什么触发下、现有替代是什么、痛点与信任要求是什么、哪些已服务好/哪些弱」。
> 数据边界：只使用 Step 1–4 正式文档（`01-market-overview-and-user-jobs.md`、`02-ecosystem-map.md`、`03-player-positioning.md`、`04-competition-map.md`）、Step 4 已评审 evidence cards（`evidence/04-*.md`）与 `/tmp/agentb5/` 中已检查判定可用的 `visa.html`、`pymnts.html`。
> AIX 纪律：本卡**不定义 AIX 当前或目标生态位**，不给最终 AIX 目标推荐；AIX 当前能力与地理（地区、币种、机制、缺口）**不得定义任何用户 segment**，正文以市场需求为唯一视角。
> 判定纪律：每条判断标 **Fact / Inference / Unknown**；Unknown ≠ No；营销覆盖数字不进入资格判定；future ≠ current；无调查数据时不得编造用户态度百分比。

---

## 0. 缓存资产与来源可用性（/tmp/agentb5，2026-08-30 已检查）

| 缓存文件 | 内容状态 | 可用性 | 本卡用途 |
|---|---|---|---|
| `visa.html` | 完整正文：Visa「Crypto card activity rebounds, expands globally」（Visa Economic Empowerment Institute） | ✅ **可用** | J2 网络级行为证据：日常零售支付、POS 即时转换、区域分布、2021–2025 轨迹 |
| `pymnts.html` | PYMNTS Crypto 主题页（canonical `https://www.pymnts.com/topic/crypto/`，modified 2026-08-07）：含标题级头条与报告名 | ⚠️ **部分可用** | 只用于标题/框架级信号（如「Crypto Card Spending Jumps Threefold in a Year, Paymentscan Data Shows」「From Asset to Everyday Money」），**不含正文与调查统计** |
| `coingecko2024.html` / `coingecko2025.html` | CoinGecko Challenge Verification 页 | ❌ 排除 | 无正文，不产生任何事实 |
| `bitget.html` | Bitget 新闻页 "Page not found"（React 壳） | ❌ 排除 | 404 壳页 |
| `bitgetres.html` | Bitget Academy Research 列表页 | ❌ 排除 | 内容目录页，非用户需求证据 |
| `chainalysisgeo.html` | "Page not found - Chainalysis" | ❌ 排除 | 404 |
| `circle.html` | Circle Research 项目目录（open-source technical research） | ❌ 排除 | 研究目录页，非用户需求/调查证据 |
| `cryptocom.html` | Crypto.com Research Hub `__next_error__` 壳 | ❌ 排除 | 渲染错误壳页 |
| `mastercardres.html` | "Access Denied" | ❌ 排除 | 被访问控制拦截 |
| `securityorg.html` | "Page not found | Security.org" | ❌ 排除 | 404 |
| `tmp2.html` | Wayback Machine 壳页 | ❌ 排除 | 无目标内容 |
| `worldbank.html` | Cloudflare "Just a moment..." | ❌ 排除 | challenge 页 |

**关于「调查类结论」的显式排除**：全部可用缓存与 Step 1–4 正式文档中，**没有任何可用的用户态度调查统计**（如「x% 的持有者想…」）。本卡禁止断言任何未支持的用户调查结论；PYMNTS 缓存只提供标题/报告名级框架信号，不提供其调查正文或数据。

---

## 1. 证据基线（Step 1–4 已评审 + 两张可用缓存）

### 1.1 Step 1–4 已确认的事实口径

- 市场边界：**consumer crypto/stablecoin → real-world purchasing power**（消费者把 Crypto/Stablecoin 转化为现实世界购买力）；卡只是 Spend Rail 之一（`01-market-overview-and-user-jobs.md`）。
- 三个 Job Family：
  - **J1**：获得并持续使用一种稳定、可跨境的钱（收 / 存 / 转 / 花）。
  - **J2**：已持有 Crypto（含 stablecoin），低摩擦变成日常购买力。
  - **J3**：不卖 Crypto、保持敞口的同时获得消费流动性。
- Step 4 市场级纪律：Unknown ≠ No；merchant acceptance ≠ issuance/service eligibility；future/waitlist ≠ current；样本缺失 ≠ 市场空白（`04-competition-map.md`）。
- Step 4 密度（样本内 14 modes）：PH / AU / SG / MX-BR / EEA+UK（聚合）均观察到 ≥3 个已证实 J2 provider；J1「Money Account confirmed × region confirmed」组合 = 0；J3 只有少数机制样本（`04-agent-e-regional-maturity-density.md`）。

### 1.2 `visa.html` 可引用事实（Fact，Visa 官方网络数据）

1. Visa 观察到 crypto card 使用「renewed and accelerating consumer interest in leveraging cryptocurrencies and stablecoins for everyday retail payments」（用于 everyday retail payments）。
2. Visa crypto card programs 允许消费者在任意接受 Visa 的商户花 cryptocurrencies 或 stablecoins；**digital assets → local fiat 的转换在销售点即时发生**，商户侧无改动，按现有 Visa settlement 收款。
3. VisaNet 数据轨迹：以 2021-01 为 1x，2022-04 峰值约 11x；Terra Luna 后回落并在 2023 年走平；**2024 年起恢复增长，大体跟随 stablecoin issuance**；**2025 年底接近此前高点**，区域分布明显更多元，**亚太由 issuer 区域口径看占比最大**（2025-10 时点）；stablecoin supply 2025-11 约为 2021-01 的 9x。
4. 图注口径：来源为 VisaNet + Visa Onchain Analytics Dashboard；regional share 按 issuer 区域，不代表持卡人所在地或逐国资格。

### 1.3 `pymnts.html` 可引用信号（标题/框架级，不是统计）

1. 头条标题：**"Crypto Card Spending Jumps Threefold in a Year, Paymentscan Data Shows"**（2026-08-07 前后主题页）——提示 Paymentscan/媒体把 crypto card spend 作为高增长叙事；精确数字以 Step 1 已评审的 a16z/Paymentscan 口径为准（约 $759M/月、约 2.5x YoY、约 9M 笔、约 $86/笔），**不得用标题的 "threefold" 代替精确口径**。
2. 报告名：**"From Asset to Everyday Money: Making Digital Currencies Spendable"**——「从资产到日常货币/可花」是行业使用的需求框架信号。
3. 报告名：**"The Wallet Effect: How Credit Unions Can Close the Digital Currency Access Gap"**——「数字通证的可及性差距（access gap）」是机构侧使用的框架信号，无调查正文，不生成统计事实。

---

## 2. Segment 1：稳定币 / 全球货币用户（J1 Global Money）

> 用户问题（Step 1 定义，Fact）：**我要一种稳定、可跨境、能持续收 / 存 / 转 / 花的钱，而不是每次都要转换/绕路。**

### 2.1 触发与频率

| 项 | 内容 | 标记 |
|---|---|---|
| 触发 | 跨境收工资 / 收发票 / 收汇款；日常收付；跨境购物与旅行资金；把 stablecoin 当长期「钱」使用，而不是一次性投机资产 | **Inference**（由 J1 定义与玩家叙事推导；`01-market-overview-and-user-jobs.md`；KAST "receive salary/invoices / every move" 为品牌定位证据） |
| 频率 | 重复性资金行为，账户级使用频率高；但“切换主账户”是一次性低频决策 | **Inference**（无逐户频率统计数据） |
| 子段 | ① 跨境工薪/汇款接收者；② 已有稳定币、想要统一账户心智的用户；③ 跨境经营/自由职业者（收外币发票） | **Inference**（仅 J1 定义内可推导；无调查支持细分占比） |

### 2.2 当前替代

| 替代 | 证据 | 标记 |
|---|---|---|
| 传统跨境银行/电汇/汇款 rails（ACH/SEPA/SWIFT/当地银行体系） | Step 1 Money Friction 概念；Step 4 非卡 rails 证据（bank/remittance cash-out、InstaPay/PESONet） | **Fact**（rails 存在）；跨行摩擦程度 = **Inference** |
| 交易所卖出 → 法币/本地 e-wallet → 再消费（两步 off-ramp） | Step 4 非卡 rails：GCash GCrypto / Maya 两步路径 | **Fact**（路径存在） |
| 现有 crypto-原生 money account / 账户产品 | KAST（Unified Balance、US/EU account、ACH/SEPA/SWIFT/Fedwire、receive/send/spend）；Plasma One（global account services via Bridge）；Bleap（Europe/MX/BR）；OKX Pay/Card SG（SG 限定）；Karta（receive/payouts 为 Q3 2026 future） | **Fact**（产品特性/区域 claims 取自 `04-agent-a-j1-global-money-card.md`） |
| 本地 e-wallet 作为日常主账户 | PH 生态（GCash/Maya）为 e-wallet 场景背景 | **Fact**（路径存在，具体市占 Unknown） |

### 2.3 主要摩擦

1. **跨 Money Friction**：跨境收付需要多步、等待、多账户/多余额，用户感知为「慢、贵、绕」——这是 Step 1 两个摩擦之一的解释性结论（**Inference**；产品叙事如 KAST "one account for every move" 是对同一摩擦的回应，**Fact**）。
2. **统一性不足**：多数替代是「充值→消费」或「卖出→转账」两步结构，不是同一余额直接收/存/转/花（**Inference**；Step 4 把多数卡产品判为 Spend Feature / Account-adjacent，**Fact**）。
3. **逐国可服务性不透明**：样本内 0 个「Money Account confirmed × region confirmed」组合；KAST / Plasma One / Karta 逐国资格 Unknown，Bleap 明确限制 PH/VN，OKX SG 仅 SG（**Fact**，`04-agent-e`）。这是**证据缺口**，不是“无玩家”或“无需求”。
4. **机制不确定性**：KAST 卡机制存在官方 Source Conflict（Y Unknown），影响 J1 玩家能否完整兑现「同一余额直接花」（**Fact**/沿用 Step 3，`03-player-positioning.md`）。

### 2.4 转向理由（为什么用户可能换）

- 一个账号/余额完成 receive + send + spend，减少多账户切换与 off-ramp 步骤（**Inference**；KAST Unified Balance 为产品回应，**Fact**）。
- stablecoin 为底层的账户可跨境、即时转换、绕开传统汇率与等待（**Fact**：Visa 证明 POS 即时转换存在；**Inference**：用户感知价值未用调查证实）。
- 跨境收入场景下避免「收到外币→换汇→再花」的多段摩擦（**Inference**）。

### 2.5 信任要求

| 信任项 | 内容 | 标记 |
|---|---|---|
| 资金安全与托管边界 | 用户需要知道余额是存款还是 crypto-equivalent obligation（KAST 官方公开 "not a bank" / crypto-equivalent 表述） | **Fact**（披露存在）；对用户重要性 = **Inference** |
| 牌照/银行 rails | 账户背后是否有银行伙伴、e-money/PSP/VA 许可与结算 rails | **Inference**（除已知 issuer/许可披露外，逐国许可 Unknown） |
| 收/转/花可靠性 | 收款路径、发送到账、卡扣款、退款/冲正的一致性与 SLA | **Unknown**（无 SLA/实测证据） |
| 透明度 | 汇率、手续费、汇率差价、限额与地区限制的完整披露 | **Unknown**（多数玩家完整费表未证；KAST 卡机制冲突） |

### 2.6 已有服务 vs 弱服务

| 维度 | 结论 |
|---|---|
| **Well-served（产品级）** | 账户形态已被验证存在：KAST 提供最完整 Money Account（Unified Balance + US/EU 账户 + 多 rails）；Plasma/Bleap/OKX SG 为同类方向；KAST 1M+ users / ~$5B annualized volume / $80M Series A 为品牌级规模信号（**Fact**，品牌自述，不进入逐国资格） |
| **Weakly-served（可用性/证据级）** | 没有任何 region 的逐国资格被确认；PH/VN/AU 下 J1 组合 = 0 confirmed；用户能否真正「在我所在地区」获得服务是 Unknown；没有用户调查说明满意度或未满足比例（**Fact**：组合为 0；**Unknown**：需求缺口大小） |
| **Net 读数** | J1 的产品方向存在且被资本/规模叙事支持；但「今天谁在哪里真正能拿到」是主要未证项。**本卡不下 AIX 结论。** |

### 2.7 事实/推断/未知小结

- **Fact**：J1 定义；KAST/Plasma/Bleap/Karta/OKX 产品与区域状态；0 confirmed region×role 组合；稳定币供应/账户叙事（Step 1–4）。
- **Inference**：触发场景、频率、摩擦感知、信任要求、转向理由。
- **Unknown**：逐国资格、实际使用与留存、用户态度调查、需求缺口量化、KAST 机制冲突的最终裁决。

---

## 3. Segment 2：已有 Crypto 持有者 → 日常购买力（J2 Crypto → Spend）

> 用户问题（Step 1 定义，Fact）：**我已经持有 Crypto / Stablecoin，怎样最低摩擦把它变成现实购买力。**

### 3.1 触发与频率（含证据支持的子段）

| 子段 | 用户 | 触发 | 频率 | 标记 |
|---|---|---|---|---|
| **2a｜stablecoin-starting 日常消费** | 已有 USDT/USDC（交易所/自托管/钱包） | 日常零售、在线购物、账单、乘车、点餐等场景想直接花掉 | **Medium–High**（推论；以网络行为佐证：2026-07 约 $759M/月、约 9M 笔、约 $86/笔，Step 1/a16z 口径为 **Fact**） | 子段存在 = **Fact**（Step 3/4 证实 PH/AU/SG 等 ≥3 provider）；频率细分 = **Inference** |
| **2b｜波动币（BTC/ETH 等）持有者消费** | 持有 BTC/ETH 等，愿意在消费时卖出/转换一部分 | 同一日常消费触发，但起点资产是波动币 | **Medium–High 推论**；无独立笔数拆分 | 子段存在 = **Fact**（RedotPay 支持 BTC/ETH 等、Bybit payment crypto 消费时 convert/sell）；独立规模 = **Unknown** |

网络级行为证据（`visa.html`，**Fact**）：crypto card PV 2024 起稳步增长、大体随 stablecoin issuance 走，2025 年底接近高点；亚太区（按 issuer 口径）2025-10 占比最大；销售点即时从 digital assets 转成 local fiat。PYMNTS 标题（`pymnts.html`，标题级）：「Crypto Card Spending Jumps Threefold in a Year, Paymentscan Data Shows」与「From Asset to Everyday Money」——只作为趋势/框架信号引用，不引入标题数字。

### 3.2 当前替代

| 替代 | 证据 | 标记 |
|---|---|---|
| 交易所卖出 → 银行/e-wallet → 消费（两步） | Step 4 非卡 rails 合成路径 | **Fact** |
| e-wallet 两步（GCash GCrypto / Maya） | `04-agent-g2-non-card-substitute-rails-evidence-card.md` | **Fact** |
| 商户直付/扫码（Coins.ph QRPH stablecoin payments） | `04-agent-g2` | **Fact** |
| Gift/prepaid/eSIM（Bitrefill） | `04-agent-g2` | **Fact** |
| 稳定币/加密卡直接消费（多个 live provider） | RedotPay（X2×B auto-convert）、Bitget Wallet Card（Y=A）、ether.fi Direct Pay、Bybit（X2×B）、Crypto.com（X1×A，SG/AU modes） | **Fact**（`03-player-positioning.md`、`04-agent-b`、`04-agent-c`） |

### 3.3 主要摩擦

1. **预转换/off-ramp 摩擦**：不是所有替代都能「持有即花」；Crypto.com 明确 crypto 不能直接 load 卡，须先转成当地货币（**Fact**）；Bitget/Karta 走 top-up 后 spend（**Fact**）。
2. **费用透明度**：RedotPay、Bitget、ether.fi Direct Pay 完整 FX/ATM/top-up/limit 费表未证（**Fact/Unknown**，`04-sources.md` / `04-agent-b`）；OKX SG 费用帮助页 404（**Fact**：缓存不可用）。
3. **逐国资格碎片化**：Bitget 官方 availability 含 PH/VN/AU；Bybit 只见 program 名（PH Unknown）；Crypto.com 只证 SG/AU；ether.fi VN 存在 available-vs-restricted 冲突（**Fact**，`04-agent-e`）。
4. **用户侧不确定性**：无调查数据证明「愿意卖一部分」用户的渗透率、被费用劝退比例或受阻场景（**Unknown**）。

### 3.4 转向理由

- **POS 即时转换**：Visa 官方描述 digital assets → local fiat 在销售点即时发生、商户无改动（**Fact**，`visa.html`）；等于用户不需要提前卖币。
- **可用范围广**：任意接受 Visa 的商户；卡是成熟 rail（**Fact**，Visa 网络级描述；不构成 issuance 资格）。
- **减少两步路径**：从「卖→提→付」变成「直接付」（**Inference**；产品叙事与 Visa 机制一致）。
- **成本/返现竞争**：Bitget 0 开卡/年费、RedotPay 收费结构、cashback 等构成可比较变量（**Fact**：具体费项；**Inference**：对用户的重要性）。
- **网络级动量**：PV 恢复增长且亚太占比最大（**Fact**，`visa.html`）；媒体以「crypto card spend 一年三倍」为叙事（标题级，精确数字以 Step 1 为准）。

### 3.5 信任要求

| 信任项 | 内容 | 标记 |
|---|---|---|
| 发卡/合规包装 | Issuer、许可证（如 OKX SG MAS MPI、Crypto.com SG/AU 区域模式）与卡网络规则 | **Fact**（已披露项）；逐国完整合规 = **Unknown** |
| 资金安全 | 托管余额/卡余额是否隔离；损失/冻结路径（Bitget 失去 seed phrase 后不能 top-up/withdraw 的官方描述） | **Fact**（披露存在）；用户重要度 = **Inference** |
| 费用与汇率透明 | 开卡、top-up、FX、ATM、转换差价与返现上限 | **Unknown**（多数完整表未证） |
| 地区限制透明 | restricted/available 列表是否清晰可查（RedotPay 约 49 个 restricted 地区；Bitget "issuing partners vary by region"） | **Fact**（列表存在）；完整性 = **Unknown** |
| 稳定币储备/结算质量 | 币种储备、结算银行与稳定币选择 | **Unknown**（本卡缓存无此信息） |

### 3.6 Well-served vs Weakly-served

- **Well-served**：
  - 多个已证实 provider 在同一 segment 竞争：PH/AU/SG/MX-BR/EEA+UK（聚合）≥3（**Fact**，`04-agent-e`；Agent C 另增 Oobit 不在本卡来源内，不引用）。
  - 多种机制（托管即时转换、top-up、self-custody 直扣）都能满足「已有币→卡消费」；网络层扩容（Visa 描述 + 媒体报道框架）表明供给在变厚（**Fact**）。
- **Weakly-served**：
  - 费用/汇率/限额完整披露普遍缺失——用户难以做成本比较（**Fact/Unknown**）。
  - VN 只有 1 个 confirmed provider 且包含 conflict；US 样本内 confirmed = 0（**Fact**；样本缺失 ≠ 市场无玩家）。
  - 「稳定币起点→卡 load」路径对部分玩家（Crypto.com）未证；波动币起点细分无独立规模/留存证据（**Unknown**）。
  - 没有任何调查证据说明「现有方案是否已经足够好」；**未满足需求不能被量化**（**Unknown**）。

### 3.7 事实/推断/未知小结

- **Fact**：定义；provider 与机制；Visa 网络轨迹与 POS 转换；$759M/9M 笔（Step 1）；区域密度读数；费用表缺口。
- **Inference**：触发频率、摩擦感知（多步/贵/绕）、转向理由、信任项排序。
- **Unknown**：活跃用户/留存、逐国资格上限、波动币细分规模、用户态度与未满足比例、完整费表、Phoenix 等（不涉及）。

---

## 4. Segment 3：不卖 Crypto、但要流动性的用户（J3 Keep Crypto → Liquidity）

> 用户问题（Step 1 定义，Fact）：**我不想卖掉 Crypto（不想失去敞口/不想触发卖出），但需要可消费的流动性。**

### 4.1 触发与频率

| 项 | 内容 | 标记 |
|---|---|---|
| 定义 | 不卖 Crypto、保持敞口的同时获得消费流动性 | **Fact**（Step 1） |
| 触发 | 大额或紧急消费（不想此时卖）；长期看涨但当前需要日常流动性；DCA/持有策略与消费资金分离 | **Inference**（J3 定义内推导；无调查） |
| 频率 | 借款/额度建立是低频结构决策，额度内的消费可高频；整体低于 J2 直接 spend | **Inference**（Step 5 Agent A 比较框架方向；本卡不引用 Step 5 文件，按推理标注） |
| 子段 | ① 已持有波动币、反对卖出（RedotPay Credit 明确稳定币不计入 collateral → 该样本面向波动币持有者）；② 持有稳定币+波动币组合、用波动币抵押、稳定币日常花（机制上可行但样本未完全证明）；③ 愿意接受借息/清算风险换取流动性 | **Inference**；机制边界为 **Fact** |

### 4.2 当前替代

| 替代 | 证据 | 标记 |
|---|---|---|
| 卖出部分 Crypto（放弃敞口） | 与 J3 互斥的替代；J3 的存在即表示用户不想要这个选项 | **Inference** |
| 法币信用卡/个人贷款（依赖收入与信用记录，不依赖加密抵押） | 常规金融替代；本仓证据未覆盖其渗透 | **Unknown**（仅常识性存在，不展开） |
| 加密抵押借款→现金/稳定币（borrow-to-cash，无卡消费闭环） | Ledn（BTC-backed loans 至 USD/USDC/本地货币）、YouHodler Get Cash | **Fact**（相邻替代，不合并为 borrow-to-spend） |
| 加密抵押直接消费（borrow-to-spend card/credit） | Nexo Card Credit Mode（EEA+UK；"spend without selling"）；ether.fi Cash Card Borrow Mode（PH/AU available-page；VN conflict）；RedotPay Credit（live；PH/VN/AU 资格 Unknown；稳定币不计 collateral） | **Fact**（`04-agent-d-credit-borrow-to-spend-evidence-card.md`） |

### 4.3 主要摩擦

1. **机制复杂与风险暴露**：LTV、risk index、margin call、liquidation 与利息并存（RedotPay 0.05%/day simple interest、0.6/0.8/0.9 risk 阈值；Nexo LTV 50–90% 按资产；ether.fi 经 Aave 计息）——**Fact**。
2. **资产类型门槛**：RedotPay Credit 明确 BTC/BNB/ETH/GRAM/S/SOL/TON/TRX/XRP 可作 collateral、**USDT/USDC 不计入 credit limit**（**Fact**）→ 纯稳定币持有者不适用该样本。
3. **地区门槛高**：Nexo Credit 仅 EEA+UK（**No** for PH）；ether.fi Borrow PH/AU available-page、VN conflict；RedotPay Credit 逐国资格 Unknown（**Fact/Unknown**）。
4. **无规模证据**：没有任何 J3 专属月度/增速统计或活跃用户数据（**Unknown**）；现有机制样本少不能推导为空缺或蓝海。
5. **用户侧认知门槛**：借息、清算、抵押锁定与还款规则复杂，无明显调查说明用户理解度或受阻率（**Unknown**）。

### 4.4 转向理由

- **保留敞口**：官方叙事均为「不卖 / spend without selling / retain upside」（Nexo、ether.fi、RedotPay Credit）——**Fact**（官方 claim）；对用户的价值排序 = **Inference**。
- **绕过信用审查**：Nexo 官方 claim「no credit checks、无固定还款计划」（**Fact**，品牌 claim）；借款以 crypto 抵押自动估值（**Inference** 便利性）。
- **即时有额度**：RedotPay 官方「instant credit line for daily purchases」、Nexo「instant approval」类表述（**Fact**，品牌 claim）。
- **避免税/卖出事件**：不卖出则无卖出触发（**Inference**；本仓无税务数据，不扩展）。

### 4.5 信任要求

| 信任项 | 内容 | 标记 |
|---|---|---|
| 清算与保证金规则透明 | LTV、risk index、margin call/liquidation 阈值、auto-collateral 行为必须清楚 | **Fact**（官方披露存在：RedotPay/Nexo/ether.fi 参数）；对用户重要性 = **Inference** |
| 利息计算透明 | 利率、按日/按年、复利与否、还款优先级 | **Fact**（RedotPay principal-only 声明；Nexo 1.9% 起 marketing）；完整 = **Unknown** |
| 担保资产安全 | 抵押资产存放、可提取条件（RedotPay 未偿余额时不可 withdraw）、发生风险时的处置 | **Fact**（披露项）；执行层面 = **Unknown** |
| 监管/发卡主体 | 卡发行人（Nexo 经 DiPocket UAB、EEA+UK）、放债主体（RedotPay HK 放债人牌照为背景披露） | **Fact**（已披露项）；逐国适用 = **Unknown** |
| 消费者保护 | 争议/退款路径、超额扣款、清算时的申诉机制 | **Unknown**（无证据） |

### 4.6 Well-served vs Weakly-served

- **Well-served（狭窄意义上）**：
  - 机制已存在两条路线：托管式（Nexo Credit，S6-Custodial，地区明确 EEA+UK）与链上/自托管式（ether.fi Borrow，S6-onchain candidate，PH/AU available-page）；RedotPay Credit 为第三方 live 样本（地区 Unknown）。
  - 关键产品承诺（不卖、无固定还款计划、即时额度）已有官方表述支撑。
- **Weakly-served**：
  - confirmed 地理覆盖极窄/未证：EEA+UK 之外明确 No（Nexo）；PH/AU 只有 available-page 级证据（ether.fi，VN conflict 未裁决）；RedotPay Credit 逐国 Unknown。
  - 无规模、增速、留存或真实活跃用户证据；整体证据强度最低。
  - 稳定币持有者被 RedotPay 样本明确排除（稳定币不计 collateral），“已有加密资产”内部的波动币起点更容易被该机制服务；无调查验证这是否是普遍缺口。
  - 消费者保护与清算公平性的证据空白显著。

### 4.7 事实/推断/未知小结

- **Fact**：J3 定义；Nexo/ether.fi/RedotPay Credit/Ledn/YouHodler 的机制、利率、LTV/risk 参数、币种边界与区域状态。
- **Inference**：触发场景与频率、转向理由排序、信任要求相对重要性。
- **Unknown**：J3 用户规模与增速、逐国资格、稳定币用户的缺口比例、清算体验与满意度、任何调查类结论。

---

## 5. 三个 segment 的横向读数（仅市场级，无 AIX 推荐）

1. **J2 是唯一有已发生行为证据的 segment**：月度消费/笔数（Step 1 事实）、Visa 网络恢复增长与 APAC 占比（`visa.html` 事实）、PYMNTS 标题框架（`pymnts.html` 标题级）。但「未满足」不能被量化：费用不透明、地区资格缺口与调查缺失是主要 Unknown。
2. **J1 是产品形态最完整但可用性证据最稀薄的 segment**：账户级「收/存/转/花」已有 live 样本（KAST），但 0 个 region×role confirmed 组合意味着「用户今天能否获得」高度 Unknown；命题「稳定币作为日常钱」存在，但用户态度/规模无调查。
3. **J3 是范围最窄、证据最弱的 segment**：机制真实存在且差异化明确（不卖币），但区域、规模、体验证据全部薄弱；**不能把「样本少」写成「未满足需求大」**。
4. **共性信任要求**：资金安全与托管边界、费用/汇率透明、逐国资格透明、监管/发卡主体可查；三个 segment 都缺乏完整费表或用户调查作为验证（**Fact/Unknown**）。
5. **本卡不选择、不排序、不推荐 AIX 目标方向**；三个 segment 的吸引力/缺口大小留给 Step 5 主流程。

---

## 6. 排除与纪律自检

- ✅ 未联网、未浏览、未补抓；只读 Step 1–4 正式文档、`evidence/04-*.md` 与 `/tmp/agentb5/visa.html`、`/tmp/agentb5/pymnts.html`。
- ✅ 显式排除：CoinGecko challenge 页、Bitget 404/研究目录、Chainalysis 404、Circle 研究目录、Crypto.com 错误壳、Mastercard Access Denied、Security.org 404、Wayback 壳、World Bank challenge。
- ✅ **调查类结论显式排除**：可用缓存与正式文档不含可用用户调查统计；未断言任何「x% 用户」类结论。
- ✅ AIX 当前能力/地理未定义任何用户 segment；正文无 AIX 目标推荐；AIX 仅在纪律声明中出现。
- ✅ Unknown ≠ No；merchant acceptance ≠ eligibility；future（Karta receive/payout、YouHodler Card、Bleap 扩展）未当 current。
- ✅ 营销覆盖数字（170+ / 180+ / 150M / 100M merchants 等）未进入任何资格或规模判定。
- ✅ 只创建一个文件：`research/aix-market-positioning/evidence/05-agent-b-user-unmet-needs.md`；未触碰其它文件。

---

## 7. 来源映射

| 本卡内容 | 来源 |
|---|---|
| J1/J2/J3 定义、市场边界、两个摩擦、区域纪律 | `01-market-overview-and-user-jobs.md`；`04-competition-map.md` |
| 玩家机制/Money Account/Account Role 落位（KAST/Plasma/Bleap/Karta/OKX） | `evidence/04-agent-a-j1-global-money-card.md` |
| J2 托管/交易所/预充值卡事实（Bitget/Bybit/Crypto.com；Binance 仅时点参考不采用） | `evidence/04-agent-b-custodial-exchange-prefunded-card.md` |
| J2 self-custody 样本（ether.fi Direct Pay 等） | `evidence/04-agent-c-self-custody-wallet-native-evidence-card.md` |
| J3 样本（Nexo/ether.fi Borrow/RedotPay Credit/Ledn/YouHodler） | `evidence/04-agent-d-credit-borrow-to-spend-evidence-card.md` |
| 区域可用性/密度读数（PH 3 confirmed、J1 0 confirmed、J3 少数） | `evidence/04-agent-e-regional-maturity-density.md` |
| 非卡替代 rails（bank/e-wallet/QRPH/gift/P2P） | `evidence/04-agent-g2-non-card-substitute-rails-evidence-card.md` |
| Step 3 four-AND 与 KAST 机制冲突 | `03-player-positioning.md`；`evidence/03-sources.md` |
| Visa 网络级事实（日常零售、POS 即时转换、2021–2025 轨迹、APAC 占比） | `/tmp/agentb5/visa.html`（canonical `https://corporate.visa.com/en/sites/visa-economic-empowerment-institute/crypto-linked-cards.html`） |
| PYMNTS 标题级框架信号（crypto card spend 增长、asset-to-everyday-money、access gap） | `/tmp/agentb5/pymnts.html`（canonical `https://www.pymnts.com/topic/crypto/`） |
| 无效/排除缓存 | `/tmp/agentb5/` 全部文件状态检查（见 §0） |

---

## 8. 输出 JSON

```json
{
  "outcome": "PASS",
  "summary": "Materialized Step 5 Agent B user-unmet-needs evidence card segmented by Job/trigger (J1 stablecoin/global-money users; J2 existing crypto holders wanting everyday purchasing power with stablecoin-starting and volatile-crypto subsegments; J3 keep-crypto users wanting liquidity), using only Step 1-4 formal docs, reviewed 04-* evidence cards and the two usable /tmp/agentb5 caches (visa.html, pymnts.html). Card covers trigger/frequency, current alternatives, main friction, reason to switch, trust requirements, well-served vs weakly-served, and Fact/Inference/Unknown labels with per-item sources. Explicitly excluded: CoinGecko challenge pages, Bitget 404/Academy hub, Chainalysis 404, Circle research catalog, Crypto.com error shell, Mastercard Access Denied, Security.org 404, Wayback shell, World Bank challenge, and all unsupported survey claims (no usable cache contains survey statistics). No AIX capabilities/geography define any user segment; no final AIX target recommendation is made.",
  "changedFiles": ["research/aix-market-positioning/evidence/05-agent-b-user-unmet-needs.md"],
  "tests": [
    "single-file write via Python pathlib.Path.write_text to the exact target path; no other file created or modified",
    "source-basis check: every cited fact traces to Step 1-4 docs, evidence/04-*.md, visa.html or pymnts.html; no new URL or live browsing",
    "cache-eligibility audit: only visa.html and pymnts.html treated as usable; coingecko2024/2025 (challenge), bitget.html (404), bitgetres.html (hub), chainalysisgeo.html (404), circle.html (catalog), cryptocom.html (error shell), mastercardres.html (Access Denied), securityorg.html (404), tmp2.html (Wayback shell), worldbank.html (challenge) are explicitly excluded",
    "survey-guardrail check: no percentage/attitude claim is asserted from any cache; PYMNTS used at title/framework level only",
    "AIX-guardrail check: no AIX capability or geography defines a segment; no target recommendation in body",
    "discipline check: Unknown != No, merchant acceptance != eligibility, future features not treated as current",
    "wc -l and tail -10 executed after write; JSON embedded at end of file"
  ],
  "commands": [
    "python3 - <<'PY' (pathlib.Path(...).write_text(...)) to write research/aix-market-positioning/evidence/05-agent-b-user-unmet-needs.md",
    "wc -l research/aix-market-positioning/evidence/05-agent-b-user-unmet-needs.md",
    "tail -10 research/aix-market-positioning/evidence/05-agent-b-user-unmet-needs.md",
    "rg -n 'coingecko|chainalysisgeo|mastercardres|worldbank|cryptocom' /tmp/agentb5 to confirm excluded cache states"
  ],
  "decisionsRequired": [
    "Decide whether J1's 0-confirmed region x role combination should drive a re-check/evidence-collection task or be treated as closed gap input in Step 5",
    "Decide how strongly to weight missing user-attitude survey data across J1/J2/J3 when ranking candidates (unmet needs currently not quantifiable)",
    "Resolve KAST card mechanism source conflict (Y Unknown) before treating J1 money accounts as fully validated supply",
    "Close full fee/FX/limit disclosure gaps for RedotPay/Bitget/ether.fi and other providers before cost-based user-friction conclusions",
    "Resolve ether.fi VN available-vs-restricted conflict and J3 country eligibility (RedotPay Credit PH/VN/AU) before any J3 density conclusion",
    "Confirm whether PYMNTS topic-page titles may be used as directional framing in Step 5 or should be removed in favor of the a16z/Paymentscan exact figures already in Step 1"
  ],
  "requiresGptReview": true
}
```
