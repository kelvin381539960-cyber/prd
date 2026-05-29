---
module: security
feature: otp-verification
version: "1.2"
status: active
source_doc: archive/legacy-prd/security/identity-verification/README.md；archive/legacy-prd/app/registration-login/README.md
source_section: OTP / Email OTP / Mobile OTP / IVS session verification
last_updated: 2026-05-28
owner: 吴忆锋
readers: [product, ui, dev, qa, business, ai]
tags: [security, otp, email-otp, mobile-otp, ivs]
---

# OTP Verification OTP 验证

> Code alignment note: 2026-05-28 按 AIX 前端代码 `src/data/ivs/IvsData.ts`、`src/data/ivs/IvsRepo.ts`、`src/data/ivs/OtpData.ts`、`src/services/ivs/IvsFlowStarter.ts` 补充运行时可确认事实。本次只写入代码可直接证明的 IVS session/challenge 结构、OTP legacy 接口、session 化 invoke/verify 接口、OTP 返回字段和 challenge 路由；不补充代码无法确认的频控、锁定时长、验证码有效期、每日次数或攻击防护策略。

## 0.1 代码可确认的运行时事实补充（2026-05-28）

以下内容来自 AIX 当前代码实现，仅作为运行时事实补充；若与历史 PRD 描述存在差异，以当前代码和后端业务事实复核为准。

### 0.1.1 IVS challenge 类型

代码可确认 `IvsChallengeType` 包含：

- `CURRENT_LOGIN_PASSWORD`
- `otp`
- `capturingLiveness`
- `biometric`

同时，IVS 路由分发中按大写 challenge type 处理以下运行时类型：

- `EMAIL_OTP`
- `MOBILE_OTP`
- `CURRENT_LOGIN_PASSWORD`
- `DTC_FACE`
- `BIOMETRIC`

注意：`otp` 与 `EMAIL_OTP` / `MOBILE_OTP` 的关系不能仅从当前前端代码推导为完全等价。

### 0.1.2 IVS session 结构

代码可确认 `IvsAuthSession` 包含：

- `sessionId`
- `scenario`，可选。
- `allStagesCompleted`，可选。
- `nextStage`，可选。
- `notAvailableInfo`，可选，包含 `cta`。

`nextStage` 包含：

- `stageId`
- `options`

每个 `IvsChallengeOption` 包含：

- `challengeId`
- `challengeType`
- `priority`，可选。
- `extra`，可选。

`extra` 当前可确认字段为：

- `deliveryTarget`，注释标识可能为 email、sms、phone。

### 0.1.3 IVS verify 入参

代码可确认 `IvsVerifyParams` 包含：

- `sessionId`
- `stageId`
- `challengeId`
- `credential`

`credential` 可包含：

- `otpCode`
- `password`
- `signature`
- `timestamp`

### 0.1.4 OTP 返回结构

代码可确认 `OtpData` 包含：

- `otpSessionId`
- `remainTimes`，可选。
- `resendTime`，可选。

当前代码只能确认字段存在，不能确认 `remainTimes` 的业务含义、`resendTime` 的单位、验证码有效期、每日次数或锁定时长。

### 0.1.5 Email OTP legacy 接口

代码可确认 Email OTP legacy 接口包括：

- `sendEmailOtp(email, sessionId)`
  - 当 `sessionId` 为空时，请求 `Urls.emailOtpFirst`，参数为 `email`。
  - 当 `sessionId` 存在时，请求 `Urls.emailOtp`，参数为 `otpSessionId`。
- `verifyEmailOtp(sessionId, otpCode)`
  - 请求 `Urls.emialVerify`。
  - 参数为 `otpSessionId`、`otpCode`。

### 0.1.6 Phone OTP legacy 接口

代码可确认 Phone OTP legacy 接口包括：

- `sendPhoneOtp(phone, areaCode, otpSessionId)`
  - 当 `otpSessionId` 为空时，请求 `Urls.phoneOtpFirst`，参数为 `mobile`、`areaCode`。
  - 当 `otpSessionId` 存在时，请求 `Urls.phoneOtp`，参数为 `otpSessionId`。
- `verifyPhoneOtp(otpSessionId, otpCode, countryCode)`
  - 请求 `Urls.phoneVerify`。
  - 参数为 `otpSessionId`、`otpCode`、`countryCode`。

### 0.1.7 Session 化 IVS 接口

代码可确认 session 化 IVS 接口包括：

- `invoke(sessionId, stageId, challengeId, extra)`
  - 请求 `Urls.ivsInvoke`。
  - 参数为 `sessionId`、`stageId`、`challengeId`、`extra`。
- `verify(session)`
  - 请求 `Urls.ivsVerify`。
  - 参数为完整 `IvsVerifyParams`。

### 0.1.8 IVS challenge 路由分发

代码可确认 `gotoIvsNextStep(session)` 会遍历 `session.nextStage.options`，并按 challenge type 路由到对应页面：

| challengeType | 跳转页面 |
|---|---|
| `EMAIL_OTP` | `IvsEmailOtpPage` |
| `MOBILE_OTP` | `IvsPhoneOtpPage` |
| `CURRENT_LOGIN_PASSWORD` | `IvsPwdPage` |
| `DTC_FACE` | `IvsLivenessPage` |
| `BIOMETRIC` | `IvsBiometricPage`，以 modal 方式打开。 |

如果 `nextStage.options` 不存在，前端会清理当前 IVS session 并返回未处理。

### 0.1.9 Biometric 不可用时的处理

代码可确认：启动 IVS 流程时会检查设备 biometric 可用性。如果 biometric 不可用且 `nextStage.options` 存在，前端会过滤掉 challenge type 为 `BIOMETRIC` 的选项。

### 0.1.10 不从代码推导的内容

以下内容本次不从代码补充：

- OTP 每日最多发送或验证次数。
- OTP resend 倒计时具体秒数。
- `remainTimes` 的具体业务含义。
- 验证码有效期。
- 错误次数后的锁定时长。
- OTP 攻击防护、IP / 设备 / 邮箱 / 手机号维度频控。
- Email OTP 与 Phone OTP 在所有场景下是否都开放。
- IVS challenge 的最终优先级策略。
- `otp` 与 `EMAIL_OTP` / `MOBILE_OTP` 是否完全等价。
- 账户级锁定、场景级锁定或 CTA 展示的完整规则。

## 1. 文档定位

本文件维护 AIX 中 OTP / Email OTP / Mobile OTP 与 IVS 验证相关的运行时事实、接口边界和客服回答限制。

## 2. 客服回答原则

- 可以说明系统支持邮箱 OTP、手机 OTP，以及 IVS session 化验证流程。
- 可以说明验证码接口返回可能包含 `otpSessionId`、`remainTimes`、`resendTime`。
- 不得承诺具体验证码有效期、每日次数、锁定时长或风控策略，除非后端配置或产品确认文档明确给出。
- 遇到用户反馈收不到验证码、验证码错误、次数用尽或安全验证不可用，应按当前客服流程收集账号、场景、时间、邮箱/手机号、设备和错误截图，再转人工或技术排查。

## 3. Sources

- AIX frontend: `src/data/ivs/IvsData.ts`
- AIX frontend: `src/data/ivs/IvsRepo.ts`
- AIX frontend: `src/data/ivs/OtpData.ts`
- AIX frontend: `src/services/ivs/IvsFlowStarter.ts`
