---
module: knowledge-base
feature: kb-governance
version: "1.0"
status: active
source_doc: knowledge-base/README.md；knowledge-base/_kb-ingestion-process.md；knowledge-base/_ai-query-router.md；knowledge-base/changelog/knowledge-gaps.md；knowledge-base/_meta/cs-eval-set.md；用户确认结论 2026-05-29
source_section: runtime KB steady-state governance / freshness / ownership / change-sync / feedback loop
last_updated: 2026-05-29
owner: 吴忆锋
readers: [product, dev, qa, ai, cs, business]
---

# Knowledge Base Governance 知识库治理与保鲜

> 定位：本文是 runtime KB 的**稳态治理规范**，与 `_kb-ingestion-process.md`（如何把来源转成事实）互补——前者管「怎么写进来」，本文管「写进来之后怎么保鲜、归属、同步、验收」。本文不新增业务事实。
>
> 标「建议默认（待确认）」的数值 / 人选需 owner 拍板后生效，未确认前按建议值试运行，不视为强制 SLA。

## 1. 角色与归属（Ownership）

| 角色 | 当前 | 说明 |
|---|---|---|
| KB Owner | 吴忆锋 | 总负责，最终裁决 |
| Backup Owner | 待指定 | 降低单点（bus-factor）风险——当前为单一 owner，**建议尽快指定备份** |
| Module reviewers | 待指定 | 按模块（account/card/wallet/kyc/security/common/integrations）分派复核人 |
| CS answer reviewer | 待指定 | 复核 cs-answer-cards / ai-answer-policy 的对客口径 |

风险登记：当前 KB 为单一 owner，属已知 bus-factor 风险（见第 7 节）。

## 2. 评审节奏与保鲜 SLA（建议默认，待确认）

| 对象 | 建议节奏 | 触发式复核 |
|---|---|---|
| active 事实文件 | 每季度抽检一次 | 对应代码 / PRD 变更时立即复核 |
| `changelog/knowledge-gaps.md` | 每月过一遍，更新状态 / owner / 目标日期 | 新缺口随时追加 |
| `common/cs-answer-cards.md`、`_meta/ai-answer-policy.md` | 每月复核 | 合规边界或费用 / 能力变更时立即复核 |
| `_meta/compliance-boundaries.md` | 每季度复核 | 合规 / 牌照 / 能力开关变更时立即复核 |
| `_meta/cs-eval-set.md` | 跟随上述文件回归 | 见第 6 节质量门 |

保鲜判据：每个 active 文件的 `last_updated` 超过一个季度且对应能力有过版本变更 = 需复核。

## 3. 代码 / PRD 变更 → KB 同步触发

当以下任一发生，必须更新对应事实文件（按 `_kb-ingestion-process.md` 流程）：

1. 前端枚举 / 数据结构 / 接口 endpoint / 计算规则变化（如 CardStatus、CryptoMainNet、Urls.* 等）。
2. PRD 中某能力从删除线 / out-of-scope 转为 active，或反向下线（如 2026-05-29 Forgot Password 转 active）。
3. 合规边界变化（如 Withdraw 后续开放）。
4. 费用 / 限额 / 有效期 / 数量限制变化（同步 `_meta/limits-and-rules.md`）。

同步动作：更新事实文件正文 + frontmatter（`version` 递增、`last_updated`、`source_doc` / `source_section`）+ 必要时更新 `cs-answer-cards` / `ai-answer-policy` / `cs-eval-set` + 在 `knowledge-gaps.md` 收口相关 ALL-GAP。

## 4. 未答问题回流机制（Feedback Loop）

1. 客服坐席 / Bot 遇到 confirmed KB 无依据的问题 → 不杜撰，按 `ai-answer-policy` 转人工。
2. 同时把该问题作为新 `ALL-GAP-XXX` 追加到 `changelog/knowledge-gaps.md`（标 owner / 优先级 / 状态）。
3. 缺口确认后，回填对应事实文件，并视情况补 `cs-answer-cards` 用例与 `cs-eval-set` 用例。
4. 高频未答问题应优先升级优先级。

## 5. 版本与变更记录规则

1. 每次实质变更递增 frontmatter `version`，更新 `last_updated`，并在 `source_doc` / `source_section` 反映新来源。
2. 用户确认类结论统一写「用户确认 YYYY-MM-DD」并关联 ALL-GAP 编号。
3. 不在模块文件内新增本地 checklist / TODO / gap 表（唯一缺口表是 `changelog/knowledge-gaps.md`）。
4. 不把建设期过程文件（review / correction / implementation log）混入 runtime KB。

## 6. 质量门（Release Gate）

1. 上线 / 重大变更前，按 `_meta/cs-eval-set.md` 重跑全集。
2. 建议门槛（待确认）：A 类 ≥ 95% 且零越权；B/C/D 类零容忍。
3. 未通过的用例若源于 KB 缺口 → 回流 ALL-GAP，不打补丁式杜撰。
4. 评测结果不写入 runtime 事实文件（属过程产物）。

## 7. 风险登记

| 风险 | 现状 | 缓解 |
|---|---|---|
| 单一 owner（bus-factor） | 仅吴忆锋 | 指定 Backup Owner + 模块复核人（第 1 节） |
| 缺口老化 | 69+ 条 ALL-GAP 多为 deferred、缺 owner / 日期 | 每月过表，补 owner 与目标日期（第 2 节） |
| 资金类 P0 缺口未闭环 | ALL-GAP-017~029 等仍 deferred | 由后端 / 账务推进；对客侧已先行转人工（cs-answer-cards §7） |
| 对客口径漂移 | answer-cards 可能滞后于能力变更 | 触发式复核 + 质量门（第 3、6 节） |
| 本地化缺失 | KB 为中英混排内部笔记，无终端本地化话术 | 需产品 / 文案补 EN / 本地语言层（范围外，本文仅登记） |

## 8. Sources

- (Ref: knowledge-base/README.md)
- (Ref: knowledge-base/_kb-ingestion-process.md)
- (Ref: knowledge-base/_ai-query-router.md)
- (Ref: knowledge-base/_meta/cs-eval-set.md)
- (Ref: knowledge-base/changelog/knowledge-gaps.md)
- (Ref: 用户确认结论 2026-05-29)
