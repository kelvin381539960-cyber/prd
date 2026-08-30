# AIX 市场格局与产品定位研究任务

- **状态**：Active
- **开始日期**：2026-08-29
- **研究对象**：AIX
- **核心目标**：建立 AIX 所处的 Crypto / Stablecoin 现实购买力市场底图，识别真实用户 Jobs、生态位、竞争关系与 AIX 应占据的位置。
- **重点竞品样本**：RedotPay；其他玩家按市场证据纳入，不预设名单。

## 🚨 Next Agent 必读：本任务的最高研究深度

**本任务不是功能设计 / PRD 任务。最高研究深度固定为 `Strategy + Capability Level`。**

本任务负责回答：
- AIX 应进入什么市场、服务什么用户 Job、建立什么用户关系；
- AIX 应具备哪些**核心产品能力（Capabilities）**，为什么需要这些能力；
- 哪些能力现在已有 / 缺失 / 需要验证；
- 能力之间的优先级、阶段顺序、依赖、商业可行性、关键约束与 Roadmap Gate；
- 什么证据足以支持“需要 / 不需要 / 现在不做 / 后续验证某项能力”。

**到这里必须停止。** 默认不继续回答“这个能力内部具体怎么做”。具体功能方案、流程、规则与交互属于后续独立 PRD / Product Design Task，不属于本研究任务。

### Capability Level 的定义

`Capability` 仅指面向用户 Job / 市场结果的高层能力；子功能、内部行为、规则、流程节点或技术组件即使被改名为 Capability，也不属于本任务范围。

允许研究到：
- `需要 Send / Receive / Hold / Spend / Local QR / Bank or E-wallet rail 等能力吗？`
- `这些能力分别解决什么 Job，战略价值是什么？`
- `哪项能力应该先做，哪项可以延后？`
- `当前是否已具备该能力，是否存在关键 Vendor / 合规 / 经济性 / 数据约束？`
- `能力达到什么业务证据后，Roadmap 才进入下一阶段？`

默认不得继续研究：
- Send 页面怎么设计、收款人怎么填、地址簿怎么做；
- QR 扫码后的页面、确认流程、失败流程、退款流程；
- 功能字段、枚举、状态机、接口、参数、错误码；
- 具体额度、频控、超时时间、异常分支；
- 页面入口、CTA、文案、组件、原型；
- PRD 需求规则、验收规则或技术实现方案。

### 一句话边界

> **本任务决定“AIX 应该成为什么、需要哪些能力、先做什么后做什么、为什么”；不决定“每个功能具体怎么设计和实现”。**

### Evidence Stop Rule

代码、数据、Vendor、监管或竞品细节只允许用于回答战略 / Capability 判断，例如：
- 当前是否存在某能力；
- 某能力是否可行；
- 某能力有哪些会影响优先级的硬约束；
- 某战略假设是否有事实支持。

**一旦已经足以回答上述问题，就必须停止继续深挖。** 不得因为已经打开代码、接口文档、竞品流程或数据表，就顺势研究该功能的详细方案。
若在 Capability Level 内证据仍不足，结论必须记为 `Unknown / downstream validation required` 并停止；不得以验证 feasibility 为由继续研究 Vendor API/SDK、集成流程、数据字段/查询/埋点、技术方案或功能内部规则。仅允许记录“该能力仍需下游专项验证”，不在本研究任务内完成该专项。

### 新任务切换规则

只有用户明确提出类似“开始做某功能 PRD / 具体流程 / 页面 / 交互 / 接口 / 状态设计”时，才视为开启一个**新的、独立的下游 PRD / Product Design Task**；该请求不会改变本 `TASK.md` 的研究 scope。不得把当前战略研究自然延伸成该任务。

## 执行层级与 Scope Guardrails（强制）

本节是本研究后续执行的硬护栏，只约束任务范围，不修改既有市场结论、证据分级或已完成阶段产物。

### 1. 当前主任务层级

当前主任务层级固定为：**Business Strategy + Product Strategy + Strategic Roadmap + Key Assumption Validation + Capability Prioritization**；研究最高深度为 **Capability Level**。

默认允许输出：

- 市场选择、用户 Job、竞争格局；
- 战略定位、业务模式、产品形态、能力组合；
- 阶段目标、Roadmap、进入/退出条件；
- 关键假设、验证指标、Current → Target Gap、优先级与依赖。
- 核心 Capability 清单及其战略理由，但不展开 Capability 内部功能设计。

### 2. 默认禁止下钻

默认禁止把研究下钻为以下页面/产品设计/实现层内容：**页面结构、具体 UI、CTA/文案、字段/API 映射、状态机、异常文案、PRD 章节、原型、技术实现细节**。本任务内不得切换到具体设计 / PRD / 页面 / 接口层级。只有用户明确要求另开独立的下游 PRD / Product Design Task 时，才可在新任务中进入该层级；本任务及其产物仍保持 Capability Level，不把下游设计结果回灌为本研究的默认 scope。即使判断某项 Capability “应该做”，也不代表允许继续定义该 Capability 的内部功能、流程、规则或交互。

实现、代码或 Vendor 事实，只能用于回答战略决策所需的 **feasibility / constraint / gap**。发现实现细节，不得自动把任务切成产品设计或 PRD。

### 3. 每个新 Phase 的 Scope Check

每次开始新 Phase（包括以 Step 命名的阶段）前，执行 Agent 必须先回答：

1. 本阶段要回答的战略问题是什么？
2. 本阶段需要判断哪些 Capability，以及为什么？
3. 当前分析和预期输出是否仍处于战略 / Capability 层？
4. 哪些问题属于后续 PRD / Product Design，必须明确留在本任务之外？

如果分析内容开始回答“页面怎么做、字段怎么写、接口怎么接”，必须立即停止该分析分支，回到本阶段的战略问题，并将问题重写为能力、约束、Gap 或验证问题。未完成 Scope Check，不得开始该 Phase 的证据采集或结论撰写。

如果一个问题已经从“是否需要某能力 / 能力优先级”变成“这个能力具体怎么做”，无论是否还能查到更多资料，都必须停止。

### 4. Agent 分工同样受护栏约束

- **执行 Agent**：只收集与当前战略问题直接相关的证据；不得主动产出页面方案、交互方案、字段/API 方案或 PRD。
- **能力研究 Agent**：可以判断某项 Capability 的必要性、价值、优先级、依赖与硬约束；不得把 Capability 拆成详细功能需求后继续设计。
- **Reviewer**：除事实、推理和证据质量外，必须检查 scope drift；一旦发现下钻，先退回战略问题，不能以页面/PRD 产出替代研究结论。
- **所有 Agent**：不得因看到实现、代码或 Vendor 细节，就自行扩大任务层级。

### 5. Roadmap 的默认单位与当前逻辑

Roadmap 阶段的默认单位是**业务能力、用户关系、产品形态、市场验证**，不是 feature list。

当前 Roadmap 逻辑固定为：

> **Current → Phase 1 One Money Relationship → Phase 2 Multi-rail Everyday Spend → Phase 3 Everyday Money Account**

其中：

- **A6** 是 GTM wedge；
- **A3** 是 product form；
- **A1** 是 target user/account role。

三者是分层、递进的 staged path，不得写成三个并行产品或三个并行战略。

### 6. Stop Rule

只要出现页面/交互/字段/API/状态机/异常规则/具体流程等设计决策，即视为 **scope drift**，不需要等“连续两个以上”。必须立即停止，删除/搁置该下钻分支，并回到当前战略问题；不得继续累积为研究产物。

如果产出已经可以直接交给研发作为具体功能需求，则说明研究深度已越界，应回退到 Capability 表述。

## 研究原则
1. 先研究市场与用户，再研究品牌；不从竞品功能表倒推市场。
2. 每个阶段必须形成独立结论文档，并保留证据索引与关键评审记录。
3. 外部事实必须可追溯；不同统计口径不得合并成一个 TAM。
4. User Job、资金位置、购买力产生机制、Spend Rail、消费场景必须分层。
5. 重要阶段结论需经过独立模型严格评审；未通过则修正并复审。
6. 最终回答：AIX 是什么、服务谁、核心场景是什么、与各类玩家是什么竞争关系。

## 阶段计划
| 阶段 | 内容 | 状态 | 产物 |
|---|---|---|---|
| Step 1 | 市场大盘 + 用户 Jobs | ✅ Completed | `01-market-overview-and-user-jobs.md` |
| Step 2 | 生态位地图：Solution Axes + 玩家落位方法 | ✅ Completed | [`02-ecosystem-map.md`](02-ecosystem-map.md) |
| Step 3 | 重点玩家定位与核心用户研究 | ✅ Completed | [`03-player-positioning.md`](03-player-positioning.md) |
| Step 4 | 市场竞争结构：直接 / 相邻 / Rail 替代 / 潜在 | ✅ Completed | [`04-competition-map.md`](04-competition-map.md) |
| Step 5 | AIX 当前生态位、目标生态位与市场白地 | ✅ Completed | [`05-aix-positioning.md`](05-aix-positioning.md) |
| Roadmap v1 | Business + Product Strategic Roadmap | ✅ Completed | `06-strategic-roadmap.md` |
| Final | 综合市场地图与管理层结论 | ✅ Completed | `final-market-positioning.md` |
| Strategic Validation v1 | Business Strategy + Product Strategy + Key Assumption Validation | ✅ Completed | [`07-strategic-validation.md`](07-strategic-validation.md) |
| Strategic Validation Update 08 | P1 evidence upgrade + P2/J1 discovery refinement | ✅ Completed | [`08-strategic-validation-update.md`](08-strategic-validation-update.md) |
| Strategic Validation P1 Gate Closure 09 | P1 temporal-persistence validation and direct fund-retention evidence boundary | ✅ Completed | [`09-p1-gate-closure.md`](09-p1-gate-closure.md) |

## 当前阶段验收
Step 1 已于 2026-08-29 经 **Advance Codex CLI → ARouter → grok-4.6 → xhigh** 两轮严格评审：
- Round 1：FAIL，要求修正市场边界、Jobs 维度混杂、区域推断强度和 Card 商品化结论。
- Round 2：PASS。

评审记录：`reviews/01-grok46-review.md`
证据索引：`evidence/01-sources.md`

### Step 2 验收

Step 2 先经 **6 路 GLM xhigh 采集 + GPT-5.6 Sol 独立评审**完成第一轮收口；随后按项目要求追加 **Advance Codex CLI → ARouter → grok-4.6 → xhigh** 终审。

Grok 4.6 xhigh：
- Round 1：**FAIL**。结构性问题：X 轴混入 Account Role；cell=物种与 S6 跨 cell 冲突；AIX `S1↔S3 / S1→S3` 超出现有事实。
- 修正后：X 改为实际消费价值容器；Money Account 改为 overlay；cell 改为 occupancy map；AIX current 仅保留 `X1 confirmed / Y Unknown / Species Unknown`。
- Round 2：**FAIL**。4 项收口问题：Plasma One live 状态、Bitget X1/S1 过度落位、直接竞品条件存在“或”、KAST current SWIFT/Fedwire 证据未同步。
- 再修正：Plasma One 改 current live；Bitget 改 `Y=A confirmed / X=Unknown / S1 candidate`；直接竞品改四项 AND；KAST 同步 Unified Balance + ACH/SWIFT/Fedwire + receive/send/spend。
- Final re-review：**PASS**（Job `job_01M16YFZR1C0VZMAE7YBTM2RRS`），无新增 P0/P1。

评审记录：`reviews/02-gpt56-review.md`、`reviews/02-grok46-review.md`。
证据索引：`evidence/02-sources.md`

### Step 3 验收

Step 3 按既定流程完成 **多路 GLM-5.3-Flash 证据采集 → GPT-5.6 Sol 主审/收口 → Agent E 独立 four-AND 交叉验证 → Advance Codex CLI → ARouter → grok-4.6 → xhigh 最终终审**。

关键验收结果：
- Agent E 独立重算 14 个 product modes：**PASS**。
- Evidence-level Direct candidates 仅保留：**RedotPay generic auto-convert card / Bitget Wallet Card / ether.fi Direct Pay**。
- KAST 新证据触发历史结论更新：Step 2 的 `X2×C / S3` 不再作为 current mechanism；Step 3 current 为 **`X2 confirmed / Y Unknown / Strategy Cluster Unknown`**，原因是 2026-08-09 官方文档存在 Source Conflict；Money Account 判断保留。
- Grok-4.6 xhigh final review：**PASS**，0 个 P0/P1 阻塞问题（Job `job_01M174DR32R3602D9FF6WWH975`）。

评审记录：`reviews/03-grok46-review.md`。
证据索引：`evidence/03-sources.md`。


### Step 4 验收

Step 4 按修正后的市场级方法完成：**多路证据采集 → GPT-5.6 Sol 主审/收口 → Advance Codex CLI → ARouter → grok-4.6 → xhigh 独立终审**。

关键验收结果：
- 市场边界保持为 **`consumer crypto/stablecoin → real-world purchasing power`**；不以 AIX 当前地区、资产、Card Balance、功能或架构定义市场。
- Confirmed Direct 固定为四项 AND：**same current market/region + same core Job + overlapping starting money pool + substitutable real-world purchasing-power outcome**。
- Direct **不要求** same X / Y / custody / rail；这些只作为差异化变量。
- 市场拆为 **J1 Global Money / J2 Crypto → Spend / J3 Keep Crypto → Liquidity** 三个 Job 战场，并把 Card、QR、Bank/E-wallet、Gift/Prepaid、Merchant-direct、P2P 作为 Spend Rail 层处理。
- PH stablecoin-starting J2 card segment 中，**RedotPay / Bitget Wallet Card / ether.fi Direct Pay** 通过用户层 four-AND，可形成 player-to-player Confirmed Direct set。
- KAST 保留 Money Account 强证据，同时保留 current mechanism Source Conflict：**`X2 confirmed / Y Unknown / Strategy Cluster Unknown`**。
- Grok-4.6 xhigh final review：**PASS，0 个 P0/P1**（Job `job_01M17BHP99XK9W2T1MT4M4VF9Z`）。

评审记录：`reviews/04-gpt56-review.md`、`reviews/04-grok46-review.md`。
证据索引：`evidence/04-sources.md`。

### Step 5 验收

Step 5 按既定流程完成 **6 路 DeepSeek-V4-Flash/high Multi-Agent 证据 → GPT-5.6 Sol 综合合成 → Advance Codex CLI → ARouter → grok-4.6 → xhigh 独立终审**。

关键验收结果：
- 终审 **PASS，0 个 P0/P1**（Job `job_01M1847J19W5W0V6G782CGNBPQ`），Step 5 可进入 Final。
- 最终决策：**Target = Stablecoin-native Everyday Money Account**；**J1 primary / J2 secondary**；**PH 为 current-evidence proof market**；**WS-1 为 Low–Medium candidate**；**A6 → A3 → A1 staged path**。
- 终审 residual risks 原样保留：J1 demand 量化不充分；PH non-card 证据栈采集偏差不得外推为全球最优；WS-1 可能被 KAST / Oobit / Plasma / Coins.ph 收窄；A6→A3→A1 是 staged 而非并列战略；stablecoin-primary 不得漂移为 fiat-native neobank。

评审记录：`reviews/05-gpt56-review.md`、`reviews/05-grok46-review.md`。
证据索引：`evidence/05-sources.md`。

### Roadmap v1 验收

Roadmap v1 已经 **AChatGPT GPT-5.6 Sol/high：PASS**，**P0=0、P1=0**，结论为 **ROADMAP ACCEPT**；下一步：**可固化 v1**。

正式执行方式：**Gate 串行、Discovery 并行**。Discovery 可提前进行，但前一 Gate 未成立前不提前规模化建设。

### Strategic Validation v1 验收

Strategic Validation v1 已经 **AChatGPT GPT-5.6 Sol/high：CLEAN PASS**（Job `job_01M19EH1H4YFW81YB1ZH2YM7S2`），**P0=0、P1=0、P2=0**，结论为 **STRATEGIC_VALIDATION ACCEPT**。

当前战略验证状态：
- **P1 One Money Relationship**：`NOT YET VALIDATED / DATA GAP`；需补 anonymous cohort，证据不足不得判负向，余额停留不得单独当 retention。
- **P2 Multi-rail Everyday Spend**：**QR Ph P2M = Priority Discovery Rail**；仅为 discovery priority，不是 committed build / white space / moat。
- **P3 / J1**：**OFW / cross-border remittance = Primary J1 Discovery Wedge**；不是已证明的 AIX 产品方向；Payroll / freelancer invoice 继续作为 secondary research tracks。

Roadmap 阶段顺序不变：**Current → P1 → P2 → P3**；正式执行方式继续保持 **Gate 串行、Discovery 并行**。

评审记录：`reviews/07-achatgpt56sol-review.md`。
证据索引：`evidence/07-sources.md`。

### Strategic Validation Update 08 验收

Update 08 已经 **AChatGPT GPT-5.6 Sol/high：CLEAN PASS**（Job `job_01M19GTX3XF7R0NQP811XTW5S6`），**P0=0、P1=0、P2=0**，结论为 **STRATEGIC_UPDATE ACCEPT**。

当前状态：
- **P1 One Money Relationship**：`NOT_YET_PASS — positive repeat-relationship signal proven; linked fund-retention evidence gap`。重复入金/重复消费/renewed inflow/跨期及完整循环已有生产聚合正向证据，但尚未证明资金在 AIX 内形成留存关系；P2 scale 继续被 Gate 阻断。
- **P2 QR Ph P2M**：继续 **Priority Discovery Rail / KEEP**；需补 named partner、经济性、运营角色与真实增量使用证据，不构成 build 授权或 moat。
- **P3 / J1 Remittance**：继续 **Primary J1 Discovery Wedge / KEEP**；SG→PH 仅作为 primary ASEAN discovery sample，MY→PH 为 comparator，US/Saudi 为 scale benchmarks，global first corridor 仍为 Unknown。

Roadmap 与阶段顺序不变：**Current → P1 → P2 → P3**；继续 **Gate 串行、Discovery 并行**。

证据：[`08-strategic-validation-update.md`](08-strategic-validation-update.md)、[`evidence/08-sources.md`](evidence/08-sources.md)。评审：[`reviews/08-achatgpt56sol-review.md`](reviews/08-achatgpt56sol-review.md)。

### Strategic Validation P1 Gate Closure 09 验收

本阶段已完成结论与证据索引的物化，并经 **AChatGPT GPT-5.6 Sol/high CLEAN PASS** 独立验收（Job `job_01M19MB53DW9DJJ8XP6BTS475Q`；**P0=0、P1=0、P2=0、FINDINGS=NONE、P1_GATE=`NOT_YET_PASS`、P1_EVIDENCE=`REPEAT_PROVEN / TEMPORAL_PROXY_POSITIVE / DIRECT_RETENTION_UNPROVEN`、ROADMAP=`UNCHANGED`、SCOPE=`PASS`**）。`Gate Closure` 表示证据阶段收口，不等于 P1 acceptance。Reason: All counts, evidence boundaries, claim classifications, roadmap constraints, scope guardrails, and Gate-stage distinction are consistent。

关键验收结果：
- **P1 One Money Relationship** 保持 `NOT_YET_PASS — positive repeat-relationship signal proven; linked fund-retention evidence gap`；重复关系已证实，时间持久性 proxy 为正向，但 direct linked historical fund-retention 仍未证实。
- 成功 card TOP_UP 聚合为 198 笔 / 23 用户，显式 `test_user_info` contamination 为 0；captured Purchase 聚合为 166 笔 / 22 用户。
- Retention-proxy A 与 B 均提供正向时间关系信号，但不证明后续 card TOP_UP 由更早的 wallet Deposit 供资，也不证明同一笔资金持续留在 AIX。
- `WalletPO` 无 balance field；实时 wallet snapshot、未实际使用的 wallet-history DTO、placeholder activity enum，以及 card-side `transaction_balance_record` 均不足以构成 direct wallet historical fund-retention source。
- **P2 scale 继续被阻断**；Roadmap 顺序不变；Discovery 可继续并行；不新增任何数值 Gate threshold。
- 最小下一证据状态为 `Unknown / downstream validation required`：需要与 repeat active use 关联的 non-PII historical balance/ledger-derived holding-duration aggregate，以区分 retained funds 与 just-in-time funding。本阶段不设计其 schema、instrumentation、API 或实现。

阶段边界：本阶段只完成 Strategy + Capability Level 的证据收口，不新增 Capability，不输出 feature、PRD、page、API、state-machine 或实现方案。

证据索引：[`evidence/09-sources.md`](evidence/09-sources.md)。评审：[`reviews/09-achatgpt56sol-review.md`](reviews/09-achatgpt56sol-review.md)。

## 下一位主控接手协议

### 当前 handoff：P1 Gate Closure 09 之后

- 当前战略问题：时间关系 proxy 是否足以关闭 P1 的 direct linked historical fund-retention evidence gap？当前答案是：**不足，P1 仍为 `NOT_YET_PASS`**。
- 本轮只允许判断 One Money Relationship 的证据充分性、Capability-level 关系判断、P1/P2 阶段依赖与 Roadmap Gate 影响；不要把 proxy 计数改写成 Gate threshold。
- 最小下一证据为 non-PII linked historical balance/ledger-derived holding-duration aggregate tied to repeat active use；当前状态是 `Unknown / downstream validation required`。
- **Hardened Capability-level guardrail：** 后续工作必须停留在 Strategy + Capability Level；不得下钻到页面/UI/CTA/文案、字段/API mapping、状态机、异常流程、schema/instrumentation、PRD 需求或实现设计。若 Capability-level 证据仍不足，记录 `Unknown / downstream validation required` 后停止。
- P2 scale 仍被 P1 Gate 阻断；Roadmap 仍为 `Current → P1 → P2 → P3`，Discovery 可并行。

接手本任务时，先执行以下检查，再做任何研究：
1. 用一句话复述当前战略问题；
2. 列出本轮只需要判断的 Capability / 战略假设；
3. 明确写出本轮 **不会研究** 的具体设计内容；
4. 若现有证据已经足以做 Capability 决策，不再继续深挖功能内部细节；
5. Reviewer 必须把 `是否越过 Capability Level` 作为独立 Gate。发生越界时，即使事实正确，也判执行偏航并退回。

默认交付格式优先为：**战略结论 → Capability 需求/优先级 → 依据 → Unknown/风险 → Roadmap/Gate 影响**。不输出功能详细方案。

## 后续维护规则
每完成一个 Step：
1. 新增 `NN-*.md` 结论文档；
2. 更新 `evidence/NN-sources.md`；
3. 如有外部模型评审，保存到 `reviews/NN-*.md`；
4. 更新本文件阶段状态与关键决策；
5. 不覆盖历史结论，结论变化时记录“旧结论 → 新证据 → 新结论”。
