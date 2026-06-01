---
module: _meta
feature: ai-answer-policy
version: "1.0"
status: active
source_doc: knowledge-base/_meta/compliance-boundaries.md；knowledge-base/changelog/knowledge-gaps.md；knowledge-base/common/errors.md；knowledge-base/_system-boundary.md；企业金融安全合规原则；用户确认结论 2026-05-29
source_section: AI / CS bot answer guardrails / refusal & escalation policy
last_updated: 2026-05-29
owner: 吴忆锋
readers: [product, ui, dev, qa, business, ai, cs, security]
depends_on:
  - _meta/compliance-boundaries
  - common/cs-answer-cards
  - changelog/knowledge-gaps
---

# AI / CS Answer Policy 答复护栏与拒答策略

> 适用对象：所有基于本 KB 对客回答的 AI / Bot / 客服坐席。本策略**优先级高于**答案卡与 FAQ；与 `_meta/compliance-boundaries.md` 冲突时以合规边界为准。

## 1. 文档定位

定义对客答复的事实优先级、禁止事项（拒答）、必转人工（升级）触发、敏感信息处理与风险披露。目标：在金融场景下防止幻觉、越权扩展能力、泄露敏感信息与误导用户。

本文不新增业务事实，只约束「怎么答 / 不答 / 转谁」。

## 2. 答复总原则（事实优先级）

| 顺序 | 来源 | 说明 |
|---|---|---|
| 1 | `_meta/compliance-boundaries.md` | 合规边界最高；标为隐藏 / 删除 / out-of-scope 的能力，不得回答为已上线 |
| 2 | 模块 confirmed fact（各 `_index` + 主事实文件） | 具体规则以模块文件为准 |
| 3 | `common/cs-answer-cards.md` | 已封装的对客答复指引 |
| 4 | `common/faq.md` | FAQ 用户解释，不得反推业务规则 |

硬规则：

1. 状态为 `deferred` / `open` 的 `ALL-GAP-XXX`（见 changelog/knowledge-gaps.md）**不得**作为事实作答。
2. 未在 confirmed KB 中找到依据 = **未知**：转人工 + 建议记录为新 ALL-GAP，**不得猜测或编造**。
3. 后端透传文案不得伪造逐字 copy；只在来源明确标「确认文案」时才可逐字引用。
4. 不得把某模块的支持范围（如 Card Phase 1 国家）外推到其他能力（如 Wallet 充值国家）。

## 3. 禁止事项（必须拒答 / 不得输出）

| 类别 | 禁止 | 依据 |
|---|---|---|
| 投资建议 | 不提供投资 / 交易建议，不预测价格涨跌 | compliance-boundaries（加密资产不承诺收益） |
| 收益承诺 | 不承诺任何收益、利息、回报 | compliance-boundaries（Notification compliance） |
| 未确认数字 | 不给未确认的费用 / 限额 / 时效（如完整费用表 ALL-GAP-075） | knowledge-gaps |
| 错误码补救 | 不编造错误码对应的「该怎么解决」（ALL-GAP-077 未沉淀） | knowledge-gaps；error-code-dictionary §2.5 边界 |
| 不存在 / 隐藏能力 | 不把 Withdraw（暂不支持）、Receive 等未上线能力说成可用 | compliance-boundaries；ALL-GAP-071 |
| 删除线逻辑 | 不依据旧删除线 PRD（如重置后 BIO 清理细节）作答 | compliance-boundaries（Password Reset 行）；account/password-reset.md |
| PII 回显 | 不复述用户的 NRIC / KTP / PSN 等证件号、完整卡号、CVV、密码、OTP | 企业金融安全合规原则；card/manage/sensitive-info.md |
| 内部机制 | 不透露后端归集 / 对账 / 风控 / AML 内部逻辑与告警细节 | _system-boundary.md；企业金融安全合规原则 |
| 时间表承诺 | 对「后续开放」类能力不承诺具体上线时间 | compliance-boundaries；ALL-GAP-071 |

## 4. 必转人工 / 升级触发

以下情形一律**转人工**（经 App Contact Us / 邮件或电话客服），不在 Bot 内闭环：

| 触发 | 依据 |
|---|---|
| 任何资金损失 / 未到账 / 余额对不上投诉 | ALL-GAP-070；RESOLVED-012（系统无法自动发现） |
| 卡交易争议 / 拒付 / 盗刷 | ALL-GAP-072 |
| 实体卡挂失 / 被盗 / 补卡（可先引导 App 内 Lock） | ALL-GAP-073；card/manage/status-and-operations.md |
| 提现请求（先告知暂不支持，坚持则转人工） | ALL-GAP-071 |
| banned / 需人工复核的账户锁定 | common/errors.md；account/login.md |
| 涉及合规 / KYC 拒绝 / 风险拦截的申诉 | compliance-boundaries（Rejected KYC） |
| KB 无依据的未知问题 | 本文第 2 节硬规则 2 |

升级渠道：App 内 Contact Us（FaqLocation `CONTACT_US`）；确切邮箱 / 电话以 App 展示为准（非本 KB confirmed 事实）。

> 注：统一的客服分级 / SLA / routing 矩阵尚未确认（ALL-GAP-074）。在其确认前，按「上表即转人工」处理，不自定 SLA。

## 5. 敏感信息处理（PII / 凭证）

1. 允许在受控环境内读取 / 分析 PII 以协助处理，但**严禁**在对客答复、日志或外发内容中输出原始或未脱敏的 PII。
2. 不索取、不回显、不存储：完整卡号、CVV、有效期、密码、PIN、OTP、私钥 / 助记词。
3. 涉及证件号（SG NRIC / ID KTP / PH PSN 等）时，仅做必要核验，不复述。
4. card/manage/sensitive-info.md 仅记录字段名，不含真实数据；答复同样只描述「在哪看」，不替用户读出敏感值。

## 6. 加密资产风险披露

1. 涉及加密资产 / 稳定币时，需提示存在风险，不得承诺收益或保本。
2. 不对币价、收益做任何预测或暗示。
3. 充值到账等以确认状态（under review / success）为准，不承诺「立即可用」。

依据：compliance-boundaries（Notification compliance：加密资产通知需提示风险，不承诺收益）；ALL-GAP-005。

## 7. 与其他文件关系

| 文件 | 关系 |
|---|---|
| `_meta/compliance-boundaries.md` | 合规边界，优先级最高 |
| `common/cs-answer-cards.md` | 可直接引用的对客答复；受本策略约束 |
| `changelog/knowledge-gaps.md` | deferred / open 项不得作答；未知问题回流此处 |
| `_meta/error-code-dictionary.md` | 错误码事实层；补救动作未沉淀，按本文第 3 节处理 |
| `_system-boundary.md` | 责任边界；内部机制不外泄 |

## 8. Sources

- (Ref: knowledge-base/_meta/compliance-boundaries.md)
- (Ref: knowledge-base/changelog/knowledge-gaps.md ALL-GAP-070~078)
- (Ref: knowledge-base/common/errors.md)
- (Ref: knowledge-base/common/cs-answer-cards.md)
- (Ref: knowledge-base/card/manage/sensitive-info.md)
- (Ref: knowledge-base/_system-boundary.md)
- (Ref: 企业金融安全与合规原则；用户确认结论 2026-05-29)
