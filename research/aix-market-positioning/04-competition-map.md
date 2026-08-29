# Step 4｜市场竞争结构：谁在争夺同一类用户？

> 日期：2026-08-30
> 市场边界：**consumer crypto/stablecoin → real-world purchasing power**
> 方法：本步骤研究市场竞争结构，不以 AIX 当前地区、资产、Card Balance、现有功能或架构作为市场锚点；AIX 的目标位置留到 Step 5。

## 1. 结论先说

这个市场**不是 Crypto Card 市场**。Card 只是把 Crypto / Stablecoin 变成现实购买力的一种 Spend Rail。真实竞争发生在三个 User Job 战场：

| 战场 | 用户真正要解决的问题 | 代表玩家 / mode | 当前判断 |
|---|---|---|---|
| **J1 Global Money** | 我要一种稳定、跨境、能收 / 存 / 转 / 花的钱 | KAST、Plasma One、Bleap、OKX SG、Karta | 已有成熟样本，但逐国覆盖证据不完整，竞争密度 **Unknown** |
| **J2 Crypto → Spend** | 我已经有 Crypto / Stablecoin，怎样最方便变成现实购买力 | RedotPay、Bitget、Bybit、Crypto.com、MetaMask、ether.fi Direct、Bleap、OKX、Gnosis Pay 等 | **当前样本最拥挤**，机制和 rail 最多 |
| **J3 Keep Crypto → Liquidity** | 我不想卖 Crypto，但需要可消费流动性 | Nexo Credit、ether.fi Borrow、RedotPay Credit；Ledn / YouHodler 邻接 | 独立的抵押信贷战场 |

最重要的竞争规律是：

> **用户买的是 Job 和结果，不是底层架构。**

因此 Custodial / self-custody、预充值 / 即时换币、Card / QR 即使机制不同，也可能直接争夺同一个用户。

---

## 2. 竞争关系怎么判

### 2.1 Confirmed Direct 的四个硬条件

必须同时满足：

1. **Same current market / region**：用户当下能真实获得两个产品；
2. **Same core Job**：用户雇佣两者解决的是同一个核心任务；
3. **Overlapping starting money pool**：用户做选择前手里的钱相同或明显重叠；
4. **Substitutable real-world purchasing-power outcome**：在目标场景下，最终购买力可以互相替代。

**Direct 不要求 same X、same Y、same custody、same rail。**
X / Y / custody / rail 是差异化变量，不是市场边界。

### 2.2 四类竞争关系

- **Confirmed Direct**：四项全部 Confirmed，用户可以真实二选一。
- **Conditional Direct**：用户层逻辑成立，但 region / eligibility / starting-pool 等仍有关键 Unknown；补证后可能升级。
- **Adjacent**：用户或资金池高度重叠，但 core Job 或最终结果不同，不能完整替代。
- **Rail Substitute**：同 Job、同资金起点和高阶购买力目标，但 rail / merchant coverage / use case 不同；覆盖重合时可形成场景级 Direct。

证据纪律：

- **Unknown ≠ No**
- **merchant acceptance ≠ issuance / service eligibility**
- **future / waitlist / coming soon ≠ current**
- **样本中未出现 ≠ 市场不存在**

---

## 3. J2：当前最拥挤的主战场

J2 的共同用户不是“想办一张 Crypto Card 的人”，而是：

> **已经持有 Crypto（Stablecoin 也属于 Crypto），希望低摩擦获得现实购买力的人。**

当前已经观察到四类策略：

| 策略 | 代表玩家 / mode | 用户感知 |
|---|---|---|
| 托管余额，消费时自动换币 | RedotPay、Bybit | 把 Crypto 放进去，支付时自动处理 |
| 先充值 / 预转换，再消费 | Bitget、Crypto.com、Karta | 先准备消费余额，再支付 |
| Self-custody / wallet-native 直接消费 | MetaMask、ether.fi Direct、Bleap、OKX SG、Gnosis Pay、Plasma One | 资产尽量留在自己的 wallet，支付时再扣 |
| Money Account + Spend | KAST、Plasma One、Bleap | 不只消费，而是把 Stablecoin 当日常钱使用 |

玩家证据主要来自：
- [J2 custodial / prefund evidence](evidence/04-agent-b-custodial-exchange-prefunded-card.md)
- [J2 self-custody evidence](evidence/04-agent-c-self-custody-wallet-native-evidence-card.md)

### 3.1 机制不同，仍然可以是直接竞争

一个已经有 USDT / USDC 的菲律宾用户，要解决“今天就能拿这笔钱日常刷卡”的 J2：

- **RedotPay**：X2 × B，消费时转换；
- **Bitget Wallet Card**：Y=A confirmed、X Unknown，top-up 后消费；
- **ether.fi Direct Pay**：X3 × C candidate，Vault stablecoin 支撑支付。

现有 current evidence 支持三者在 **PH stablecoin-starting J2 card spend** 这个具体 segment 上满足 four-AND，因此：

> **RedotPay ↔ Bitget Wallet Card ↔ ether.fi Direct Pay = player-to-player Confirmed Direct set。**

这个例子说明：即使三者的 X / Y / custody 不同，用户仍可能真实二选一。

其他已观察到的 market overlap 包括 AU 的 Bitget / ether.fi、SG 的 Bitget / OKX SG、MX / BR 的 MetaMask / Bleap；具体 pair 仍须按 segment、starting asset 与逐国 eligibility 判断。

### 3.2 竞争密度

当前 market-level 样本中，PH、AU、SG、MX/BR，以及聚合口径的 EEA+UK 都已经观察到 **≥3 个 J2 providers**。这是样本下限，不是完整市场规模；EEA+UK 也不是精确的逐国密度。

因此 J2 的真正问题不是“要不要做 Crypto Card”，而是：

> **面对同一个已经持币、想把币变成现实购买力的用户，凭什么让用户选你的机制、rail 和体验。**

区域证据见：
- [Regional maturity / density evidence](evidence/04-agent-e-regional-maturity-density.md)

---

## 4. J1：争的是“钱的主账户心智”

J1 用户要的不是单一消费入口，而是：

> **稳定、跨境、能持续收 / 存 / 转 / 花的钱。**

### 4.1 当前最强 Money Account 样本：KAST

现有证据中，KAST 的 Money Account 结构最完整：

- Global Account；
- US account / EU IBAN；
- ACH / SEPA / SWIFT / Fedwire；
- receive / send / spend；
- `Unified Balance — Spend, send, and receive from one account`。

但 KAST Card 的购买力机制存在官方 **Source Conflict**：同一时期官方资料同时出现“从余额直接扣”和“secured credit line”口径。因此当前只确认：

- **X2 confirmed**
- **Y Unknown**
- **Strategy Cluster Unknown**

不能静默裁决。这个冲突不影响其 Money Account 角色。

其他方向：

- **Plasma One / Bleap**：Money Account-leaning；
- **Karta**：current top-up/spend 已明确，但 receive / payouts / bank rails 部分仍是 future；
- **OKX Pay/Card SG**：区域型 stablecoin wallet + pay/card 样本，目前更适合 Account-adjacent 描述。

因为逐国 eligibility 证据仍不完整，J1 当前竞争密度应写 **Unknown**，不能写 Low，也不能据此判断“蓝海”。

J1 证据见：
- [J1 Global Money evidence](evidence/04-agent-a-j1-global-money-card.md)

---

## 5. J3：独立的 No-sell Liquidity 战场

J3 的核心 Job 是：

> **我不想卖掉 Crypto，但希望拿到可消费流动性。**

当前主要样本：

- **Nexo Credit**：X2 × D / S6-Custodial；
- **ether.fi Borrow**：X3 candidate × D / S6-Onchain candidate；
- **RedotPay Credit**：current live collateral-credit sample；
- **Ledn / YouHodler**：更接近 borrow-to-cash，解决相同上层流动性问题，但缺直接 spend rail，因此归 Adjacent。

J2 与 J3 最终都可能产生消费，但 core Job 不同：

- J2 接受花掉 / 转换资产；
- J3 的硬要求是不卖资产、保留资产敞口。

因此不能把 J2 / J3 合并为同一个 Direct pool。

J3 证据见：
- [Credit / borrow-to-spend evidence](evidence/04-agent-d-credit-borrow-to-spend-evidence-card.md)

---

## 6. Card 只是 Rail：非卡路径也在抢现实购买力

只研究 Card 会漏掉真实竞争。当前已确认的 Non-card Rail 至少包括：

| Rail | 代表证据 | 作用 |
|---|---|---|
| **Direct QR / merchant pay** | Coins.ph QRPH Stablecoin Payments | 扫 QR Ph，直接用 crypto/stablecoin 或 PHP+crypto mix 完成支付 |
| **Two-step e-wallet** | GCash GCrypto、Maya | crypto → PHP/e-wallet balance → QR / bills / load |
| **Gift / prepaid / top-up** | Bitrefill | crypto → voucher / top-up / eSIM → 本地购买力 |
| **Merchant-side crypto rail** | Solana Pay、OpenNode | 商户侧接收链上 / Lightning / stablecoin 类支付 |
| **Bank / remittance cash-out** | InstaPay、PESONet、remittance rails | crypto/平台余额 → 本地银行/现金体系 |
| **P2P / OTC** | NoOnes 等 | 通过 bank/mobile wallet/gift card 等对手方换成可用资金 |

### 6.1 当前最强的 Non-card 直接支付证据

Coins.ph 官方 Help Center 的 **QRPH Stablecoin Payments**（2026-08-09）证明：用户可以扫描 QR Ph，用 crypto/stablecoin，或 PHP + crypto 混合方式支付。这是当前样本里最清晰的 **direct-at-merchant non-card** 路径。

GCash GCrypto 和 Maya 则不同：当前证据指向：

> **crypto → PHP/e-wallet balance → QR / bills / load**

这是 two-step 路径，不能写成 direct stablecoin merchant payment。

Bitrefill 提供 voucher / top-up / eSIM bridge，但实时 PH 页面被 Cloudflare 阻断，因此具体 PH catalog 保持 Partial / Unknown。

Solana Pay / OpenNode 代表 merchant-side rails。Solana Pay 的 Shopify 状态存在 **Source Conflict**：Solana 侧资料描述 integration，而当前 Shopify App Store 页面显示 unavailable，不能单边裁决。

BSP 的 digital-payment 数据只能证明本地数字支付 rail 已成熟，**不能推导 stablecoin-specific spend volume**；该体量仍为 Unknown。

因此：

> **Card 与 QR / e-wallet 可以是 Rail Substitute；只有在具体 market + merchant/use-case coverage 重合时，才升级成场景级 Direct。**

Non-card 证据见：
- [Non-card substitute rails evidence](evidence/04-agent-g2-non-card-substitute-rails-evidence-card.md)

---

## 7. Region 本身就是竞争结构

市场高度碎片化，不存在一个“全球竞品榜单”。逐国 eligibility 会直接改变谁和谁竞争。

当前证据要求保持三条纪律：

1. `150M merchants`、`180+ countries` 等 acceptance 不能推导开户 / 发卡 eligibility；
2. EEA+UK 聚合口径不能当作每个欧洲国家的精确竞争密度；
3. 当前样本里玩家少，不等于该市场没有其他玩家。

所以竞争地图必须理解成：

> **Job × Starting Money × Region × Purchasing-power Outcome**

而不是一张脱离地区的公司排名表。

---

## 8. 真正决定胜负的变量

进入同一用户竞争池之后，玩家主要在这些维度竞争：

1. **Job depth**：Spend Feature / Money Account / Credit；
2. **Starting asset breadth**：Stablecoin-only vs BTC/ETH 等广义 Crypto；
3. **Custody / control**：托管 vs self-custody；
4. **Purchasing-power mechanism**：预充值、即时转换、稳定币直扣、抵押借款；
5. **Rail breadth**：Card、QR、bank/e-wallet、gift/prepaid、P2P 是否组合；
6. **Region eligibility**：用户实际能否获得产品；
7. **Cost**：issuance、FX、top-up、ATM、conversion、interest；
8. **Experience**：是否需预操作、支付成功率、到账速度、KYC 摩擦；
9. **Trust / risk**：custody、issuer、regulatory wrapper、credit/liquidation risk；
10. **Rewards / Yield**：是否显著降低用户净成本或增加留存。

这些变量决定“为什么用户选我”，而不是决定“是不是同一个市场”。

---

## 9. 市场竞争图

```text
                    consumer crypto/stablecoin
                              │
                  → real-world purchasing power
                              │
           ┌──────────────────┼──────────────────┐
           │                  │                  │
           ▼                  ▼                  ▼
      J1 Global Money     J2 Crypto → Spend    J3 Keep Crypto
       钱本身更好用         已有币变购买力        不卖币拿流动性
           │                  │                  │
 KAST / Plasma / Bleap   custodial / prefund   Nexo Credit
 Karta / OKX ...         / self-custody ...     ether.fi Borrow
                                                RedotPay Credit
           └──────────────────┼──────────────────┘
                              │
                         Spend Rail Layer
                              │
          Card / QR / Bank-Ewallet / Gift-Prepaid / Merchant / P2P
```

**竞争发生在 Job × Starting Money × Region × Purchasing-power Outcome 的交叉点；产品技术路线是交叉点里的竞争手段。**

---

## 10. 给 Step 5 的输入，但不替 Step 5 做决定

Step 5 应按以下顺序选择目标：

> **Job → Region → Starting Money Pool → Product Role → Rail Portfolio → X/Y/Custody**

目标态确定后，才把**目标 AIX**与**当前 Implementation Baseline**做 Gap Analysis。

Step 4 到此只回答市场竞争结构，**不回答 AIX 应该选哪个方向。**
