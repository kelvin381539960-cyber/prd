# AIX 市场格局与产品定位研究任务

- **状态**：Active
- **开始日期**：2026-08-29
- **研究对象**：AIX
- **核心目标**：建立 AIX 所处的 Crypto / Stablecoin 现实购买力市场底图，识别真实用户 Jobs、生态位、竞争关系与 AIX 应占据的位置，并据此完成 Strategy + Capability Level 的能力决策。
- **重点竞品样本**：RedotPay；其他玩家按市场证据纳入，不预设名单。

## 任务目标（硬约束）

本任务必须回答：AIX 应该成为什么、需要哪些核心 Capability、为什么需要、各项 Capability 的优先级与顺序是什么、Roadmap / Gate 如何安排，以及什么证据足以支持进入下一阶段。

本任务只做战略定位、Capability 判断、优先级/顺序、关键约束与证据边界；不把能力判断延伸为具体合作或实现指令。

## 🚨 Next Agent 必读：本任务的最高研究深度

**本任务不是功能设计 / PRD 任务。最高且唯一的研究深度固定为 `Strategy + Capability Level`。**

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

### Out of Scope（明确禁止）

以下内容一律不属于本 task：

- 具体 Vendor / partner selection or onboarding；
- 内部 owner / sponsor identification 或 handoff；
- 商务报价、商业条款或合同谈判；
- 具体牌照、监管责任或责任拆分谈判；
- API、字段、状态、技术集成或接口方案；
- 实现级 fund-flow、技术方案或代码；
- 功能细节、页面、UX、交互、文案、原型或 PRD。

### Vendor / Partner Stop Rule

允许在战略层确认某类 Capability 存在可行的供应路径或市场先例，用于判断 Capability 的可行性、约束、优先级或证据强弱；不允许在本 task 内推进具体执行。一旦问题变成“找哪家、找谁、怎么合作、多少钱、怎么接”，必须标记为 `Downstream Vendor/Implementation Validation` 并立即停止，不得继续在本 task 选择 Vendor / partner、识别内部 owner / sponsor、推进 handoff、谈判商务/合规责任或设计集成。

### Stage 10–12 证据上限

Stage 10–12 只能作为 **QRPh Capability 的可行性与证据上限**：可用于判断 QRPh Capability 是否值得继续发现、当前有哪些 Unknown / hard constraints、以及其优先级和 Gate 影响。Stage 10–12 的既有文本、历史 next action 或 Vendor Validation 表述不构成当前任务的执行授权。

Stage 10–12 不得成为继续做 Stage 13 owner / sponsor / vendor execution 的依据；本任务不启动或延续 Stage 13 的内部 owner 定位、sponsor 确认、partner onboarding、商务/合规落地或具体实现验证。超出 QRPh Capability 判断的问题统一标记为 `Downstream Vendor/Implementation Validation` 并停止。既有 Stage 10–12 报告、证据与 review 不删除、不改写。

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

当前不可变状态：P1 = `NOT_YET_PASS`；P2 scale blocked by P1；Roadmap = `Current → P1 One Money Relationship → P2 Multi-rail Everyday Spend → P3 Everyday Money Account`；执行方式 = `Gate Serial / Discovery Parallel`。后续研究不得改写这些状态，只能在 Capability / evidence / Gate 影响层补充依据。

### 6. Stop Rule

只要出现页面/交互/字段/API/状态机/异常规则/具体流程等设计决策，即视为 **scope drift**，不需要等“连续两个以上”。必须立即停止，删除/搁置该下钻分支，并回到当前战略问题；不得继续累积为研究产物。

如果产出已经可以直接交给研发作为具体功能需求，则说明研究深度已越界，应回退到 Capability 表述。

### 越界自检

每次输出前检查：若产出可以直接交给商务、合规或研发去执行具体合作或实现，则已越界；立即停止该分支，标记为 `Downstream Vendor/Implementation Validation`，并回退到 Capability、证据、优先级或 Gate 影响。

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
| Strategic Validation 10 | QR Ph named partner + operating model + economics discovery | ✅ Completed | [`10-qrph-partner-operating-model.md`](10-qrph-partner-operating-model.md) |
| Strategic Validation 11 | Netbank public feasibility closure | ✅ Completed | [`11-netbank-public-feasibility-closure.md`](11-netbank-public-feasibility-closure.md) |
| Strategic Validation 12 | Netbank internal relationship validation route | ✅ Completed | [`12-netbank-internal-relationship-validation-route.md`](12-netbank-internal-relationship-validation-route.md) |
| Strategic Validation 13 | Netbank internal owner route identification | ⚠️ Historical scope drift / archived | [13-netbank-internal-owner-route.md](13-netbank-internal-owner-route.md) |
| Strategic Validation 14 | Target User Group Analysis | ⏳ Pending | — |

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

### Strategic Validation 10：QR Ph Partner Operating Model & Economics Discovery

本阶段已完成 **Strategy + Capability Level 的物化**，并经 **AChatGPT GPT-5.6 Sol / high CLEAN PASS** 独立验收（Review job `job_01M19NENC9PCFW2M9X6Z91SJ66`；**VERDICT=PASS、P0=0、P1=0、P2=0、FINDINGS=NONE、QR_DISCOVERY=KEEP、PRIMARY_PARTNER_CANDIDATE=NETBANK、PARTNER_STATUS=DISCOVERY_CANDIDATE_NOT_APPROVED、OPERATING_MODEL=PARTNER_LED_POOLED_SETTLEMENT_PROPOSAL、ECONOMICS=UNKNOWN_COMMERCIAL_QUOTE_REQUIRED、FULL_STABLECOIN_TO_QRPH_PATH=UNKNOWN、AIX_REGULATORY_ROLE=UNKNOWN、P2_SCALE=BLOCKED_BY_P1、ROADMAP=UNCHANGED、SCOPE=PASS**）。Reason: All 16 evidence, classification, roadmap, and capability-scope guardrails pass。Netbank remains a discovery candidate, not an approved or selected vendor；pooled settlement remains Proposal。本阶段不等于 build authorization、partner approval 或 P2 scale acceptance。

关键决策：
- QR Ph P2M 从 generic `Priority Discovery Rail` 升级为 **`Netbank-led payer-side discovery path / KEEP`**；Netbank 为 **Tier-1 discovery candidate**，Maya / PayMongo 为 Tier-2 backup。
- Netbank 的 Tier-1 结论仅基于公开证据组合：QR Ph Sender/Receiver 角色、payer-side QRPh 能力证据、BaaS Settlement Account 模型和 international payment company 支持；不代表 partner willingness 或已批准商业条款。
- 首先验证 **partner-led pooled settlement** Proposal；per-user Netbank Account-as-a-Service / white-label account 仅作为 fallback；direct AIX OPS / merchant-acquisition route 不作为下一步 discovery。
- Economics 为 **`Unknown / commercial quote required`**；PHP10 generic disbursement 和 1.0–1.4% merchant-acceptance pricing 仅为 benchmark，不是 AIX payer-side cost，也不新增 pass threshold。
- BSP OPS 边界意味着 partner-led integration 不会自动消除 AIX 监管义务；AIX exact role/classification、stablecoin→PHP→QRPh 完整路径、责任拆分与 partner terms 仍为 Unknown。

Roadmap 影响：P2 discovery 更具体，但 **P2 scale 仍被 P1 Gate 阻断**；Roadmap 仍为 `Current → P1 → P2 → P3`，不改变 Gate Serial / Discovery Parallel。

证据索引：[`evidence/10-sources.md`](evidence/10-sources.md)。评审：[`reviews/10-achatgpt56sol-review.md`](reviews/10-achatgpt56sol-review.md)。

### Strategic Validation 11：Netbank Public Feasibility Closure

本阶段已完成 **Strategy + Capability Level 的公开证据收口**，并经 **AChatGPT GPT-5.6 Sol / high CLEAN PASS** 独立验收（Review job `job_01M1AP9VBDQY5QJMBQ2C3JQVRV`；**VERDICT=PASS、P0=0、P1=0、P2=0、FINDINGS=NONE、PUBLIC_RESEARCH=STOP、QR_DISCOVERY=KEEP、NON_RESIDENT_FIT=SUPPORTED_CATEGORY_LEVEL、AIX_SPECIFIC_APPROVAL=UNKNOWN、POOLED_INFRA_PATTERN=SUPPORTED、AIX_RETAIL_P2M_PERMISSIBILITY=UNKNOWN、STABLECOIN_TO_PHP_LEG=SUPPORTED_LOCAL_PAYOUT、FULL_STABLECOIN_TO_QRPH_PATH=UNKNOWN、COMPLIANCE_SPLIT=UNKNOWN、ECONOMICS=UNKNOWN_COMMERCIAL_QUOTE_REQUIRED、CURRENT_PARTNER_STATUS=DISCOVERY_CANDIDATE_NOT_APPROVED、NEXT_ACTION=VENDOR_VALIDATION、FUTURE_SUCCESS_STATUS=PARTNER_VALIDATED_CANDIDATE、P2_SCALE=BLOCKED_BY_P1、ROADMAP=UNCHANGED、SCOPE=PASS**）。Reason: All 16 guardrails are consistently bounded, classified, and traceable; public research closes without implying partner validation or build authorization。Stage 11 row 的 `✅ Completed` 仅表示 **public-evidence closure completed, NOT vendor validation completed**。

**Netbank current status remains `DISCOVERY_CANDIDATE_NOT_APPROVED`**；`PARTNER_VALIDATED_CANDIDATE` 仅是未来满足 Vendor Validation 条件后的 conditional state。本次 review 不产生 vendor validation、partner approval、build authorization 或 P2 scale acceptance。

关键验收结果：
- **Non-resident partner fit：`SUPPORTED AT CATEGORY LEVEL`**。Netbank 明确覆盖 non-resident payment processors / remittance companies，BaaS 结构支持由其他国家组织的 TPSP；但 **`AIX-specific eligibility/approval = UNKNOWN`**，仍需确认 AIX entity、licenses、business model 与 intended fund flow。
- **Pooled-settlement infrastructure pattern：`SUPPORTED`；AIX retail P2M permissibility：`UNKNOWN`**。Settlement Account 与 corporate-account-funded QRPH primitive 足以支持能力级验证问题，但不证明单一 pooled account 可代表多个 AIX end-users 进行 QRPh merchant payments。
- **Stablecoin → PHP leg：`SUPPORTED` for local payouts via licensed VASP partner**；完整 **`stablecoin → PHP → QRPh end-user merchant spend` = `UNKNOWN`**。
- BaaS agreement 显示 TPSP/AIX 在 End-User terms、support、product/applicable-law compliance、privacy consent 方面承担 material product-level burden；Netbank 保留 approval/authentication/audit roles。完整 **AML/KYC/transaction-monitoring/consumer-protection split = UNKNOWN**。
- Economics 继续为 **`UNKNOWN / commercial quote required`**。不把 public generic PHP10 或 merchant-acquiring percentages 当作 AIX actual cost，不新增阈值。
- 最低下一步是 **Vendor Validation**，不是继续 public research；仅确认 AIX/non-resident eligibility、pooled corporate settlement、USDC/USDT→PHP→QRPh composition、exact commercial quote/all-in economics、required licenses/OPS status、责任拆分，以及 user-frequency/everyday-spend use case 是否可接受。

Decision trigger：若 Netbank 确认 **eligibility + acceptable pooled model + credible stablecoin→PHP composition + acceptable regulatory burden + viable all-in economics**，路径升级为 **`PARTNER_VALIDATED_CANDIDATE`** 供 P2 discovery；这仍不是 build authorization，P2 scale 继续被 P1 阻断。若核心条件失败，则 downgrade Netbank 并转 Tier-2 partner discovery。

Roadmap 仍为 `Current → P1 One Money Relationship → P2 Multi-rail Everyday Spend → P3 Everyday Money Account`；Gate Serial / Discovery Parallel 不变；P1 仍为 `NOT_YET_PASS`，P2 scale 仍 blocked。

阶段边界：本阶段只完成 Strategy + Capability Level closure；明确不进入 partner outreach message、contract negotiation wording、API endpoint、implementation-level fund-flow diagram、feature、UX、PRD、state machine、error handling、schema、code。

证据索引：[`evidence/11-sources.md`](evidence/11-sources.md)。评审：[`reviews/11-achatgpt56sol-review.md`](reviews/11-achatgpt56sol-review.md)。

### Strategic Validation 12：Netbank Internal Relationship Validation Route

本阶段已完成 **Strategy + Capability Level 的内部关系证据升级物化**，并经 **AChatGPT GPT-5.6 Sol / high 第二轮 CLEAN PASS** 独立验收（Review job `job_01M1AR5YW2V8B9CG6MVGQD4870`；**VERDICT=PASS、P0=0、P1=0、P2=0、FINDINGS=NONE**）。前一轮的 2 个 P1 已全部解决，且未发现新的 P0/P1/P2。

关键验收结果：
- **Internal Organization/Collaboration Fact：** Atome/Advance wider group 已存在 `EXISTING_ACTIVE` 的菲律宾 Netbank 运营关系，涵盖 Savings/Transfer 相关 live integration、生产事件协调、Netbank 降级/宕机处理、callback/status reconciliation 与 direct channel verification。
- **Decision：** 该关系升级的是执行路径与 vendor-access risk，不是 AIX partner validation。AIX-specific partner status 仍为 **`DISCOVERY_CANDIDATE_NOT_APPROVED`**；不得把 Atome/Advance group usage 推断为 AIX approval、partner willingness、contract/commercial reuse 或 technical reuse。
- **Decision：** vendor-access risk 为 **`REDUCED_NOT_ELIMINATED`**（reduced, not eliminated）；精确 vendor/commercial/compliance owner identity 及其是否能 sponsor AIX onboarding 尚未建立。
- **Proposal / minimum next action：** `INTERNAL_OWNER_HANDOFF_THEN_AIX_VENDOR_VALIDATION`（internal owner handoff, then AIX vendor validation）。先定位既有内部 Netbank vendor/commercial/compliance owner path，再执行 Stage 11 已定义的 capability-level validation questions；本阶段未执行 handoff、未起草或发送消息、未发起 contact action。
- **Validation failure fallback：** 若 AIX-specific Vendor Validation 在一个或多个核心条件上失败（eligibility、acceptable pooled model、credible stablecoin→PHP composition、acceptable regulatory burden、viable all-in economics），则 **downgrade Netbank and resume Tier-2 partner discovery**。Roadmap order、P1 Gate（`NOT_YET_PASS`）、P2 scale block 及 `Gate Serial / Discovery Parallel` 均不变；AIX 仍为 `DISCOVERY_CANDIDATE_NOT_APPROVED`。
- **Unknown：** contract/commercial reuse 与 technical capability reuse 均保持 `UNKNOWN`；pooled multi-end-user retail P2M permissibility、完整 stablecoin→PHP→QRPh composition、AIX-specific approval/licensing、compliance split、all-in economics 与 use-case acceptance 等 Stage 11 Unknowns 均不变。
- **Roadmap / Gate：** `P1 NOT_YET_PASS`、P2 scale 仍被 P1 阻断；roadmap 仍为 `Current → P1 One Money Relationship → P2 Multi-rail Everyday Spend → P3 Everyday Money Account`；Gate Serial / Discovery Parallel 不变。

阶段边界：本阶段只完成 Strategy + Capability Level 的内部关系/执行路径证据升级，不进入 partner outreach、contract negotiation、employee identification、API、implementation-level fund-flow diagram、feature、UX、PRD、state machine、error handling、schema 或 code。

证据索引：[`evidence/12-sources.md`](evidence/12-sources.md)。评审：[`reviews/12-achatgpt56sol-review.md`](reviews/12-achatgpt56sol-review.md)。

### Historical scope drift note — Strategic Validation 13

Stage 13 曾经执行并形成历史产物，但按当前 authoritative scope 复核后被判定为超出本研究任务边界。它涉及 internal owner/sponsor route，属于 `Downstream Vendor/Implementation Validation`，不是 active task，也不是 continuation point。其历史文件可保留用于审计，但不得作为后续 owner/vendor/商务/合规落地工作的授权或 handoff；当前主线先进入 Strategic Validation 14，不进入 owner/vendor route 或 Remittance / QR / Send capability prioritization。

### Strategic Validation 14 — Target User Group Analysis（Pending）

**状态：`Pending`。** 这是下一独立阶段，且必须先于 Remittance / QR / Send capability prioritization。它要重新回答：“谁是 AIX 的核心目标用户？”既有阶段对 J1、OFW / remittance、crypto-native、stablecoin-native 或其他群体的结论，只能作为待复核的历史假设，不得直接当作本阶段的用户前提。

此前生成但未评审的 Remittance Stage 14 草稿（14-j1-remittance-strategic-model.md、evidence/14-sources.md）已作废并删除，不属于正式研究产物、证据源或 continuation point；Remittance 仅作为待本阶段重新验证的用户/场景假设。

#### 阶段战略问题与边界

本阶段只在 **Strategy + Capability Level** 判断候选用户群、核心 User Jobs、AIX 应建立的用户关系及其对定位 / Roadmap / Capability 的影响，不做功能设计或实现设计。

不得因 AIX 当前能力、当前地区覆盖、现有渠道或既有 Roadmap 反推核心用户。每个候选群体必须按证据逐项判断；证据不足时保留 `Unknown`，没有证据不得将任何群体升级为 **Core Target User**。

#### 最低研究维度

至少覆盖以下维度，并为每个候选群体标注证据强弱与 Unknown：

- 候选用户群及其可区分的分层依据；
- 核心 Jobs；
- 收入 / 资金来源及币种形态（`fiat` / `crypto` / `stablecoin`）；
- 当前金融行为与 crypto 行为；
- stablecoin 认知与真实使用；
- 为什么愿意持有或使用 stablecoin；
- 痛点强度；
- 使用频率与价值；
- 当前替代方案；
- AIX fit；
- 市场规模与证据强度；
- 可触达性；
- 留存 / 资金关系潜力。

#### 币种口径硬约束

必须明确区分 **“收入 / 资金来源的币种”** 与 **“进入 AIX 后用户愿意持有或使用的资金形态”**。前者不得推导后者；两者分别记录 `fiat` / `crypto` / `stablecoin` / `Unknown`，并说明证据边界。

#### 阶段输出与完成条件

阶段输出必须包括：

- `Primary / Secondary / Non-target` 用户分层；
- 可被证据支持的核心用户定义；
- 各分层、各关键维度的证据强弱与 `Unknown`；
- 对定位、Roadmap 与 Capability 优先级的影响，以及仍需验证的 Gate / 假设。

在本阶段完成并形成可审计结论前，暂停 Remittance / QR / Send 的进一步优先级结论；它们的 capability prioritization 是本阶段之后的下游工作。全程保持 **Strategy + Capability Level**，禁止下钻到功能、页面、API、Vendor、partner、owner 或实现细节。

## 下一位主控接手协议

### 当前 handoff：Strategic Validation 14 — Target User Group Analysis

下一步只做 Target User Group Analysis：重新判断 AIX 的核心目标用户，不预设 OFW / Remittance、crypto-native 或 stablecoin-native 任一群体为核心；完成前不得继续形成 Remittance / QR / Send 的进一步 capability prioritization 结论。

- 研究单位是候选用户群、User Jobs、资金关系、市场证据与 AIX fit，最终回传 Primary / Secondary / Non-target 分层及其对定位、Roadmap、Capability prioritization 的影响；不是 Vendor、partner、内部 owner 或 feature list。
- 逐项核对候选用户群、Jobs、收入 / 资金来源币种、当前金融 / crypto 行为、stablecoin 认知与真实使用、持有 / 使用动机、痛点、频率 / 价值、替代方案、AIX fit、市场规模 / 证据强度、可触达性与留存 / 资金关系潜力。
- 严格分开“收入 / 资金来源币种”与“进入 AIX 后愿意持有 / 使用的资金形态”；任一关键判断无证据时标记 `Unknown`，不得升级为 Core Target User。
- 不因 AIX 当前能力、当前地区或既有 Roadmap 倒推用户；既有 J1 / OFW / Remittance / crypto-native / stablecoin-native 结论均作为待复核假设，而非预设答案。
- 确认分析与预期输出仍处于 Strategy + Capability Level；不得研究功能、页面、API、Vendor、partner、owner、商务 / 合规落地或实现细节。
- 本阶段不研究 Vendor / partner / supply path；既有外部证据仅可用于理解用户当前替代方案，不在本阶段形成新的供应可行性、合作方或实施结论。
- P1 保持 **`NOT_YET_PASS`**；P2 scale 继续 blocked by P1；Roadmap 保持 `Current → P1 One Money Relationship → P2 Multi-rail Everyday Spend → P3 Everyday Money Account`；`Gate Serial / Discovery Parallel` 不变。

接手本任务时，先执行以下检查，再做任何研究：
1. 用一句话复述本轮要回答的“谁是 AIX 核心目标用户”战略问题；
2. 列出不预设结论的候选用户群，并对每个群体逐项检查最低研究维度、证据强弱与 Unknown；
3. 确认分析与预期输出仍处于 Strategy + Capability Level；
4. 明确本轮不会研究功能、页面、API、Vendor、partner、owner、商务 / 合规落地或实现细节；
5. 在 Stage 14 结论完成前，不形成 Remittance / QR / Send 的进一步优先级结论；发生 scope drift 时立即停止并回退。

默认交付格式优先为：**候选用户群 → Primary / Secondary / Non-target → 核心用户定义 → 证据强弱 / Unknown → 定位 / Roadmap / Capability 影响**。不输出功能详细方案。

## 后续维护规则
每完成一个 Step：
1. 新增 `NN-*.md` 结论文档；
2. 更新 `evidence/NN-sources.md`；
3. 如有外部模型评审，保存到 `reviews/NN-*.md`；
4. 更新本文件阶段状态与关键决策；
5. 不覆盖历史结论，结论变化时记录“旧结论 → 新证据 → 新结论”。
