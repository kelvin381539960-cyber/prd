---
module: account
feature: password-reset
version: "2.1"
status: deleted_out_of_scope
source_doc: archive/legacy-prd/app/registration-login/README.md；archive/legacy-prd/security/identity-verification/README.md
source_section: Registration Login / 7.3 Password Reset 删除线内容；AIX 代码 src/data/set-pwd/SetPwdRepo.ts（仅记录封装存在性）
last_updated: 2026-05-29
owner: 吴忆锋
readers: [product, ui, dev, qa, business, ai]
---

# Password Reset 忘记密码流程

## 1. 当前结论

Password Reset / Forgot Password 相关内容在 `archive/legacy-prd/app/registration-login/README.md` 中属于删除线内容。

用户已确认：删除线内容等同已删除，不再作为待确认逻辑，也不纳入当前 App runtime knowledge-base。

## 2. Runtime 处理

| 项目 | 处理 |
|---|---|
| Forgot Password 入口 | 不作为当前 Login confirmed 入口 |
| Reset Password Page | 不作为当前 active 页面 |
| 重置密码后清除 BIO / 关闭 BIO | 不作为当前 confirmed runtime fact |
| OTP / Face Auth / Password Policy | 仍由 Security 模块维护，但不代表 Password Reset 流程存在 |

## 3. 使用规则

1. 回答当前 App 是否支持 Forgot Password / Password Reset 时，应说明：当前 runtime KB 不纳入该能力，因为源 PRD 对应内容为删除线。
2. 不得根据删除线中的页面、接口、BIO 清理逻辑推导当前能力。
3. 若后续产品重新启用该能力，需要新的 active PRD 作为证据，再重建本文件。

## 0.1 代码封装存在性说明（2026-05-29，不改变 deleted 结论）

> Code alignment note: 2026-05-29 核对 AIX 前端代码，发现忘记密码 / 修改密码的接口封装在当前代码库中存在。**代码封装存在 ≠ 该能力对用户开放。** 本节仅登记代码事实，不改变本文件 `deleted_out_of_scope` 结论，也不作为重新启用的依据。

代码可确认（`src/data/set-pwd/SetPwdRepo.ts`）当前存在以下封装：

- `initForgetPwd(method)` → POST `Urls.forgetPwdStep1`；`method` 为 `{ email }` | `{ mobile, areaCode }` | `{ sessionId }`
- `setForgetPwd(method, newPassword)` → POST `Urls.forgetPwdStep2`，提交 `{ ...method, newPassword }`
- `initChangedPwd()` → POST `Urls.changePwdStep1`
- `setChangePwd(newPassword)` → POST `Urls.changePwdStep2`，提交 `{ newPassword }`

判定边界：

1. 这些封装的存在 **不** 证明 Forgot Password / Reset Password 页面或入口在当前 App 中对用户可见、可达或已启用。
2. 是否启用、入口位置、与 BIO 清理 / Security 模块的关系，必须由现行 active PRD + 产品确认，不能由代码推导。
3. 在产品给出 active 证据前，本文件保持 `status: deleted_out_of_scope`，对客口径仍按第 1 节“当前 runtime KB 不纳入该能力”。
4. `changePwd*`（登录态内修改密码）与 `forgetPwd*`（忘记密码）是不同能力；本文件只针对 Password Reset / Forgot Password，修改密码能力的沉淀同样需产品确认后另立。

## 4. Sources

- (Ref: archive/legacy-prd/app/registration-login/README.md / 7.3 Password Reset 删除线)
- (Ref: archive/legacy-prd/security/identity-verification/README.md / OTP / Password / BIO 支撑能力，不代表 Password Reset active)
