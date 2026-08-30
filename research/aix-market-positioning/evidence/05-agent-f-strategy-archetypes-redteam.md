# Step 5 Agent F｜独立战略红队：Future-entry Strategic Archetypes

> 日期：2026-08-30
> 角色：独立执行子 Agent F（Archetype 红队）。
> 职责边界：只构造互斥 / 清晰不同的 future-entry strategic archetypes；为每个 archetype 做 strongest-case / kill-case；**不做筛选、不排序、不选最终赢家**；不以 AIX 当前能力作为准入条件。
> 输入：Step 1–4 正式文档 + Step 4 source index（`evidence/04-sources.md`）。未读取任何其他 Step 5 Agent 产物。
> 输出用途：作为 Step 5 后续 Agent / 主审的独立输入，不代表最终战略结论。

---

## 0. 方法声明与独立性约束

### 0.1 方法

1. 以 Step 1–4 已确认的市场边界为唯一市场定义：**consumer crypto / stablecoin → real-world purchasing power**。
2. 以四个用户层变量作为 archetype 的区分核心：**Job（J1/J2/J3）→ Starting Money → Product Role → Money Location & Purchasing Mechanism（X/Y）→ Rail Portfolio → Region**（沿用 Step 4 的建议顺序，但不代表选择顺序）。
3. 每个 archetype 描述为**完整 entry strategy**（战略意图 + 用户 + 机制 + 商业模型），不做 feature list。
4. 红队纪律：每个 archetype 同时写 **strongest-case（最强成立路径）** 与 **kill-case（最可能杀掉它的路径）**；不允许只有乐观面。
5. **不筛选**：不按 AIX 当前 Wallet/Card 架构、地区、牌照、托管关系或 Step 2 的 X1 现状排除任何 archetype。
6. **不排序**：不给出“推荐”“优先级”“首选”或其他隐含排序。

### 0.2 独立性约束自检

- ✅ 只读取 Step 1–4 正式文档与 Step 4 source index；未读取 `05-*.md`、其他 Step 5 Agent 产物或 reviews 中 Step 5 相关记录。
- ✅ 未用 AIX 当前能力作为 archetype 筛选条件：AIX 只作为“未来进入者”锚点出现。
- ✅ 未选最终赢家；六种 archetype 保持互斥 / 清晰不同。
- ✅ 外部事实均来自 Step 1–4 已评审证据（本文件不新增未经索引的 URL）。

### 0.3 Evidence baseline（本卡引用来源）

| 引用内容 | 来源 |
|---|---|
| 市场边界：consumer crypto/stablecoin → real-world purchasing power；排除纯交易/纯 Earn/内部搬币 | `research/aix-market-positioning/01-market-overview-and-user-jobs.md` |
| 三层市场规模（L1 ≈ $390B run-rate；L2 ≈ $153B consumer-related；L3 card spend 2025 ≈ $4.5–5.2B / 2026-07 ≈ $759M 月、~9M 笔） | `01-market-overview-and-user-jobs.md`；`evidence/01-sources.md` |
| J1 / J2 / J3 三个 Job Family | `01-market-overview-and-user-jobs.md`；`04-competition-map.md` |
| X：Consumption Value Container（X1 Dedicated Card Balance / X2 Provider-custodied Account / X3 Self-custody） | `02-ecosystem-map.md` |
| Y：Purchasing-power Mechanism（A Pre-fund / B At-payment convert / C Stable-value deduction / D Collateral credit） | `02-ecosystem-map.md` |
| Account Role overlay：Spend Feature / Money Account / Account-adjacent | `02-ecosystem-map.md` |
| 已观察策略簇 S1–S6 与 occupancy map | `02-ecosystem-map.md` |
| AIX current 坐标（X1 confirmed / Y Unknown / Species Unknown；Account Role 最多 Account-adjacent）——仅作未来进入者上下文，不作筛选依据 | `02-ecosystem-map.md` §7；`03-player-positioning.md` §2 |
| 玩家落位矩阵、KAST Source Conflict（X2 confirmed / Y Unknown / Cluster Unknown）、3 个 evidence-level Direct candidate | `03-player-positioning.md`；`evidence/03-sources.md` |
| Step 4 竞争结构：four-AND；J1/J2/J3 战场；Card 只是 rail；非卡 rails（QR / e-wallet / gift / merchant / bank-remittance / P2P） | `04-competition-map.md`；`evidence/04-sources.md` |
| Step 5 选择顺序（Job → Region → Starting Money → Product Role → Rail → X/Y/Custody） | `04-competition-map.md` §10 |

---

## 1. Archetype 总览（互斥依据）

六个 archetype 是“start-state + primary Job + value-capture logic”层面的不同进入路径。它们可以后续被组合，但作为独立 archetype 互斥或清晰不同：

| # | Archetype | Primary Job | 核心差异（一句话） |
|---|---|---|---|
| A1 | **Money Account-first** | J1 | 把稳定币变成本地可收付的“主资金账户”，消费只是账户输出之一 |
| A2 | **Crypto Spend-first（instant convert）** | J2 | 最大化“已有币 → 现实消费”的摩擦最小化，消费本身是产品 |
| A3 | **Stablecoin Multi-rail Account** | J1 / J2 双主 | 稳定价值账户 + 多种现实 rails（卡 / QR / 银行 / 转账），以 rail 覆盖取胜 |
| A4 | **Self-custody Spend** | J2（部分 J1） | 资产留在用户链上钱包，以“非托管 / 钱包主权”为唯一信任诉求 |
| A5 | **Collateralized Liquidity（Keep Crypto → Spend）** | J3 | 不卖币，用加密资产抵押生成可消费流动性 |
| A6 | **Local-market Purchasing-power Bridge** | J1（区域性） | 以单一高摩擦国家的本地 rails（QR / e-wallet / 汇款通道）为入口，稳定币作底层结算 |

> 互斥说明：A1 与 A3 都做“账户”，但 A1 的优先级是“账户心智 + 银行式收付”，A3 的优先级是“rails 组合 + 稳定币结算覆盖”；A2 与 A4 都做 crypto spend，但信任轴相反（托管包装 vs 自托管）；A5 与 A2 的资产结果是相反的（保留敞口 vs 转换资产）；A6 与 A1 的地区策略相反（单点深挖 vs 全球统一账户）。每个 archetype 即使最终组合，也必须作为独立假设先承受红队检验。

---

## 2. A1｜Money Account-first（稳定币 Global Money Account）

### 2.1 Summary

进入 J1：让用户把稳定币当“钱”而不是“资产”，提供收 / 存 / 转 / 花的统一账户体验。消费能力（卡 / 转账 / 支付）是账户能力的输出，不是产品本身。

### 2.2 Target Job / User

- **Primary Job**：J1（获得并持续使用一种稳定、可跨境、能收 / 存 / 转 / 花的钱）。
- **Target users**：
  - 跨境工作者：海外收入（Uber / freelancer / 远程工资）需要低成本回到本地并直接消费；
  - 稳定币持有者中“把稳定币当存款账户”的人群（不追求 yield，追求可用性）；
  - 本地法币不稳 / 汇款通道贵地区的长期用户（但 A1 的全球化定位意味着不做单一国家深挖）。
- **关键用户测试**：用户是否会说“这是我的账户 / 我的钱”，而不是“这是一个可以刷卡的 app”。

### 2.3 Starting Money

- 用户进入前已持有 USDT / USDC / 当地稳定币（Step 1：Stablecoin 属于 Crypto；J2 与 J1 的 starting pool 可重叠）；以及从法币体系转入的资金（ACH / SEPA / SWIFT / 本地银行入金）。
- A1 必须同时承接“已持有稳定币”和“法币入金”两类起点，否则只是 J2 的一个变体。

### 2.4 Value Proposition

- 一个账户，统一余额：能收、能存、能发、能花，不需要 cashing out 到银行再消费；
- 跨境资金流（收工资 / 汇款 / 转账）直接以稳定价值沉淀，避免双重换汇；
- 比银行快的接入（分钟级开户、多币种/多本地结算能力）；
- 用户获得“稳定币银行账户”的心智，而不是“玩具卡”。

### 2.5 Account Role

- **Money Account（完整闭环）**：必须有单一统一余额（或等价账户结构）支撑 receive + hold + send + spend。
- 以 Step 4 KAST 样本为参照：Global Account + US/EU IBAN + ACH/SEPA/SWIFT/Fedwire + Unified Balance 是成熟参考；但 KAST 的购买力机制存在官方 Source Conflict（X2 confirmed / Y Unknown），A1 设计**必须自行证明 Y**，不能默认“直接扣稳定币”。

### 2.6 Core Mechanism（方向性设计，不等同于当前事实）

- **X / Y**：X2（平台托管统一账户余额）为主，Y=C（稳定价值直接扣减）为默认方向；但 A1 必须同时验证 Y=A（预充值）与 Y=D（余额担保 credit line）作为候选实现，不能预设。
- **资金流动**：入金（链上稳定币 / ACH / 本地银行）→ 统一余额 → 消费 / 转账 / 提现。
- **Custody**：平台托管（第三方托管或银行/信托包装）优先，因为 J1 用户要的不是“主权”，是“可用 + 安全 + 合规”。

### 2.7 Rails

- Card（Visa/Mastercard 发卡）作为默认 spend rail；
- Bank rails：ACH / SEPA / SWIFT / Fedwire（KAST 参照）以及本地银行出金；
- Transfer / P2P：账户间转账（可能链上结算或内部记账）；
- QR / local e-wallet 作为区域增强（不是 A1 的主轴）。

### 2.8 Monetization

- 月费 / Premium 订阅（KAST 参照：免费 + premium 模式）；
- FX / conversion 点差（链上稳定币 → 本地法币结算）；
- 卡发卡费（虚卡/实卡）、ATM 费、跨国交易费（Fee table 需与竞品对比，不预设数字）；
- 商户侧手续费（若自营 merchant rail）或 interchange；
- 不依赖高利率贷款收入（A1 不是信贷生意）。

### 2.9 Defensibility

- **账户心智与切换成本**：用户把收 / 存 / 转 / 花放在一个账户后，迁移成本高于单点 spend 工具（Step 4：Money Account 带来更高切换成本）；
- **沉淀余额与网络效应**：账户余额 + 收付习惯形成双向网络；
- **合规/托管壁垒**：多国牌照/托管关系（US/EU/PH）一旦建立，新进入者难以复刻；
- **数据与产品循环**：资金流数据（工资到账、消费习惯、跨境频率）支撑风控与个性化。

### 2.10 Key Risks

- **机制落地风险**：KAST Source Conflict 说明“余额直扣 vs 信用担保”在官方层面都没讲清；A1 若把 Y=C 当默认，可能遭遇结算/监管障碍（如 card network 对 stablecoin balance deduction 的 settlement 规则不明）；
- **监管/银行关系风险**：多国账户 + 发卡 + 汇款需要多重牌照；银行关系一旦被切断，整个账户产品停机；
- **加密合规红线**：KYC/AML、稳定币 reserve 审计、资金隔离要求高；违反任何一条即系统性风险；
- **竞争挤压**：KAST 已占据 Money Account 心智；A1 若不做差异化，会成为“另一个 KAST”；
- **成本结构**：统一账户 + 多 rails 的基础设施成本高；如果活跃用户不足以支撑，单位经济为负；
- **稳定币资产风险**：若储备币种（USDT/USDC）本身遭遇信任危机，整个账户产品受损。

### 2.11 Strongest Case

- 在跨境收入 / 汇款高频地区（如 PH、LATAM、中东），用户最痛的不是“能不能刷卡”，而是“钱能不能低成本、稳定地跨体系流动”。
- 若 A1 能证明：**收工资（稳定币/银行）→ 本地卡消费的全程成本 < 传统银行 + 汇率损耗**，且体验接近 neobank，则用户会把 A1 当作主资金账户。
- 账户余额沉淀带来低资金成本 + 高留存；随合规/银行关系扩展，形成 KAST 级别的 Money Account 壁垒，且比 KAST 更早/更准确地解决机制冲突（Y 维度透明化）。
- **成功信号**：用户月活中“收+存+花”闭环占比 > 单纯 top-up 消费占比；资金留存时间（balance duration）显著高于 spend-first 产品。

### 2.12 Kill Case

- **如果**：稳定币支付本身始终是“小众边缘流量”（L3 card spend 2025 仅 $4.5–5.2B，即使 2.5x YoY，也远小于传统卡市场），而 J1 用户真正想要的是“稳定 + 本地化 + 存款保险”的银行服务——那么 A1 会被两类产品夹死：本地 neobank（有存款保险、本地 rails）和 KAST 类先行者（已有账户心智）。
- **如果**：监管者把稳定币账户定义为“e-money/money transmission”，每国都要牌照，A1 的全球化叙事变成“每国一张牌”的重资产模式，无法规模化；
- **如果**：稳定币储备资产在目标市场遭遇挤兑/脱锚，A1 的用户信任瞬间归零，而传统银行有保险兜底；
- **如果**：用户测试证明“稳定币用户不想要账户，只想要快速把币花掉”，A1 将为一个不存在的主账户心智付出全局成本。
- **Kill 判定**：若 12 个月内无法证明单一市场（非试点）中 ≥ 某阈值用户把 A1 当主账户（收+存+花闭环），A1 应被降级为 A3 的子能力（先 rails 后账户），而不是继续烧账户基础设施。

---

## 3. A2｜Crypto Spend-first（Instant-convert 消费，托管余额）

### 3.1 Summary

进入 J2：用户已经持有 Crypto（含 Stablecoin），最想要的是“把手里的币变成现实购买力”的最低摩擦路径。产品形态是托管钱包余额 + 支付时自动转换/扣减 + 卡（或 QR）。

### 3.2 Target Job / User

- **Primary Job**：J2（已持有 Crypto，愿意卖/换一部分，低摩擦变成日常购买力）。
- **Target users**：
  - 交易所/自托管钱包的存量持币用户（USDT/USDC/BTC/ETH）；
  - “不想要复杂流程，只想花币”的实用主义者（刷卡时自动转换）；
  - 对“账户”不感兴趣、对“消费入口”感兴趣的用户。
- **关键用户测试**：用户说“我把币放进去，直接花就行”，而不是“我要管理我的钱”。

### 3.3 Starting Money

- 与 A1 不同，A2 的核心起点是 **已持有的 crypto（stablecoin 只是其中一种）**；没有法币入金叙事。
- 若 A2 只支持稳定币起点，它会退化为 A1/A3 的子集；A2 的战略价值在于**波动币 + 稳定币混合起点**（Step 3：RedotPay/Bybit 覆盖更宽起点池）。

### 3.4 Value Proposition

- 零预操作：不需要先 top-up / 先转换，支付时自动卖出/转换（RedotPay generic auto-convert、Bybit Card 样本）；
- 一个入口支持多种资产（稳定币直接扣，波动币实时转）；
- 用户保留“持有资产直到最后一刻”的控制感。

### 3.5 Account Role

- **Spend Feature / Account-adjacent**：A2 不需要 Money Account 闭环；转账/收款能力是加分项，不是必要条件。
- 关键：A2 的目标是“消费入口”，不是“主账户”；如果 A2 试图做 Money Account，它会变成 A1/A3。

### 3.6 Core Mechanism

- **X2 × B（托管余额，支付时转换）** 为默认机制；稳定币余额可走 C 直接扣。
- 支付流程：用户持币 → 平台托管钱包 → 支付时自动 convert/扣款 → 结算给商户。
- 波动币转换的滑点/时机是产品核心变量（用户感知是“刷了就花了”，实际是“刷的时候卖了”）。

### 3.7 Rails

- Card 为主（虚拟卡先发，实体卡按需）；
- 可选 QR / 本地 e-wallet 作为追加 rail，但 A2 不做 rails 全栈。

### 3.8 Monetization

- 交易/转换费（FX + spread）：A2 的天然收入（用户对转换成本不敏感时是蜜糖，敏感时是毒药）；
- 卡发卡费 / 月费 / ATM 费；
- 商户侧收入（interchange 或自营 merchant 返佣）；
- 不靠账户沉淀生息（用户余额波动性高）。

### 3.9 Defensibility

- **转换效率与价格透明度**：谁能把“持币 → 消费”的全成本（转换费 + 汇率 + 卡费）做到最低、最可预测，谁就赢；
- **资产起点宽度**：支持越多资产（稳定币 + BTC/ETH + 其他），替代交易所提现路径越强；
- **分发渠道**：与交易所/钱包合作（预装卡入口）是最强获客杠杆（Step 3：RedotPay/Bitget 已证明）；
- **支付成功率**：卡网络拒付率/授权失败率低是高留存关键，技术壁垒在中端。

### 3.10 Key Risks

- **价格竞争**：转换费是显性成本；用户一比较就会发现 1–2% 的 spread 太贵（交易所提现 + 本地卡便宜时，A2 失去价值）；
- **波动币合规**：支付时自动卖出 = 实时 FX/兑换业务；多国监管认为这是 money transmission + 兑换业务，牌照复杂度高于稳定币直扣；
- **滑点/时机责任**：用户会因为“刷的时候卖在了低点”而投诉/流失；风控与滑点保护是产品责任；
- **同质化**：RedotPay/Bybit 已占据该位；A2 若无差异化（费率 / 地区 / 资产 / 体验），只是跟随者；
- **资产错配**：波动币余额的充值波动导致卡余额不足，用户体验受损。

### 3.11 Strongest Case

- 在 PH stablecoin-starting J2 segment，RedotPay / Bitget / ether.fi Direct Pay 已通过 four-AND 被确认为 Direct competitors（Step 3），说明**该 segment 已有真实需求且竞争已验证**；A2 若能以更低全成本或更好的资产起点覆盖进入，需求侧不需要重新教育用户。
- 若 A2 与某大型交易所/钱包达成预装合作（用户钱包里直接出现 spend 入口），获客成本接近零，转化率高于独立 app；
- 波动币用户（持有 BTC/ETH）是稳定币-only 竞品无法覆盖的增量池（Step 3：AIX 起点更窄，A2 不做此限制）；
- **成功信号**：单用户月消费次数、activation→first spend 时间（越短越好）、转换成本在市场最低 1/3。

### 3.12 Kill Case

- **如果**：conversion fee 被压到接近零（稳定币桥接入、交易所自营卡、银行直接支持 crypto 入金），A2 的中间层利润消失，变成纯获客漏斗；
- **如果**：监管要求“支付时自动卖出”视同证券/外汇交易，需要额外牌照或禁止零售自动转换，核心机制被法规掐死；
- **如果**：用户发现“直接卖币到本地银行再刷卡”成本更低（例如当地交易所出金 + 传统卡），A2 的便利性溢价无法覆盖成本；
- **如果**：KAST 类 Money Account 把余额直扣体验做到完全无感，J2 用户直接跳过“转换”心智，A2 被抽象成“卡背后的引擎”，失去独立品牌地位；
- **Kill 判定**：若在目标市场，A2 的全成本（转换+卡费+汇率）无法比“交易所出金 + 本地卡”低 15%+，或 activation→first spend 转化低于行业基准，A2 应被放弃或降级为 A1/A3 的支付引擎组件。

---

## 4. A3｜Stablecoin Multi-rail Account（稳定币结算 + 多 rails 组合）

### 4.1 Summary

进入 J1/J2 交界：以稳定币为统一结算层，不追求“主账户心智”，而是追求**在任何现实 rails 上都能消费**（卡 / QR / 银行转账 / 本地 e-wallet / P2P）。用户感知是“我有一笔稳定币钱，想怎么花都行”。

### 4.2 Target Job / User

- **Primary Job**：J1（钱本身更好用）+ J2（已有稳定币直接花）双主。
- **Target users**：
  - 稳定币持有者中“消费场景多样”的用户（卡场景 + 本地 QR 场景 + 转账场景混合）；
  - 商户侧接受度低地区（卡覆盖差，但 QR / e-wallet 覆盖好）的用户；
  - 不想切换多个 app 的“rails 聚合”需求者。
- **关键用户测试**：用户说“同一笔余额，我在哪都能花”，而不是“这是一个银行账户”或“这是张卡”。

### 4.3 Starting Money

- 稳定币（USDT/USDC/本地稳定币）为主；也可以从银行/ACH 入金转换为稳定币余额。
- 与 A1 的区别：A3 不强求“账户就是主心智”，接受“余额是消费层”；与 A2 的区别：A3 默认是**稳定价值余额**，不做波动币自动转换。

### 4.4 Value Proposition

- **一个 balance，多个 rails**：card / QR / bank / e-wallet / P2P 全部从同一稳定币余额结算，消除“卡有钱、QR 没钱”的碎片化；
- 商户覆盖不再依赖单一卡网络：卡接受度低时走 QR，QR 不行时走银行转账；
- 稳定币作为统一结算层，天然跨境。

### 4.5 Account Role

- **Money Account-leaning / Account-adjacent**：A3 需要有统一余额（X2×C or X3×C），但可以不做完整银行式收付（e.g. 不一定需要 IBAN）；核心是 rails 组合能力。
- 如果 A3 试图同时做 banking rails（ACH/SWIFT），它会向 A1 漂移；必须明确 rails 组合的边界。

### 4.6 Core Mechanism

- X2（托管）或 X3（self-custody）均可，Y=C 稳定价值直接扣减为主。
- 结算层：稳定币余额 → 各 rails 的 fiat/local settlement（通过发卡行 / 本地支付牌照 / 商户聚合）。
- 关键机制变量：rails 的 settlement 时点（即时 vs T+1）、失败回滚、汇率锁定。

### 4.7 Rails

- Card（Visa/MC）；
- 本地 QR（PH QR Ph、LATAM QR、SG QR 等；Step 4 已有 Coins.ph QRPH 稳定币支付证据）；
- 银行转账（本地 instant transfer，如 PH InstaPay / PESONet）；
- Local e-wallet（GCash/Maya 类）；
- P2P / OTC（作为末端出金补位）。

### 4.8 Monetization

- 每次 rails 转换的服务费（卡 FX、QR 转换、转账费）；
- 订阅/账户费（如果 rails 覆盖高频）；
- 商户端手续费（若直接服务商户）；
- 资金沉淀利息/收益（稳定币 yield，但需注意监管与用户告知）。

### 4.9 Defensibility

- **Rails 覆盖的本地牌照与银行关系**：每多一个本地 rails，竞争对手需要重做一遍集成，形成“地区式”壁垒；
- **统一余额的网络效应**：用户使用 rails 越多，迁移成本越高；
- **失败率数据**：各 rails 的真实成功率/回滚经验形成运营数据壁垒；
- **稳定币结算成本**：如果能做到 rails 之间 0 转换损耗，用户粘性极强。

### 4.10 Key Risks

- **Rails 集成不确定性**：每个 rails 的商户网络、结算规则、合规要求完全不同；集成延误导致“多 rails”变成“多 bug”；
- **监管归类混乱**：跨 rails 稳定币结算可能同时触发 e-money、money transmission、支付聚合、汇款等不同许可；一国之内的归类不清会拖延上线；
- **稳定币结算的可逆性**：QR/卡/转账的可逆规则不同（退款、chargeback），一个 rails 的失败会污染余额；
- **竞品跟随**：KAST/Plasma 类产品一旦补齐 rails，A3 的“rails 组合”差异消失；
- **成本复杂度**：多 rails 的运营团队与风控成本可能吃掉所有毛利。

### 4.11 Strongest Case

- 在卡接受度低但 QR/e-wallet 发达的单一市场（如 PH：QR Ph + GCash/Maya 渗透率高），A3 是唯一能把“稳定币余额”映射到“本地全 rails”的方案；Step 4 已确认非卡 rails 是真实替代路径（Coins.ph QRPH、GCash GCrypto、Maya 两步路径）。
- 若 A3 在单一高密度市场做出“余额 → 任何 rails 都能花”的标杆，再横向复制到第二个市场，形成 rails 网络的规模效应；
- 用户结构上，A3 同时服务 J1（收/存）与 J2（花），比 A2 用户留存更久（余额沉淀），比 A1 更容易启动（无需先建银行级账户）。
- **成功信号**：单用户 rails 使用数（card+QR+transfer 中 ≥2 种）和 rails 间余额流向（余额不回流交易所，而是在 rails 间流动）。

### 4.12 Kill Case

- **如果**：本地 QR / e-wallet 已高度被银行与 GCash/Maya 类垄断，且它们开始支持稳定币直付，A3 的中间结算层被绕开（用户直接在 GCash 里花稳定币，无需 A3）；
- **如果**：每个 rails 的合规成本叠加后，A3 的单用户单位经济为负（rails 数量多但单条 rails 使用率低）；
- **如果**：稳定币结算的 chargeback / 可逆性风险导致 card rails 合作方（发卡行/网络）要求 A3 提供全额担保，挤死现金流；
- **如果**：用户实际只用一个 rails（例如 90% 用户只用卡），A3 的多 rails 承诺变成“无用的复杂度”（用户选择了简单的 A2/A1）；
- **Kill 判定**：若在目标市场 12 个月内 rails 组合没有带来 ≥30% 的用户用 ≥2 个 rails，或 rails 成本/收入比不达标，A3 应被降级为 A1/A2 的 rails 功能（而不是独立战略）。

---

## 5. A4｜Self-custody Spend（钱包主权 + 直接消费）

### 5.1 Summary

进入 J2（部分 J1）：资产留在用户控制的链上钱包，支付时才扣减/转换。核心信任叙事是“非托管”：无需把币交给平台，消费时直接由智能合约/链下授权完成。

### 5.2 Target Job / User

- **Primary Job**：J2（已有 crypto，愿意低摩擦消费）；次级 J1（把自托管钱包当“钱的存放地”）。
- **Target users**：
  - 拒绝托管交易所/平台的钱包原教旨主义者；
  - 持有大量自托管资产、不想为消费把币转入第三方托管的产品；
  - Web3-native（钱包优先，app 次之）用户。
- **关键用户测试**：用户说“我的币还在我钱包里”，并且把“无需托管”当作选择的第一理由。

### 5.3 Starting Money

- 用户已持有链上 USDC/USDT/ETH/BTC（在 MetaMask / 其他 self-custody wallet / Vault）。
- 起点是**链上地址余额**，不是平台余额；这决定了整个产品形态（钱包连接、签名、授权）。

### 5.4 Value Proposition

- 资产主权不转移：消费授权由用户签名/钱包控制；
- 无需 top-up，钱包里有什么就能花什么（条件：支持对应链/资产）；
- 对加密原生用户是唯一的“不背叛钱包信仰”的现实消费入口（Step 3：MetaMask Card / ether.fi Direct Pay 样本）。

### 5.5 Account Role

- **Spend Feature / Wallet-native layer**：不做“账户”，做“钱包的消费扩展”；可以有 vault/portfolio 视角，但核心是 spend。
- 不做 Money Account：试图把 self-custody 做成银行账户会引入托管/保管责任，自相矛盾。

### 5.6 Core Mechanism

- **X3**：消费时资产仍在用户钱包/Vault；
- **Y=C（稳定币直扣）** 为主要机制（ether.fi Direct Pay 方向；USDC/USDT 直接从 Vault 扣）；Y=B（付款时卖波动币）作为延伸（MetaMask Card 方向）。
- 技术形态：智能合约 vault + 支付授权（session keys / delegate / 链下签名）；结算层把扣款转成法币给商户。

### 5.7 Rails

- Card（Visa/MC，网络端由授权方/发行方结算）；
- QR / merchant-direct（链上稳定币支付，如 Solana Pay / OpenNode 方向，但保留 Step 4 的 Shopify Source Conflict 纪律，只作为方向不当作成熟 status）；
- 无法依赖银行 rails（self-custody 与银行账户体系不兼容，除非桥接到托管层）。

### 5.8 Monetization

- 每次消费/转换的小额费用（网络 fee 之外的产品费）；
- 发卡/授权服务费（self-custody card 通常需要第三方发行层）；
- 高级功能订阅（多链、vault 策略、支出限额）；
- 不靠余额沉淀（余额不在平台）。

### 5.9 Defensibility

- **钱包生态绑定**：与主流钱包/Vault 生态深度集成后，用户迁移成本高（授权、历史、vault 结构）；
- **协议/审计壁垒**：智能合约的安全审计与保险形成信任壁垒；
- **政策性的差异化**：对手托管产品无法声称“我们碰不到你的钱”，这个叙事对目标用户有强吸引力；
- **链上网络效应**：支持链/资产越多，覆盖用户越广。

### 5.10 Key Risks

- **安全性即生死线**：一旦 vault/授权合约被攻击，或用户私钥/会话密钥泄露，资金永久损失；单一安全事故可终结产品（Step 4 纪律：不能把 self-custody 当 feature，它是信任主轴）；
- **监管反噬**：非托管支付仍受 money transmission / 发卡监管约束；监管可能要求授权方承担消费者保护（退款、欺诈责任），与“非托管”叙事冲突；
- **用户体验摩擦**：签名/授权/网络费用比托管产品重；Web3 用户接受，但主流用户不接受；
- **链选择风险**：押注的链/资产若生态萎缩，用户池变小；跨链复杂度又会破坏安全；
- **竞品已占位**：MetaMask Card、ether.fi Direct Pay、Plasma One、Bleap、OKX SG 已占据 self-custody spend 方向（Step 2/3/4），A4 需要差异化（链、地区、vault 策略、成本）。

### 5.11 Strongest Case

- 在“交易所信任危机 + 自托管浪潮”背景下（Step 1 证据中的加密原生用户结构），有真实且增长的自托管资产池（数十亿美元级 USDC 在链上钱包），这些用户目前要么不消费，要么被迫把资产转回托管；
- 若 A4 能把“自托管 → 消费”的体验做到接近托管卡（授权次数少、无感签名、低成本），它获得的是其他托管竞品永远无法获得的“主权溢价”用户；
- Step 3/4 已确认 ether.fi Direct Pay 在 PH 是 four-AND Direct candidate，说明该机制的早期需求在特定市场已出现；
- **成功信号**：钱包连接 → 首次消费时间、人均消费次数、以及“从自托管钱包直接消费占比”（而非先提币到交易所）。

### 5.12 Kill Case

- **如果**：监管/发卡网络要求 self-custody spend 必须有全额托管担保（例如 chargeback 需要平台资金池兜底），则“非托管”只是营销，实际仍是托管（平台控制担保金/授权密钥），信仰用户识破后流失；
- **如果**：安全事件（vault 漏洞 / 签名钓鱼）引发一次大规模损失，整个品类信任受损，A4 无法单独存活；
- **如果**：用户体验差距无法缩小（签名次数、网络费、链上失败率），主流用户继续选择托管竞品，A4 只服务极窄的原教旨人群，规模不足；
- **如果**：钱包生态自建消费层（MetaMask/OKX 直接做全栈），A4 作为独立层被生态吸收，失去独立价值；
- **Kill 判定**：若目标市场中“自托管用户现实消费意愿”的实测转化远低于预期（例如 <1% 钱包用户每月消费一次），或安全/合规成本使单位经济为负，A4 应停止独立战略，仅保留为 A1/A3 的集成选项。

---

## 6. A5｜Collateralized Liquidity（不卖币拿消费流动性 / J3）

### 6.1 Summary

进入 J3：用户不想出售 Crypto（保留价格敞口），但需要可消费流动性。产品用加密资产抵押生成 credit line，用户可以在不改变底层资产所有权的情况下消费。

### 6.2 Target Job / User

- **Primary Job**：J3（不卖 Crypto、保持敞口的同时获得消费流动性）。
- **Target users**：
  - 长期持币（BTC/ETH/稳定币）但现金流紧张的用户；
  - “币会涨，不想卖”的信念型持有者；
  - 希望通过消费而不是卖币来获得流动性、且愿意接受利息/清算风险的进阶用户。
- 关键用户测试：用户说“我不卖币，但我需要生活费/消费额度”，并理解抵押与清算。

### 6.3 Starting Money

- 已有加密资产（BTC/ETH/稳定币）作为抵押品；
- 借贷方（平台）提供稳定币/法币 credit line（或直接由 card network 提供 credit）；
- 与 A2 的根本区别：资产不被卖出/转换；形成债务。

### 6.4 Value Proposition

- 免卖币：不触发资本利得、不放弃上涨敞口、不退出市场；
- 快速流动性：抵押后分钟级获得可消费额度；
- 对长期持有者是“资产不卖也能生活”的唯一路径（Step 4：J3 是独立战场，代表玩家 Nexo Credit / ether.fi Borrow / RedotPay Credit）。

### 6.5 Account Role

- **Spend Feature / Credit facility**：核心不是“账户”，是“信用额度 + 抵押管理”；可以有钱包成分（抵押托管），但消费入口是债。
- 不做“存储用户主资金”的角色：用户主资金是抵押品，不是消费余额。

### 6.6 Core Mechanism

- X2×D（托管抵押 + credit line，Nexo 样本）或 X3×D（链上抵押 + onchain debt，ether.fi Borrow 样本）；
- 消费时从 credit line 扣款（card / transfer），不是从余额扣；
- 核心机制变量：LTV、清算线、利息、抵押品波动处理、稳定币/波动币抵押品混合。

### 6.7 Rails

- Card（credit card 发行，消费走 credit line）；
- Bank transfer / stablecoin payout（提取 credit 到本地账户，再自行消费）——但若只是 cash-out 则偏 Adjacent（Ledn/YouHodler 样本），A5 应尽量提供直接 spend rail 以区别于 cash-only 竞品；
- 可选：QR / e-wallet（若 credit 能映射到本地 rails）。

### 6.8 Monetization

- 利息（borrow spread）是核心收入；
- 卡费/交易费（credit card interchange）；
- 抵押品管理费用（托管、保险、审计）；
- 清算费用/罚金（但高频清算 = 产品失败信号）。

### 6.9 Defensibility

- **抵押品/信用额度关系**：高 LTV 提供能力 + 稳健清算引擎是最强技术壁垒；
- **资金成本**：能获得低成本稳定币/法币资金（借贷池、机构资金）的平台才能把利率压低；利率优势 = 持久壁垒；
- **用户资产锁定**：抵押中的资产迁移成本高（解除抵押 + 结算 + 再抵押）；
- **风控数据**：跨周期（牛市/熊市）清算数据与客户行为数据形成风控 moat。

### 6.10 Key Risks

- **市场崩盘/清算潮**：抵押品暴跌时，用户被清算并损失资产，口碑与合规风险同时爆发（J3 的“保留敞口”承诺在市场极端时失效）；
- **利率竞争**：传统借贷/交易所借贷利率低时，A5 的利率无优势；
- **监管定性**：加密借贷在 US/EU/APAC 多国曾被定性为证券/银行活动，牌照门槛高；
- **信用风险**：credit line 逾期/坏账需要真正风控团队，不是纯技术产品；
- **与 J2 的用户混淆**：多数用户声称“不想卖币”，但实际消费需求低；J3 市场可能比 J2 小很多（Step 4：J3 是独立战场，但样本更少）。

### 6.11 Strongest Case

- 长期持币者（特别是 2020–2025 牛市后持有大幅浮盈的用户）有真实的“不卖币但需要流动性”需求（交税/生活/再投资），A5 是唯一不违背其信念的路径；
- 若 A5 把“抵押 → 直接消费”做成完整闭环（credit line 直接刷卡，而不是先提现到银行），它比 Ledn/YouHodler 类 cash-out 产品更接近用户最终购买力目标（Step 4 将 Ledn/YouHodler 归 Adjacent，正是因为没有 spend rail）；
- 在加密原生用户中，利率敏感度低于传统人群；一个“免卖币 + 直接可花”的产品有 premium 定价空间；
- **成功信号**：抵押资产规模、credit line 利用率、清算率低于行业基准、用户留存（抵押持续时长）。

### 6.12 Kill Case

- **如果**：下次加密熊市/暴跌中，A5 发生大规模清算事件（用户被强平并公开投诉），监管介入并禁止/限制零售加密抵押借贷，产品一夜死亡；
- **如果**：用户实际行为显示“想保敞口”是伪需求——大多数目标用户最终选择卖掉一部分币（J2）或用银行信用（不抵押），J3 真实 TAM 过小；
- **如果**：利率被传统 DeFi 借贷协议（链上直接抵押 → 稳定币 → 自己刷卡）压到接近零，A5 的托管中间层无利可图；
- **如果**：稳定币抵押品也可被 A1/A3 支持（余额担保 credit line，KAST 的 Y=D 可能性），Money Account 产品直接吞掉 A5 的“不卖也能花”卖点；
- **Kill 判定**：若试点市场 12 个月抵押资产规模无法达到规模化门槛，或清算率/风险成本使单位经济为负，A5 应降级为 A1 的 add-on（余额担保 credit，而不是独立抵押信贷平台）。

---

## 7. A6｜Local-market Purchasing-power Bridge（单点深挖 + 本地 rails 全渗透）

### 7.1 Summary

选择一个高摩擦/高渗透率的单一国家市场，以“稳定币 ↔ 本地购买力”的最小可行路径切入：本地 QR / e-wallet / 银行转账 / P2P 全覆盖，稳定币作底层结算。不做全球账户，做“一个国家所有花钱通道”。

### 7.2 Target Job / User

- **Primary Job**：J1（本地可用的钱）+ J2（已有稳定币直接花）双主，但**限于单一国家**。
- **Target users**：
  - 本地隐形经济参与者（无银行账户/少银行账户人群）；
  - 跨境汇款接收者（海外亲属汇稳定币/汇款到本地）；
  - 已通过交易所接触稳定币、但缺少本地消费通道的用户（如 PH：GCash GCrypto / Maya 已提供两步路径，A6 要做“一步本地化”）。
- 关键用户测试：用户说“这笔钱在我本地能直接花，不用转来转去”。

### 7.3 Starting Money

- 稳定币（USDT/USDC/本地稳定币）为主要起点；
- 以及本地法币（通过银行/e-wallet 入金转换）；
- 汇款接收（海外 → 本地）是 A6 的重要流入场景（J1 的 remittance 子场景）。

### 7.4 Value Proposition

- **本地 rails 全渗透**：QR Ph / InstaPay / PESONet / e-wallet / 卡，一笔稳定币余额全通；
- **汇款直达消费**：海外发稳定币 → 本地直接购物/缴费，不经银行换汇排队；
- **本地信任 + 加密底层**：面向非加密原生用户，“感觉像本地钱包，底层是稳定币”；
- 与 A1/A3 的区别：A6 不追求全球/多国账户，把全部资源投入单一国家的 rails、合规、商户网络与用户习惯。

### 7.5 Account Role

- **Money Account-leaning（本地）**：本地用户的收/存/花闭环；但不做全球 IBAN 类功能，以「本地余额 = 本地可用钱」为心智。
- 期望形态：本地 e-wallet 体验（GCash/Maya 式）+ 稳定币结算后端。

### 7.6 Core Mechanism

- X2（本地托管余额）为主，Y=C（稳定价值直扣）或 Y=A（本地法币余额）均可；
- 关键：**本地结算优先**——消费时尽量以本地币（PHP 等）结算，稳定币仅为入金/出金层；
- 与本地银行/支付网络/商户聚合直接集成（BSP 支付基础设施；Step 4 已确认 PH 本地数字支付 rails 成熟，但不能推导 stablecoin volume）。

### 7.7 Rails

- 本地 QR（PH QR Ph）；
- 本地 instant transfer（InstaPay / PESONet）；
- Local e-wallet（GCash / Maya 合作或直接竞争，取决于监管与商业关系）；
- Card（本地/国际卡）作为补充；
- P2P / OTC 作为最后一公里。

### 7.8 Monetization

- 本地 rails 的交易费/转换费（稳定币 → 本地币 → 商户结算）；
- 汇款/出金费（海外入金 + 本地提现）；
- 商户端费率（QR 收单 / 聚合支付）；
- 订阅/基础账户费（若用户把余额当主账户）。

### 7.9 Defensibility

- **本地 rails 独占与商户覆盖**：QR/商户网络接入后，新进入者需要重复全部商务与合规工作；
- **本地监管牌照与银行关系**：与 BSP/本地银行/支付协会关系是强壁垒；
- **本地用户习惯与分销**：与本地渠道（汇款点、线下商户、e-wallet 生态）绑定；
- **聚焦带来的“单市场密度”**：同一市场内 rails 数量与用户密度超过任何全球玩家（KAST 类在中低渗透市场反而不灵活）。

### 7.10 Key Risks

- **本地巨头反击**：GCash/Maya/BSP 可能直接推出稳定币功能（Step 4：GCash GCrypto / Maya 已支持 crypto→balance→pay 两步路径），把 A6 的中间层吸收；
- **单点市场风险**：全部收入押注一个国家；监管政策变化（稳定币禁令、e-wallet 限制）可能摧毁全部业务；
- **商户议价能力**：本地 QR/收单市场往往被一两家主导，费率被压；
- **跨境叙事缺失**：A6 的“全球性”弱；高价值跨境用户可能选择 A1/A3 类产品；
- **稳定币本地认知**：本地用户可能不信任稳定币/加密底层，A6 必须做用户教育。

### 7.11 Strongest Case

- PH 类市场：本地数字支付 rails 成熟（BSP 数据支持 rail maturity）、GCash/Maya 广泛渗透、同时有稳定币（GCrypto）用户基础；A6 可以把“稳定币持有者 → 本地全 rails 消费”做成单一市场的绝对主导（Step 4 已确认非卡 rails 是真实路径）；
- 汇款场景：海外 PH 工人汇款是高频正现金流；如果 A6 能用稳定币把汇款成本从 5–8% 降到 <1% 且直达消费，用户价值极其明确；
- 全球化玩家无法在每个国家深耕本地 rails；A6 的“一个国家做到极致”是巨头不愿/不能快速复制的护城河；
- **成功信号**：本地 rails 使用占比（QR/InstaPay/e-wallet vs 卡）、汇款 → 消费的转化率（汇入后 7 天内本地消费占比）、用户留存。

### 7.12 Kill Case

- **如果**：本地 e-wallet 巨头（GCash/Maya）直接推出“稳定币余额 + 全 rails”整合（在现有两步路径上加一步），A6 的所有 rails 都被替代，只剩稳定币结算差价（很小）；
- **如果**：BSP/央行推出官方稳定币/央行数字货币（CBDC）并支持本地 rails，A6 的“稳定币中间层”被政府基础设施挤出；
- **如果**：监管要求 A6 持有支付/e-money 牌照并缴纳高额保证金，单市场收入无法覆盖合规成本；
- **如果**：用户调查显示目标用户更信任既有 e-wallet，不愿安装新 app（A6 获客成本超过终身价值）；
- **Kill 判定**：若在单一市场 12–18 个月无法成为 rails 使用率前三（或达到规模化用户数），或本地巨头宣布同功能路线导致资金方撤资，A6 应停止独立扩张，只保留为 A1/A3 的区域 rails 模块。

---

## 8. 横向对比表（红队视角，不代表排序）

| 维度 | A1 Money Account-first | A2 Crypto Spend-first | A3 Stablecoin Multi-rail | A4 Self-custody Spend | A5 Collateralized Liquidity | A6 Local Bridge |
|---|---|---|---|---|---|---|
| Primary Job | J1 | J2 | J1+J2 | J2（+部分J1） | J3 | J1+J2（单国） |
| Starting Money | 稳定币 + 法币入金 | 广义 Crypto（含稳定币） | 稳定币为主 | 链上钱包余额 | 加密资产（抵押） | 稳定币 + 本地法币 + 汇款 |
| Money Location | X2 托管 | X2 托管 | X2 或 X3 | X3 自托管 | X2/X3 抵押 + credit | X2 本地托管 |
| Purchasing Mechanism | Y=C（待验证） | Y=B/C | Y=C | Y=C/B | Y=D | Y=C/A |
| Account Role | Money Account | Spend Feature | Money Account-leaning | Spend / Wallet-native | Credit facility | Local Money Account-leaning |
| Primary Rail | Card + Bank | Card | Card + QR + Bank + e-wallet | Card + Onchain | Card + Transfer | QR + e-wallet + Bank + Card |
| Core Revenue | 订阅 + FX + 卡费 | 转换费 + 卡费 | Rails 服务费 | 交易费 + 授权费 | 利息 | Rails 费 + 汇款费 |
| Main Moat | 账户心智 + 合规 | 起点宽度 + 分发 | Rails 覆盖 + 本地关系 | 主权叙事 + 安全 | 资金成本 + 风控 | 本地 rails 独占 |
| Fatal Risk | 机制/监管落地 | 转换费被压为零 | 本地巨头吞并 | 安全事件 / 监管 | 清算潮 / J3 TAM | 单点政策风险 + e-wallet 巨头 |
| Kill-case Trigger | 用户不把稳定币当主账户 | 转换中间层利润消失 | 用户只用单一 rails | 实际仍要托管担保 | 极端行情清算 | 本地巨头做同功能 |

> 说明：比较表仅用于红队审视差异，不构成评分、排序或选择。

---

## 9. 红队交叉审视（六个 archetype 之间的关系）

- **A1 与 A3 的边界**：A1 是“账户心智先行”，A3 是“rails 覆盖先行”。若 A3 证明 rails 组合能自然长出主账户心智，A1 可能被 A3 吸收；反之若 A1 证明 rails 只是账户的附属能力，A3 可能被 A1 吸收。两者不能同时作为“独立战略”进入同一市场，否则自相竞争。
- **A2 与 A4**：都做 crypto spend，信任轴相反。A4 的安全/信任风险是 A2 的托管优势；A2 的体验摩擦是 A4 的叙事优势。两者共同挤占同一 J2 用户池。
- **A5 与 A1/A3**：A5 的“余额担保 credit”（Y=D）若被 A1/A3 内化为账户功能（KAST 的 Y=D 可能性），A5 作为独立产品失去差异化；反之若 A5 把 credit 直接 spend 做到极致，A1/A3 的“余额直扣”无法替代“不卖币”用户。
- **A6 与 A1/A3**：A6 是单点市场版本，A1/A3 是全球/多 rails 版本；A6 若成功会是 A1/A3 的区域模块，A1/A3 若成功会是 A6 的竞争者（本地 rails 可能拒绝与全球账户合作）。
- **红队结论（非选择）**：六种 archetype 的“生死线”分别落在**用户主账户心智（A1）、转换中间层利润（A2）、rails 使用密度（A3）、安全/监管信任（A4）、极端行情与 J3 TAM（A5）、本地巨头与政策（A6）**。任何进入决策都必须先验证对应生死线，而不是先做功能堆叠。

---

## 10. 对 Step 5 后续环节的输入（不提供答案）

1. 本文件不回答“AIX 应选哪个 archetype”；
2. 后续 Step 5 Agent 应把六种 archetype 作为独立假设逐一红队，再自行选择/组合；
3. 若后续组合（例如 A1+A3 或 A2+A5），组合后的新 archetype 必须重新做 strongest/kill case，不能简单相加；
4. 所有 archetype 的机制变量（X/Y）都需要 current 市场验证，不能把本文件的方向性设计当成市场事实；
5. 本文件不新增 URL，外部事实均引用 Step 1–4 已评审证据；如需新证据请走证据索引流程。

---

## 11. JSON（执行记录）

```json
{
  "outcome": "completed",
  "summary": "Agent F 独立红队产出六个互斥/清晰不同的 future-entry strategic archetype（Money Account-first、Crypto Spend-first instant-convert、Stablecoin Multi-rail Account、Self-custody Spend、Collateralized Liquidity、Local-market Purchasing-power Bridge），每个均含 target Job/user、starting money、value proposition、account role、mechanism、rails、monetization、defensibility、key risks、required proof、strongest-case 与 kill-case；未筛选、未排序、未选赢家；已读取 Step1–4 正式文档与 Step4 source index，未读取其他 Step5 Agent 产物。",
  "changedFiles": [
    "research/aix-market-positioning/evidence/05-agent-f-strategy-archetypes-redteam.md"
  ],
  "tests": [
    "独立性自检：仅读取 Step1–4 正式文档与 evidence/04-sources.md，未读取其他 Step5 产物",
    "输出路径与文件名符合任务要求",
    "JSON 位于文件末尾，outcome/summary/changedFiles/tests/commands/decisionsRequired/requiresGptReview 字段齐全",
    "未包含最终赢家选择或排序表述",
    "未以 AIX 当前能力（X1/Y Unknown/Account-adjacent）作为任何 archetype 的筛选条件"
  ],
  "commands": [
    "mkdir -p research/aix-market-positioning/evidence",
    "apply_patch add research/aix-market-positioning/evidence/05-agent-f-strategy-archetypes-redteam.md"
  ],
  "decisionsRequired": [
    "六种 archetype 是否覆盖决策者关心的未来进入空间；是否需要新增/替换 archetype（如 B2B/汇款-only/稳定币收益型）",
    "是否允许后续 Step5 Agent 读取本文件作为红队输入（本文件自身未读取其他 Step5 产物）",
    "是否需要联网补充 2026-08-30 current 高质量证据（本文件基于 Step1–4 已评审证据，未新增 URL）"
  ],
  "requiresGptReview": true
}
```
