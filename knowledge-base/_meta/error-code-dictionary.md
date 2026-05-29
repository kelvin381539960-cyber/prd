---
module: _meta
feature: error-code-dictionary
version: "2.1"
status: active
source_doc: archive/legacy-prd/**/README.md；knowledge-base/* 已校准模块；knowledge-base/common/errors.md §0.1（AIX 代码 packages/common/src/network/error/*、src/network/ApiErrorUtils.ts、src/data/biometric/EnableBiometricRepo.ts）
source_section: converted PRD corpus / error code dictionary；前端错误处理框架层（AixError / ErrorCodes / ErrorEventType / BiometricError）
last_updated: 2026-05-29
owner: 吴忆锋
readers: [product, ui, dev, qa, business, ai]
---

# Error Code Dictionary 错误码与提示字典

> Code alignment note: 2026-05-29 从 `common/errors.md §0.1`（已按 AIX 前端代码校准）抽取错误处理**框架层**的运行时可确认事实，沉淀为本字典第 2.5 节。本次只搬运代码可直接证明的错误对象结构与框架级错误码常量，**不补**后端业务错误码全集与其对应展示文案（后端透传，前端无固定 copy；该缺口见 ALL-GAP-038 / ALL-GAP-043 / ALL-GAP-077）。

## 1. 文档定位

本文沉淀已确认的错误码 / 错误类型索引。完整用户文案详见 common/errors.md；模块内详细规则仍以模块文档为准。

本字典分两层：第 2 节为模块级已确认的错误码 / 错误类型（来自各 converted-prd 模块）；第 2.5 节为前端错误处理框架层（代码可确认）。两层都不是后端业务错误码全集。

## 2. 已确认错误码 / 错误类型

| Code / Type | 模块 | 说明 | 处理 | 来源 |
|---|---|---|---|---|
| 31031 | Card PIN | PIN 设置失败时使用后端返回文案覆盖默认失败文案 | 展示后端文案 | card/manage/pin.md |
| FACE_QUALITY_TOO_POOR | KYC / Face | Face / KYC 错误码映射来源之一 | 按 KYC / Security 映射展示 | kyc/account-opening.md；security/face-authentication.md |
| USER_TIMEOUT | KYC / Face | Face 超时 / 用户超时相关错误 | 进入 Face Failed / Loading Failed 规则 | kyc/account-opening.md；security/face-authentication.md |
| SIMILARITY_FAILED | KYC / Face | Face comparison 相似度失败 | 按错误码映射展示 | kyc/account-opening.md |
| PROOF_DOCUMENT_MATCHING_FAILED | KYC / POA | POA 资料匹配失败 | 按 POA error code 映射展示 | kyc/account-opening.md |
| DATA_VERIFICATION_FAILED | KYC | 数据验证失败 | 按 KYC 错误码映射展示 | kyc/account-opening.md |
| USER_SUBMISSION_FAILED | KYC | 用户提交失败 | 按 KYC 错误码映射展示 | kyc/account-opening.md |
| DTC unknown error | Transaction / Card | DTCPay 返回当前错误码之外的其他错误 | Lark 报警，等待产品和渠道确认 | card/transaction-detail.md |
| FAIL / EXPIRED / incomplete / empty | Face Auth | DTC 返回失败、过期、不完整或空值 | 进入 Face Auth Failed Page | security/face-authentication.md |

## 2.5 前端错误处理框架层（代码可确认）

以下来自 AIX 当前前端代码（详见 `common/errors.md §0.1`），是错误处理**框架层**事实，独立于上表的模块级业务错误码。

### 2.5.1 统一错误对象 AixError

`AixError extends Error { code, rawCode(私有), data, extra, message, pending? }`。前端用 `getErrorCode(error)` / `getErrorMessage(error)` 读取 `code` / `message`。来源：`AixError.ts`、`ApiErrorUtils.ts`。

### 2.5.2 框架级错误码常量 ErrorCodes（代码可确认 8 个）

| 常量 | 含义 / 用途 | 来源 |
|---|---|---|
| `UNAUTHORIZED` | 未授权 / 鉴权失效 | ErrorCodes.ts（@aix/common） |
| `NETWORKERROR` | 网络错误（配合 isNetworkError 判定） | ErrorCodes.ts |
| `SUCCESS` | 框架级成功标识 | ErrorCodes.ts |
| `FAILED` | 框架级失败标识 | ErrorCodes.ts |
| `NEED_SECURITY_VERIFICATION` | 需要安全验证 | ErrorCodes.ts |
| `IVS_CODE_RESP_HANDLED` | IVS 二次验证已处理（needSecurityVerification 判据） | ErrorCodes.ts；ApiErrorUtils.ts |
| `IVS_VALID_FAILED` | IVS 验证失败 | ErrorCodes.ts |
| `ACCOUNT_STATUS_ABNORMAL` | 账户状态异常 | ErrorCodes.ts |

> 关键边界：这是**前端框架层**常量集合，不是后端业务错误码全集。业务错误码（如 `USER_NOT_FOUND`、`DEVICE_BIOMETRIC_STATUS_NOT_MATCH`、`BIO_INCORRECT`）**不在** `ErrorCodes` 里——它们是后端透传的 `aixError.code` 字符串，前端按字符串值分支处理。完整业务错误码及其展示文案仍以后端为准，见 ALL-GAP-038 / ALL-GAP-043 / ALL-GAP-077。

### 2.5.3 网络错误判定 isNetworkError

`AixError.code === 'NETWORKERROR'`，或 axios 无 `response`，或 axios `code` 为 `ECONNABORTED` / `ERR_NETWORK`；兜底文案取 i18n key `network_error_page_check_your`。来源：`ApiErrorUtils.ts`。

### 2.5.4 安全验证判定 needSecurityVerification

`error.code === IVS_CODE_RESP_HANDLED` 时为真，用于衔接 IVS 二次验证流程（security 模块）。来源：`ApiErrorUtils.ts`。

### 2.5.5 二次验证事件流 ErrorEventType（代码可确认 6 值）

`started`、`progress`、`success`、`failed`、`cancelled`、`completed`。`AixError.subscribe()` 订阅事件，登录等场景据 `success` / `failed` 决定重试或报错。来源：`ErrorObserver.ts`。

### 2.5.6 生物识别错误 BiometricError（代码可确认 4 值）

| 枚举 | Android 原生码映射 | 来源 |
|---|---|---|
| `USER_ATTEMPTS_EXCEEDED` | 原生 `7` / `9` | EnableBiometricRepo.ts |
| `USER_CANCEL` | 原生 `10` / `5` / `13` | EnableBiometricRepo.ts |
| `AUTH_DENIED` | （枚举值，未映射特定原生码） | EnableBiometricRepo.ts |
| `SYSTEM_ERROR` | 其余原生码兜底 | EnableBiometricRepo.ts |

详见 `security/biometric-verification.md`。

## 3. 锁定类错误

| 场景 | 阈值 | 结果 | 来源 |
|---|---|---|---|
| OTP / Email OTP / Login Passcode / Face Auth | 24 小时内失败 5 次 | 锁定 20 分钟 | security/global-rules.md |
| OTP / Email OTP / Login Passcode / Face Auth | 24 小时内失败 10 次 | 锁定 24 小时 | security/global-rules.md |
| Face Auth / KYC API | 接口连续发起 20 次 | 锁定 20 分钟 | security/face-authentication.md；kyc/account-opening.md |

## 4. Sources

- (Ref: knowledge-base/common/errors.md；§0.1 前端错误处理框架层)
- (Ref: knowledge-base/security/global-rules.md)
- (Ref: knowledge-base/security/biometric-verification.md)
- (Ref: knowledge-base/kyc/account-opening.md)
- (Ref: knowledge-base/card/manage/pin.md)
- (Ref: knowledge-base/card/transaction-detail.md)
- (Ref: AIX 代码 packages/common/src/network/error/{AixError,ErrorCodes,ErrorObserver}.ts；src/network/ApiErrorUtils.ts；src/data/biometric/EnableBiometricRepo.ts)
- (Ref: knowledge-base/changelog/knowledge-gaps.md ALL-GAP-038 / ALL-GAP-043 / ALL-GAP-077)
