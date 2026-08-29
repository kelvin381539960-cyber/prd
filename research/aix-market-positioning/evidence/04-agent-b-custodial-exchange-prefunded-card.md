# Step 4 Agent B 收口｜J2 Custodial / Exchange / Pre-funded Card 最终证据卡

> 状态：Step 4 Agent B CLOSEOUT（2026-08-30）
> 类型：evidence card / mode-level 固定稿；「J2 已有 Crypto → 现实购买力」消费簇中，托管 / 交易所 / 预充值卡类模式的最终证据固化。
> 数据边界：只使用 `/tmp/aix-evidence-04/` 已采集官方缓存与 Step 1–3 已评审定义文件；**未联网、未补抓、未新增 URL**。
> AIX 纪律：AIX 仅是未来进入者。本卡不以 AIX 为锚点；AIX 当前事实（X1 confirmed / Y Unknown / PH 锚点等）不得过滤、升级或降级任何竞品行。市场玩家之间关系与 AIX 是否存在无关。
> 本卡不替代 Step 4 主文档 `04-competition-map.md` 的 R1–R5 分类；只做证据级收口。

---

## 0. 范围与不纳入

- **纳入本卡**：Bitget Wallet Card、Bybit Card、Crypto.com Card（SG/AU region modes）、Binance Card（Wayback 缓存，Closeout 首次物化）。
- **缓存存在但无效、不纳入落位**：Coinbase（Cloudflare challenge + Help 404，无有效内容）；OKX `/en/cards`（404 / soft-degrade，无产品内容）；Wirex card 页（404；首页仅营销，无 mode 级证据）。Step 3 中已由 Agent C 评审的 OKX SG 证据不受此缓存影响。
- **不在本卡范围**：RedotPay / KAST（Agent A 已覆盖 custodial card 与 Money Account 证据）、self-custody / credit 簇（Agent C / Agent D）。本卡不重复展开、不改写其结论。

## 1. 缓存证据清单（/tmp/aix-evidence-04）

| 缓存文件 | 缓存来源（cache HTML canonical） | 采集时间 | 有效性 |
|---|---|---|---|
| `bitget-card.html/.txt` | https://web3.bitget.com/card | 2026-08-30 00:40 | ✅ 有效，完整产品页 + FAQ |
| `bybit-spending.html/.txt` | https://www.bybit.com/en/help-center/article/How-to-Consult-Your-Bybit-Card-and-Spending-Information | 2026-08-30 00:40 | ✅ 有效 |
| `bybit-payments.html/.txt` | https://www.bybit.com/en/help-center/article/How-to-Make-Payments-with-Bybit-Card | 2026-08-30 00:40 | ✅ 有效 |
| `bybit-management.html/.txt` | https://www.bybit.com/en/help-center/article/Bybit-Card-Management-Settings-Guidelines | 2026-08-30 00:43 | ✅ 有效 |
| `crypto-au.html/.txt` | https://crypto.com/au/cards | 2026-08-30 00:40 | ✅ 有效（AU region mode） |
| `crypto-sg.html/.txt` | https://crypto.com/sg/cards | 2026-08-30 00:40 | ✅ 有效（SG region mode） |
| `crypto-sg-fees.html/.txt` | https://help.crypto.com/en/articles/6043620-...（SG residential fees & limits） | 2026-08-30 00:43 | ✅ 有效 |
| `binance-20250930205557.html/.txt` | https://www.binance.com/en/cards（Wayback 20250930205557） | 2026-08-30 00:49 | ✅ 有效，时点快照 2025-09-30 |
| `binance-20251108092015.html/.txt` | https://www.binance.com/en/cards（Wayback 20251108092015） | 2026-08-30 00:49 | ✅ 有效，时点快照 2025-11-08；文本与上一份一致 |
| `crypto-ph.html/.txt` | PH 页面（cache 内容为 404 页，无 canonical） | 2026-08-30 00:46 | ⚠️ 仅记录「PH 专用页面未取到」；不作产品证据 |
| `bybit-card.html/.txt`、`bybit-fees.html/.txt`、`bybit-apac.html/.txt` | Bybit 通用/费用/APAC 页 | 2026-08-30 00:43–00:45 | ❌ 「This article is currently not supported on this site」/通用页，无效 |
| `coinbase-card.html/.txt`、`coinbase-card-faq.html/.txt`、`coinbase-help-cards.html/.txt` | Coinbase | 2026-08-30 00:46 | ❌ Cloudflare challenge / 404，无效 |
| `okx-card.html/.txt` | https://www.okx.com/en/cards | 2026-08-30 00:40 | ❌ 404 / soft-degrade，无效 |
| `wirex-card.html/.txt`、`wirex-cards.html/.txt` | Wirex card 页 | 2026-08-30 00:43 | ❌ 404；不纳入 |
| `wirex-home.html/.txt` | https://www.wirexapp.com | 2026-08-30 00:46 | ⚠️ 营销首页，无 mode 级证据；不纳入 |
| `nexo-card.html/.txt`、`kast-global-accounts.html/.txt`、`redotpay-*.html/.txt` | Nexo / KAST / RedotPay | 2026-08-30 00:40–00:46 | ✅ 有效，但属 Agent A / D 覆盖范围，本卡不展开 |

## 2. 判定口径（沿用 Step 1–3，不重算）

- **J2**：用户已持有 Crypto（含稳定币），低摩擦转化为现实购买力（`01-market-overview-and-user-jobs.md`）。
- **X / Y / S1–S6 / Account Role**：沿用 `02-ecosystem-map.md`；X 看「消费真正发生时被扣的价值余额」，Y 看「购买力形成机制」。
- **Region 纪律**：逐国 issuance/service eligibility 未证 = Unknown ≠ No；营销口径（50+ / 100+ / 150M / 170+ 等）不进入 issuance 判定。
- **Wayback 纪律**：Binance 两份缓存是时点快照，结论标记 point-in-time；不冒充 2026-08-30 的 live 声明。
- 本卡不做 four-AND / R1–R5 判定，只固定 mode 级事实。

## 3. Mode 证据卡

### 3.1 Bitget Wallet Card（Step 3 M3；坐标不变）

**缓存依据**：`bitget-card.html/.txt`（canonical https://web3.bitget.com/card）。

已固化事实：

- 卡片“currently available”：EEA+UK；LATAM 10 国（Argentina, Brazil, Chile, Colombia, Ecuador, El Salvador, Guatemala, Mexico, Panama, Peru）；APAC（Singapore, South Korea, Japan, Vietnam, Malaysia, mainland China, Taiwan, Australia, Thailand, Philippines）；South Africa；Pakistan, Bangladesh。
- Physical card 当前地区：Singapore, South Korea, Japan, Vietnam, Malaysia, Taiwan, Australia, Thailand, Philippines。
- 申请路径：`Apply online and verify your identity` → `Activate your card, top up, and spend`。
- 支持 USDT / USDC / ETH / SOL top-up；Visa/Mastercard 全球商户；Apple Pay / Google Pay / WeChat Pay / Alipay。
- 费用：0 opening & annual fee；no interest markup / no monthly card fee / no hidden charges；月度消费约 $200–$400 触发 up to 3% assetback（基础 2%），奖励通常覆盖大部分 top-up 与 currency conversion 费用；超出 assetback allowance 后 standard fees apply。
- 钱包失控表述：失去 seed phrase 后已激活卡仍可消费，但不能 top-up / withdraw、不能恢复 card account 或钱包资产。

判定：

| 维度 | 结论 | 依据边界 |
|---|---|---|
| X | **Unknown** | 官方只证明 top-up → spend，未证明消费前形成独立 Dedicated Card Balance |
| Y | **A confirmed** | 官方明确 activate → top up → spend |
| Cluster | **S1 candidate only** | X Unknown，不得升 confirmed |
| Account Role | **Spend Feature** | 无 receive + hold + send/spend + unified balance 证据 |
| Region | PH / VN / AU availability confirmed | availability 与 physical card 均含三地；逐国 issuer 终表未证 |

Unknown：X；完整 top-up / FX / ATM / replace 费表；KYC tier；Wallet→Card 资金路径细节（手动/自动）。

### 3.2 Bybit Card（Step 3 M4；坐标不变）

**缓存依据**：`bybit-spending.html/.txt`、`bybit-payments.html/.txt`、`bybit-management.html/.txt`。

已固化事实：

- Spending Power = Funding Account 的 base currency available balance + 所选 payment crypto asset 按 base currency 折算。
- 可选最多 3 种 payment crypto；默认优先级 `USDC > BTC > ETH > MNT > TON > XRP`。
- 交易授权时冻结 Funding Account 金额，授权完成后扣减；crypto 消费明细可在 `Crypto Sold` 查看。
- 卡管理：freeze/unfreeze、CVV unblock、online/ATM toggle、PIN reset、replace、terminate、Apple Pay / Google Pay / Samsung Pay（按 program）。
- 可见 card programs：Argentina、Brazil、AIFC、Asia Pacific、Mexico（program 名不是逐国 issuance 表）。

判定：

| 维度 | 结论 | 依据边界 |
|---|---|---|
| X | **X2 confirmed** | 消费冻结/扣减发生在 provider-custodied Funding Account |
| Y | **B confirmed** | payment crypto 在支付时 converted/sold（Crypto Sold） |
| Cluster | **S2** | X2×B |
| Account Role | **Spend Feature** | Funding Account 支撑卡消费，Money Account 结构未证 |
| Region | PH / VN / AU **Unknown** | 只见 program names；`bybit-apac` 等页面在缓存中 unsupported |

Unknown：逐国 issuance/issuer；完整费表（`bybit-fees` 缓存不可用）；KYC/申卡前置。

### 3.3 Crypto.com Card（Step 3 M5；SG/AU region modes，坐标不变）

**缓存依据**：`crypto-au.html/.txt`、`crypto-sg.html/.txt`、`crypto-sg-fees.html/.txt`。

已固化事实：

- 官方 FAQ：Crypto.com Card 是 **prepaid card**，需 top up，不直接连接银行账户（非 debit）。
- Top-up 来源：Crypto Wallet、Cash Account、其他 credit/debit cards（Card tab → Top up）。
- **Cardholders cannot load cryptocurrency directly**；crypto 必须先转换为对应市场货币再 load 进卡。
- SG tier 结构（Midnight/Ruby/Indigo-Jade/Icy-Rose/Obsidian）与 SG residential 费表：ATM 2% on amounts above monthly free limit；debit top-up 0%、credit 1%、Apple Pay 2%；close account S$50；card replacement 按 tier；foreign transaction fee 0.5%–无 且 2026-09-01 有更新条款（Midnight 0.5%→2.0%；Ruby/Indigo 免费额度+2.0%）；inactivity S$5/month（2026-09-01 起 S$6）。
- SG limits：aggregated top-up S$100,000/day/month/12m；card max balance S$20,000；e-commerce 默认 S$1,000（2025-02-20 起 MAS 指引，可手动移除）。
- AU product mode：AUD tier、CRO lockup、cashback、免费 ATM 额度（$200–$1,000/month）、ATM cap $10,000/month、top-up limit $30,000/month。
- `crypto-ph.html/.txt` 为 404 缓存：**仅记录 PH 专用页面未取到**；不构成 PH No。

判定：

| 维度 | 结论 | 依据边界 |
|---|---|---|
| X | **X1 confirmed**（SG/AU modes） | prepaid card 消费前需 top up，存在独立卡余额 |
| Y | **A confirmed**（SG/AU modes） | 先 convert/top-up，再 spend |
| Cluster | **S1**（SG/AU modes） | X1×A |
| Account Role | **Spend Feature** | prepaid + top-up 不构成 Money Account |
| Region | SG residential mode、AU mode 已证；PH **Unknown**（无证据）；且 PH 页面缓存为 404 | 不推广为逐国 issuance 表 |

Unknown：PH 及其他国家 issuer/eligibility；stablecoin→card load 的精确路径（官方只证明 crypto 须先转换成市场货币，未证明 USDT/USDC 起点池同构）；完整 KYC 条款。

### 3.4 Binance Card（Closeout 新增；Wayback point-in-time 证据）

**缓存依据**：`binance-20250930205557.html/.txt`、`binance-20251108092015.html/.txt`（均为 https://www.binance.com/en/cards 的 Wayback 快照；两份提取文本一致）。

已固化事实（**2025-09-30 / 2025-11-08 时点快照，不是 2026-08-30 live 声明**）：

- 官方 FAQ：“Your Binance Account country of residence must be one of the supported countries of Binance Card. Currently we support: **Brazil**。”
- Brazil 申请材料：EKYC / Driving License / ID Card / Passport / Resident’s Permit。
- 支付机制：real-time crypto conversion，“spend with your card without having to pre-convert to a fiat currency”；支持 USDT、USDC、FDUSD、BNB、BTC、ETH、SOL、ADA、LINK、XRP。
- 费用：Crypto Conversion Fee 1%；Foreign Exchange Fee 2%；Annual Fee 0 BRL；Card Issuance Fee 0 BRL；physical card cancellation 30 BRL（1 年内）/ 0 BRL（1 年后）；ATM 每月 2 次免费，之后每次 1.5 USD。
- 限额：Spending Daily 25,000 BRL / Monthly 50,000 BRL / Annual 200,000 BRL；ATM withdrawal Daily 3,000 BRL / Monthly 25,000 BRL / Annual 200,000 BRL；ATM 次数 3/30/360（日/月/年）；更高验证等级提升限额。
- 其他：2% cashback、每月上限 120 BRL；无年费/发卡费、免费配送；申请后立即可用 virtual card。

判定：

| 维度 | 结论 | 依据边界 |
|---|---|---|
| X | **Unknown** | 缓存未明确消费扣减的是专属卡余额还是交易所钱包余额；不得强写 X2 |
| Y | **B confirmed** | 官方明确 real-time crypto conversion / 无需预转换 |
| Cluster | **S2 candidate only** | X Unknown，不升级 confirmed（沿用 Step 2 纪律） |
| Account Role | **Spend Feature at most** | 本缓存无 receive/send/unified 证据 |
| Region | **Brazil only（时点快照）** | 无 PH / VN / AU 证据；不排除其他可能，但没有证据不得写 Yes |

Fits J2：是「已有 crypto → card real-world spend」的 evidence-level 交易所卡样本；是否与 AIX 直接竞争不由本卡判定（AIX 仅未来进入者）。

Unknown：X 容器；其 cashback 存入「wallet」是否意味着交易所钱包扣款（未明确）；2025-11-08 后是否变化；逐国资格。

## 4. 汇总表（mode-level）

| Player / mode | Cache 依据 | X×Y | Cluster | Account Role | 已证 Region | PH/VN/AU | J2 |
|---|---|---|---|---|---|---|---|
| Bitget Wallet Card | bitget-card | X Unknown × A | S1 candidate | Spend Feature | 50+ 国列表内含 PH/VN/AU（availability） | Yes / Yes / Yes（availability；issuer 未证） | J2 primary |
| Bybit Card | bybit-{spending,payments,management} | X2 × B | S2 | Spend Feature | 仅 program names | Unknown | J2 primary |
| Crypto.com Card | crypto-{au,sg,sg-fees} | X1 × A | S1（SG/AU） | Spend Feature | SG / AU region modes | PH Unknown（PH 页缓存 404） | J2 primary |
| Binance Card | binance-2025*（Wayback） | X Unknown × B | S2 candidate | Spend Feature at most | Brazil（时点快照） | 无证据 | J2 |

无效缓存（不落位）：Coinbase（challenge/404）、OKX `/en/cards`（404）、Wirex card 页（404；首页营销不足）。

## 5. 与 Step 1–3 的衔接

- Bitget / Bybit / Crypto.com 的 X/Y/Cluster/Account Role 与 Step 3 Agent B 结论**完全一致**；本卡只是把 `/tmp/aix-evidence-04` 官方缓存物化为可回溯证据，不重算、不升级。
- Binance Card 是 Step 4 缓存中新增的 evidence-level 样本，按同一 X/Y 纪律落位（Y=B confirmed / X Unknown / S2 candidate），不因 AIX 存在与否而调整。
- 本卡不修改 `04-competition-map.md` 的 M1–M14 与 R1–R5（Binance 未进入 Step 3 已评审 mode 集；如需进入竞争图，交 Step 5 处理）。
- AIX 对照仅一条纪律：AIX 是未来进入者，其 X1/Y Unknown/PH 锚点不参与任何竞品间事实判定。

## 6. 约束自检

- ✅ 未联网、未补抓、未新增 URL；所有论断可回溯到缓存文件或 Step 1–3 文件。
- ✅ Unknown ≠ No：Bybit / Crypto.com / Binance 的 PH/VN/AU 行保持 Unknown 或仅记录缓存缺失。
- ✅ point-in-time：Binance 两份 Wayback 快照明确标注时点，不冒充 current。
- ✅ merchant/marketing 数字（150M、170+、50+ 等）未进入 issuance 判定；Bitget 的 50+ 只作为其官方 availability 表达引用。
- ✅ AIX 过滤扫描：全卡未用 AIX 事实改变任何竞品落位；AIX 仅在纪律声明出现。
- ✅ 本卡不替代 Step 4 主文档 R1–R5；不写任何 new R 关系。

## 7. 来源映射

| 本卡内容 | 来源 |
|---|---|
| X/Y/S1–S6/Account Role 判定 | `02-ecosystem-map.md` |
| J2 定义 | `01-market-overview-and-user-jobs.md` |
| Bitget / Bybit / Crypto.com Step 3 结论 | `03-player-positioning.md`；`evidence/03-agent-b-custodial-cards.md` |
| 缓存提取事实 | `/tmp/aix-evidence-04/` 文件（见 §1） |
| Step 3 直接候选与 Unknown 纪律 | `evidence/03-agent-e-crosscheck.md` |
| Step 4 边界 | `04-competition-map.md`；并行 Agent A/C/E 证据卡；共享 `04-sources.md` 由 Step 4 收口流程统一维护，本卡不独占 |

## 8. 输出 JSON

```json
{
  "outcome": "PASS",
  "summary": "Step 4 Agent B closeout materialized the final J2 custodial/exchange/pre-funded card evidence card from /tmp/aix-evidence-04 caches plus Step 1-3 definitions only (no browsing, no new URLs). Fixed facts: Bitget Wallet Card = Y A confirmed / X Unknown / S1 candidate / Spend Feature / PH-VN-AU availability confirmed; Bybit Card = X2 x B / S2 / Spend Feature / programs-only region, PH-VN-AU Unknown; Crypto.com Card = X1 x A / S1 (SG/AU region modes) / Spend Feature / PH Unknown (PH page cache is 404); Binance Card (new, Wayback 2025-09-30 and 2025-11-08 snapshots) = Y B confirmed / X Unknown / S2 candidate / Spend Feature at most / Brazil-only per snapshot, 1% crypto conversion + 2% FX + 0 issuance/annual fees. Invalid caches excluded from placement: Coinbase (challenge/404), OKX /en/cards (404), Wirex card pages (404; homepage marketing only). AIX kept strictly as future entrant; no AIX facts filtered or changed any competitor row.",
  "changedFiles": [
    "research/aix-market-positioning/evidence/04-agent-b-custodial-exchange-prefunded-card.md"
  ],
  "tests": [
    "every cited cache file exists and its extracted text supports the quoted fact (checked bitget-card, bybit spending/payments/management, crypto-au/sg/sg-fees, binance 2025-09-30/2025-11-08)",
    "invalid cache audit: coinbase-card/coinbase-faq/coinbase-help, okx-card, wirex-card/wirex-cards and bybit-fees/bybit-apac/bybit-card marked non-evidence (404/unsupported/challenge)",
    "X/Y discipline check: Binance kept X Unknown / Y B confirmed / S2 candidate (no X2 claim without deduction-source proof); Bitget kept X Unknown / S1 candidate",
    "Unknown != No check on PH/VN/AU rows for Bybit, Crypto.com and Binance",
    "Wayback point-in-time check: Binance facts labeled 2025-09-30/2025-11-08 snapshots, not 2026-08-30 live",
    "merchant/marketing numbers not used as issuance evidence",
    "AIX guardrail scan: no AIX row filters/upgrades/downgrades any competitor fact; AIX appears only as future-entrant discipline",
    "shared-file conflict check: this card is self-contained and does not modify 04-competition-map.md, 04-sources.md, or another agent's evidence card while parallel Step 4 agents are writing"
  ],
  "commands": [
    "rg -n 'binance-2025|bitget-card|bybit-spending|crypto-sg' /tmp/aix-evidence-04/*.txt to verify cache content cited",
    "rg -n -i 'AIX' research/aix-market-positioning/evidence/04-agent-b-custodial-exchange-prefunded-card.md to confirm AIX appears only in discipline statements",
    "ls -la research/aix-market-positioning/evidence/04-agent-b-custodial-exchange-prefunded-card.md"
  ],
  "decisionsRequired": [
    "Decide whether Binance Card (evidence-level, Wayback point-in-time) should enter Step 4 competition map as a new mode or stay as a Step 5 input",
    "Resolve Bybit PH/VN/AU country-level issuance eligibility (only program names proven)",
    "Resolve Crypto.com stablecoin-starting pool -> card load path before counting it in J2 segment density",
    "Resolve Binance card X container (dedicated card balance vs exchange wallet deduction) with current official evidence",
    "Re-verify Binance Card live supported countries after 2025-11-08 snapshot before treating Brazil-only as current",
    "Decide whether Rollup of Coinbase/OKX/Wirex invalid caches belongs in Step 5 as a re-check list"
  ],
  "requiresGptReview": true
}
```
