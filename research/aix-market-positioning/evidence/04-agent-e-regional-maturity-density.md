# Step 4 Agent E｜区域可用性 × 产品成熟度 × 竞争密度地图（市场级）

> 状态：Step 4 Agent E **修复稿 v2（2026-08-30）**。
> 旧稿结论（作废）：同日初稿以 PH/VN/AU 作为主读数，L1/L2/L3 与密度读数均按 AIX 现行地区（Wallet Deposit = PH、Card Phase 1 = PH/VN/AU）组织，违反 Step 4「AIX 仅未来进入者、不得用 AIX 现行地理决定主要市场」纪律。本稿取代初稿；初稿结论不再作为当前输入。
> 类型：Step 4 输入地图；**不定义 AIX 的当前或目标生态位**；不替代 Step 4 主文档 `04-competition-map.md` 的 R1–R5 分类。
> 证据边界：只汇编 Step 1–3 已确认结论与 `evidence/03-agent-a–f-*.md`、`evidence/03-sources.md` 中已记录官方证据；**不联网、不新增 URL、不补抓**。
> 判定口径承接：Step 3 的 four-AND 结果、Unknown 纪律与 X/Y/S1–S6 定义原样沿用，不重算、不升级。

---

## 0. 市场级读法

| 读法 | 问题 | 判定纪律 |
|---|---|---|
| **L1 玩家×区域可用性** | 每个玩家 mode 当前在哪些区域有已证实服务/发卡资格？ | 按玩家逐区域记录 confirmed / No / Unknown；unlisted ≠ No；merchant acceptance、100+ / 170+ / 180+ / 150M 等全球数字一律不作为 issuance 依据 |
| **L2 产品成熟度** | 该产品机制与功能有多确定？ | Live（current 产品） / Emerging（live 但关键事实冲突或功能未完） / Future（coming soon，不视为 current）；机制、区域证据强度、账户闭环、费表四维评分 |
| **L3 竞争密度** | 同一市场 × 同一 segment 有几个可替代提供者？ | 只按已证实 footprint 数 confirmed；unknown-eligible 单列；密度区间 = confirmed .. (confirmed + unknown)；不用任何 AIX 区域作为主市场 |

---

## 1. AIX 当前事实（仅 future-entrant 输入，不参与本图判定）

- AIX 完整 `stablecoin → AIX → card spend` journey 当前最强确认地域 = PH；Wallet Crypto Deposit = PH；Card Phase 1 = PH/VN/AU；VN/AU 完整 journey = Unknown（`03-agent-f-aix-anchor.md`）。
- AIX 机制锚点：X1 confirmed / Y Unknown / Species Unknown / Account Role 最多 Account-adjacent / J3 unsupported。
- **本图用途**：以上事实只作为「AIX 是未来进入者」的参考输入，**不进入 L1/L2/L3 判定**；本文件所有「已证实市场」均来自竞品官方证据并集，与 AIX 是否在这些地区开展业务无关。
- Step 3 的 Direct candidate（RedotPay / Bitget Wallet Card / ether.fi Direct Pay）是相对 AIX 的证据级判定，本图不重算、不引用为市场级分类。

---

## 2. L1 玩家×区域可用性（按玩家，市场级）

| 玩家 / mode | 已证实可服务/可发卡（evidence-confirmed） | 明确不支持（confirmed No） | 其余区域（unlisted = Unknown） |
|---|---|---|---|
| **RedotPay** generic auto-convert card | **PH**（Card Issuance Restrictions 不含 PH；受通用 onboarding/KYC 约束） | US、SG、Indonesia、India、Türkiye、Morocco、mainland China 等约 49 个 restricted 地区（Step 2 列出的示例，完整列表未转录） | VN/AU 等其余区域 Unknown |
| **KAST** | **0 个国家 confirmed**（仅 signup dropdown 检查；无逐国列表） | 无国家级 No（restricted 逻辑无公开列表） | 所有区域（含 PH/VN/AU）Unknown |
| **Bitget Wallet Card** | 官方 availability 条目：EEA+UK（合并）；LATAM AR/BR/CL/CO/EC/SV/GT/MX/PA/PE（10）；APAC SG/KR/JP/VN/MY/mainland CN/TW/AU/TH/PH（10）；ZA；PK/BD。Physical card 子集：SG/KR/JP/VN/MY/TW/AU/TH/PH | 无 certified No（issuing partners vary by region） | 列表外区域 Unknown |
| **Bybit Card** | **0 个国家 confirmed**（programs：AR/BR/AIFC/Asia Pacific/MX + “Australian Users” 标题；不足为逐国证据） | 无 | 全部 Unknown |
| **Crypto.com Card** | **SG、AU 两个 region-specific product modes confirmed** | 无国家 No（US/UK/CA/EU/BH+GCC 仅 fee/limits 文档族，≠ issuance list） | 其余（含 PH）Unknown |
| **MetaMask Card** | **45 国 current list**（Andorra、AR、AT、BE、BR、BG、CA、CL、CO、CR、HR、CY、DK、DO、SV、FI、FR、DE、GI、GR、GT、GG、HU、IS、IE、IM、IT、JE、LI、LU、MT、MC、NL、NO、PA、PL、PT、RO、SK、SI、ES、SE、CH、UY） | PH/VN/AU 不在 current list → **No**；US/UK signup temporarily closed（与 Metal Card 文案冲突，不裁决） | 列表外区域 No；waitlist 区域为 Future |
| **Plasma One** | **0 个国家 confirmed**（issuance/service country list 未公布；Bridge US/EEA/other residents ≠ 国家列表） | 无 | 全部 Unknown（180+ countries 仅 acceptance，不进入 issuance） |
| **Bleap** | **Europe（聚合）、MX、BR confirmed** | PH/VN/AU 不在 current → **No**；未列入 current 区域按 current list 判 No；扩展为 Future | Europe 内部国家列表与扩展区域未拆 |
| **Karta** | **0 个国家 confirmed**（service country list 未公布） | 无 | 全部 Unknown（150M merchants 不进入 issuance） |
| **OKX Pay/Card SG** | **SG mode confirmed** | 非 SG 区域不适用（仅 SG mode） | SG 内 issuance/issuer 细节 Unknown |
| **ether.fi Direct Pay** | **PH、AU**（available countries 页） | 无 | VN 为 registered conflict（available vs restricted，不裁决）；其余 listed jurisdictions 未转录 → Unknown；US states listed restricted |
| **ether.fi Borrow** | **PH、AU**（available 页；J3 mode） | 无 | VN 同页 conflict 不裁决；其余 Unknown |
| **Nexo Debit** | **EEA+UK**（areaServed 明确；DiPocket UAB 发行） | EEA+UK 外 **No** | — |
| **Nexo Credit** | **EEA+UK**（areaServed 明确） | EEA+UK 外 **No** | — |

**不能从本表推出的结论：**
- 50+ / 100+ / 170+ / 180+ / 150M 不进入任何 issuance 判定。
- unlisted ≠ No；只有官方 current 列表/areaServed 明确时，缺席才是 No（MetaMask、Bleap、OKX SG、Nexo 属于此类）。
- EEA+UK / Europe / LATAM 是聚合区域，逐国拆分后才能做精确 per-country 密度。
- 本表只覆盖 Step 3 评审纳入的 14 个 product modes；区域 confirmed 为 0 不代表该市场没有其他玩家。

---

## 3. L2 产品成熟度矩阵（市场级）

> 成熟度档次：**T1 Live / 机制较确定**；**T2 Live / 关键事实待核**；**T3 Future / 不视为 current**。

| 玩家 / mode | Live 状态 | 机制确定性 | 市场级地区证据强度 | Account Role | 费表透明度 | 档次 |
|---|---|---|---|---|---|---|
| **RedotPay** generic card | Live | **S2（X2×B）confirmed**；卡费 Virtual $10 / Physical $100 已证 | 1 国 confirmed（PH）+ ~49 restricted；其余 Unknown | Spend Feature / Account-adjacent | 卡费已证；完整 FX/ATM/limits 未证 | **T1**（地区 + 费表缺口） |
| **Bitget Wallet Card** | Live | **Y=A confirmed / X Unknown / S1 candidate only** | 官方 availability 覆盖 EEA+UK / LATAM 10 / APAC 10 / ZA / PK+BD；issuer 终表未证 | Spend Feature | opening/annual 0 已证；完整 top-up/FX/ATM 未证 | **T1**（X 缺口） |
| **Bybit Card** | Live（program 级） | **S2（X2×B）confirmed** | 0 国 confirmed | Spend Feature | 未证 | **T1**（地区缺口） |
| **Crypto.com Card** | Live（region-specific） | **S1（X1×A）confirmed**（SG/AU modes） | SG/AU confirmed；逐国列表未证；stablecoin 起点池未证 | Spend Feature | SG residential 费表已证；其他地区未证 | **T1/T2** |
| **MetaMask Card** | Live（部分区域；US/UK temporarily closed） | **S5（X3×B）confirmed**；stablecoin mode S4 candidate | 45 国 confirmed；PH/VN/AU No；US/UK 文案冲突 | Spend Feature（Card mode） | 完整费表未证 | **T1/T2** |
| **Plasma One** | Live（残留 waitlist 文案冲突已记录） | **S4（X3×C）较强**；unified/same-balance 未钉死 | 0 国 confirmed | Money Account-leaning | Plasma fees 0 claim；partner fees 未完整 | **T2** |
| **Karta** | **Emerging**（card/top-up/send live；receive/payouts future） | **Y=A confirmed / X Unknown / S4 direction–S1 candidate boundary** | 0 国 confirmed | Account-adjacent（Money Account 不成立） | activation/消费/ATM 费率已证；bank rails future 不生效 | **T2** |
| **Bleap** | Live（Europe/MX/BR） | **S4（X3×C）**；MPC wallet + EURA/USDC spendable balance | 3 个区域 confirmed（Europe 为聚合） | Money Account-leaning | adding/converting/spend free 已证；完整表未证 | **T2** |
| **OKX Pay/Card SG** | Live（SG mode） | **S4（X3×C）沿用 Step 2** | 1 国 confirmed | Spend Feature / Account-adjacent | 营销 “no fees” 仅 snapshot 证据；完整表未证 | **T2** |
| **KAST** | Live | **X2 confirmed / Y Unknown（C vs D 官方冲突）/ Cluster Unknown**；Money Account 结构强 | 0 国 confirmed | **Money Account** | 卡费/FX/ATM/limits 大体已证；Y 冲突未决 | **T2** |
| **ether.fi Direct Pay** | Live | **S4 candidate（X3×C）**；non-custodial claim + Vault direct deduction | PH/AU available-page confirmed；VN conflict；其余未转录 | Unknown / Account-adjacent candidate | Direct Pay 无利息 claim；完整消费费表未证 | **T2** |
| **ether.fi Borrow** | Live | **S6 onchain candidate（X3 candidate × D）**；collateral/LTV 已证 | PH/AU available-page confirmed；VN conflict | — | 借息/LTV 已证；完整消费者费表未证 | **T2** |
| **Nexo Debit** | Live（EEA+UK） | **X2 confirmed / Y Unknown** | EEA+UK confirmed；其余 No | Spend Feature at most | FX/ATM/activation 部分已证 | **T1**（地区 No） |
| **Nexo Credit** | Live（EEA+UK） | **X2×D / S6-Custodial confirmed** | EEA+UK confirmed；其余 No | Spend Feature at most | 部分已证；card-mode borrow 参数未证 | **T1**（地区 No） |
| Karta receive/payout、Bleap expansion、MetaMask waitlist regions、Plasma 残留 waitlist copy | **Future / 不视为 current** | — | — | — | — | **T3** |

---

## 4. L3 竞争密度地图（市场 × segment）

> 密度只统计**消费市场内、有现实购买力产出的 product mode**（card / direct spend）；同一品牌多 mode 可重复计数；J3（ether.fi Borrow、Nexo Credit）单列。市场行按「已证实提供者」从市场证据并集生成，**与 AIX 是否进入无关**。

### 4.1 按市场（J2 stablecoin/crypto-starting card segment；14-mode 样本内）

| 市场 | 确认密度（confirmed） | Unknown 潜在（unknown-eligible） | 明确不在（No） | 密度区间 |
|---|---|---|---|---|
| **PH** | **3**：RedotPay generic card、Bitget Wallet Card、ether.fi Direct Pay | **5**：KAST、Bybit、Crypto.com、Plasma One、Karta | **5**：MetaMask、Bleap、OKX SG、Nexo Debit、Nexo Credit | **3 – 8**（J3：ether.fi Borrow confirmed） |
| **AU** | **3**：Bitget Wallet Card、Crypto.com AU mode、ether.fi Direct Pay | **5**：RedotPay、KAST、Bybit、Plasma One、Karta | **5**：MetaMask、Bleap、OKX SG、Nexo Debit、Nexo Credit | **3 – 8**（J3：ether.fi Borrow confirmed） |
| **VN** | **1**：Bitget Wallet Card | **7**：RedotPay、KAST、Bybit、Crypto.com、Plasma One、Karta + ether.fi Direct Pay（available-vs-restricted **conflict**，不裁决） | **5**：MetaMask、Bleap、OKX SG、Nexo Debit、Nexo Credit | **1 – 8**（J3：ether.fi Borrow conflict 未决） |
| **SG** | **3**：Bitget Wallet Card、Crypto.com SG mode、OKX Pay/Card SG | **5**：KAST、Bybit、Plasma One、Karta、ether.fi Direct Pay | **5**：RedotPay（restricted 含 SG）、MetaMask、Bleap、Nexo Debit、Nexo Credit | **3 – 8**（J3：ether.fi Borrow Unknown） |
| **EEA+UK（聚合）** | **4（粒度待拆）**：Bitget（EEA+UK）、MetaMask（大部分 EEA 国；UK 冲突）、Bleap（Europe 聚合）、Nexo Debit | **7**：RedotPay、KAST、Bybit、Crypto.com（fee 文档族）、Plasma One、Karta、ether.fi Direct Pay | **1**：OKX SG | **4 – 11**（J3：Nexo Credit confirmed；ether.fi Borrow Unknown；国别拆分后调整） |
| **MX / BR** | **3**：Bitget、MetaMask、Bleap | **7**：RedotPay、KAST、Bybit、Crypto.com、Plasma One、Karta、ether.fi Direct Pay | **3**：OKX SG、Nexo Debit、Nexo Credit | **3 – 10**（J3：ether.fi Borrow Unknown） |
| **AR / CL / CO / EC / SV / GT / PA / PE** | **2**：Bitget、MetaMask | **7**：RedotPay、KAST、Bybit、Crypto.com、Plasma One、Karta、ether.fi Direct Pay | **4**：Bleap、OKX SG、Nexo Debit、Nexo Credit | **2 – 9**（J3：ether.fi Borrow Unknown） |
| **UY / CR / DO、CA** | **1**：MetaMask | **8**：RedotPay、KAST、Bitget、Bybit、Crypto.com、Plasma One、Karta、ether.fi Direct Pay | **4**：Bleap、OKX SG、Nexo Debit、Nexo Credit | **1 – 9**（J3：ether.fi Borrow Unknown） |
| **KR / JP / MY / CN / TW / TH、ZA、PK / BD** | **1**：Bitget Wallet Card | **7**：RedotPay、KAST、Bybit、Crypto.com、Plasma One、Karta、ether.fi Direct Pay | **5**：MetaMask、Bleap、OKX SG、Nexo Debit、Nexo Credit | **1 – 8**（J3：ether.fi Borrow Unknown） |
| **US** | **0 confirmed（样本内）** | **5**：KAST、Bybit、Crypto.com（fee 文档族）、Plasma One、Karta | **7**：RedotPay（restricted）、MetaMask（closed/conflict）、Bleap、OKX SG、Nexo Debit、Nexo Credit、ether.fi Direct Pay（US states restricted） | **0 – 5**（J3：ether.fi Borrow Unknown；样本缺失 ≠ 市场无玩家） |

> 行内计数核对：每行 confirmed + unknown + No + J3 单列 = 14 modes（M1–M14）。

### 4.2 按用户 segment（市场级）

| Segment | 已证实提供者（市场 × mode） | 说明 |
|---|---|---|
| **J2 stablecoin/crypto-starting card spend** | PH 3、AU 3、SG 3、MX/BR 3、EEA+UK 4（粒度待拆）、AR/CL/CO/EC/SV/GT/PA/PE 2、VN 1（+conflict）、KR/JP/MY/CN/TW/TH/ZA/PK/BD 1、UY/CR/DO/CA 1、US 0 | 最高 confirmed 密度出现在多个市场；不因 AIX 地理而设主市场 |
| **J1 stablecoin money account** | 0 个「Money Account confirmed × region confirmed」组合（KAST role confirmed 但 0 国 confirmed；Plasma/Bleap leaning 未钉） | 这是证据空白，不是「无玩家」结论 |
| **J3 credit / borrow（不卖币）** | Nexo Credit 在 EEA+UK confirmed；ether.fi Borrow 在 PH/AU available-page confirmed（VN conflict）；RedotPay Credit 邻接 Unknown | 与 J2 消费簇不重叠；AIX J3 unsupported（仅 future-entrant 输入） |

### 4.3 按策略簇（mode-level，全球证据计数）

| 策略簇 | 已确认 / 当前样本 | 候选 / 边界样本 | 密度读数 |
|---|---|---|---|
| **S1 Pre-funded balance** | Crypto.com（SG/AU region modes，confirmed） | Bitget（S1 candidate only，X Unknown）、Karta（Y=A / X Unknown，S1-candidate boundary） | 1 confirmed + 2 candidate |
| **S2 Custodial instant-convert** | RedotPay、Bybit（2 confirmed） | — | 2 |
| **S3 Custodial stable-value** | **0 confirmed**（KAST Y Unknown 后不硬归 S3） | KAST（Step 2 历史 S3 → Step 3 降级 Unknown） | 0 confirmed，KAST 待厂商澄清 |
| **S4 Self-custody stable-value** | Plasma One（强）、Bleap（current）、OKX SG（Step 2/3） | ether.fi Direct Pay（candidate）、Karta（direction） | 3 current + 2 candidate |
| **S5 Self-custody instant-convert** | MetaMask（1 confirmed） | — | 1 |
| **S6 Crypto-backed credit** | Nexo Credit（custodial，confirmed） | ether.fi Borrow（onchain candidate）、RedotPay Credit（adjacent，非独立 four-AND row） | 1 confirmed + 2 candidate |

### 4.4 密度读数（市场级，AIX 不参与）

1. **已证实提供者 ≥3 的市场**：PH、AU、SG、MX/BR、EEA+UK（J2 card segment）。这是 RedotPay / Bitget / Crypto.com / OKX / MetaMask / Bleap / Nexo / ether.fi 官方证据并集的结果，与 AIX 在这些地区是否经营无关；没有任何市场被本图指定为“primary”。
2. **只有 1 个 confirmed 的市场**：VN（+ether.fi conflict）、KR/JP/MY/CN/TW/TH、ZA、PK/BD、UY/CR/DO、CA。这些市场的密度上限取决于逐国 eligibility 文档，不是营销覆盖数。
3. **VN 是唯一同时存在 confirmed 与官方 available-vs-restricted conflict 的市场**（ether.fi 两 mode 同页冲突，不裁决）。
4. **0 国 confirmed 的玩家**（Bybit、KAST、Plasma One、Karta）+ 仅 1 国 confirmed 的 RedotPay + 仅 SG/AU confirmed 的 Crypto.com，构成全图最大的“未知 footprint”变量。
5. **J1 money account 在样本内没有任何 confirmed role × confirmed region 组合**；J3 credit 是独立成熟簇（Nexo Credit EEA+UK、ether.fi Borrow PH/AU、RedotPay Credit 邻接）。
6. **US 在样本内 confirmed 为 0 或关闭/受限**（MetaMask closed、RedotPay restricted、ether.fi US states restricted）；不得把样本缺失写成“市场无玩家”。

---

## 5. 决定密度与成熟度的关键变量（市场级）

1. **逐国 issuance/service eligibility**：KAST、Bybit、Plasma One、Karta（0 国 confirmed）、Crypto.com（SG/AU 以外）、RedotPay（PH 以外）的资格文档决定各市场密度上限。
2. **聚合区域拆分**：EEA+UK、Europe、LATAM 需拆到国家后再做精确 per-market 密度；Bitget “issuing partners vary by region” 意味着其 24 条目是 availability 证据而非 issuer 终表。
3. **KAST Y 冲突（C vs D）**：决定 KAST 归 S3 还是 S6 机制簇，改变 PH/全球密度构成（数量不变，构成变）。
4. **ether.fi available vs restricted 页在 VN 的冲突**：决定 VN 密度从 1 升到 2（或维持 1）。
5. **Crypto.com stablecoin→card load 起点池**：若在同一地区证明成立，会把它从 Unknown 升为 J2 segment 提供者。
6. **Karta Q3 2026 receive/payout**：若上线并公开 service country list，将改变其成熟度与各市场密度。
7. **完整费表**：RedotPay / Bitget / ether.fi 等 FX / ATM / top-up / withdrawal 费表未证，当前密度无法按成本加权。

---

## 6. 证据缺口与 Step 4 主文档核验问题

1. KAST / Bybit / Plasma One / Karta 的 service/issuance country list（0 国 confirmed）。
2. Crypto.com 在 SG/AU 以外的逐国资格；RedotPay 在 PH 以外的逐国资格；Bitget 的 issuer-partner 终表。
3. EEA+UK / Europe / LATAM 聚合区域的国别拆分。
4. MetaMask US/UK signup 状态的矛盾文案（closed vs Metal Card available）；Plasma waitlist copy 与 unified/same-balance。
5. KAST card 购买力机制官方冲突（C vs D）——需要厂商澄清或更高层级官方页。
6. ether.fi available vs restricted 页在 VN 的冲突。
7. Bitget top-up 后的资金容器（X = X1 vs X2）。
8. Crypto.com 的 stablecoin 起点 → card load 路径。
9. RedotPay / Bitget / ether.fi Direct Pay 完整费表与 limits。
10. OKX SG 需要 2026-08-29 后最新 live 页复核（上轮直连超时）。
11. Karta receive/payout 上线时间；Bleap Europe 国家明细。

---

## 7. 约束自检

- ✅ **市场级主读数**：L1/L2/L3 与密度读数不再以 PH/VN/AU 为锚；AIX 事实只在 §1 作 future-entrant 输入，不参与任何判定。
- ✅ 已证实市场全部来自竞品官方证据并集；不存在「AIX 支持哪些地区所以哪些地区重要」的推导。
- ✅ Unknown ≠ No；unlisted ≠ No；KAST / Bybit / Plasma / Karta 等保持 Unknown。
- ✅ Future 未当 current：Karta receive/payout、Bleap expansion、MetaMask waitlist regions、Plasma 残留 waitlist copy 均标 T3。
- ✅ merchant acceptance / 100+ / 170+ / 180+ / 150M 未进入 issuance 判定。
- ✅ 未联网、未新增 URL、未补抓；所有论断可回溯到 Step 1–3 证据文件。
- ✅ 本文件不替代 Step 4 主文档的 R1–R5 竞争分类。

---

## 8. 来源映射（仅本地证据文件，无新 URL）

| 本文件内容 | 来源 |
|---|---|
| RedotPay / KAST 全部行 | `evidence/03-agent-a-redotpay-kast.md`；`evidence/03-sources.md` R/K 索引 |
| Bitget / Bybit / Crypto.com | `evidence/03-agent-b-custodial-cards.md`；`evidence/03-sources.md` B/By/C 索引 |
| MetaMask / Plasma / Bleap / Karta / OKX SG | `evidence/03-agent-c-self-custody.md`；`evidence/03-sources.md` 对应索引 |
| ether.fi / Nexo | `evidence/03-agent-d-credit.md`；`evidence/03-sources.md` E/N 索引 |
| AIX 当前事实（仅 future-entrant 输入，未用作锚点） | `evidence/03-agent-f-aix-anchor.md`；`evidence/02-agent-f-aix-current-position.md` |
| 市场边界 / Job / 规模分层 | `01-market-overview-and-user-jobs.md` |
| X/Y/S1–S6 / Account Role 定义 | `02-ecosystem-map.md` |
| four-AND 直接候选与 Unknown 纪律 | `03-player-positioning.md`；`evidence/03-agent-e-crosscheck.md` |
| Step 4 边界提示 | `reviews/03-grok46-review.md`（Residual risks 1–6） |

---

## 9. 输出 JSON

```json
{
  "outcome": "PASS",
  "summary": "Repaired Agent E's Step 4 region/maturity/density map from a PH/VN/AU-anchored analysis to a market-level one. The PH/VN/AU-centric draft is superseded: L1 now records each player's evidence-confirmed footprint (Bitget 24 region entries, MetaMask 45-country current list, Bleap Europe+MX/BR, ether.fi PH/AU available-page with VN conflict, RedotPay PH confirmed via restricted-list absence, KAST/Bybit/Plasma/Karta with 0 confirmed countries); L3 density is rolled up per market from competitor evidence only, so PH, AU, SG, MX/BR and EEA+UK each show >=3 confirmed J2 providers, VN shows 1 confirmed plus a contested ether.fi cell, and US shows 0 confirmed within the 14-mode sample. AIX facts appear only as future-entrant input and no current AIX geography (Wallet deposit PH, Card Phase 1 PH/VN/AU) determines which markets are primary or any density reading. Maturity tiers, Unknown != No, future-not-current, merchant-acceptance exclusion and no-new-URL guardrails were re-verified; no AIX current/target positioning statement was introduced.",
  "changedFiles": ["research/aix-market-positioning/evidence/04-agent-e-regional-maturity-density.md"],
  "tests": [
    "market-level primary scan: no PH/VN/AU-centric density reading remains; PH/AU appear only as rows in the market roll-up",
    "every confirmed region cell traced to Step 1-3 evidence files (no new URLs or invented facts)",
    "count reconciliation: each market row sums to the 14-mode sample (confirmed + unknown + No + J3 single-listed); PH 3-8, AU 3-8, VN 1-8 with contested ether.fi, SG 3-8, EEA+UK 4-11, MX/BR 3-10, LA-8 2-9, remaining single-provider markets 1-8/1-9, US 0-5",
    "AIX guardrail scan: AIX geography used only in the future-entrant input section; no L1/L2/L3 judgment depends on it",
    "Unknown != No discipline check on KAST/Bybit/Plasma One/Karta and all unlisted regions",
    "merchant acceptance exclusion check: 100+/170+/180+/150M claims not used as issuance evidence",
    "live vs future check: Karta Q3 2026 receive/payouts, Bleap expansion, MetaMask waitlist regions and Plasma waitlist copy remain non-current",
    "JSON self-check: embedded JSON matches final response fields"
  ],
  "commands": [],
  "decisionsRequired": [
    "Obtain country-level issuance/service eligibility for KAST, Bybit, Plasma One and Karta (all currently 0 confirmed markets), plus Crypto.com beyond SG/AU and RedotPay beyond PH",
    "Break EEA+UK/Europe/LATAM aggregates into country-level lists (incl. Bitget issuer-partner final table) before exact per-market density",
    "Resolve KAST card mechanism source conflict (C vs D) via official product-level confirmation",
    "Resolve ether.fi available-vs-restricted page conflict for Vietnam",
    "Prove or close Crypto.com stablecoin-starting pool -> card load path before counting it in the J2 segment",
    "Track Karta receive/payout (Q3 2026) and service-country list, and Bleap Europe country list, as re-check points",
    "Collect full fee/FX/ATM/limit tables for RedotPay, Bitget and ether.fi Direct Pay before any cost-weighted density comparison",
    "Decide how Step 4 main doc treats MetaMask US/UK signup contradiction and Plasma One's residual waitlist copy / unified-balance unproven detail"
  ],
  "requiresGptReview": true
}
```
