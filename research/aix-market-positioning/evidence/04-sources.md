# Step 4｜证据索引与主审采用范围

> 日期：2026-08-30
> 原则：Agent 输出只作为 evidence input；最终竞争规则与结论以主审 `04-competition-map.md` 为准。任何旧 AIX-current-anchor 段落不进入 Step 4 市场结论。

## 1. Agent 验收

| Agent | Evidence file | Verdict | 主审采用范围 |
|---|---|---|---|
| A J1 | `04-agent-a-j1-global-money-card.md` | **PARTIAL PASS** | KAST / Plasma / Bleap / Karta / OKX 玩家事实采用；旧 AIX current / PH-centric 对照不采用 |
| B J2 custodial | `04-agent-b-custodial-exchange-prefunded-card.md` | **PASS** | Bitget / Bybit / Crypto.com mode 事实采用；Binance 仅 2025 Wayback reference，不作为 2026 current |
| C self-custody | `04-agent-c-self-custody-wallet-native-evidence-card.md` | **PARTIAL PASS** | MetaMask / Plasma / Bleap / Karta / OKX / ether.fi / Gnosis Pay 事实采用；旧 AIX 对照不采用 |
| D J3 | `04-agent-d-credit-borrow-to-spend-evidence-card.md` | **PARTIAL PASS** | Nexo / ether.fi Borrow / RedotPay Credit / Ledn / YouHodler 事实采用；旧 AIX 对照不采用；generic borrow 参数不自动当 card-specific |
| E region | `04-agent-e-regional-maturity-density.md` | **PASS AFTER REVISION** | 首稿 PH/VN/AU-centric 判 FAIL；修订后的 market-level 版本采用；文件里的 AIX baseline 不采用 |
| F 第一轮 | 已清除污染产物 | **FAIL** | 越权修改 TASK/main/source 且夹带旧 AIX anchor；不采用 |
| F2 framework | `04-agent-f2-competition-framework.md` | **FAIL / REJECTED** | 错误要求 Direct 必须同 X/Y/container/mechanism；仅保留审计，不作为竞争结论来源 |
| G2 non-card | `04-agent-g2-non-card-substitute-rails-evidence-card.md` | **PASS ON ARTIFACT** | Job 最终因 429 退出，但证据文件在失败前已写入且 JSON validation 通过；采用其中 source-grounded facts |

## 2. Direct 固定规则

Confirmed Direct 必须同时满足：

1. same current market / region；
2. same core Job；
3. same / overlapping starting money pool；
4. substitutable real-world purchasing-power outcome。

**不要求 same X、same Y、same custody、same rail。**

原因：这些是产品实现与差异化变量，用户是否二选一取决于 Job、起始资金、可获得性和最终购买力结果。

## 3. 证据纪律

- Stablecoin 属于 Crypto，J2 不等于 volatile-crypto-only。
- Unknown ≠ No。
- merchant acceptance ≠ issuance / service eligibility。
- future / waitlist / coming soon ≠ current。
- Card 是 Spend Rail，不是市场本身。
- KAST current mechanism 保留 Source Conflict：X2 confirmed / Y Unknown / Cluster Unknown。
- Solana Pay Shopify integration 保留 Source Conflict，不做单边裁决。
- BSP digital-payment 数据只证明 rail maturity，不证明 stablecoin spend volume。
- Region density 是样本下限；EEA+UK aggregate 不等于逐国精确密度。
- Step 4 不定义 AIX 当前或目标定位；Step 5 才选择目标位置。

## 4. Step 4 采用的主证据文件

- `evidence/04-agent-a-j1-global-money-card.md`
- `evidence/04-agent-b-custodial-exchange-prefunded-card.md`
- `evidence/04-agent-c-self-custody-wallet-native-evidence-card.md`
- `evidence/04-agent-d-credit-borrow-to-spend-evidence-card.md`
- `evidence/04-agent-e-regional-maturity-density.md`
- `evidence/04-agent-g2-non-card-substitute-rails-evidence-card.md`

审计但不采用：
- `evidence/04-agent-f2-competition-framework.md`
