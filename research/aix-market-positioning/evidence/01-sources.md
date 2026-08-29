# Step 1 证据索引（01-sources）

> 用途：记录 Step 1 结论所依赖的外部来源、各自支持范围与限制。
> 原则：外部来源只作为证据引用，不代表仓库业务事实；口径冲突时按下方“必注口径”处理。

## 来源清单

### 1. McKinsey + Artemis：Stablecoins in payments

- URL：https://www.mckinsey.com/industries/financial-services/our-insights/stablecoins-in-payments-what-the-raw-transaction-numbers-miss
- 支持范围：L1 真实 stablecoin payments ≈ $390B run-rate（2025-12 月活动年化）；L3 stablecoin-linked card spend 2025 ≈ $4.5B；区分“真实支付”与链上原始交易量。
- 限制：L1 含大量 B2B；数据为时点口径；不直接支持“consumer PMF 已验证”。

### 2. a16z / Paymentscan：Stablecoin card spend 2026-07

- URL：https://a16zcrypto.com/posts/article/charts-payment-card-stablecoin-spend
- 支持范围：stablecoin-linked card spend 2026-07 约 $759M/月、同比约 2.5x、近 9M 笔；显示 card rail 从小基数高速增长。
- 限制：包含第三方统计（Paymentscan）；必须与 Paymentscan 另两个口径分列：约 $1.038B headline、约 $642M pure-on-chain view；不要外推 J1/J3 PMF。

### 3. Reuters：RedotPay stablecoin card spending forecast

- URL：https://www.reuters.com/business/finance/stablecoin-card-spending-forecast-hit-50-billion-year-by-2028-redotpay-2026-08-25/
- 支持范围：RedotPay >$14B annualized payment volume（含 topups / card spends）；2028 $50B forecast 为其品牌预测口径。
- 限制：品牌 volume 不进总盘；预测不代表本仓库结论。

### 4. Chainalysis 2025：Global / LATAM / SSA / North America / Europe / MENA

- 支持范围：各区域 Crypto activity / adoption 的事实背景与宏观趋势。
- 限制：区域 adoption 不等于 Region × Job；不得据此写“LATAM=J1、North America=J2/J3”；仅作背景与待验证假设来源。

### 5. World Bank Remittance Prices

- URL：https://remittanceprices.worldbank.org/
- 支持范围：跨境汇款成本/通道背景，支撑 J1“稳定、可跨境的钱”与 cross-border income/remittance 场景的存在性。
- 限制：宏观数据，不直接证明某个 Job Family 的具体规模或玩家覆盖。

### 6. Bybit：Bybit Card and Spending Information

- URL：https://www.bybit.com/en/help-center/article/How-to-Consult-Your-Bybit-Card-and-Spending-Information
- 支持范围：交易所（资金初始位置）发行 Card 的具体机制示例。
- 限制：单一玩家产品文档；只用于机制示例，不用于市场总盘。

### 7. MetaMask Card

- URL：https://metamask.io/card
- 支持范围：自托管钱包语境下消费卡机制示例（不卖 Crypto 或低摩擦消费型路径的证据来源之一）。
- 限制：单一玩家产品页；机制示例，不代表市场规模。

### 8. ether.fi：Cash Card Borrow Mode vs Direct Pay Mode

- URL：https://help.ether.fi/en/articles/326983-understanding-your-cash-card-borrow-mode-vs-direct-pay-mode
- 支持范围：J3 型机制（不卖 Crypto、以资产支持/借贷获得消费流动性）以及 Direct Pay 的对照示例。
- 限制：单一玩家文档；机制示例；J3 是否只是 J2 约束 segment 需 Step 2 验证。

### 9. Visa：Crypto-linked cards

- URL：https://corporate.visa.com/en/sites/visa-economic-empowerment-institute/crypto-linked-cards.html
- 支持范围：Card 作为 spend rail、2024-2026 card spend 重新增长、覆盖与模式扩展。
- 限制：品牌公开材料；不用于市场规模加总，具体扩展以合同/公告为准。

### 10. Mastercard：Crypto card program

- URL：https://www.mastercard.com/us/en/business/payments/consumer-payments/next-gen-payments/digital-asset-solutions/crypto-card-program.html
- 支持范围：Card rail 的 Issuer / BIN / Acceptance 模式背景、多种机制并存。
- 限制：品牌公开材料；不做总盘。

### 11. Visa + Bridge 2026：expand stablecoin-linked cards to 100+ countries

- URL：https://investor.visa.com/news/news-details/2026/Visa-and-Bridge-Expand-Collaboration-with-Plans-to-Bring-Stablecoin-Linked-Cards-to-Over-100-Countries/default.aspx
- 支持范围：Visa/Bridge 扩覆盖、模式与 settlement 的 2026 证据。
- 限制：计划性公告；实际落地范围与时间待验证。

### 12. Mastercard stablecoin settlement 2026

- URL：https://www.mastercard.com/global/en/news-and-trends/press/2026/june/mastercard-expands-settlement-capabilities-to-include-stablecoin.html
- 支持范围：Mastercard 扩展 stablecoin settlement 能力，支持“多种机制并存”的结论。
- 限制：公告口径；不直接证明消费者侧规模。

## 必注口径（引用时不得省略）

1. **L1 / L2 / L3 不相加**，不合成单一 TAM。
2. **$390B 是 run-rate**，且含大量 B2B，不是纯 consumer 市场规模。
3. **$153B 是 consumer-related flow（C2C $77B + C2B $76B）**，不是 Consumer Spend，更不是 TAM。
4. **品牌 volume 不进总盘**（如 RedotPay >$14B annualized payment volume）。
5. **区域 adoption 不等于 Region × Job**；区域只作事实背景 + 待验证假设。
