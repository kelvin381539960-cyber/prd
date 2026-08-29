# Step 2 评审记录（GPT-5.6 Sol, xhigh）

> 评审链路：Advance Codex CLI → ARouter → GPT-5.6 Sol → xhigh
> 日期：2026-08-29
> 结果：Round 1 FAIL → 补证 → Round 2 PASS

## Round 1：FAIL（需要修正，不是全盘失败）

### P0-1 品牌出身偏差

- **问题**：Bitget Wallet 一开始容易被归 "self-custody direct spend"（S5），但 current 官方明确要求 **Card Top-Up / 独立卡余额**。
- **修正**：Bitget Wallet Card 当前主流程应归 **S1**（先充卡再花）， despite 入口是助记词/MPC 钱包。MetaMask 才是 S5 强样本。

### P0-2 Account vs Card

- **问题**：RedotPay 有 wallet/transfer 能力不等于 S3（Managed Global Account）。其 current 主支付机制是**托管 Crypto/Stablecoin 付款时自动换本地货币**。
- **修正**：RedotPay 主生态位应归 **S2**（Custodial Instant-convert Spend）。KAST 才有 Global USD Account + Unified Balance 的强 S3 证据。

### P1-1 Live vs Future

- **问题**：Karta Receive/Payments 官网标注 Coming Q3 2026；Plasma One 有 early-access/scaling 语义。
- **修正**：**future 不能当 current**。Karta 属于 S4 direction，但 receive/payout 部分标 future；Plasma One 标 emerging。

### P1-2 Region 映射

- **问题**：merchant acceptance / global / 100+ countries 不能映射到 card issuance eligibility。
- **修正**：Unknown 应保留；产品/region 模式可能不同；Step 2 只建立证据纪律，region matrix 留给 Step 4。

### P1-3 AIX 机制未确认

- **问题**：AIX Card Balance vs Wallet Balance 分离已确认，但 **Wallet → Card 机制未确认**，不能假装已知。
- **修正**：AIX 暂时接近 S1↔S3 边界，但最重要的下一事实问题是确认 funding/扣款机制与是否 Unified Balance。

## 补证（Round 1 → Round 2 之间）

| 补证对象 | 采集内容 |
|---|---|
| **Bitget current card/help** | current Card Top-Up、countries、fees；helpCenter 425 + 277 |
| **KAST global accounts** | Global USD Account / Unified Balance / receive-send-spend |
| **RedotPay services/restrictions** | wallet/assets/auto-convert/100+；card issuance restrictions |
| **MetaMask current card/help** | self-custody until payment + eligible countries |
| **OKX SG Pay** | smart wallet until pay、stablecoin direct spend、SG Visa |
| **ether.fi mode/country** | Direct Pay vs Borrow；available/restricted countries |
| **Plasma / Karta / Bleap** | current pages、early-access 标注、Coming Q3 2026 |

## Round 2：PASS

### 通过原因

1. **6 个物种均由 money residence + mechanism + account behavior 解释**：分类轴不是公司出身，而是消费前钱在哪里 + 购买力怎么形成 + 是否持续资金账户。
2. **非公司起源分类**：没有把 CEX/Wallet 品牌当分类维度。
3. **同品牌多 cell**：ether.fi、Nexo、Gate 等同一品牌跨多个生态位，被正确识别并分开机制。
4. **Region/infra 分层**：Region 和 Card infra 被正确降级为 constraint layer，不参与生态位分类。
5. **AIX Unknown 保留**：不硬归物种，funding/Unified Balance 机制保留为待验证。
6. **普通产品人员能 3 分钟理解**：S1–S6 命名直观，矩阵可读。

## 保留给后续 Step 的风险

1. **S3/S4 内部 "account maturity" 细分**：KAST vs OKX Pay vs Gnosis Pay 的账户成熟度不同，可在 Step 3 玩家研究中细分，但**不应在 Step 2 继续拆物种**。
2. **Wirex current consumer 模式**：需要继续查产品/地区级证据，当前只标 S2/S3 boundary。
3. **AIX 地区与 funding 机制**：Wallet → Card 扣款机制和 KYC/地区口径需核验；这是 Step 4 最重要的输入之一。
