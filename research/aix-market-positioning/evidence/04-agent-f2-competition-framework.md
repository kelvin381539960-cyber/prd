# Step 4 Agent F2｜独立市场级竞争关系框架与模式级应用（Cross-check）

> 状态：Step 4 Agent F2 独立交付稿（2026-08-30）。
> 类型：方法论 / 交叉检验 agent。**不以任何 AIX 事实为锚点**构建市场级竞争关系框架；框架先独立成立，再应用到已观察产品 mode，最后对 `04-competition-map.md` 主文档做独立核验。
> 证据边界：只使用 Step 1–3 已评审结论与 `evidence/03-*.md` 记录的事实；不联网、不新增 URL、不引入新事实、不把推测写成事实。
> 边界声明：本文件**不是** AIX 战略 agent，不给出 AIX 当前或目标生态位。

---

## 0. 身份与方法边界（为什么独立）

F2 判定「任意两个市场玩家 mode 之间是否竞争、以何种方式竞争」。为做到这一点，框架必须**先于任何品牌存在**：竞争关系的定义不能依赖 AIX 是否存在、AIX 落在哪个 cell、AIX 与谁同段。

约束：

1. 判定单元是 product mode（同一品牌可多 mode，mode 之间才算关系）。
2. 市场级关系对所有玩家 mode 对成立，与 AIX 无关；AIX 不得反向改写任何玩家落位与 Unknown。
3. 关系必须有证据可达：D 维度落到 Step 1–3 已确认结论；Unknown 不得补全、不得升级、不得降级为 No。
4. 区域资格是**门**，不是营销话术：merchant acceptance / 100+ countries / 150M merchants 不参与任何区域判定。

---

## 1. 框架从哪里来（First-principles 推导，不引用任何品牌）

### 1.1 需要回答的问题

市场级竞争关系要回答三件事：

- **同一用户的钱，能不能被另一个产品以等效方式变成同样的现实购买力？**（结果替代）
- **即使结果相同，用户切换是否会产生额外成本或心智差异？**（切换摩擦，来自钱放在哪、购买力怎么产生、账户角色）
- **现在能不能判定，还是证据只够说「可能」？**（证据三态纪律）

### 1.2 为什么用「消费前价值容器」和「购买力形成机制」

从用户视角，一笔现实消费可以拆成四个独立环节：

1. **消费前，钱停留在什么形态 / 位置**（用户自己的链上钱包、产品托管的通用余额、独立卡余额）；
2. **购买力如何产生**（预先充值、付款时转换、直接扣稳定价值、抵押借贷）；
3. **用户带着什么资产、什么 Job 进入产品**（已持有稳定币 / 波动币；要「钱」、要「消费」、要「不卖币」）；
4. **最终拿到了什么现实结果**（卡消费 / 直接支付 / 转账形成的购买力）。

这四个环节只要有一个在证据上不同，竞争关系就不是「直接替代」，而是相邻、结果替代或潜在。**产品营销话术（「全球账户」「self-custody」）不进入框架**，只进入证据核对。

### 1.3 为什么区域必须单独成门

两个产品即使四个环节完全相同，若不在同一个可服务市场，用户仍不可能在二者间选择。因此：

- 共同市场 = 双方在**至少一个相同地理市场**的 issuance/service 资格均有证据（confirmed）；
- 任一方 Unknown → 共同市场 Unknown → 关系降为 potential（R4）；
- 任一方明确 No（且无其他已证共同市场）→ 当前市场关系关闭（R5 或 R3c 仅作全球最弱读法，不升级为 confirmed）。

---

## 2. 市场级替代维度（D1–D4，F2 定义）

| 维度 | 名称 | 判定问题 | 三态 |
|---|---|---|---|
| **D1** | 消费前价值容器重合度 | 消费发生时，用户价值驻留在同一/可互换容器类别（X1 / X2 / X3）吗？ | Same / Different / Unknown |
| **D2** | 购买力形成机制重合度 | 购买力由同一/可替代机制形成（Y=A/B/C/D 同簇）吗？ | Same / Different / Unknown |
| **D3** | 用户起点与 Job 重合度 | 双方服务的 starting money pool 与主要 Job family（J1/J2/J3）重叠吗？ | Same / Different / Unknown |
| **D4** | 最终现实结果替代度 | 双方最终产出的现实购买力结果（card spend / direct spend）可替代吗？ | Same / Different / Unknown |

规则：

- D 维度判定只看证据：Same 需要该维度的确认证据；Different 需要该维度的明确差异证据；其余一律 Unknown。
- 「Same」语义 = 同一类别或证据上可互换；「Different」不要求完全相反，只要求框架维度不同。
- D3 由「starting money pool × 主要 Job」复合决定；同一 Job 但起点池不同 → Different。

---

## 3. 市场级竞争关系类型（R1–R5，F2 定义）

| 关系 | 名称 | 判定条件 | 门禁 |
|---|---|---|---|
| **R1** | Direct Substitute（直接替代） | D1 Same/可互换 **且** D2 Same/可替代 **且** D3 Same **且** D4 Same | **共同市场 confirmed（双方至少一个相同市场资格均已证实）**。缺门禁 → R1-cluster candidate（同簇候选），不得写 R1-confirmed |
| **R2** | Adjacent / Neighbor（相邻） | D3 Same；D1 或 D2 至少一项 Different；D4 Same/等效 | 至少存在 plausible 共同市场（不是双方在所有已知市场均 No）；否则 R4/R5 |
| **R3** | Outcome-substitute / Rail-substitute（结果替代） | D4 Same/等效；D1 或 D2 或 D3 至少一项 Different | 同上（plausible 共同市场）；区域不重合时仅作最弱候选 R3c，不视为 confirmed |
| **R4** | Potential / Future（潜在） | 任一 D 维度 Unknown；或共同市场 Unknown；或同簇但无共同市场已证 | 无 |
| **R5** | Out of Scope / Complement（范围外/互补） | D4 不等效；或属于另一市场边界（J3 credit vs J1/J2 消费；纯交易所 / 纯 Earn / 纯 B2B）；或双方在所有已知市场均 No | 无 |

与 Step 3 four-AND 的区别：

- Step 3 four-AND 只回答「某 player 是否 direct 于 AIX」（AIX 比较锚，4 项全 Yes → Direct，任一 Unknown → Unknown，任一 No → Not Direct）；
- Step 4 R1 回答「任意两个市场玩家 mode 之间」的替代（无 AIX 锚），并要求**共同市场门禁**才能 confirmed。
- R3 是 Step 4 新增的市场级关系，不来源于 four-AND；R3 不等于 four-AND Direct。

**关系等级**：`R1-cluster candidate`（四个维度同簇） → `R1-confirmed`（再满足共同市场 confirmed） → `R2/R3`（维度差分 + 门禁） → `R4`（Unknown 主导） → `R5`（范围外）。

---

## 4. 应用到产品模式（14 个 mode，无 AIX 参与）

> 输入全部来自 Step 3 已评审结论（`03-player-positioning.md`、`evidence/03-agent-a..d.md`、`03-agent-e-crosscheck.md`）。下表是 F2 独立应用结果，不是新事实。

| ID | 玩家 / mode | X×Y（证据态） | Account Role | Job（inference） | 区域证据 vs PH | F2 关系指纹 |
|---|---|---|---|---|---|---|
| M1 | RedotPay generic auto-convert card | X2(c)×B(c) | Spend Feature / Account-adjacent | J2 primary | PH confirmed；VN/AU Unknown | D1=D2=D3=D4 Same；对 M4 为 R1-cluster candidate（区域门缺失）；对 M3/M11 为 R2/R3 candidate（PH 共市场已证，但 D1/D2 有差/Unknown） |
| M2 | KAST Card/Global Account | X2(c)×Y Unknown | Money Account | J1 primary；J2 secondary | PH Unknown | D2 Unknown → 对所有 card modes R4；账户极带来高切换摩擦（不改变关系等级） |
| M3 | Bitget Wallet Card | X Unknown×A(c) | Spend Feature | J2 primary | PH/VN/AU confirmed | D1 Unknown → 对 M1/M11 R2/R3 candidate；X 补证后可评估 R1-cluster |
| M4 | Bybit Card | X2(c)×B(c) | Spend Feature | J2 primary | PH Unknown | D1=D2=D3=D4 Same 对 M1 → R1-cluster candidate；区域门缺失 → R4 |
| M5 | Crypto.com Card（SG/AU modes） | X1(c)×A(c) | Spend Feature | J2 primary | PH Unknown；AU mode 存在但逐国 Unknown | 对 M3 同 Y=A 方向 → R2 candidate；起点池 Unknown → R4 vs PH cluster |
| M6 | MetaMask Card | X3(c)×B(c) | Spend Feature | J2 primary | PH/VN/AU No | 对 M1 同 D2=D3=D4 → R2 candidate（容器 X3 vs X2）；区域分区 → 主要 R4/R3c |
| M7 | Plasma One | X3(c)×C(c) | Money Account-leaning | J1 primary；J2 secondary | PH Unknown | 对 M11 同 D1=D2=D3=D4 → R1-cluster candidate（门：M11 PH confirmed vs M7 Unknown）；对 M2 账户心智相近但 D2 Unknown → R4 |
| M8 | Karta | X Unknown×A(c) | Account-adjacent | J1-leaning | PH Unknown | D1+区域 Unknown → 全 R4；Y=A confirmed 仅支撑 S1-candidate boundary |
| M9 | Bleap | X3(c)×C(c) | Money Account-leaning | J1 primary；J2 secondary | PH/VN/AU No（Europe/MX/BR） | 对 M7/M10/M11 同簇 → R1-cluster candidate（门：区域 No/Unknown → R4/R3c） |
| M10 | OKX Pay/Card SG | X3(c)×C(c) | Spend Feature / Account-adjacent | J1 primary；J2 secondary | PH/VN/AU No（SG only） | 对 M7/M9/M11 同簇 → R1-cluster candidate（门：仅 SG → R4/R3c） |
| M11 | ether.fi Direct Pay | X3(c)×C(c) | Unknown / Account-adjacent | J2 secondary | PH confirmed；VN Conflict；AU available page | 对 M7/M9/M10 同 D1–D4 → R1-cluster candidate（门：除 M11 外区域 Unknown/No → R4/R3c）；对 M1/M3 PH 共市场 → R2/R3 candidate（容器/机制维度有差） |
| M12 | ether.fi Borrow | X3 cand×D(c) | — | J3 primary | PH available（J3 战场） | D4 与消费 mode 不同 → 对 M1–M11/M13 全 R5；对 M14 同 D2=D3 → R4 candidate（无共同市场） |
| M13 | Nexo Debit | X2(c)×Y Unknown | Spend Feature at most | J2-compatible | No（EEA+UK only） | D4 Same + 区域 No（相对 PH 战场）→ R3c/R4 candidate；欧内可评估 R2/R3 |
| M14 | Nexo Credit | X2(c)×D(c) | Spend Feature at most | J3 primary | No（EEA+UK only） | 对 M12 同 D2=D3 → R4 candidate（无共同市场）；对 J1/J2 modes 全 R5 |

**应用结论（框架独立于 AIX）：**

1. 市场级「直接替代」的充分必要结构 = D1–D4 全 Same + 共同市场 confirmed；**当前 14 个 mode 中没有任何 pair 达到 R1-confirmed**。
2. 最强**同簇候选（R1-cluster candidate）**出现在两处：S2 簇 M1↔M4（X2×B，门=Bybit PH Unknown）与 S4 簇 M7/M9/M10/M11（X3×C，门=除 M11 外区域 Unknown/No）。这与主文档一致，但**共同市场缺失使这些 pair 全部停留在 R4 级别的潜在关系**，不能写成 confirmed 竞争。
3. 共享市场就是硬门：M1↔M3↔M11（三者 PH 均已证）是唯一在证据上「用户可实际二选一」的三角，但 D1/D2 维度有差/Unknown，因此只能判 R2/R3 candidate；这比 R1-cluster 弱一等，却是当前唯一 confirmed 共同市场下的实际替代 set。
4. KAST 的 Money Account 角色不升级任何竞争关系，只解释「为什么即使同段，用户切换成本更高」。
5. J3 credit 簇（M12/M14）与 J1/J2 消费簇不存在 D4 等效，全部 R5；只在「同一品牌双 mode」（ether.fi M11/M12、Nexo M13/M14）时通过品牌连接，不改变 mode 级关系。

---

## 5. 模式级关系网格（F2 版，仅列有实质关系的 pair）

| Pair | D1/D2/D3/D4 | 共同市场 | F2 定级 | 主文档定级 | 差异 |
|---|---|---|---|---|---|
| M1↔M4 | Same/Same/Same/Same | Unknown（Bybit PH Unknown） | R1-cluster candidate → R4 | R1-cluster candidate → R4 | 一致 |
| M1↔M3 | Diff/Unknown/Same/Same | **PH confirmed** | R2/R3 candidate | R2 | 主文档 R2 可成立；F2 保留 Unknown 不升级 confirmed |
| M1↔M11 | Diff/Same/Diff(job 权重)/Same | **PH confirmed** | R2/R3 candidate | 未单列（归 card-spend R3） | F2 突出 PH 已证三角 |
| M3↔M11 | Unknown/Same/Diff/Same | **PH confirmed** | R2/R3 candidate | 未单列 | 同上 |
| M7↔M9/M10 | Same/Same/Same/Same | Unknown / No | R1-cluster candidate → R4/R3c | R1-cluster candidate → R4 / R3 | 一致 |
| M11↔M7 | Same/Same/Same/Same | Unknown（M7） | R1-cluster candidate → R4 | R4（M7 PH Unknown） | 一致 |
| M11↔M9/M10 | Same/Same/Same/Same | No | R1-cluster candidate → R3c/R4 | R3 | 一致（区域 No 只允许最弱结果替代读法） |
| M2↔M7 | Same/Unknown/Same/Same | Unknown | R4（D2+区域双 Unknown） | R2（主文档列相邻） | **F2 降级**：D2 Unknown + 共同市场 Unknown 不支撑 confirmed R2 |
| M6↔M1 | Diff/Same/Same/Same | 未证（M6 多国已证但与 M1 交集未证） | R2 candidate → R4 | R2 | **F2 降级为 candidate**：无共同市场证据 |
| M12↔M14 | Diff(n/a)/Same/Same/Diff 结果 | No（PH vs EEA/UK） | R4 candidate | R4 | 一致 |

> 网格口径：R2/R3 若共同市场 Unknown 或维度 Unknown，F2 一律标 `candidate`，不写 confirmed。主文档 §3.2/§3.3 的多处 R2/R3 是**全球最弱读法**，可接受为候选层级，但不能作为已证实相邻/结果替代引用。

---

## 6. 对 `04-competition-map.md` 的独立交叉检验

### 6.1 方法

- 只重读主文档、Step 1–3 结论与 `evidence/03-*.md`；不联网、不新抓。
- 检查项：AIX 是否被用作市场级锚点；R1–R5 是否一致；Unknown 是否被升级/降级；区域门是否成立；mode 粒度是否保持；AIX 未来进入者段是否越权。

### 6.2 结论：**PASS（条件通过，0 P0 / 0 P1）**

| # | 检查项 | 结果 |
|---|---|---|
| 1 | 市场级关系不以 AIX 为锚；§0、§6 纪律明确 | ✅ 通过。AIX 只出现在 §6 future-entrant，且不参与任何 R1–R5 |
| 2 | D1–D4 / R1–R5 框架完整、可回溯 | ✅ 通过。定义与 Step 2 X/Y / Step 3 four-AND 不冲突 |
| 3 | R1-confirmed 纪律（共同市场双方资格） | ✅ 通过。主文档明确「当前没有任何 R1-confirmed」 |
| 4 | Unknown 纪律（KAST Y / Bitget X / PH eligibility 5 项） | ✅ 通过。全部保留 Unknown，未被升级或降级 |
| 5 | 区域门（merchant acceptance 不作为资格） | ✅ 通过。§3.x 与 §5 未用 100+/150M 等营销口径 |
| 6 | AIX future-entrant 段 | ✅ 通过。全部标 inference；未写 current 竞争关系 |
| 7 | mode 粒度（M1–M14 与 Step 3 对齐） | ✅ 通过。14 个 mode 一致，品牌多 mode 拆分正确 |

### 6.3 非阻塞观察（P2/P3，不阻止 Draft 状态）

1. **P2**：主文档 §3.2 的 M2↔M7 标为 R2，但 D2（KAST Y）Unknown 且无共同市场证据；F2 建议改为「R2-candidate / R4」，与 R1-cluster 纪律同口径。
2. **P2**：§3.2 的 M6↔M1、M6↔M11 等 R2 关系建立在「全球同段」读法上，而 M6 在 PH/VN/AU 明确 No；建议全表加注 `R2c（region-gated candidate）`，避免被 Step 5 当 confirmed 相邻引用。
3. **P2**：§3.3 的「所有 card-spend modes 互为 R3」是**无区域约束的最弱读法**；建议明确标注「仅全球结果替代候选，不代表任一共同市场已证」，并把 PH 已证三角（M1/M3/M11）单列为最强实际替代 set。
4. **P3**：§3.2 M2↔M14 行尾残留「修正说明」字样，属草稿编辑痕迹，建议清理。
5. **P3**：Step 4 主文档引用的 `evidence/04-agent-e-regional-maturity-density.md` 与 `04-sources.md` 已存在；本 F2 文件加入 `evidence/` 后，`04-sources.md` 索引表应补一行 F2 条目（由主文档收口时处理，不越权改）。

---

## 7. 给 Step 5 的最小输入（只传框架事实，不传 AIX 定位）

1. PH confirmed 共同市场三角 = **{M1 RedotPay, M3 Bitget Wallet Card, M11 ether.fi Direct Pay}**；这是当前唯一「用户可实际二选一」的已证共同市场 set，竞争强度比较必须从这三个开始（费率 / 发行 / KYC / 体验）。
2. 5 个区域 Unknown（M2 KAST / M4 Bybit / M5 Crypto.com / M7 Plasma / M8 Karta）每确认一个，对应 pair 从 R4 升级一档（R1-cluster 或 R2/R3），Step 5 需按证据更新，不得提前升级。
3. S4 簇（M7/M9/M10/M11）是全球同簇度最高的 R1-cluster candidate；任何一国共同市场确认即可能产生 R1-cluster pair，是本地图对区域证据最敏感的簇。
4. J3 credit（M12/M14）与 J1/J2 消费是两个 D4 不等效的战场；竞争图应保持双战场，不合并。
5. 框架本身（D1–D4 + R1–R5 + 共同市场门）可复用为 Step 5 的 AIX 进入判定骨架，但进入判定仍须由定位 agent 单独执行，F2 不代做。

---

## 8. 输出 JSON

```json
{
  "outcome": "PASS",
  "summary": "Agent F2 independently derived a market-level competition relationship framework (D1 value container, D2 purchasing-power mechanism, D3 starting pool x Job, D4 final real-world outcome; R1 direct / R2 adjacent / R3 outcome-substitute / R4 potential / R5 out-of-scope) WITHOUT anchoring on any AIX fact, then applied it to all 14 reviewed product modes and cross-checked the Step 4 main doc. Framework-first results: no pair reaches R1-confirmed because no two modes share both D1-D4 alignment and a confirmed common market; the strongest R1-cluster candidates are S2 (M1 RedotPay <-> M4 Bybit, region gate) and S4 (M7/M9/M10/M11, region gates); the only confirmed shared-market set is the PH triangle M1 RedotPay / M3 Bitget Wallet Card / M11 ether.fi Direct Pay, graded R2/R3 candidates not R1. Cross-check of 04-competition-map.md: PASS with 0 P0/P1; 5 non-blocking observations (P2: M2-M7 and M6-M1 type R2 relations lack confirmed/common-market grounding and should be labeled candidates; P2: blanket all-card-modes-are-R3 needs a region-gated-candidate caveat; P2: PH triangle should be isolated as the strongest actual substitution set; P3: stray 修正说明 edit mark in section 3.2; P3: 04-sources.md index should later add this F2 file). No new facts, no network fetches, no AIX positioning; all Unknowns preserved.",
  "changedFiles": ["research/aix-market-positioning/evidence/04-agent-f2-competition-framework.md"],
  "tests": [
    "AIX-anchor scan: market-level framework and mode application contain no AIX-dependent relationship (AIX appears only as a minimal non-participating scope note)",
    "framework independence: D1-D4 and R1-R5 derived from first principles before any brand named",
    "Unknown discipline check: KAST Y, Bitget X, 5 PH eligibility Unknowns preserved as Unknown (never upgraded/downgraded)",
    "shared-market gate recomputation: no mode pair achieves R1-confirmed; PH confirmed triangle M1/M3/M11 identified",
    "mode-level granularity check: 14 product modes consistent with Step 3; brand multi-mode splits (ether.fi, Nexo) preserved",
    "main-doc cross-check: 7 gate checks (AIX anchor, framework consistency, R1 discipline, Unknowns, region gates, future-entrant scope, mode granularity) all PASS; 5 non-blocking observations listed",
    "no-new-fact scan: no new URLs, no network calls, no invented fields/states"
  ],
  "commands": [],
  "decisionsRequired": [
    "Decide whether Step 4 main doc relabels non-shared-market R2/R3 rows to R2c/R3c candidate before Step 5 citation (P2)",
    "Decide whether to isolate the PH confirmed triangle (RedotPay / Bitget / ether.fi Direct Pay) as the priority set for competitive-intensity comparison in Step 5 (P2)",
    "Authorize later addition of this F2 file to evidence/04-sources.md during main-doc closure (P3)",
    "Keep excluding AIX current facts from market-level relationship edits; any AIX entry decision belongs to Step 5 agent, not F2"
  ],
  "requiresGptReview": true
}
```
