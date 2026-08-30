# Step 5 Agent E｜AIX Implementation Baseline → Candidate Direction Gap（feasibility / overlay only）

> 状态：Step 5 子证据稿（2026-08-30）
> 角色本分：**只做 feasibility / gap overlay**。本稿不定义市场、不定义目标、不给最终战略推荐；目标方向选择由 Step 5 主文档（`05-aix-positioning.md`）与最终决策负责。
> 只读来源：Step 1–4 正式文档（`01-market-overview-and-user-jobs.md`、`02-ecosystem-map.md`、`03-player-positioning.md`、`04-competition-map.md`）、仓内已有 AIX 现状证据（`evidence/02-agent-f-aix-current-position.md`、`evidence/03-agent-f-aix-anchor.md`）、Step 3/4 已评审的 J-cluster evidence cards（Agent A/B/C/D/E/F2/G2）。
> 事实纪律：
> 1. AIX 当前实现事实一律标 **`Implementation Baseline`**；证据缺失一律标 **`Unknown`**，不得把 Unknown 升级为 Yes / No，不得用推测补全。
> 2. 本稿所有方向都是 **candidate target-state hypothesis（Step 5 输入），不是 AIX 现状，也不是本稿的选择**。
> 3. **实现难度不自动否决高价值方向**；难度只作为落地成本/风险 overlay，价值判断交给 Step 5 主流程。

---

## 0. 用途与边界

Step 4 已确立市场边界为 **consumer crypto/stablecoin → real-world purchasing power**，并把竞争拆为 J1 Global Money / J2 Crypto → Spend / J3 Keep Crypto → Liquidity 三个 Job 战场（`04-competition-map.md`）。Step 5 需要回答「AIX 当前在哪、目标在哪、市场白地是什么」。

本稿只回答其中一个子问题：**若 Step 5 把候选方向 A–D（以及 J3 方向）作为目标态，AIX 现有实现基线到目标态之间缺什么、依赖什么、难度与迁移风险如何、能否分阶段。**

本稿明确不回答：

- AIX 应该选 J1 / J2 / J3 中的哪个。
- 哪个方向市场价值最高、是否有白地。
- 是否应因难度或迁移风险放弃某个方向。

---

## 1. AIX Implementation Baseline（固定事实底图）

> 以下 AIX 事实全部来自 `evidence/02-agent-f-aix-current-position.md` 与 `evidence/03-agent-f-aix-anchor.md`；凡标 `Implementation Baseline` 的条目均为当前实现/已确认运行事实（时点：知识库多为 2026-05-29 更新，不保证 2026-08-30 运行态未变）。

| 维度 | AIX 当前事实 | 证据状态 |
|---|---|---|
| 产品形态 | 面向东南亚的「托管稳定币钱包 + 实体/虚拟卡 + KYC 开户」App | Implementation Baseline |
| 资产范围 | 仅稳定币：USDC、USDT、WUSD、FDUSD；无 volatile crypto balance 产品 | Implementation Baseline |
| 资产托管 | DTC 外部供应商托管（Master Account / Sub Account 模型），非 self-custody；AIX 与 DTC Sub Account 是否一一对应未确认 | Implementation Baseline + Unknown |
| 入金 | GTR / Exchange 地址充值 + WalletConnect / Self-custodial Wallet 充值两条稳定币入金子路径；入金支持网络矩阵（USDC BASE/BSC/ETH/SOL；USDT BSC/ETH/SOL；WUSD ETH；FDUSD BSC/ETH/SOL） | Implementation Baseline |
| 入金地区 | Wallet Crypto Deposit 支持国家 = Philippines（PH）only | Implementation Baseline |
| 余额结构 | Wallet Balance 与 Card Balance 分离；卡消费扣 Card Balance（生态位 X1 confirmed）；普通用户 Wallet → Card 主动充值/购买时自动 funding 机制未确认 | Implementation Baseline + Unknown |
| 发卡 | Virtual / Physical Card；Card Application Phase 1 = PH / VN / AU；最多 5 张卡；制卡费 Virtual USD 5 / Physical USD 10；退款/冲正/入账事件触发 Card → Wallet 自动归集 | Implementation Baseline |
| Send | 向 AIX 平台存量用户发送同一币种稳定币（Phone / Email / AIX Tag）；运行态待产品/后端核验 | Implementation Baseline / runtime confirmation pending |
| Swap | 同一用户不同稳定币之间兑换（OTC Rate / dtcQuoteId 一次性）；运行态待核验 | Implementation Baseline / runtime confirmation pending |
| Receive | 独立 Receive 入口/范围未确认；交易历史有 Receive 类型但无独立入口路由 | Unknown |
| Withdraw | 当前不支持，入口隐藏；后续开放时间表未知 | Unknown（当前不可用事实为 Baseline） |
| 法币入金 | DTC 存在 `FIAT_DEPOSIT=6` 分类，但 AIX 用户路径未见确认 | Unknown |
| KYC | Passport OCR、Face、POA、waitlist / forbidden 国家处理；外部依赖 AAI（OCR/Liveness/人脸）、KUN（KYC 编排）；KYC 是否为 Deposit / Card 前置未确认；KYC 国家白名单版本口径存在冲突 | Implementation Baseline + Unknown |
| 其它外部依赖 | WalletConnect（已接入入金）、Binance/GTR Wallet（出金/报备）、区块链网络；AIX 只感知 DTC 结果/字段，不维护其内部实现 | Implementation Baseline |
| 生态位坐标 | X1 confirmed；Y Unknown；Species Unknown；Account Role 最多 Account-adjacent（Receive Unknown / Send-Swap runtime pending / Withdraw 不可用，不能称 Money Account） | Baseline + Unknown |
| Job 关系（analysis inference） | J1 plausible/incomplete；J2 对受支持稳定币起点 segment strong/plausible；J3 unsupported（无 collateral / credit / borrow 能力） | analysis inference only |

**方向无关的既有 Unknown（任何方向都必须先关闭或显式保留）：**

1. Wallet → Card funding 机制（Y 轴；决定 Species 精确归类）。
2. Send / Swap 真实 runtime 状态。
3. 独立 Receive 是否存在及范围。
4. Card Balance 与 Wallet Balance 币种是否一致。
5. AIX user ↔ DTC Sub Account 映射、WalletAccount.status 与能力准入映射。
6. KYC 与 Deposit / Card 的前置关系 + KYC 国家白名单权威版本。
7. 完整费用表（FX、ATM、跨境、Swap 价差、Send gas 等）。
8. Card → Wallet 对账完整链路与关联字段。
9. 法币入金/出金（Withdraw）能力与合规边界。

---

## 2. D1：J1 Money Account（稳定币为底层的全球资金账户）

**方向定义（仅 overlay）**：AIX 从「充值 → 卡消费」闭环扩展为可 **receive + hold + send/transfer + spend**、具备 unified/same-balance 的稳定币金额账户，并成长为目标市场里的长期「钱的主账户」。这是 Step 4 中 KAST 所代表的 J1 方向（`04-agent-a-j1-global-money-card.md`），不代表 AIX 已是 Money Account。

### 2.1 当前可复用能力

| 能力 | 状态 |
|---|---|
| 托管稳定币钱包与四币资产（USDC/USDT/WUSD/FDUSD） | Implementation Baseline |
| 两条稳定币入金路径（GTR / WalletConnect） | Implementation Baseline |
| Send（平台存量用户、同币种稳定币） | Implementation Baseline / runtime confirmation pending |
| Swap（同用户稳定币互兑） | Implementation Baseline / runtime confirmation pending |
| Card 消费 + 退款/冲正自动归集 Wallet | Implementation Baseline |
| KYC / 开户 / OTP / Face Auth 基础 | Implementation Baseline |
| DTC Master/Sub Account 账户结构与余额查询接口 | Implementation Baseline |

### 2.2 关键新增能力

| 新增能力 | 当前状态 |
|---|---|
| 独立 Receive（对外收款地址/别名、收款页、与 Deposit 的关系） | Unknown（历史有 Receive 类型但无入口） |
| Unified / same-balance（同一用户余额同时支撑 receive/send/spend） | **当前不成立**：Wallet Balance 与 Card Balance 分离；未确认统一扣款模型 |
| 主动/自动 Wallet → Card funding | Unknown |
| 链外/外部发送（对非 AIX 用户的银行、钱包、链上发送；与现有 Withdraw 能力边界） | Withdraw 不支持（Baseline）；外部 send 路径 Unknown |
| 法币入金 / 出金银行 rails（如 ACH/SEPA/InstaPay/PESONet 类） | Fiat deposit Unknown；无用户路径 |
| 逐国/多区域 eligibility 与完整费表 | KYC 白名单版本冲突（Unknown）；完整费表 Unknown |

### 2.3 依赖

- **供应商**：DTC（外部收款/发送/法币 rails 能力未知）、银行/支付 rails 合作方（入金出金）、现有 KUN/AAI（KYC）、WalletConnect（已接入）。
- **合规**：按目标区域判断 e-money / PSP / virtual-asset 许可、资金转入转出监管、travel rule 边界（现有全局旅行规则仅覆盖白名单钱包入金）；KYC 国家白名单版本必须先收敛。
- **Ledger**：统一余额模型或等价的「多余额但用户感知同一」结构；Card ↔ Wallet 对账缺口必须先补齐；外部 send/withdraw 的 ledger 状态机。
- **Pay**：银行 rails 结算、费用/汇率展示、退款跨 rails 语义。
- **UX**：Receive 入口、统一资产页、资金转出/入金流程、异常态（风险冻结、失败、限额）。

### 2.4 可行性 overlay

| 维度 | 判断 | 依据/边界 |
|---|---|---|
| 实现难度 | **High** | 需要新增 Receive/外部发送/银行 rails 多个能力，且涉及账户模型与对账重构；不因难度否决价值 |
| 迁移风险 | **High（若做统一余额）/ Medium（若先做增量功能）** | 合并 Wallet/Card 余额会触碰现有卡扣款、退款归集、余额展示；增量上线（先 Receive/外部 send）风险较低 |
| 可分阶段路径 | **可分** | P1：确认 Wallet→Card funding + 独立 Receive + 平台内/稳定币外部 send（最小闭环）；P2：PH 银行 rails（InstaPay/PESONet）+ 统一余额展示；P3：多区域资格与许可扩展 |

---

## 3. D2：J2 Custodial Instant-Convert Spend（托管余额、支付时自动转换）

**方向定义（仅 overlay）**：AIX 提供提供商托管的余额（稳定币以外可扩展到波动币），用户不用预先卖出/预充值，支付时自动转换为结算购买力（Step 2 的 X2×B / S2 方向，样本 RedotPay / Bybit）。本方向包含两个机制子变体（本稿不裁决哪个为目标）：

- D2a：稳定币/波动币余额在授权/结算点自动转换为法币结算（X2×B 典型形态）。
- D2b：稳定币在购买时自动从 Wallet 补入 Card Balance / 转换后消费（是否仍为 X1 取决于资金容器设计；当前 Y Unknown 的事实本身不改变）。

### 3.1 当前可复用能力

| 能力 | 状态 |
|---|---|
| 托管钱包 + DTC 账户/余额基础设施 | Implementation Baseline |
| 稳定币资产与入金路径 | Implementation Baseline |
| Card 消费、授权、退款/归集 | Implementation Baseline |
| Swap（同一用户稳定币互兑；可作为转换引擎雏形） | Implementation Baseline / runtime confirmation pending |
| 卡交易详情/汇率展示 | Implementation Baseline |

### 3.2 关键新增能力

| 新增能力 | 当前状态 |
|---|---|
| 波动币资产托管/清算（BTC/ETH 等） | 无 volatile balance 产品（Baseline）；DTC 是否支持波动币托管 Unknown |
| 支付时自动转换（auto-convert / auto-fund at purchase） | Wallet→Card funding / purchase-time 机制 Unknown |
| 实时价格源、转换/加价率、授权冻结与结算扣减 | 未知（新增） |
| 转换敏感的交易/退款/失败语义（部分授权、撤销、汇率回溯） | 现有退款按交易时汇率折算（Baseline）；新增波动币场景语义 Unknown |
| 波动币风控：限额分级、波动保护、滑点/汇率风险和客服闭环 | Unknown |

### 3.3 依赖

- **供应商**：DTC（波动币托管、转换/报价能力未知）、卡 Issuer/Processor（授权时转换与结算）、市场数据源；现有 WalletConnect/GTR 仅覆盖入金/出金，不覆盖支付转换。
- **合规**：波动币 = 虚拟资产服务（VASP）边界与许可影响；旅行规则/AML 对新资产类型的适用；目标区域（先 PH 或扩展）的资产准入。
- **Ledger**：波动币余额 + 稳定币余额 + 转换 PnL/费用拆分；Card ↔ Wallet 对账（已有缺口）；转换记录与卡交易一一对应。
- **Pay**：授权时冻结/结算时扣减、退款币种与汇率、失败回滚。
- **UX**：是否需要预操作（越少越好）、转换确认、限额提示、费用透明。

### 3.4 可行性 overlay

| 维度 | 判断 | 依据/边界 |
|---|---|---|
| 实现难度 | **Medium-High** | 若只做稳定币自动转换（D2b），属于现有栈增量；若加波动币托管与实时转换（D2a），涉及新资产类别与风险系统 |
| 迁移风险 | **Medium** | 新增资产/转换不破坏现有稳定币卡链路；风险集中在授权/费率/退款语义与 Card↔Wallet 对账 |
| 可分阶段路径 | **可分** | P1：确认并补齐 stablecoin Wallet→Card auto-fund/purchase-time convert（不新增资产）；P2：小范围波动币（如 BTC/ETH）托管 + 限额内自动转换；P3：扩资产、扩区域、完整费率与风控 |

---

## 4. D3：J2 Stablecoin Account + Multi-Rail Spend（稳定币账户 + 多轨消费）

**方向定义（仅 overlay）**：AIX 以稳定币账户为统一 spendable balance，用户无需先把手动装进独立卡余额，即可通过 **Card + QR + 银行/e-wallet + 账单/充值 + P2P** 等多条 Rail 消费（Step 4 中的 Rail Layer，样本 Coins.ph QR Ph、GCash/Maya two-step、Bitrefill bridge，见 `04-agent-g2-non-card-substitute-rails-evidence-card.md`）。本方向不要求波动币，也不要求完整 J1 银行账户闭环（但可与 D1 叠加）。

### 4.1 当前可复用能力

| 能力 | 状态 |
|---|---|
| 托管稳定币 Wallet 与四币资产 | Implementation Baseline |
| 入金（GTR / WalletConnect） | Implementation Baseline |
| Card rail 及退款归集 | Implementation Baseline |
| Send（平台内同币种；P2P 雏形） | Implementation Baseline / runtime confirmation pending |
| Swap / USD 估算（多币种统一展示雏形） | Implementation Baseline / runtime confirmation pending |

### 4.2 关键新增能力

| 新增能力 | 当前状态 |
|---|---|
| Unified spendable balance 或稳定的 Wallet→Card auto-fund（避免手动预充） | Unknown（当前余额分离；Y Unknown） |
| QR Ph 商户直付（支付点稳定币→PHP 转换） | 无 QR spend rail（Baseline）；Coins.ph 已有市场样本，AIX 无证据 |
| 银行/e-wallet rails（InstaPay / PESONet / 本地 e-wallet 划转） | Withdraw 不支持 (Baseline)；Fiat deposit Unknown；无本地 rails 证据 |
| 账单支付 / 充值 / 礼品券 rails | Unknown |
| P2P 扩展（AIX 用户之外、跨币种/跨平台） | Send 仅平台存量用户同币种（Baseline）；扩展 Unknown |
| 多 rail 统一限额/费表/汇率展示 | Unknown |

### 4.3 依赖

- **供应商**：DTC（统一余额/分 rail 结算能力未知）、QR 聚合商或 BSP QR Ph 参与者、e-wallet/银行 rails 合作方、现有卡 Issuer。
- **合规**：本地支付牌照/PSP 许可、商户 rails 接入规则、P2P 扩展的 AML；现有 KYC 白名单版本冲突仍阻塞区域判断。
- **Ledger**：统一/分账余额、每 rail 结算与对账、卡/ QR /转账同余额下的状态一致。
- **Pay**：各 rail 的汇率/费率/结算时点；退款跨 rail 语义（QR 退款、卡退款不同）；失败/限额/重复支付。
- **UX**：支付方式选择器、费用预览、默认 rail 规则、空状态/失败状态。

### 4.4 可行性 overlay

| 维度 | 判断 | 依据/边界 |
|---|---|---|
| 实现难度 | **Medium** | 稳定币不新增资产类别；难度集中在多 rail 集成与统一余额/对账，而非新资产 |
| 迁移风险 | **Medium** | 统一余额涉及现有 Card Balance 扣款模型；若保持「卡余额+自动补足」则风险较低，但用户心智仍是两笔余额 |
| 可分阶段路径 | **可分** | P1：确认 Wallet→Card 自动补足 + 费用透明（单 rail 闭环）；P2：PH QR 或账单 rail 先行；P3：银行/e-wallet rails + P2P 扩展；区域扩展放最后 |

---

## 5. D4：J2 Self-Custody Spend（自托管钱包直付）

**方向定义（仅 overlay）**：AIX 让用户资产留在自托管/用户控制的钱包或 Vault 中，直到支付时才被扣减（Step 2 的 X3×C / X3×B 方向，样本 ether.fi Direct Pay、OKX SG、Plasma One/MetaMask）。AIX 已接入 WalletConnect **仅用于入金**，本方向要求把同一类技术能力延伸到支付授权。

### 5.1 当前可复用能力

| 能力 | 状态 |
|---|---|
| WalletConnect 连接自托管钱包（入金侧：连接、白名单、支付意图、QR/deeplink） | Implementation Baseline（仅入金） |
| KYC / 卡 rails / 交易详情 | Implementation Baseline |
| 区块链网络接入知识（多链入金矩阵） | Implementation Baseline |
| DTC 托管模型（自托管 spend 若并存，可作为对照基线） | Implementation Baseline |

### 5.2 关键新增能力

| 新增能力 | 当前状态 |
|---|---|
| 支付时从用户自托管钱包直接扣款（非先转入托管余额） | Unknown（WalletConnect 支付授权未确认） |
| 支持直扣的 Issuer/Processor（non-custodial 结算伙伴） | Unknown（新伙伴） |
| 自托管支付链路的 gas / 网络费用 / 签失败 / 钱包离线处理 | Unknown（新增） |
| X3 型直扣或支付点转换的精确机制（C 或 B） | Unknown（目标态设计未定） |
| 自托管 UX：授权会话、限额、撤销、key 丢失/恢复边界、兼容钱包清单 | Unknown；AIX 现有产品无 self-custody 账户叙事 |
| 并存运营：托管 + 自托管双模式下的客服/风控/对账矩阵 | Unknown |

### 5.3 依赖

- **供应商**：WalletConnect（已接入，但支付会话能力未知）、non-custodial issuer/processor（新）、区块链网络（已接入）、可能 Bridge 类 global account service（无 AIX 证据）。
- **合规**：非托管 liability 边界、KYC 是否保留、旅行规则/AML 对链上支付的适用、争议处理归属；AIX 当前 DTC 托管模型的法律关系不同。
- **Ledger**：链上支付 vs 卡结算对账、授权防重放、退款回链/余额语义；现有 Card↔Wallet 对账缺口会放大。
- **Pay**：扣款时点（authorization vs settlement）、部分授权、汇率/转换、签名中断恢复。
- **UX**：与现有 App 流程差异大；需钱包兼容、授权确认、失败重试、教育内容。

### 5.4 可行性 overlay

| 维度 | 判断 | 依据/边界 |
|---|---|---|
| 实现难度 | **High** | 新架构（非托管结算 + 新伙伴 + 新 UX），并需与现有 DTC 托管模型并存或迁移 |
| 迁移风险 | **High（并存）/ 极高（整体转换）** | 整体转自托管会废弃现有 DTC 托管链路；并存则双体系客服/风控/对账成本高 |
| 可分阶段路径 | **可分（但不小）** | P1：用现有 WalletConnect 做低限额「连接钱包→授权→卡消费」试点；P2：选择少量链/资产/区域，接入 non-custodial 结算伙伴；P3：评估托管与自托管并存策略；每阶段都需合规与对账先行 |

---

## 6. D5：J3 Collateral-Backed Liquidity（抵押不卖、获得消费流动性）

**方向定义（仅 overlay）**：AIX 允许用户以 Crypto/稳定币作抵押获得信用额度或消费流动性，**不卖出资产**（Step 2 Y=D / S6；样本 Nexo Credit、ether.fi Borrow、RedotPay Credit，见 `04-agent-d-credit-borrow-to-spend-evidence-card.md`）。AIX 当前 J3 unsupported（Baseline）。

### 6.1 当前可复用能力

| 能力 | 状态 |
|---|---|
| 托管钱包与稳定币/资产托管（可作为抵押物持有层） | Implementation Baseline |
| Card rail 与交易历史（信用消费的载体） | Implementation Baseline |
| KYC / 开户 / 通知 | Implementation Baseline |
| DTC 账户/余额结构（不含信贷能力） | Implementation Baseline；信贷能力 Unknown |

### 6.2 关键新增能力

| 新增能力 | 当前状态 |
|---|---|
| 抵押物估值 / LTV / 风险指数 / 追加保证金 / 清算 | Unknown（新增；RedotPay 样本有 0.6/0.8/0.9 阈值模式，非 AIX 事实） |
| 信贷 ledger：额度、债务、利息、还款、抵押释放、逾期状态 | Unknown（新增） |
| 卡授权与信用额度打通（消费扣 credit 而非 wallet balance） | 当前卡消费扣 Card Balance（Baseline）；credit 语义 Unknown |
| 抵押物范围与稳定币是否计入（竞品口径不一：RedotPay 排除稳定币、Nexo 计入；AIX 无设计） | Unknown（设计决策，非现状） |
| 退款/冲正与信贷余额的交互 | Unknown |
| 放贷牌照/消费信贷合规、利率上限、披露、催收/违约运营 | Unknown（地区相关） |

### 6.3 依赖

- **供应商**：DTC（抵押托管/信贷 ledger 能力 Unknown）、卡 Issuer（信用授权）、信贷/风控引擎（新）、估值/清盘服务（新）、法务。
- **合规**：目标市场放贷/信贷牌照与消费者保护（如利率上限）、虚拟资产抵押的法律定性、AML/制裁；地区决定许可成本。
- **Ledger**：抵押物 + 信用双子账、利息/还款/清算、与卡交易对账；现有差额人工对账模式不满足信贷规模。
- **Pay**：授权时信用额度检查、还款/抵押释放与卡消费同步、退款方向（回信贷余额还是抵押物）。
- **UX**：借款/还款流程、清算预警、风险揭示、限额与客服 SLA。

### 6.4 可行性 overlay

| 维度 | 判断 | 依据/边界 |
|---|---|---|
| 实现难度 | **High** | 新金融垂直，重合规/风控/信贷系统；不是现有 wallet+card 栈的增量 |
| 迁移风险 | **Medium-High** | 若与现有卡余额混用会带来「余额 vs 债务」认知与退款/限额混乱；可做独立 Credit Account（如 RedotPay）降低迁移风险，但仍是新系统 |
| 可分阶段路径 | **可分（前提多）** | P0：牌照与准入评估 + DTC/Issuer 信贷能力确认；P1：小额抵押信贷试点（有限资产、独立 Credit Account、低 LTV）；P2：扩抵押资产与额度、清算/追缴自动化；P3：多区域与产品扩展；未取得许可前不能进入 P1 |

---

## 7. 跨方向依赖与共享积木（overlay 视图）

| 共享积木 | D1 J1 Money Account | D2 Custodial instant-convert | D3 Stablecoin + multi-rail | D4 Self-custody spend | D5 J3 Credit |
|---|---|---|---|---|---|
| 统一余额 / Wallet→Card auto-fund | 必要 | 必要（D2a/b 均需） | 必要 | 不适用（非托管直扣） | 不必要 |
| 外部资金 rails（银行/e-wallet/QR） | 必要（银行 rails） | 不需要（转换为主） | 必要（多 rail） | 不需要 | 还款可能需要 |
| 波动币托管 | 非必要 | 必要（D2a）；D2b 不需要 | 非必要 | 可选（X3×B 时） | 可选（抵押物范围设计） |
| Non-custodial 结算伙伴 | 不必要 | 不必要 | 不必要 | 必要 | 不必要 |
| 信贷引擎 + 放贷许可 | 不必要 | 不必要 | 不必要 | 不必要 | 必要 |
| 完整费表/汇率透明 | 必要 | 必要 | 必要 | 必要 | 必要 |
| KYC/区域准入收敛 | 必要 | 必要 | 必要 | 必要 | 必要 |
| Card↔Wallet/新 rails 对账 | 必要 | 必要 | 必要（多 rail 放大） | 必要（链上对账） | 必要（信用对账） |

**D0：方向无关的先行核验项（不是方向，不构成推荐）**

任何方向落地前，以下 Unknown 必须先关闭或显式保留为风险：

1. Wallet → Card funding 机制（Y）——D1/D2/D3 的精确可行性都依赖它。
2. Send / Swap runtime 状态——D1/D3 的闭环能力依赖它。
3. 独立 Receive / Withdraw / Fiat rails——D1/D3 的核心增量。
4. DTC 能力边界：波动币托管、法币/银行 rails、统一余额、信贷、外部发送——决定 D1/D2/D3/D5 是否需要换/加供应商。
5. KYC 国家白名单与 Deposit/Card 前置——所有方向的地域可验证性。
6. 完整费表——所有方向的市场竞争可行性比较（Step 4 变量之一）。

---

## 8. Overlay 结论（非战略结论）

1. **五个方向在现有 Implementation Baseline 上的增量差异很大**：D2/D3 是对现有托管稳定币栈的增量；D1 是账户/rails 边界扩展；D4 是托管模型变更；D5 是新金融垂直。此排列只描述落地形态差异，不构成优先级或价值判断。
2. **每个方向都至少有一个阻塞性 Unknown**（D1：Receive/银行 rails/unified balance；D2：波动币托管与 purchase-time convert；D3：统一余额与 rails 合作方；D4：non-custodial 结算伙伴；D5：信贷许可与引擎）。在对应 Unknown 关闭前，任何「该方向 ready」的表述都禁止。
3. **难度和迁移风险不自动否决高价值方向**；本稿提供的难度/风险只供 Step 5 主流程与最终决策做可行性与路径规划。
4. **本稿没有给出最终战略推荐**；J1/J2/J3 选择、目标市场、白地与优先级全部留给 Step 5 主文档。

---

## 9. 来源映射

| 本稿内容 | 来源 |
|---|---|
| AIX 现状（资产/托管/入金/卡/KYC/地区/Unknown） | `evidence/02-agent-f-aix-current-position.md` |
| AIX 生态位锚点（X1/Y Unknown/Species/Account Role/J1-J3 inference/four-AND） | `evidence/03-agent-f-aix-anchor.md` |
| 市场边界与 J1/J2/J3 定义 | `01-market-overview-and-user-jobs.md` |
| X/Y/S1-S6 / Account Role / 约束纪律 | `02-ecosystem-map.md` |
| 玩家 mode 落位与 Direct candidate | `03-player-positioning.md` |
| 竞争结构、Rail Layer、给 Step 5 的输入顺序 | `04-competition-map.md` |
| J1 样本与 Money Account 判定 | `evidence/04-agent-a-j1-global-money-card.md` |
| J2 custodial/prefund 样本 | `evidence/04-agent-b-custodial-exchange-prefunded-card.md` |
| J2 self-custody 样本 | `evidence/04-agent-c-self-custody-wallet-native-evidence-card.md` |
| J3 credit 样本与机制 | `evidence/04-agent-d-credit-borrow-to-spend-evidence-card.md` |
| 区域/密度读数（市场级） | `evidence/04-agent-e-regional-maturity-density.md` |
| 竞争关系框架（D1-D4/R1-R5/PH 三角） | `evidence/04-agent-f2-competition-framework.md` |
| 非卡 rails 证据 | `evidence/04-agent-g2-non-card-substitute-rails-evidence-card.md` |
| four-AND 独立交叉验证 | `evidence/03-agent-e-crosscheck.md` |

---

## 10. 输出 JSON

```json
{
  "outcome": "PASS",
  "summary": "Step 5 Agent E produced the AIX Implementation Baseline -> candidate direction gap/feasibility overlay only. Read Step 1-4 formal docs plus existing AIX anchors (02-agent-f current position, 03-agent-f anchor) and Step 4 J-cluster evidence cards, without defining the market or the target and without giving a final strategic recommendation. All current AIX facts are labeled Implementation Baseline (custodial stablecoin wallet via DTC, GTR/WalletConnect deposit, PH wallet-deposit country, PH/VN/AU card Phase 1, Wallet/Card balance separation with X1 confirmed, Y Unknown, Species Unknown, Account Role at most Account-adjacent, J3 unsupported); missing evidence is marked Unknown (Wallet->Card funding, Receive, Send/Swap runtime, Withdraw/Fiat rails, KYC whitelist, full fee tables, DTC capability boundaries). Each candidate direction - D1 J1 Money Account, D2 J2 custodial instant-convert spend (with D2a/D2b mechanism variants), D3 J2 stablecoin account + multi-rail spend, D4 J2 self-custody spend, D5 J3 collateral-backed liquidity - is evaluated for reusable baseline capabilities, new capabilities, vendor/compliance/ledger/pay/UX dependencies, implementation difficulty (High for D1/D4/D5, Medium for D3, Medium-High for D2), migration risk, and phased paths. A cross-direction shared-building-block table and a D0 direction-independent verification list are included. Explicitly no final strategic recommendation, no direction ranking by value, and difficulty is not used to veto any high-value direction; several blocking Unknowns must be closed before any direction can be considered ready.",
  "changedFiles": [
    "research/aix-market-positioning/evidence/05-agent-e-aix-gap-feasibility.md"
  ],
  "tests": [
    "Step 1-4 main docs read and cited: 01-market-overview-and-user-jobs.md, 02-ecosystem-map.md, 03-player-positioning.md, 04-competition-map.md",
    "AIX current-fact sources read and cited: evidence/02-agent-f-aix-current-position.md and evidence/03-agent-f-aix-anchor.md; every current AIX fact labeled Implementation Baseline",
    "candidate coverage: D1 J1 Money Account, D2 custodial instant-convert spend, D3 stablecoin account + multi-rail spend, D4 self-custody spend, D5 collateral-backed liquidity each has reusable capabilities, new capabilities, vendor/compliance/ledger/pay/UX dependencies, difficulty, migration risk, phased path",
    "Unknown discipline: every gap with insufficient evidence is Unknown; no inference upgraded to fact; KAST/ether.fi VN/Send-Swap runtime conflicts not adjudicated",
    "no final strategic recommendation: no J1/J2/J3 choice, no direction ranking by value, no go/no-go, no market/target definition from current AIX facts",
    "output-path check: only research/aix-market-positioning/evidence/05-agent-e-aix-gap-feasibility.md written; TASK.md/sources.md/reviews untouched",
    "JSON self-check: embedded JSON matches final response fields"
  ],
  "commands": [
    "git status --short (clean before and after; no commit performed)",
    "rg --files research/aix-market-positioning/evidence to confirm target file path did not exist before and now exists"
  ],
  "decisionsRequired": [
    "Resolve AIX Wallet->Card funding mechanism (Y) before any direction can be mapped to a precise species (blocks D1/D2/D3)",
    "Confirm Send/Swap runtime status and independent Receive existence before J1 Money Account (D1) feasibility can be completed",
    "Confirm KYC country whitelist version and Deposit/Card KYC prerequisites before any region-dependent feasibility",
    "Confirm DTC capability boundaries: volatile-crypto custody, fiat/bank rails, unified-balance/ledger, external send, credit-line support (currently all Unknown)",
    "Decide in Step 5 main whether D3 multi-rail spend requires local QR/bank/e-wallet partners in the initial target state or can phase them",
    "Decide whether D4 self-custody spend requires a non-custodial issuer/processor partner (currently unknown) before further evaluation",
    "Decide whether D5 requires lending license and credit-risk system investment before P1 is considered; keep difficulty as feasibility overlay, not veto"
  ],
  "requiresGptReview": true
}
```
