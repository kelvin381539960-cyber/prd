---
module: account
feature: password-reset
version: "2.2"
status: active
source_doc: archive/legacy-prd/app/registration-login/README.md；archive/legacy-prd/security/identity-verification/README.md；AIX 代码 src/data/set-pwd/SetPwdRepo.ts；用户确认结论 2026-05-29（ALL-GAP-078）
source_section: Forgot Password 当前支持（SMS OTP 验证）；SetPwdRepo 封装；旧 7.3 Password Reset 删除线（不作为流程依据）
last_updated: 2026-05-29
owner: 吴忆锋
readers: [product, ui, dev, qa, business, ai]
---

# Password Reset 忘记密码流程

## 1. 当前结论

用户确认 2026-05-29：当前 App **支持 Forgot Password / 忘记密码**。用户通过 **SMS OTP 验证**身份后即可重置密码。本能力为 active runtime fact（ALL-GAP-078 resolved-by-user）。

旧 `archive/legacy-prd/app/registration-login/README.md` 7.3 Password Reset 章节为删除线，其页面、文案、BIO 清理逻辑**不作为**本能力的流程依据；当前能力以本节 active 结论 + 代码封装（§0.1）+ 后续 active PRD 为准。

页面级 UX（具体页面数、文案、错误页、与 BIO 清理的关系）尚无 active PRD，暂不沉淀为事实（见 ALL-GAP-078）。

## 2. Runtime 处理

| 项目 | 处理 |
|---|---|
| Forgot Password 入口 | 当前为 confirmed 能力（用户确认 2026-05-29） |
| 身份验证方式 | SMS OTP（用户确认 2026-05-29）；OTP 通用规则见 security/otp-verification.md |
| Reset Password 流程 | 代码封装 `initForgetPwd`（step1，发起）+ `setForgetPwd`（step2，提交新密码），见 §0.1 |
| 重置密码后清除 BIO / 关闭 BIO | 旧删除线逻辑，仍**不**作为 confirmed runtime fact，需新 PRD 确认 |
| 页面级 UX 细节 | 暂无 active PRD，不沉淀（ALL-GAP-078） |
| Password Policy | 重置后的新密码仍受 security/password-policy.md 约束 |

## 3. 使用规则

1. 回答当前 App 是否支持 Forgot Password 时：**当前支持**，经 SMS OTP 验证后重置密码（用户确认 2026-05-29）。
2. 不得根据旧删除线中的页面、文案、BIO 清理逻辑推导当前页面级 UX 或 BIO 行为；这些仍待 active PRD。
3. 不得把 SMS OTP 路径外推为 email / sessionId 路径已对客开放（见 §0.1 判定边界 3）。
4. 页面级 UX 等细节补齐前，相关追问引用 ALL-GAP-078。

## 0.1 代码封装与能力确认（2026-05-29）

> Code alignment note: 2026-05-29 核对 AIX 前端代码，忘记密码 / 修改密码的接口封装在当前代码库中存在；同日产品确认 Forgot Password 经 SMS OTP 对用户开放，本文件已转 `active`（见 §1）。SMS OTP 路径对应 `initForgetPwd({mobile, areaCode})`。本节登记代码封装事实；页面级 UX 仍需 active PRD。

代码可确认（`src/data/set-pwd/SetPwdRepo.ts`）当前存在以下封装：

- `initForgetPwd(method)` → POST `Urls.forgetPwdStep1`；`method` 为 `{ email }` | `{ mobile, areaCode }` | `{ sessionId }`
- `setForgetPwd(method, newPassword)` → POST `Urls.forgetPwdStep2`，提交 `{ ...method, newPassword }`
- `initChangedPwd()` → POST `Urls.changePwdStep1`
- `setChangePwd(newPassword)` → POST `Urls.changePwdStep2`，提交 `{ newPassword }`

判定边界：

1. 用户确认 2026-05-29：Forgot Password 当前对用户开放，经 SMS OTP 验证后重置密码（`initForgetPwd({mobile, areaCode})` → `setForgetPwd`）。
2. 入口位置、页面级 UX、与 BIO 清理的关系仍需 active PRD，不能由代码推导。
3. `initForgetPwd` 的 `email` / `sessionId` 路径封装存在，但本次仅确认 SMS OTP（`mobile + areaCode`）对客开放；email / sessionId 是否对客启用未确认，不写成事实。
4. `changePwd*`（登录态内修改密码）与 `forgetPwd*`（忘记密码）是不同能力；本文件只针对 Forgot Password，修改密码能力的沉淀同样需产品确认后另立。

## 4. Sources

- (Ref: 用户确认 2026-05-29 / ALL-GAP-078：Forgot Password 当前支持，SMS OTP 验证)
- (Ref: AIX 代码 src/data/set-pwd/SetPwdRepo.ts / initForgetPwd / setForgetPwd)
- (Ref: knowledge-base/security/otp-verification.md / OTP 通用规则)
- (Ref: knowledge-base/security/password-policy.md / 新密码策略)
- (Ref: archive/legacy-prd/app/registration-login/README.md / 7.3 Password Reset 旧删除线，不作为流程依据)
