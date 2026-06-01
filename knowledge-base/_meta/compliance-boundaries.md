---
module: _meta
feature: compliance-boundaries
version: "2.1"
status: active
source_doc: archive/legacy-prd/**/README.md；knowledge-base/* 已校准模块；用户确认结论 2026-05-29（ALL-GAP-071 / ALL-GAP-078）
source_section: converted PRD corpus / compliance boundaries；Withdraw 当前支持状态；Forgot Password 当前支持状态
last_updated: 2026-05-29
owner: 吴忆锋
readers: [product, ui, dev, qa, business, ai]
---

# Compliance Boundaries 合规边界

## 1. 文档定位

本文沉淀 AIX App runtime knowledge-base 中已确认的合规边界，用于防止 AI 或产品文档错误扩展能力。

## 2. 已确认合规边界

| 边界 | 结论 | 来源 |
|---|---|---|
| Wallet Withdraw | 用户确认 2026-05-29：Withdraw 当前暂不支持，后续开放；App 隐藏 Withdraw 入口。后续开放需以新 PRD 为准（ALL-GAP-071） | wallet/assets.md；wallet/deposit.md；用户确认 2026-05-29 |
| Waitlist KYC | Waitlist 用户无法申请开通钱包；停留在 Waitlist Page | kyc/account-opening.md；home/app-home.md |
| Rejected KYC | 因高风险被 DTC 拒绝的用户会被拦截开户且隐藏激活钱包入口 | kyc/account-opening.md；home/app-home.md |
| Notification compliance | 金融信息合规优先，营销类需用户明确同意；加密资产通知需提示风险，不承诺收益 | common/notification.md |
| Push preference | inactive / Closed / banned 停止全部消息推送 | common/notification.md |
| MoEngage subscribe sync | 删除线内容，不作为 confirmed fact | common/notification.md |
| Website / Marketing | 当前 runtime KB 不纳入 Website / Marketing PRD | knowledge-base/README；prd-source-alignment |
| Password Reset / Forgot Password | 用户确认 2026-05-29：当前支持 Forgot Password，经 SMS OTP 验证后重置密码（已转 active，ALL-GAP-078）；旧注册登录 PRD 7.3 删除线内容不作为流程依据 | account/password-reset.md；用户确认 2026-05-29 |
| Card Home click conflicts | Home PRD 与 Card Application PRD 对部分首页卡片点击跳转冲突，不自行裁决 | card/card-home.md |

## 3. 使用规则

1. 若某能力被标为隐藏、删除线、待确认或 out of scope，不得回答为已上线事实。
2. 合规边界优先级高于 FAQ 用户解释。
3. Website / Marketing PRD 不进入 runtime KB，除非后续显式变更范围。

## 4. Sources

- (Ref: archive/legacy-prd/wallet/asset/README.md)
- (Ref: archive/legacy-prd/wallet/deposit-send-swap/README.md)
- (Ref: archive/legacy-prd/kyc/wallet-opening/README.md)
- (Ref: archive/legacy-prd/notification/push-inbox/README.md)
- (Ref: archive/legacy-prd/app/registration-login/README.md)
