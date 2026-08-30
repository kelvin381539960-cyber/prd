# AIX 市场格局与产品定位研究任务

- **状态**：Active
- **开始日期**：2026-08-29
- **研究对象**：AIX
- **核心目标**：建立 AIX 所处的 Crypto / Stablecoin 现实购买力市场底图，识别真实用户 Jobs、生态位、竞争关系与 AIX 应占据的位置。
- **重点竞品样本**：RedotPay；其他玩家按市场证据纳入，不预设名单。

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
| Final | 综合市场地图与管理层结论 | ⏳ Pending | `final-market-positioning.md` |

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

## 后续维护规则
每完成一个 Step：
1. 新增 `NN-*.md` 结论文档；
2. 更新 `evidence/NN-sources.md`；
3. 如有外部模型评审，保存到 `reviews/NN-*.md`；
4. 更新本文件阶段状态与关键决策；
5. 不覆盖历史结论，结论变化时记录“旧结论 → 新证据 → 新结论”。
