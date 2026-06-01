---
module: common
feature: cs-answer-cards
version: "1.0"
status: active
source_doc: knowledge-base/* 已确认事实模块；knowledge-base/_meta/limits-and-rules.md；knowledge-base/_meta/compliance-boundaries.md；knowledge-base/_meta/countries-and-regions.md；knowledge-base/account/password-reset.md；knowledge-base/changelog/knowledge-gaps.md；用户确认结论 2026-05-29
source_section: customer-service answer layer / intent → answer cards grounded in confirmed facts
last_updated: 2026-05-29
owner: 吴忆锋
readers: [product, ui, dev, qa, business, ai, cs]
depends_on:
  - _meta/limits-and-rules
  - _meta/compliance-boundaries
  - _meta/countries-and-regions
  - _meta/ai-answer-policy
  - account/password-reset
  - common/errors
  - changelog/knowledge-gaps
---

# CS Answer Cards 客服答复卡（答案层）

> 使用纪律（务必先读）：本文是**面向用户的答复指引**，每张卡都标注 confirmed 来源。
> 1. 卡内英文是**客服 / Bot 答复指引**，不等同 App 内确切文案——许多用户侧文案为后端透传（见 common/errors.md），实际展示以 App 为准。仅当来源列明确标注「确认文案」时才是可逐字引用的原文。
> 2. 状态为 `deferred` / `open` 的话题（如完整费用表 ALL-GAP-075、错误码补救字典 ALL-GAP-077、客服分级 ALL-GAP-074）**不得**当成事实作答；按本文第 9 节转人工。
> 3. 答复优先级与拒答 / 升级规则以 `_meta/ai-answer-policy.md` 为准；合规边界以 `_meta/compliance-boundaries.md` 为准。
> 4. 本文不新增事实；如某问题在 confirmed KB 中无依据，按「未知」处理（转人工 + 记 ALL-GAP），不要猜。

## 1. 文档定位

把已确认的运行时事实转成可直接用于客服 / Bot 的「意图 → 答复」卡，补齐 KB 的答案层。事实本身仍以各模块文件为准，本文只做面向用户的封装。

卡片格式：意图（用户问法）｜答复指引（英文为对客口径）｜边界 / 升级｜来源。

## 2. Account & Login

| 意图 | 答复指引 | 边界 / 升级 | 来源 |
|---|---|---|---|
| 忘记密码怎么办 | You can reset your password in the app: choose Forgot Password and verify your identity via SMS OTP, then set a new password. | 仅确认 SMS OTP 路径；email / sessionId 路径不对外宣称。页面级步骤以 App 为准 | account/password-reset.md（用户确认 2026-05-29） |
| 新密码有什么要求 | Your password must be 8–32 characters and include upper- and lower-case letters, a number, and a symbol. | — | _meta/limits-and-rules.md；security/password-policy.md |
| 注册邮箱提示已被使用 | This email is already registered. Please use another email or log in / reset your password instead. | 确认文案：`This email has been used. Please try another one.` | common/errors.md；account/registration.md |
| 账户被锁 / 提示联系客服 | Your account is locked. Please contact Customer Support to proceed. | 确认文案：`Account locked. Please contact customer support.`（banned 拦截）→ 转人工 | common/errors.md；account/login.md |
| 输错账号 / 账号不存在 | The account details look incorrect—please check them or register a new account. | 英文最终文案后端驱动，未固定（ALL-GAP-042）；勿逐字承诺 | account/login.md；ALL-GAP-042 |

## 3. Security / OTP / 验证锁定

| 意图 | 答复指引 | 边界 / 升级 | 来源 |
|---|---|---|---|
| OTP 是几位 / 多久有效 | The verification code is 4 digits and valid for 5 minutes. | OTP 与 Email OTP 同此规则 | _meta/limits-and-rules.md；security/otp-verification.md |
| OTP 能重发几次 | You can resend up to 3 times within 24 hours; after that there is a 20-minute cooldown. | — | _meta/limits-and-rules.md；security/otp-verification.md |
| 收不到 / 换设备收不到验证码 | Codes are bound to the device that requested them; switching devices invalidates them. Please request a new code on the current device. | — | common/errors.md；security/otp-verification.md |
| 提示 Too Many Attempts / 被锁 | Too many attempts: the account is temporarily locked—20 minutes after 5 failures, 24 hours after 10 failures within 24 hours. Please try again later. | 确认文案：`Too Many Attempts` | _meta/limits-and-rules.md；_meta/error-code-dictionary.md（§3 锁定类） |
| 刷脸一直转圈 / 失败 | Face verification times out after ~30 seconds with no result and shows a failure screen; you can retry. Repeated failures are rate-limited. | 5 次锁 20 分钟、10 次锁 24 小时、接口连续 20 次锁 20 分钟 | _meta/limits-and-rules.md；kyc/account-opening.md |

## 4. Card

| 意图 | 答复指引 | 边界 / 升级 | 来源 |
|---|---|---|---|
| 办卡要多少钱 | Virtual card: USD 5. Physical card: USD 10. | 仅此两项为确认费用；其他费用项（FX/ATM/跨境等）未确认（ALL-GAP-075），不要作答 | _meta/limits-and-rules.md；common/faq.md |
| 我能开几张卡 | Across pending, active, in-review and frozen, the total is limited to 5 cards (configurable), with only one application in progress at a time. | 「一人在途」DTC 可配置 | _meta/limits-and-rules.md；card/application.md |
| PIN 是几位 / 有什么限制 | The card PIN is 6 digits. A PIN where any single digit repeats more than 3 times is rejected. | — | _meta/limits-and-rules.md；card/manage/pin.md |
| 实体卡怎么激活 | Activate your physical card by entering its last 4 digits in the app. | 两步：校验后四位 → 激活 | card/manage/activation.md |
| 怎么冻结 / 解冻卡 | You can lock (freeze) and unlock (unfreeze) your card in card management. | — | card/manage/status-and-operations.md |
| 在哪看卡号 / CVV | Card number, expiry and CVV are viewable in the card's sensitive-info screen after verification. | 严禁在对话中复述完整卡号 / CVV（见 ai-answer-policy 第 5 节） | card/manage/sensitive-info.md |

## 5. Wallet / Deposit / Assets

| 意图 | 答复指引 | 边界 / 升级 | 来源 |
|---|---|---|---|
| 支持哪些稳定币 | Supported stablecoins are USDC, USDT, WUSD and FDUSD. | — | _meta/limits-and-rules.md；wallet/assets.md |
| 支持哪些国家 / 链充值 | Crypto deposit is currently supported for Philippines. Supported chains and stablecoins: BASE = USDC; BSC = FDUSD/USDC/USDT; Ethereum = FDUSD/USDC/USDT/WUSD; Solana = FDUSD/USDC/USDT. | 用户资格仍以 KYC 白名单为准；勿外推到其他国家 | _meta/countries-and-regions.md（用户确认 2026-05-29） |
| WalletConnect 二维码 / 链接多久过期 | The WalletConnect deeplink is valid for 5 minutes; the authorization lasts 1 day. | QR 过期文案：`The QR code has expired` | _meta/limits-and-rules.md；wallet/deposit.md |
| 充值多久到账 | A successful payment triggers the transfer and funds are generally available almost immediately, though a short delay can occur. | 不得承诺「立即」；以 under review / success 状态为准 | wallet/deposit.md；ALL-GAP-005 |
| Swap 汇率 / 报价过期 | Exchange quotes are single-use and can expire; if expired, refresh to get the latest rate before continuing. | 确认文案：`Exchange rate expired` | wallet/swap.md；_meta/limits-and-rules.md |

## 6. Withdraw（当前不支持）

| 意图 | 答复指引 | 边界 / 升级 | 来源 |
|---|---|---|---|
| 怎么提现 / 提现入口在哪 | Withdrawals aren't available yet. This feature is planned for a future release. | 暂不支持、后续开放；App 已隐藏入口。**不要**承诺时间表 | _meta/compliance-boundaries.md（用户确认 2026-05-29，ALL-GAP-071） |

## 7. 资金问题 / 争议 / 卡安全（必转人工）

| 意图 | 答复指引 | 边界 / 升级 | 来源 |
|---|---|---|---|
| 转账成功但钱没到 / 余额对不上 | I'm sorry about that. Please contact Customer Support so we can verify and resolve it for you. | 系统无法自动发现，依赖用户反馈 → **转人工核实/补偿** | ALL-GAP-070；RESOLVED-012 |
| 卡交易有争议 / 怀疑盗刷 / 拒付 | Please contact Customer Support (email or phone) to raise a dispute. | 争议流程 / 时效未沉淀 → **转人工** | ALL-GAP-072 |
| 实体卡丢失 / 被盗 / 要补卡 | Please contact Customer Support (email or phone). You can also lock the card in the app immediately. | 挂失 / 注销 / 补卡流程未沉淀 → **转人工**（可先引导 Lock） | ALL-GAP-073；card/manage/status-and-operations.md |
| 客服邮箱 / 电话是什么 | Reach Customer Support via the Contact Us entry in the app. | 确切邮箱 / 电话非本 KB confirmed 事实，以 App Contact Us 为准 | common/faq.md（FaqLocation CONTACT_US） |

## 8. Notification

| 意图 | 答复指引 | 边界 / 升级 | 来源 |
|---|---|---|---|
| 未读数字显示 99+ | When unread messages exceed 100, the count shows as 99+. | — | _meta/limits-and-rules.md；common/notification.md |
| 收不到推送 | Push is stopped for inactive / closed / banned accounts; otherwise it follows your notification preferences. | inactive/Closed/banned 停推；优先级 user status > preference > FC & DND | _meta/compliance-boundaries.md；common/notification.md |

## 9. 必转人工 / 必拒答（速查，详见 ai-answer-policy）

| 触发 | 处理 |
|---|---|
| 资金未到账 / 余额对不上 / 任何资金损失投诉 | 转人工（ALL-GAP-070） |
| 卡交易争议 / 盗刷 / 拒付 | 转人工（ALL-GAP-072） |
| 实体卡挂失 / 被盗 / 补卡 | 转人工（ALL-GAP-073，可先引导 Lock） |
| 提现请求 | 告知暂不支持、后续开放；坚持则转人工（ALL-GAP-071） |
| banned / 需人工复核的账户锁定 | 转人工 |
| 完整费用表 / 错误码补救 / 客服 SLA 等 deferred 话题 | 不作答，转人工（ALL-GAP-074/075/077） |
| 投资建议 / 收益承诺 / 价格预测 | 拒答（见 ai-answer-policy 第 3 节） |

## 10. Sources

- (Ref: knowledge-base/_meta/limits-and-rules.md)
- (Ref: knowledge-base/_meta/compliance-boundaries.md)
- (Ref: knowledge-base/_meta/countries-and-regions.md)
- (Ref: knowledge-base/_meta/error-code-dictionary.md)
- (Ref: knowledge-base/_meta/ai-answer-policy.md)
- (Ref: knowledge-base/account/password-reset.md)
- (Ref: knowledge-base/common/errors.md)
- (Ref: knowledge-base/common/notification.md)
- (Ref: knowledge-base/common/faq.md)
- (Ref: knowledge-base/card/manage/{activation,pin,sensitive-info,status-and-operations}.md)
- (Ref: knowledge-base/wallet/{assets,deposit,swap}.md)
- (Ref: knowledge-base/changelog/knowledge-gaps.md ALL-GAP-070~078)
- (Ref: 用户确认结论 2026-05-29)
