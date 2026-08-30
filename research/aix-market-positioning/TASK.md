# AIX 市场格局与产品定位研究任务

- **状态**：Active
- **开始日期**：2026-08-29
- **研究对象**：AIX
- **核心目标**：建立 AIX 所处的 Crypto / Stablecoin 现实购买力市场底图，识别真实用户 Jobs、生态位、竞争关系与 AIX 应占据的位置。
- **重点竞品样本**：RedotPay；其他玩家按市场证据纳入，不预设名单。

## 执行层级与 Scope Guardrails（强制）

本节是本研究后续执行的硬护栏，只约束任务范围，不修改既有市场结论、证据分级或已完成阶段产物。

### 1. 当前主任务层级

当前主任务层级固定为：**Business Strategy + Product Strategy + Strategic Roadmap + Key Assumption Validation**。

默认允许输出：

- 市场选择、用户 Job、竞争格局；
- 战略定位、业务模式、产品形态、能力组合；
- 阶段目标、Roadmap、进入/退出条件；
- 关键假设、验证指标、Current → Target Gap、优先级与依赖。

### 2. 默认禁止下钻

默认禁止把研究下钻为以下页面/产品设计/实现层内容：**页面结构、具体 UI、CTA/文案、字段/API 映射、状态机、异常文案、PRD 章节、原型、技术实现细节**。只有用户明确要求“进入具体设计/PRD/页面/接口”时，才允许切换到对应层级；切换后仍须明确新的 scope。

实现、代码或 Vendor 事实，只能用于回答战略决策所需的 **feasibility / constraint / gap**。发现实现细节，不得自动把任务切成产品设计或 PRD。

### 3. 每个新 Phase 的 Scope Check

每次开始新 Phase（包括以 Step 命名的阶段）前，执行 Agent 必须先回答：

1. 本阶段要回答的战略问题是什么？
2. 当前分析和预期输出是否仍处于战略层？

如果分析内容开始回答“页面怎么做、字段怎么写、接口怎么接”，必须立即停止该分析分支，回到本阶段的战略问题，并将问题重写为能力、约束、Gap 或验证问题。未完成 Scope Check，不得开始该 Phase 的证据采集或结论撰写。

### 4. Agent 分工同样受护栏约束

- **执行 Agent**：只收集与当前战略问题直接相关的证据；不得主动产出页面方案、交互方案、字段/API 方案或 PRD。
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

若任务内容出现连续两个以上页面/交互/字段/接口级决策，而用户没有明确要求下钻，即视为 **scope drift**。必须立即停止，删除/搁置该下钻分支，并回到当前战略问题；不得继续累积为研究产物。

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

## 后续维护规则
每完成一个 Step：
1. 新增 `NN-*.md` 结论文档；
2. 更新 `evidence/NN-sources.md`；
3. 如有外部模型评审，保存到 `reviews/NN-*.md`；
4. 更新本文件阶段状态与关键决策；
5. 不覆盖历史结论，结论变化时记录“旧结论 → 新证据 → 新结论”。
