# Step 2｜生态位地图

> 状态：Final / Reviewed（2026-08-29，经 Advance Codex CLI → ARouter → glm-5.3-flash → xhigh 多 Agent 采集 + GPT-5.6 Sol 独立评审，Round1 FAIL、补证后 Round2 PASS）
> 类型：阶段结论，供后续 Step 使用；不代表 AIX 最终战略决策。

## 核心结论

研究后自然收敛为 **6 个生态物种**。分类依据是 **消费前钱放在哪里（Value Residence）× 购买力如何形成（Purchasing-power Mechanism）× 产品是否是持续资金账户**，不是公司出身、CEX/Wallet 品牌标签，也不是 Card Rail。

---

## 一、最终两条 Solution Axes

### X 轴：Value residence immediately before purchase（消费前最后钱放在哪里）

| 位置 | 含义 |
|---|---|
| **1) Separate Card / Stored-value Balance** | 独立卡余额；用户先充值/预转换到卡余额，消费前钱在独立的 Stored-value 卡账户里 |
| **2) Custodial Crypto/App Balance** | 托管平台/交易所/支付 App 里的 Crypto 余额；消费前钱在中心化托管余额中 |
| **3) Managed USD/Stablecoin Global Account** | 由产品管理的统一 USD/Stablecoin 账户；用户把它当持续资金账户，不只是卡 |
| **4) Self-custody Onchain Wallet/Vault** | 用户控制的链上钱包/金库；消费前资产留在自托管环境 |

### Y 轴：Purchasing-power mechanism（购买力如何形成）

| 机制 | 含义 |
|---|---|
| **A) Manual pre-fund / pre-convert** | 先充值/换成卡余额，再消费 |
| **B) Instant sell/convert at payment** | 支付时平台自动卖出/换汇形成法币购买力 |
| **C) Stablecoin direct/equivalent deduction** | 稳定币直接或等价扣款 |
| **D) Collateral-backed borrowing/credit** | 抵押资产形成信用/借款购买力 |

### 明确排除项

- **Card / QR / Transfer 是 Rail**：只是消费/转账通道，不是生态位轴。
- **Region / Issuer / Network / Regulation 是 constraint layer**：限制可用性，不定义生态位。

---

## 二、6 个生态物种

### S1 `先充卡，再花` / Pre-funded Card Balance

- **人话定位**：用户已有 Crypto，但愿意先把资产转入/转换到独立卡余额再消费。
- **核心 Job**：J2（已有 Crypto 变成日常购买力）。
- **资金位置**：消费前钱在独立卡余额（X=1）。
- **机制**：Manual pre-fund / pre-convert（Y=A）。
- **代表产品**：
  - Crypto.com 传统预付卡模式
  - Gate Prepaid Mode
  - Bitget Wallet Card 当前主流程（尽管入口是助记词/MPC 钱包，当前官方仍要求 Card Top-Up / 可把钱包资产转入卡余额）
- **为什么存在**：Issuer 集成简单、风险边界清晰；代价是 Top-up 摩擦。

### S2 `Crypto余额直接刷` / Custodial Instant-convert Spend

- **人话定位**：Crypto 放在托管 App / 交易所里，付款时平台自动兑换成法币，用户无需提前出金。
- **核心 Job**：J2。
- **资金位置**：消费前钱在托管 App/交易所余额（X=2）。
- **机制**：Instant sell/convert at payment（Y=B）。
- **代表产品**：
  - RedotPay（官方支持 BTC/ETH/BNB/SOL 等 + USDT/USDC，付款时自动换成本地货币；主生态位是 S2，不因有 Wallet/Transfer 能力归 S3）
  - Bybit Card
  - Gate Instant Spend
  - Wirex 部分产品模式（边界样本，需继续验证）
- **为什么存在**：用户不想提前把钱锁定到卡余额，希望托管余额随时可花可投资。

### S3 `Stablecoin版全球账户` / Managed Stablecoin Global Account

- **人话定位**：用户把产品当稳定美元/全球资金账户，持续 receive/hold/send/spend，而不只是一张卡。
- **核心 Job**：J1（获得并持续使用稳定可跨境的钱）。
- **资金位置**：Managed 统一余额（X=3）。
- **机制**：Stablecoin direct/equivalent deduction（Y=C）。
- **代表产品**：
  - **KAST（最强代表）**：Global USD Account、Unified Balance、ACH/SWIFT（如页面标 Coming Soon 则为 future）、Stablecoin/Crypto 入金、send local fiat/stablecoins、card spend
  - RedotPay 虽有 wallet + international transfer，但现有证据不足以把它主定位为 S3
- **为什么存在**：跨境用户需要的不只是消费，而是"一个当美元用的账户"。

### S4 `自托管版全球账户` / Self-custody Stablecoin Money Account

- **人话定位**：用户既要稳定币全球资金能力，又不想把资产长期交给中心化平台。
- **核心 Job**：J1。
- **资金位置**：Self-custody wallet/vault（X=4）。
- **机制**：Stablecoin direct/equivalent deduction（Y=C）。
- **代表产品**：
  - OKX Pay + Card（SG 明确 smart wallet 资金保持到付款）
  - Bleap（non-custodial stablecoin payment app）
  - Plasma One（self-custody stablecoin money app；early-access / scaling status 需标注）
  - MiniPay
  - Gnosis Pay
  - Karta（属于此方向，但其 receive/payout 部分官网显示 Coming Q3 2026，不能把 future 当 live）
  - ether.fi Direct Pay（自托管稳定币直接消费，但并非完整全球账户，属邻接模式）
- **为什么存在**：中心化托管和 DeFi 之间的折中——自托管但接近银行体验。

### S5 `钱包里的币直接刷` / Self-custody Crypto Instant Spend

- **人话定位**：已有 onchain 资产的用户，不想先搬到中心化平台或独立卡余额；资产留在自托管钱包直到支付，再在 POS 形成法币购买力。
- **核心 Job**：J2。
- **资金位置**：Self-custody onchain wallet（X=4）。
- **机制**：Instant sell/convert at payment（Y=B）。
- **代表产品**：
  - MetaMask Card（强样本：资产自托管直到支付）
- **与 S1 的区别**：Bitget Wallet Card 当前官方主流程要求 Card Top-Up / 独立卡余额 → 归 S1；MetaMask 资产不搬出钱包 → 归 S5。
- **为什么存在**：DeFi-native 用户希望保留钱包控制权，同时获得日常消费能力。

### S6 `不卖币，也能花` / Crypto-backed Credit Spend

- **人话定位**：Crypto holder 希望保留资产敞口，以资产作抵押借款/信用来消费。
- **核心 Job**：J3（不卖 Crypto、保持敞口获得消费流动性）。
- **资金位置**：取决于具体产品（托管或自托管抵押池）。
- **机制**：Collateral-backed borrowing/credit（Y=D）。
- **代表产品**：
  - ether.fi Borrow Mode
  - Nexo Credit Mode
- **同品牌跨生态位示例**：
  - ether.fi：Direct Pay = S4 邻接；Borrow = S6。两种机制不同，不合并。
  - Nexo：Debit 模式 = S2-like；Credit 模式 = S6。Debit 和 Credit 不应合并成一个机制。
- **为什么存在**：对持有大量 Crypto 的用户，卖出意味着放弃上涨预期和税务事件；抵押借款保留敞口。

---

## 三、X × Y 矩阵

> 4 列 × 4 行。一个 cell 可含多个品牌；空 cell 是正常的，不为了对称硬填。

```
                                    Purchasing-power mechanism
                    A) Manual        B) Instant       C) Stablecoin     D) Collateral
                    pre-fund         convert          direct/equiv      credit
                    ─────────────    ─────────────    ─────────────     ─────────────
X=1 Separate       S1: Crypto.com,  ─                ─                 ─
    Card Balance      Gate Prepaid,
                      Bitget Wallet
                      Card (current)

X=2 Custodial      ─                S2: RedotPay,    ─                 S6: Nexo Credit
    Crypto/App                        Bybit Card,                        (托管抵押)
    Balance                           Gate Instant,
                                      Wirex (boundary)

X=3 Managed        ─                ─                S3: KAST          ─
    USD/Stablecoin
    Global Account

X=4 Self-custody   ─                S5: MetaMask     S4: OKX Pay/Card  S6: ether.fi
    Wallet/Vault                                     (SG), Bleap,       Borrow
                                                     Plasma One,
                                                     MiniPay,
                                                     Gnosis Pay,
                                                     Karta (direction),
                                                     ether.fi Direct Pay
                                                     (adjacent)
```

### 矩阵读法

- **每一行**回答"消费前钱放在哪里"。
- **每一列**回答"购买力怎么形成"。
- **每个 cell**就是一个生态物种（S1–S6）。
- **同一品牌可跨多个 cell**（如 ether.fi、Nexo、Gate），这是正常现象。

---

## 四、玩家落位表

| 玩家 | 生态位 | 关键区分 |
|---|---|---|
| **RedotPay** | **S2** (primary) | 托管 Crypto 付款时自动换法币；有 Wallet/Transfer 但不足以归 S3 |
| **KAST** | **S3** | Global USD Account + Unified Balance + receive/send/spend 闭环 |
| **Bybit Card** | **S2** | 交易所托管余额 + 支付时自动转换 |
| **Bitget Wallet Card** | **S1** | Self-custody source，但当前官方要求 Card Top-Up → 独立卡余额 |
| **Gate** | **S1 + S2** | Prepaid Mode = S1；Instant Spend = S2 |
| **Crypto.com** | **S1** | 传统预付卡模式（先充值） |
| **OKX Pay/Card** | **S4** | SG smart wallet 资金保持到付款；region-specific programs |
| **MetaMask Card** | **S5** | Self-custody until payment；钱包里的币直接刷 |
| **ether.fi** | **S4-adjacent (Direct Pay) + S6 (Borrow)** | 两种机制分开，不合并 |
| **Nexo** | **S2-like (Debit) + S6 (Credit)** | Debit 和 Credit 是不同机制，不合并 |
| **Bleap** | **S4** | Non-custodial stablecoin payment app |
| **Plasma One** | **S4 (emerging)** | Self-custody stablecoin money app；early-access/scaling 需标注 |
| **Karta** | **S4 (direction)** | Self-custody 方向明确；receive/payout 部分 Coming Q3 2026，不能当 live |
| **MiniPay** | **S4** | Self-custody stablecoin |
| **Gnosis Pay** | **S4** | Self-custody Safe / IBAN / card infra；同时是 B2B infra |
| **Wirex** | **S2/S3 boundary** | 需产品/地区级继续验证，不强塞 |

---

## 五、Region Constraint

主文只写原则和高置信例子，不把 Unknown 填满。Region matrix 作为 Step 4 竞争分类的唯一地区依据；Step 2 只建立证据纪律。

### 原则

1. **App availability ≠ Card issuance eligibility**：产品可在某国下载，不等于可以在该国开卡。
2. **Merchant acceptance ≠ issuance eligibility**：卡在多少商户可用，不等于哪些国家可发行。
3. **"100+ countries" / "200+ countries" ≠ issuance eligibility country list**：需逐国核验。
4. **同品牌不同 region/mode 可能不同**：不能把一个地区的资格推广到全产品线。
5. **Unknown 不补**：没有确凿证据就不写具体国家。

### 高置信例子

- **Bitget Wallet Card**：current official list 明确 EEA+UK、LATAM 多国、APAC 多国、South Africa、Pakistan/Bangladesh（不同帮助页版本有细微差异，竞争阶段需按日期复核）。
- **MetaMask Card**：current help 明确多个 LATAM、EEA/UK、Canada、US 等；current page 与 2026-06 "US signup paused" 历史公告存在时间演进，使用最新 help 作为 current，历史公告保留时间线。
- **RedotPay**：Card Issuance Restrictions current list 明确 US、Singapore、Indonesia、India、Türkiye、Morocco、mainland China 等不可开卡；不能从 "100+ countries" 倒推某个国家可开。
- **ether.fi**：有详细 current supported/restricted lists，但帮助页之间存在局部冲突（如个别国家）；Competition Step 必须按最新产品资格页复核。
- **KAST**："200+ countries transfer / 150M merchant acceptance" 不能当作 Card issuance eligibility country list；具体地区未证实则 Unknown。

---

## 六、AIX 当前落位

> 依据：仅使用 `evidence/02-agent-f-aix-current-position.md`（repo evidence，非外部事实）。

### Fact（当前已确认）

- AIX 当前已确认稳定币资产：**USDC / USDT / WUSD / FDUSD**。
- 账户由外部 **DTC account/sub-account** 管理，**非 self-custody**。
- **Card Balance 与 Wallet Balance 分离**。
- **无已确认 volatile crypto 余额产品**。
- **Withdraw unsupported/hidden**。
- Send/Swap runtime 仍需核验。
- AIX 地区证据版本冲突。

### Inference / Decision

**AIX 目前不能硬归一个物种。**

基于 "Card Balance 与 Wallet Balance 分离"，暂时更接近 **S1 ↔ S3 边界**：

- 如果消费前必须 Wallet → Card 预充值 → **更接近 S1**（先充卡再花）。
- 如果 Phase 2 / 目标能力做到统一 Stablecoin 余额直接消费 + receive/send/spend 闭环 → **更接近 S3**（管理式 Stablecoin 全球账户）。

**明确不属于 S4/S5**（非 self-custody），也无 S6 证据。

### 最重要的下一事实问题

确认 **Wallet → Card funding/扣款机制** 与 **是否 Unified Balance**。

---

## 七、Step 2 结论

1. **市场主分化不是 "交易所 vs 钱包公司"**，而是 `消费前钱在哪里 × 消费购买力如何形成 × 产品是否是持续资金账户`。
2. **Card network 是 rail，不是定位**："Visa/Mastercard + crypto card" 不足以定义直接竞品。
3. **同一品牌跨多个 cell 是正常现象**（ether.fi、Nexo、Gate 等）。
4. **AIX 真正的战略岔路是 S1（卡消费桥）→ S3（管理式 Stablecoin 全球账户）**，不是简单"多做几个 Card 功能"。这里只是生态位结论，不在 Step 2 决定战略。
