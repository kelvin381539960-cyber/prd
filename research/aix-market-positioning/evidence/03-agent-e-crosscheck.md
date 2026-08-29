# Agent E｜Independent Cross-Check（Step 3 four-AND gate）

> 状态：Agent E 独立交叉验证（2026-08-29）。
> 类型：Step 3 evidence crosscheck，不是最终竞争战略结论。
> 证据边界：只读取 `evidence/03-agent-a-redotpay-kast.md`、`03-agent-b-custodial-cards.md`、`03-agent-c-self-custody.md`、`03-agent-d-credit.md`、`03-agent-f-aix-anchor.md`、`01-market-overview-and-user-jobs.md`、`02-ecosystem-map.md`。不联网、不检索、不补抓。
> 方法：对每个产品独立重算 four-AND gate，不继承任何 Agent 的 Overall 结论，只引用其 Current facts 作为输入。

---

## 0. 口径与语义（accepted semantics）

### AIX 侧锚点（来源：03-agent-f-aix-anchor.md）

| 维度 | 接受的口径 |
|---|---|
| **Region anchor** | AIX 完整 stablecoin→card current journey 的地域锚点 = **PH**。VN/AU 的完整 journey = **Unknown**。Wallet Crypto Deposit = PH，Card Phase 1 = PH/VN/AU，两者不可互推。 |
| **Starting money pool** | 用户在**选择方案之前已拥有**的资产类型与来源。指用户已从外部 wallet/exchange 持有的 USDC/USDT/WUSD/FDUSD。**不是**产品内部 custody/container（Card Balance、Vault、Funding Account 等内部容器不计入）。 |
| **J2 范围** | J2 = 已持有 Crypto → 现实购买力。**已持有稳定币**属于 J2 范围，不限于波动币。AIX 对 supported stablecoin-starting J2 segment = **strong/plausible**（analysis inference）。 |
| **J3** | AIX J3 = **Unsupported**（无 collateral/credit/borrow 能力）。 |
| **X/Y parity** | four-AND gate **不要求** X/Y parity。X/Y/Cluster 是机制描述，不是 direct 判定的第四项。 |

### 四项 AND gate

1. **Same region**：竞品当前 issuance/service 与 AIX 完整 journey region（PH）重合。
2. **Same core Job**：在 stablecoin-starting J2 segment 内，竞品与 AIX 的核心 Job 重合。
3. **Same starting money pool**：竞品支持用户进入产品前已持有的稳定币作为起点。
4. **Substitutable final outcome**：竞品最终提供可替代的现实世界卡消费。

四项 **同时 Yes** → Overall **Direct**。任何一项 **Unknown** → Overall **Unknown**。任何一项 **No** → Overall **Not Direct**。

### KAST Source Conflict 处理

Agent A 原稿将 KAST 卡机制写为 X2×C / S3。按 2026-08-09 官方页面实际证据，KAST card mechanism 存在 **Source Conflict**：

- `card-use-v2`（2026-08-09）："deducted right away — always spending your own funds, not credit" → **C-like** direct balance deduction。
- `debit-or-credit`（2026-08-09）："All KAST cards are credit cards" → **D-like** secured credit line evidence。

Agent E 独立处理：**X2 confirmed**（money from platform wallet/account），**Y = Unknown**（C vs D conflict 不裁决），**Cluster = Unknown**（不硬归 S3 或 S6），**Account Role = Money Account**（unified balance + receive/send/spend 证据独立于 Y 判定，保留）。该 Y conflict **不影响 four-AND**（four-AND 不要求 X/Y parity；KAST 的 four-AND 阻断点是 region Unknown）。

---

## 1. Four-AND 独立重算矩阵

| Product / Mode | Region vs PH | Core Job overlap | Starting pool overlap | Final outcome | Overall | Key blocker |
|---|---|---|---|---|---|---|
| **RedotPay** (generic crypto auto-convert card) | **Yes** — restricted list 不含 PH；full journey PH 成立 | **Yes** — J2 primary；stablecoin-starting segment 重合 | **Yes** — USDT/USDC from external wallet/exchange | **Yes** — card real-world spend | **Direct** | 无（限定 segment） |
| **KAST** | **Unknown** — signup dropdown only；无 PH 正面资格 | **Plausible** — J1 primary；stablecoin-starting J2 secondary inference | **Yes** — USDT/USDC from external wallet/exchange | **Yes** — card real-world spend | **Unknown** | PH card issuance/service eligibility Unknown |
| **Bitget Wallet Card** | **Yes** — current availability + physical card 列表含 PH；full journey PH 成立 | **Yes** — J2 primary；stablecoin-starting segment 重合 | **Yes** — USDT/USDC top-up | **Yes** — card real-world spend | **Direct** | 无（限定 segment） |
| **Bybit Card** | **Unknown** — 只见 program names；country-level eligibility 未证明 | **Yes** — J2 primary | **Yes** — USDC 在 payment priority | **Yes** — card real-world spend | **Unknown** | PH issuance eligibility Unknown |
| **Crypto.com Card** | **Unknown** — AU 页面存在但 AIX AU full journey Unknown；无 PH 证据 | **Yes** — J2 primary（crypto 先 convert 再 load） | **Unknown** — stablecoin pool 未证明（只证明 Crypto Wallet / Cash Account / cards） | **Yes** — card real-world spend | **Unknown** | PH 无证据；AIX AU full journey Unknown；stablecoin pool 未证明 |
| **MetaMask Card** | **No** — current list 不含 PH/VN/AU | **Yes** — J2 primary | **Partially** — 含 volatile crypto + stablecoin source | **Yes** — card real-world spend | **Not Direct** | Region No：PH/VN/AU 均不在 current list |
| **Plasma One** | **Unknown** — issuance/service country list Unknown | **Plausible** — J1 primary；stablecoin J2 secondary | **Yes** — stablecoin balance owned by user | **Yes** — card real-world spend | **Unknown** | Issuance/service country list Unknown |
| **Bleap** | **No** — Europe/MX/BR；无 PH/VN/AU | **Yes/partially** — J1 primary + J2 secondary；stablecoin spend 方向重合 | **Yes/partially** — stablecoin 或 bank transfer | **Yes** — card real-world spend | **Not Direct** | Region No：无 PH/VN/AU 重合 |
| **Karta** | **Unknown** — service country list Unknown | **Partially** — J1-leaning；stablecoin spend 方向相邻但 closure 不足 | **Yes** — USDT/USDC | **Yes/partially** — card spend 可见 | **Unknown** | Service/issuance country list Unknown |
| **OKX Pay/Card SG** | **No** — 仅 SG mode；与 AIX PH 无重合 | **Yes** — J1 primary + J2 secondary；stablecoin direct spend | **Yes** — USDT/USDC | **Yes** — real-world payment | **Not Direct** | Region No：SG 与 PH 无重合 |
| **ether.fi Direct Pay** | **Yes** — available countries 列 PH；full journey PH anchor 成立 | **Yes** — Direct Pay 从 Vault USDC/LiquidUSD 直接扣款；stablecoin-starting J2 segment 重合 | **Yes** — already-held USDC/USDT 进 Vault（starting pool 只看进入产品前，不看 Vault 内部 custody） | **Yes** — card real-world spend | **Direct** | 无（限定 PH stablecoin-starting segment） |
| **ether.fi Borrow** | **Yes** — PH 列入 available | **No** — Borrow = J3 primary；AIX J3 unsupported | Not required | Not required | **Not Direct** | AIX J3 Unsupported；Borrow 是 collateral-credit 机制 |
| **Nexo Debit** | **No** — EEA+UK only；与 PH 无重合 | **Yes** — J2-compatible for stablecoin segment | **Yes/partially** — stablecoin among Debit spend assets | **Yes** — card real-world spend | **Not Direct** | Region No：EEA+UK vs PH |
| **Nexo Credit** | **No** — EEA+UK only；与 PH 无重合 | **No** — Credit = J3 primary；AIX J3 unsupported | Not required | Not required | **Not Direct** | Region No **AND** Job mismatch（J3 vs unsupported） |

---

## 2. 独立判定与预期候选比对

| Expected candidate | Agent E 判定 | 一致？ |
|---|---|---|
| RedotPay = Direct | **Direct** | ✅ 一致 |
| Bitget Wallet Card = Direct | **Direct** | ✅ 一致 |
| ether.fi Direct Pay = Direct | **Direct** | ✅ 一致 |
| KAST = Unknown | **Unknown** | ✅ 一致 |
| Bybit Card = Unknown | **Unknown** | ✅ 一致 |
| Crypto.com Card = Unknown | **Unknown** | ✅ 一致 |
| Plasma One = Unknown | **Unknown** | ✅ 一致 |
| Karta = Unknown | **Unknown** | ✅ 一致 |
| MetaMask Card = Not Direct (region) | **Not Direct** | ✅ 一致 |
| Bleap = Not Direct (region) | **Not Direct** | ✅ 一致 |
| OKX Pay/Card SG = Not Direct (region) | **Not Direct** | ✅ 一致 |
| Nexo Debit = Not Direct (region) | **Not Direct** | ✅ 一致 |
| Nexo Credit = Not Direct (region + job) | **Not Direct** | ✅ 一致 |
| ether.fi Borrow = Not Direct (job) | **Not Direct** | ✅ 一致 |

**无分歧。** Agent E 独立重算结果与预期 direct evidence-level 候选完全一致。

---

## 3. KAST Source Conflict 补充说明

| 维度 | Agent A 原稿 | Agent E 修正 | 影响 |
|---|---|---|---|
| Y | C（stable-value balance deduction） | **Unknown**（C-like vs D-like Source Conflict） | 不影响 four-AND |
| Cluster | S3 | **Unknown** | 不影响 four-AND |
| X | X2 | X2 confirmed | 不影响 |
| Account Role | Money Account | **Money Account**（保留） | 不影响 |
| Overall four-AND | Unknown due region | **Unknown due region** | 一致 |

KAST 的 four-AND 阻断点始终是 **region Unknown**（PH issuance eligibility 未证明），不是 Y 判定。Source Conflict 的 Y/C-vs-D 问题不影响 direct 判定，但应在后续产品级核验中解决。

---

## 4. Top 5 Competition Variables

1. **PH regional eligibility**：RedotPay / Bitget / ether.fi Direct Pay 在 PH 已证可服务；KAST / Bybit / Crypto.com / Plasma / Karta 在 PH 的 issuance eligibility 是决定 direct 竞争范围的最大变量。
2. **Stablecoin-only vs volatile-crypto starting pool breadth**：AIX 当前仅稳定币起点。竞品若同时支持波动币起点（如 RedotPay / MetaMask），在非稳定币 segment 形成超集竞争，但 four-AND 判定仍限于稳定币起点 segment。
3. **Account Role（Spend Feature vs Money Account）**：KAST / Plasma One 的 Money Account 定位意味着用户可能将它们作为长期资金账户而非仅消费工具，产生不同的切换成本和竞争边界。
4. **Custody / Container model（X）**：AIX X1 vs RedotPay X2 vs ether.fi X3 vs Bitget X Unknown。Custody 差异影响用户信任、监管定位和技术迁移摩擦，但不影响 four-AND。
5. **Card issuance cost and fee structure**：RedotPay virtual 10 USD / physical 100 USD；Bitget 0 fee；KAST free / premium；ether.fi 未证明完整费表。成本结构是用户在 direct 候选间选择的关键变量，Step 4 需对比。

---

## 5. Top 5 Unresolved Evidence Gaps

1. **PH issuance eligibility for KAST / Bybit / Crypto.com / Plasma One / Karta**：这 5 个产品在 PH 的当前 issuance/service eligibility 均未证明，是 largest single blocker for Unknown rows。需查各国 Help Center 或实际 signup flow。
2. **AIX Wallet→Card funding mechanism（Y）**：决定 AIX 自身 Species 归类，以及与 X1×A（S1）或 X1×B/C 竞品的精确机制对齐。
3. **Bitget Wallet Card custody/container（X）**：官方只证明 "top up → spend"，但未证明 top-up 后形成独立 Dedicated Card Balance 还是直接从 Wallet 侧扣款。X 判定影响 mechanism-level 对比但不影响 four-AND。
4. **Crypto.com stablecoin starting pool**：官方只证明 Crypto Wallet / Cash Account / cards，但未在缓存页证明 USDT/USDC 作为稳定币起点可以进入 card load path。需确认 stablecoin-specific 入金到卡消费路径。
5. **Full fee / comparison tables for all direct candidates**：RedotPay / Bitget / ether.fi Direct Pay 的完整 FX / ATM / top-up / withdrawal 费表均未证明，Step 4 竞争强度分析需要这些数据。

---

## 6. Step 3 Evidence Set Cross-Check Conclusion

### PASS / FAIL 判定

**PASS。**

### 理由（exact）

1. **无事实矛盾**：四个 Agent 报告的 Current facts 之间未发现互相矛盾。唯一 Source Conflict（KAST card class C vs D）已被接受语义显式处理为 Y = Unknown，且不影响 four-AND。
2. **方法一致**：所有报告使用相同 four-AND gate 定义（same region + same core Job + same starting pool + substitutable outcome），并遵循 "不将 Unknown 转为 No" 纪律。
3. **独立重算一致性**：Agent E 对 14 个产品 mode 独立重算 four-AND gate，结果与预期 direct evidence-level 候选（RedotPay / Bitget Wallet Card / ether.fi Direct Pay）完全一致，无被迫对齐。
4. **语义清晰**：AIX 侧锚点文件（03-agent-f）明确定义 region anchor = PH、starting pool = 进入前已持有稳定币、J2 含已持有稳定币、J3 unsupported、four-AND 不要求 X/Y parity。所有 Agent 报告均以此口径执行。
5. **KAST Y conflict 已显式标注**：Agent A 原稿对 KAST Y=C 的判断是 stale wording；Agent E 按 accepted semantics 修正为 Y = Unknown / Cluster Unknown / Account Role 保留，并确认该 conflict 不影响 four-AND。

### 遗留限制（不阻止 PASS）

1. 5 个产品的 PH issuance eligibility Unknown（KAST / Bybit / Crypto.com / Plasma / Karta），将带入 Step 4。
2. AIX Y / Species 仍 Unknown，不影响 direct 判定但影响精确机制对比。
3. 完整费表未证明，影响 Step 4 竞争强度量化。
4. KAST card mechanism C vs D Source Conflict 需后续产品级核验。
5. Karta receive/payout/global payouts 仍为 Coming Q3 2026，不得升级为 current capability。

---

## 7. 输出 JSON

```json
{
  "outcome": "PASS",
  "summary": "Agent E independently recomputed the four-AND gate for 14 product modes using accepted semantics (PH region anchor, starting pool = user-owned stablecoins before choosing solution, J2 includes already-held stablecoins, J3 unsupported, no X/Y parity requirement). Results match expected direct candidates exactly: RedotPay, Bitget Wallet Card, and ether.fi Direct Pay are Direct. KAST, Bybit, Crypto.com, Plasma One, and Karta remain Unknown due to region or evidence gaps. MetaMask, Bleap, OKX SG, Nexo Debit, Nexo Credit are Not Direct due to region (Nexo Credit also due to Job). ether.fi Borrow is Not Direct due to Job mismatch (J3 vs AIX unsupported J3). KAST card mechanism Source Conflict (C-like direct balance vs D-like secured credit) is explicitly noted: X2 confirmed, Y Unknown, Cluster Unknown, Account Role Money Account retained; this conflict does not affect four-AND. No disagreements with expected candidates were found.",
  "changedFiles": ["research/aix-market-positioning/evidence/03-agent-e-crosscheck.md"],
  "tests": ["independent four-AND recomputation for 14 product modes", "comparison against expected direct/unknown/not-direct candidates", "KAST source conflict semantic override verification", "starting money pool semantic verification (pre-choice user-owned assets only)"],
  "commands": [],
  "decisionsRequired": ["Resolve PH issuance eligibility for KAST / Bybit / Crypto.com / Plasma One / Karta (Step 4 or follow-up evidence collection)", "Resolve KAST card mechanism Source Conflict (C vs D) via official product-level confirmation", "Collect full fee tables for RedotPay / Bitget / ether.fi Direct Pay for Step 4 competitive intensity analysis"],
  "requiresGptReview": true
}
```
