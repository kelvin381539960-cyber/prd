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
| Step 3 | 重点玩家定位与核心用户研究 | ⏳ Pending | `03-player-positioning.md` |
| Step 4 | AIX 竞争重合关系：直接 / 相邻 / 替代 / 潜在 | ⏳ Pending | `04-competition-map.md` |
| Step 5 | AIX 当前生态位、目标生态位与市场白地 | ⏳ Pending | `05-aix-positioning.md` |
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

## 后续维护规则
每完成一个 Step：
1. 新增 `NN-*.md` 结论文档；
2. 更新 `evidence/NN-sources.md`；
3. 如有外部模型评审，保存到 `reviews/NN-*.md`；
4. 更新本文件阶段状态与关键决策；
5. 不覆盖历史结论，结论变化时记录“旧结论 → 新证据 → 新结论”。
