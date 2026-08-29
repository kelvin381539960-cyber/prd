# Step 1：市场大盘与用户 Jobs（已确认结论）

> 状态：Completed（2026-08-29，经 Advance Codex CLI → ARouter → grok-4.6 → xhigh 两轮评审，Round1 FAIL、修正后 Round2 PASS）
> 类型：阶段结论草稿，供后续 Step 使用；不代表 AIX 最终战略结论。

## 1. 市场边界

- 市场定义：**consumer crypto / stablecoin → real-world purchasing power**（消费者把 Crypto/Stablecoin 转化为现实世界购买力）。
- 不是 Crypto Card 市场，也不是整个 Crypto Fintech。Card 只是其中的 Spend Rail 之一。

### 纳入 / 排除

**纳入：**
- Stablecoin 形成 / 保持现实购买力。
- 已有 Crypto 卖出 / 兑换后消费。
- 不卖 Crypto、通过资产支持形成消费流动性。
- Card / QR / Transfer / P2P 等最终 rail。

**排除：**
- 纯交易（exchanges / DEX 内部交易）。
- 纯 Earn / Yield / Staking。
- 内部搬币（wallet 间与自己账户互转）。
- B2B settlement。
- 仅投资持币（无消费意图）。
- fiat-native neobank（仅作替代参照，不算本市场玩家）。

**边界说明：** 收 / 存 / 转仅在「形成或使用现实购买力旅程」时纳入；单独收、存、转不计入。

## 2. 市场规模三层（不给单一 TAM）

| 层级 | 口径 | 数值 | 说明 |
|---|---|---|---|
| L1 | 真实 stablecoin payments | ≈ $390B run-rate（2025-12 月活动年化） | 含大量 B2B，不是纯消费者市场 |
| L2 | Consumer-related flow | C2C $77B + C2B $76B ≈ $153B run-rate | 只能称“消费者相关资金流”，不是 Consumer Spend / TAM |
| L3 | Stablecoin-linked card spend | 2025 约 $4.5B（McKinsey/Artemis）、Visa 约 $5.2B；2026-07 a16z 引 Paymentscan 约 $759M/月、同比约 2.5x、近 9M 笔 | 从非常小的基数高速增长 |

### 必须分列的 Paymentscan 口径

- Paymentscan 另有约 **$1.038B headline** 与约 **$642M pure-on-chain view**；它们与 $759M 快照存在统计口径和/或时间点差异，具体差异需以对应 Paymentscan 原始页面定义为准，引用时必须分列，不得混用。

### 不进入总盘的品牌数据

- **RedotPay >$14B annualized payment volume**（含 topups / card spends）为品牌口径，不进总盘。

### 允许 / 不允许的结论

- 允许：card rail 真实使用量明确；从小基数、高速增长；相对全球传统卡支付总量仍然很小。
- 不允许：把整个市场写成“PMF 已验证”。

## 3. 市场为何存在：两个 Friction（解释性，不是生态位轴）

1. **Money Friction**（传统货币/跨境/支付体系的摩擦）。
2. **Crypto Asset Friction**（已有 Crypto 难以低摩擦转换为现实购买力）。

两者可重叠；它们解释市场存在，但**不做 Step 2 生态位轴**。

## 4. 三个 Job Family

- **J1**：获得并持续使用一种稳定、可跨境的钱。
- **J2**：已持有 Crypto 且愿意卖/换一部分，低摩擦变成日常购买力。
- **J3**：不卖 Crypto、保持敞口的同时获得消费流动性。

### 分层映射

- **Cross-border income / remittance**：J1 资金进入场景。
- **Exchange / Custody / Self-custody**：资金初始位置。
- **Collateral / Credit / Borrow**：机制。
- **Card / QR / Transfer / P2P**：rail。
- **订阅 / 电商 / Travel / Grocery / Ride-hailing**：消费场景。

### J3 说明

- J3 后续若只是 J2 的约束 segment（仅“不想卖 Crypto”这一约束），可合并进 J2；Step 2 再验证。

## 5. 区域降级（不写 Region × Job）

- 现有证据只支持 **Crypto activity / adoption** 和宏观背景。
- **不得写** “LATAM = J1”、“North America = J2/J3” 这类结论。
- 区域 = 事实背景 + 待验证假设，**不做 Step 2 主轴**。

## 6. Card 基础设施（降级后的确认范围）

- 只确认：2024–2026 card spend 重新增长；Visa / Mastercard / Bridge 扩覆盖、模式、settlement；多种机制并存。
- “Card 商品化”**降级为待验证假设**，后续按 Issuer / BIN / Acceptance / Fees / Stability 实证。

## 7. Step 2 验收标准

对每个玩家分别证明：
1. 服务哪个 Job；
2. 钱在哪里（资金初始位置 / 旅程）；
3. 购买力怎么产生；
4. Spend Rail 是什么；
5. 实际可服务地区是否与 AIX 重合。

- 同一玩家可服务多个 Job；**禁止把 Job 直接变成品牌桶**。

## 8. AIX 当前定位：只保留待验证问题

- 核心更接近“把已有 Crypto 低摩擦用于现实消费”，还是“以 Stablecoin/Crypto 为底层的全球资金账户”，或二者有明确主次？
- Step 1 **不下最终战略结论**，留待 Step 5 / Final。

## 9. 本阶段已确认结论清单（供后续引用）

1. 市场边界 = consumer crypto/stablecoin → real-world purchasing power；不是 Crypto Card 市场，也不是整个 Crypto Fintech。
2. 规模最多给三层，不给单一 TAM：L1 $390B run-rate（含大量 B2B）、L2 $153B consumer-related flow（非 Spend/TAM）、L3 card spend 2025 $4.5B–$5.2B / 2026-07 $759M 月、2.5x YoY、~9M 笔。
3. Paymentscan $1.038B headline 与 $642M pure-on-chain 必须分列；RedotPay >$14B 品牌 volume 不进总盘。
4. 两个 Friction 只解释市场存在，不做生态位轴。
5. 3 个 Job Family（J1/J2/J3）+ 分层映射；J3 可与 J2 后合并。
6. 区域 = 事实背景 + 待验证假设；禁止直接写 Region × Job。
7. Card 基础设施只确认增长/扩圈/多机制并存；“商品化”待验证。
8. AIX 核心问题保持待验证：J2 型低摩擦消费 vs 全球资金账户，或两者主次。
