# Step 2 GLM 采集日志

> 用途：记录 Step 2 多 Agent 采集过程、Agent 贡献与收口决策。
> 采集链路：Advance Codex CLI → ARouter → glm-5.3-flash → xhigh
> 日期：2026-08-29

## 采集方式

通过 Advance Codex CLI 经 ARouter 调度 glm-5.3-flash（xhigh reasoning），启动 6 路独立 Agent 并行采集。

## 原始 Agent 任务

| Agent | Job ID | 任务 | 状态 |
|---|---|---|---|
| A | `job_01M16PXWJSSTC5RW5CE7BSV3SC` | Taxonomy | 开放式继续检索，Reviewer 取消 |
| B | `job_01M16PYCJ4BPAGF7W887ZXEW50` | Custodial players | 开放式继续检索，Reviewer 取消 |
| C | `job_01M16PYTN154B0ASE0KRHTM36Y` | Self-custody / credit | 开放式继续检索，Reviewer 取消 |
| D | `job_01M16PZBE42WGYYS03ZWA0F9WE` | Stablecoin accounts | 开放式继续检索，Reviewer 取消 |
| E | `job_01M16PZTSYVB5QC44W46KMMN22` | Region matrix | 开放式继续检索，Reviewer 取消 |
| F | `job_01M16Q08NR7C3CSSAQ12V5S5RH` | AIX facts | **完成**，落 `02-agent-f-aix-current-position.md` |

### 收口尝试

| 收口 Agent | Job ID | 结果 |
|---|---|---|
| AB 收口 | `job_01M16R0V5JT1VWM08K7H1EFH2Y` | 仍有继续展开检索倾向，取消 |
| CD 收口 | `job_01M16R1B2W28RFP027KYEW9HQ4` | 仍有继续展开检索倾向，取消 |
| E 收口 | `job_01M16R1YV8T828N01VXF0B349V` | 仍有继续展开检索倾向，取消 |

### 收口决策说明

1. **A–E Agent 做了大量官方网页/缓存采集**，但出现开放式继续检索、长时间不收口。Reviewer 在判断证据已饱和后主动取消。
2. **不能把 "running/cancelled" 当通过**。Agent 状态为 cancelled 不代表采集质量不达标，只代表 Reviewer 决定在证据饱和时停止继续投入。
3. 收口 AB/CD/E Agent 同样出现继续展开检索倾向，因此取消。
4. **关键结论来自已采集缓存 + Reviewer 独立 web 核验后写入 `02-sources`**。
5. 原始 logs 保留在 Advance runtime，**不作为长期事实源**。最终事实以 curated `02-sources.md` 为准。

## 关键 Agent 贡献

| 主题 | Agent 贡献 |
|---|---|
| **Bitget Wallet Card** | 发现 explicit eligibility（EEA+UK、LATAM、APAC、South Africa、Pakistan/Bangladesh）+ current Card Top-Up 流程，支持 S1 归类而非 S5 |
| **Gate** | 发现 Instant Spend + Prepaid 双模式并存，支持 Gate 跨 S1+S2 |
| **ether.fi** | 发现 Direct Pay vs Borrow Mode 的清晰机制区分，支持 ether.fi 跨 S4-adjacent + S6 |
| **KAST** | 发现 Global USD Account / Unified Balance / receive-send-spend 闭环，支持 KAST 作为 S3 最强代表 |
| **Gnosis Pay** | 发现 Safe / IBAN / card infra 文档，支持 Gnosis Pay S4 归类（同时注意 B2B infra 边界） |
| **AIX facts（Agent F）** | 发现 Card Balance vs Wallet Balance 分离、DTC 外部托管、Withdraw hidden、地区证据冲突等事实 |

## 最终事实来源

**以 `evidence/02-sources.md` 为准。** 本日志仅记录采集过程，不构成事实依据。
