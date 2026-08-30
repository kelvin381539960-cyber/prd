# Step 5 Agent D 物化稿｜Region × Spend-Rail 结构性机会底图（GTM materialize only）

> 状态：Step 5 Agent D MATERIALIZED（2026-08-30）。**只物化，不研究、不浏览、不新增 URL、不选目标**。
> 角色：为 Step 5 GTM / 定位决策提供「区域 × spend-rail 结构性机会」的 evidence 底图；**不定义 AIX 目标地区/产品**；AIX 当前地理与能力不参与任何区域、rail 或机会读数。
> 数据边界（唯一来源）：
> 1. Step 1–4 正式文档与已评审证据（`01-market-overview-and-user-jobs.md`、`02-ecosystem-map.md`、`03-player-positioning.md`、`04-competition-map.md`、`evidence/04-*.md`、`evidence/04-sources.md`）；
> 2. Step 4 区域/非卡证据（`04-agent-e-regional-maturity-density.md`、`04-agent-g2-non-card-substitute-rails-evidence-card.md`）；
> 3. `/private/tmp/agent-g-evidence`（2026-08-30 非卡 rails 缓存，76 文件）；
> 4. Original-D 本地缓存（`/private/tmp/aix-credit-evidence`、`/private/tmp/aix-j3-evidence-04`）。
> 不采用：Step 5 其他 Agent 产物、任何联网/补抓结果、任何 marketing 覆盖数作为资格或份额。

---

## 0. 本稿职责与不做什么

| 做 | 不做 |
|---|---|
| 把已采集证据固化为 Region × Rail 结构性机会底图 | 不选择 AIX 目标 Region / Product |
| 给每个 cell 标证据强度与 Unknown | 不给 AIX 排序、不推荐白地 |
| 保留纪律（acceptance ≠ eligibility、regulation ≠ adoption、rail adoption ≠ crypto usage、aggregate ≠ country） | 不用 AIX 当前 PH/VN/AU / stablecoin-only / X1 能力过滤市场 |
| 为 Step 5 GTM 提供可回溯 materialization | 不新增任何市场事实或 URL |

---

## 1. 六条 Spend Rail 的口径（沿用 Step 4，不重造）

| Rail | 口径 | 关键区分 |
|---|---|---|
| **Card** | Visa/MC（及等效卡网络）消费轨；含 J2 卡消费与 J3 borrow-to-spend 卡模式 | 卡轨 ≠ 市场本身 |
| **QR / local A2A** | 本地 QR、e-wallet 账户互转、PayNow/SEPA/ACH 类账户间 rails | adoption 是 rail 成熟度，不等于 crypto/stablecoin 用量 |
| **Bank / e-wallet cashout** | crypto/平台余额 → 本地银行、e-wallet、现金/OTC 取出的 off-ramp；含两步 e-wallet 路径 | borrow-to-cash（Ledn/YouHodler）为相邻 off-ramp，不是卡消费 rail |
| **Merchant-direct** | 支付点直接用 crypto/stablecoin 完成商户支付，不经卡 | direct-at-merchant 与 two-step 转换不合并 |
| **Gift / prepaid** | crypto 购买礼品卡 / 话费 / eSIM / voucher → 本地购买力 | 目录存在 ≠ 区域 catalog/资格；search-page 为 secondary |
| **P2P** | 个人间 crypto/stablecoin ↔ 本地资金（bank/mobile wallet/gift card 对手方） | 样本中无消费者用量/资格证据；Unknown ≠ opportunity |

---

## 2. 证据强度标签

- **[S] Strong**：官方一手缓存/已评审证据直接支撑（可能只证明 rail 成熟度或提供者存在，不证明 crypto 份额）。
- **[P] Partial**：secondary 证据、局部证据、官方冲突未裁决或点状能力声明。
- **[U] Unknown**：本组证据没有覆盖、缓存不可用、资格未证（Unknown ≠ No）。
- **[N] No / not-in-sample**：官方 current list / areaServed 明确排除，或 14-mode 样本内 0 confirmed（≠ 市场无人）。

---

## 3. Region × Rail 结构性机会矩阵

| Region | Card | QR / local A2A | Bank / e-wallet cashout | Merchant-direct | Gift / prepaid | P2P |
|---|---|---|---|---|---|---|
| **PH** | **[S]** J2 confirmed=3（RedotPay X2×B、Bitget Y=A×X Unknown、ether.fi Direct Pay X3×C candidate）；J3：ether.fi Borrow available-page Yes + RedotPay Credit Unknown + Nexo No；机制多样（S2 / S1-candidate / S4-candidate） | **[S]** QR Ph 2025 2.47B 笔 / PHP 1.16T / 2.29M 商户 / 48 机构（BSP 无 crypto 拆分）；GCash Pay QR（个人+商户；Alipay+ 部分国际）；Coins.ph Scan & Pay | **[S]** Coins.ph InstaPay（flat ₱5）/ PESONet（平台 0）/ Remittance/OTC pickup（min ₱1,000）/ GrabPay cash-in；GCash/Maya 两步；PHPC BSP sandbox（与 QR 支付衔接 Unknown） | **[S]/[P]** Coins.ph QRPH Stablecoin Payments（2026-08-09）＝支付点直接选 crypto + 汇率确认 + “Confirm convert and pay”；GCash/Maya 商户 QR 是两步；Solana Pay/OpenNode PH 覆盖 Unknown | **[P]** Bitrefill API（2026-03-26）＋搜索页 secondary PH GCash Voucher / GrabMart；实时 PH 页被拦截，目录资格 Unknown | **[P]/[U]** Step 4 rail 层列 NoOnes 等 P2P/OTC；GCash 个人 QR / Coins.ph Send 存在，但 crypto→local P2P 的证据未采集 |
| **AU** | **[S]** J2 confirmed=3（Bitget、Crypto.com AU、ether.fi Direct Pay）；J3：ether.fi Borrow available-page Yes；issuer 终表未证 | **[U]** 无 AU 本地 QR/A2A 缓存证据 | **[P]/[U]** Crypto.com AU top-up/limit 证据；Karta bank rails 为 future；KAST rails 仅 US/EU 产品级；AU 本地 bank/e-wallet 未证 | **[U]** | **[U]** | **[U]** |
| **VN** | **[P]** confirmed=1（Bitget availability）+ ether.fi available-vs-restricted **conflict 不裁决**；MetaMask/Bleap/OKX SG/Nexo = No；RedotPay/KAST/Bybit/Crypto.com/Plasma/Karta Unknown | **[U]** | **[U]** | **[U]** | **[U]** | **[U]** |
| **SG** | **[S]** J2 confirmed=3（Bitget、Crypto.com SG、OKX Pay/Card SG）；RedotPay restricted No；MAS MPI 为 OKX SG 监管 wrapper（≠ adoption） | **[P]/[U]** OKX SG 页面声称 stablecoin direct spend / pay stores / pay friends；无 SG 本地 QR/PayNow 专项证据 | **[P]/[U]** MAS MPI 牌照已证；SG 本地 bank/e-wallet rails 细节 Unknown；OKX fee 帮助页 404 | **[P]/[U]** OKX SG “smart wallet until payment / pay stores”点状声明；商户覆盖/资格 Unknown | **[U]** | **[U]** |
| **MX / BR** | **[S]** J2 confirmed=3（Bitget、MetaMask、Bleap）；Bleap eligibility 对 PH/VN 国籍限制 = No（不反向推出 MX/BR 逐国 issuer）；country-level issuance Unknown | **[U]** 无 MX/BR 本地 QR/A2A 证据 | **[U]** Bleap bank-transfer 证据为欧洲/全局口径，非 MX/BR 本地 rails | **[U]** | **[U]** | **[U]** |
| **EEA+UK（聚合）** | **[S]** 聚合口径 confirmed=4（Bitget EEA+UK、MetaMask 大部分 EEA 国（UK 冲突）、Bleap Europe、Nexo Debit）+ J3 Nexo Credit confirmed；KAST 0 国 confirmed；**国别拆分后才能用** | **[S]/[P]** SEPA / SEPA Instant 作为入金/转账 rail 已证（Bleap pricing、KAST EU IBAN）；消费侧 crypto/A2A 份额 Unknown | **[S]/[P]** KAST US/EU account + ACH/SWIFT/Fedwire/SEPA 产品级已证但 **0 国 confirmed**；Bleap SEPA；国家 eligibility Unknown | **[U]** | **[U]** | **[U]** |
| **AR/CL/CO/EC/SV/GT/PA/PE（LATAM-8 聚合）** | **[S]** confirmed=2（Bitget、MetaMask）+ Unknown 7；逐国 issuer 未证 | **[U]** | **[U]** | **[U]** | **[U]** | **[U]** |
| **UY/CR/DO + CA** | **[P]** confirmed=1（MetaMask）；CA 与 LATAM 是不同国家组，需拆分 | **[U]** | **[U]** | **[U]** | **[U]** | **[U]** |
| **KR/JP/MY/CN/TW/TH + ZA + PK/BD** | **[P]** Bitget availability confirmed（physical 子集不同；“issuing partners vary by region”）；其余 Unknown；逐国 issuer 终表未证 | **[U]** | **[U]** | **[U]** | **[U]** | **[U]** |
| **US** | **[N]/[U]** 样本内 card confirmed=0：MetaMask US/UK closed/conflict、RedotPay restricted、ether.fi US states restricted；KAST/Bybit/Crypto.com fee-doc/Plasma/Karta Unknown；**0 confirmed ≠ 市场无人** | **[U]** 无 US 本地 QR/A2A 样本证据 | **[P]/[U]** KAST 产品级 US account + ACH/SWIFT/Fedwire 已证，但 KAST 0 国 eligibility confirmed | **[U]** | **[U]** | **[U]** |

> 读法：矩阵是「已采集证据的结构性覆盖」，不是机会排名；空的 `[U]` cell 是证据边界，不是空白市场；`[S]` 只证明 rail/提供者证据充分，不证明 crypto/stablecoin 使用量或 GTM 收益。

---

## 4. Rail 级结构性读数（AIX-independent，不排序）

1. **Card**：Step 4 14-mode 样本内，PH/AU/SG/MX-BR 与 EEA+UK（聚合）均 ≥3 confirmed J2 提供者；机制多样（X1/X2/X3 × A/B/C，J3 另有 D）。大部分营销覆盖数（150M/180+/170+ 等）只证明 acceptance，不进入 issuance/密度。per-country issuer eligibility 是最大变量。
2. **QR / local A2A**：只有 PH 出现完整证据链（BSP 官方 QR Ph 统计 + Coins.ph QRPH stablecoin 直付 + GCash/Maya 两步 + Alipay+ 国际商户）。QR Ph 交易量是 rail 成熟度，**不是 crypto/stablecoin 份额**（BSP 报告无 crypto 拆分）。
3. **Bank / e-wallet cashout**：PH 是当前唯一有 consumer 级 crypto-adjacent cashout 帮助文档的地区（InstaPay/PESONet/Remittance/OTC/GrabPay）；KAST 的 US/EU bank rails 是产品级能力但 0 国 confirmed；Ledn/YouHodler 是 borrow-to-cash 相邻 off-ramp，无卡消费 rail，PH 资格 Unknown。
4. **Merchant-direct**：样本中唯一 direct-at-merchant consumer 证据是 Coins.ph QRPH Stablecoin Payments；Solana Pay/OpenNode 是 merchant-side 框架（Shopify availability 冲突保留），PH 消费者覆盖 Unknown。direct 与 two-step 严格分开。
5. **Gift / prepaid**：Bitrefill 提供 crypto → gift card/top-up/eSIM/voucher 桥；PH GCash Voucher/GrabMart 目前是 search-page secondary 证据，实时 PH 页 blocked；“170+/186 countries”是营销口径，不等于目录或区域资格。
6. **P2P**：Step 4 将其列为 rail layer（样本 NoOnes 等），但 agent-g / original-D 缓存中 **没有消费者级 crypto→local P2P 的用量、资格或机制证据**；不能把「P2P 概念存在」写成结构性机会。

---

## 5. 硬纪律台账（每个 GTM 结论必须过这一关）

1. **acceptance ≠ product eligibility/issuance**：QR Ph 2.29M 商户/600k+ stores、Bitrefill 170+/186 国、MetaMask 150M、Plasma/Visa 180+、Karta 150M 等一律不进入 eligibility/密度。
2. **regulation ≠ adoption**：BSP-regulated（Coins.ph）、BSP Sandbox（PHPC）、MAS MPI（OKX SG）、MiCA CASP（Bleap）、HK Money Lender's Licence [1715/2025]（RedotPay Credit）是牌照/监管 wrapper，不证明使用量、份额或逐国可服务。
3. **payment-rail adoption ≠ crypto/stablecoin usage**：BSP 数字支付 64.69% 交易量份额、QR Ph 2.47B 笔、P2M 2.93B 笔均无 crypto 拆分；不能倒推 stablecoin 用量。
4. **aggregate region ≠ country exact**：EEA+UK、Europe、MX/BR、LATAM-8、KR/JP/MY/CN/TW/TH+ZA+PK/BD 均为聚合；做 GTM 前必须拆到国家。
5. **Unknown ≠ No；future ≠ current**：Karta Q3 receive/payouts、Bleap future 扩张、MetaMask waitlist、YouHodler Card pre-order、ether.fi VN 冲突、Solana Pay/Shopify 冲突均保留、不裁决、不升级。

---

## 6. 证据强度与 Unknown 清单（按 Region）

| Region | 证据集中点（强） | 最大 Unknown / 未决 |
|---|---|---|
| PH | Card 3 confirmed；QR Ph 官方统计；Coins.ph QRPH 直付；InstaPay/PESONet/Remittance；GCash/Maya 两步；Bitrefill secondary | crypto 份额；QRPH 可用资产清单；PHPC→QR 直付；Bitrefill PH live 目录；P2P/OTC consumer 证据；RedotPay Credit 资格 |
| AU | Card 3 confirmed + ether.fi Borrow available-page 证据 | 全部非卡 rails；逐国 issuer 终表；银行 rails |
| VN | Card 1 confirmed（Bitget）+ ether.fi conflict | ether.fi available-vs-restricted 冲突；其余 rails 全 Unknown |
| SG | Card 3 confirmed；OKX SG 直付声明；MAS MPI | SG 本地 QR/A2A；OKX 费表（帮助页 404）；商户覆盖 |
| MX/BR | Card 3 confirmed；Bleap eligibility（PH/VN No） | 逐国 issuer；本地 rails；Bleap MX/BR bank rails 细节 |
| EEA+UK | Card 4 聚合 + J3 Nexo Credit；SEPA/KAST bank rails 产品级 | 国别拆分；KAST 0 国 confirmed；crypto/A2A 份额；UK MetaMask 冲突 |
| LATAM-8 / UY/CR/DO/CA | Card 1–2 confirmed（MetaMask/Bitget） | 逐国 eligibility；全部非卡 rails |
| KR/JP/MY/CN/TW/TH/ZA/PK/BD | Bitget availability（含 physical 子集差异） | issuer-partner 终表；全部非卡 rails |
| US | KAST US account + ACH/SWIFT/Fedwire 产品级；样本内 card 0 confirmed | KAST 资格；样本外玩家；不能写“蓝海” |

---

## 7. 来源映射（无新 URL）

| 本稿内容 | 来源 |
|---|---|
| 市场边界 / J1/J2/J3 / Rail 分层 | `01-market-overview-and-user-jobs.md`、`04-competition-map.md` |
| X/Y/S1–S6 / Account Role / region 纪律 | `02-ecosystem-map.md` |
| 14-mode 区域矩阵与密度区间 | `04-agent-e-regional-maturity-density.md`；`04-sources.md` |
| Card rails（J1/J2/J3） | `04-agent-a-j1-global-money-card.md`、`04-agent-b-custodial-exchange-prefunded-card.md`、`04-agent-c-self-custody-wallet-native-evidence-card.md`、`04-agent-d-credit-borrow-to-spend-evidence-card.md` |
| 非卡 rails / BSP / direct-vs-two-step | `04-agent-g2-non-card-substitute-rails-evidence-card.md`；`/private/tmp/agent-g-evidence/`（`coinsph-*`、`gcash-*`、`maya-crypto.html`、`bitrefill-docs.html`、`ddg-bitrefill.html`、`solanapay*.html`、`shopify-solanapay.html`、`opennode.html`、`bsp-2025.txt` 等） |
| J3 / Nexo / ether.fi / RedotPay Credit / Ledn / YouHodler | `/private/tmp/aix-j3-evidence-04/`（`nexo-card*`、`nexo-lending*`、`etherfi-personal*`、`redotpay-credit-*`、`ledn-home*`、`youhodler-*`）；`/private/tmp/aix-credit-evidence/`（Step 3 original-D caches）；`03-agent-d-credit.md` |
| 硬纪律（acceptance/regulation/adoption/aggregate） | `04-competition-map.md` §7；`04-sources.md` §3 |

---

## 8. 约束自检

- ✅ 只物化一个文件：`research/aix-market-positioning/evidence/05-agent-d-region-rail-gtm.md`
- ✅ 未联网、未浏览、未新增 URL、未用 apply_patch；文件由 `pathlib.Path.write_text` 写入
- ✅ 未选择 AIX 目标 Region/Product；AIX current geography/capabilities 未过滤任何 cell
- ✅ acceptance ≠ eligibility；regulation ≠ adoption；rail adoption ≠ crypto usage；aggregate ≠ country 逐条落实
- ✅ Unknown ≠ No；future/conflict 保留（ether.fi VN、Solana Pay/Shopify、MetaMask US/UK、BSP 2024 值冲突未引用）
- ✅ direct-at-merchant 与 two-step 未合并；BSP 数字只作 rail 成熟度
- ✅ 来源仅限 Step1–4 正式文档/证据、Step4 region/non-card 证据、agent-g caches、original-D caches

---

## 9. 输出 JSON

```json
{
  "outcome": "PASS",
  "summary": "Step 5 Agent D materialized the region x spend-rail structural-opportunity map under strict Step1-4 + cache-only discipline. Card: PH/AU/SG/MX-BR and EEA+UK-aggregate each show >=3 confirmed J2 providers in the Step4 14-mode sample, with J3 card-credit variants (Nexo EEA+UK, ether.fi Borrow PH/AU, RedotPay Credit PH-Unknown). Non-card rails: PH is the only region with a full evidence stack (BSP QR Ph 2.47B tx / 2.29M merchants / 48 FIs as rail maturity; Coins.ph QRPH stablecoin direct-at-merchant confirmed 2026-08-09; InstaPay/PESONet/remittance cashout; GCash/Maya two-step; Bitrefill voucher secondary; P2P listed but unevidenced in caches). Every other region/rail cell is Partial or Unknown: AU/SG/VN/MX/BR/EEA+UK/LATAM/APAC/US lack cached non-card consumer evidence; US card = 0 confirmed in sample but that is not market absence; KAST bank rails are product-level with 0 countries confirmed. Discipline gates enforced: acceptance != eligibility, regulation != adoption, rail adoption != crypto usage, aggregate region != country exact, Unknown != No; no AIX target region/product selected and current AIX geography/capabilities did not filter any cell.",
  "changedFiles": [
    "research/aix-market-positioning/evidence/05-agent-d-region-rail-gtm.md"
  ],
  "tests": [
    "one-file check: git status --short shows only research/aix-market-positioning/evidence/05-agent-d-region-rail-gtm.md as the new file",
    "source-basis check: every cited fact traces to Step1-4 formal docs/evidence, Step4 region/non-card cards, /private/tmp/agent-g-evidence, or original-D caches (/private/tmp/aix-credit-evidence, /private/tmp/aix-j3-evidence-04); no Step5-Agent conclusions or new URLs used",
    "matrix completeness: all 6 rails x 10 regions/cells have explicit evidence-strength tags (S/P/U/N) and Unknown registry",
    "discipline greps: no AIX target selection, no current AIX geography filtering any cell; acceptance/regulation/adoption/aggregate gates verified",
    "direct-vs-two-step: Coins.ph QRPH direct-at-merchant kept separate from GCash/Maya/Bitrefill two-step paths",
    "marketing-number guardrail: 600k+ stores, 170+/186 countries, 150M merchants, 180+ countries, 5M+/$20B flagged as marketing only",
    "conflict preservation: ether.fi VN available-vs-restricted, Solana Pay Shopify vs Shopify App Store, MetaMask US/UK, BSP 2024 value share left unresolved",
    "JSON validity: embedded output JSON generated via json.dumps and parses",
    "wc -l and tail -10 printed after write"
  ],
  "commands": [
    "python3 pathlib.Path(...).write_text(...) to materialize exactly one file",
    "wc -l research/aix-market-positioning/evidence/05-agent-d-region-rail-gtm.md",
    "tail -10 research/aix-market-positioning/evidence/05-agent-d-region-rail-gtm.md",
    "git status --short (read-only verification of single-file change)"
  ],
  "decisionsRequired": [
    "Resolve country-level eligibility before any GTM region/rail density use: KAST/Bybit/Plasma/Karta (0 countries confirmed), Crypto.com beyond SG/AU, RedotPay beyond PH, and issuer-partner final tables for Bitget",
    "Resolve ether.fi VN available-vs-restricted conflict and MetaMask US/UK signup conflict before per-country card reads",
    "Decide whether P2P/OTC (NoOnes 等) stays in Step 5 GTM scope without consumer-level evidence, or is explicitly marked Unknown-only",
    "Decide whether BSP QR Ph / digital-payment statistics may be used in GTM only as rail maturity, never as crypto/stablecoin adoption or spend share",
    "Perform country-level split for EEA+UK, Europe, MX/BR, LATAM-8, and APAC aggregate rows before any per-country GTM planning",
    "Re-collect or close PH non-card gaps if they become GTM-critical: Coins.ph QRPH eligible asset list, PHPC-to-QRPH direct spend, Bitrefill PH live catalog, GCash Send/Receive crypto article, Maya send/receive timing, SolanaPay/OpenNode merchant coverage",
    "Keep AIX current geography/capabilities out of opportunity filtering; target selection belongs to Step 5 main decision layer"
  ],
  "requiresGptReview": true
}
```
