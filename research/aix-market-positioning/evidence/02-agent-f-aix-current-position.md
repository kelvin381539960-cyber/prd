# Agent F｜AIX 当前产品事实落位（截至 2026-08-29）

> 用途：为 AIX Step 2 生态位地图提供“本方事实基座”。只读取 `kelvin381539960-cyber/prd` 仓库中 AIX 已确认知识 / PRD 与本地 Step 1 文档，不研究竞品，不引入市场推断。
> 状态纪律：`Current Implementation`（当前实现或已确认运行事实）≠ `PRD-defined`（PRD/设计定义，尚未确认上线）≠ `Proposal`（proposal / in-progress 需求）≠ `Unknown`（KB 未确认或缺口）。引用必须落在“现状=KB / 现状=archive 证据 / 设计=PRD / 未确认=ALL-GAP”四类路径上。
> 时点限制：仓库知识库 frontmatter 最后更新多为 2026-05-29；卡片仅表示“文档可见时点的事实”，不保证 2026-08-29 当日运行态未变。
> 汇编者：Agent F。证据索引见文末。

## 0. 事实抽取规则

1. 当前实现判断优先使用 `knowledge-base/`；该目录是已确认运行事实层，`requirements/` 默认不是确认事实源。
2. `archive/legacy-prd/` 仅用于核验来源；当 KB 已转译收口时，以 KB 为准。KB 未转译或状态冲突的，引用原始 PRD 证据并单独标注。
3. 删除线内容、`deferred` / `open` 项不写成事实；统一归入 Unknown 并引用 ALL-GAP / GAP 编号。
4. FAQ 是用户解释层，不能反推业务规则；只有 FAQ 明确与 confirmed fact 一致时才使用。
5. Website / Marketing PRD 不进入 runtime KB，只作为 visual_only 证据，不用于定位结论。
6. 不把市场推断（如 Job Family、竞品定位）写成 AIX 事实。

## 1. 资金进入

| 层面 | 结论 | 状态 |
|---|---|---|
| 稳定币充值是当前 AIX 资金进入能力 | AIX Wallet Deposit 支持稳定币入金，入金路径分为 GTR / Exchange 地址充值与 WalletConnect / Self-custodial Wallet 充值；两者不得合并为同一路径。 | Current Implementation |
| 充值目标币种 | 当前口径为 USDC、USDT、WUSD、FDUSD，排序固定为 USDC、USDT、WUSD、FDUSD，后端可配置。 | Current Implementation |
| 充值目标网络 | USDC：BASE、BSC、ETHEREUM、SOLANA；USDT：BSC、ETHEREUM、SOLANA；WUSD：ETHEREUM；FDUSD：BSC、ETHEREUM、SOLANA。 | Current Implementation |
| 法币入金 | DTC ActivityType 存在 `FIAT_DEPOSIT=6`，但 AIX 是否把它映射到 GTR 未见确认；文档中没有沉淀法币入金用户路径。不得把 Fiat Deposit 写成 AIX 已上线法币入金。 | Unknown / PRD-classification-only |
| KYC 前置 | Account Opening / KYC 是否为 GTR / WalletConnect Deposit 的产品入口前置尚未确认；WalletConnect 技术链路依赖 `D-SUB-ACCOUNT-ID`，但入口强制关系未确认。 | Unknown |

### 1.1 GTR / Exchange 地址充值

| 层面 | 结论 | 状态 |
|---|---|---|
| 路径定义 | “From an Exchange”路径生成专属钱包收款地址，用户复制地址或扫描 QR 后从外部托管钱包转账；PRD 当前口径为 Binance，实际支持范围以 DTC / GTR 配置为准。 | Current Implementation |
| 白名单行为 | GTR 地址充值不校验地址白名单；GTR Wallet 自动交易报备，不需要交易声明。 | Current Implementation |
| Quick Check | 页面提示使用 Binance wallet，发送账户必须为本人，禁止“my friend paid for me”。 | Current Implementation |
| 支持钱包范围 | 历史源 PRD 写“当前支持 GTR 的只有 Binance，DTC 后续更新列表”。KB 保持同一口径。 | Current Implementation / PRD-era evidence |
| Travel Rule | 全局旅行规则仅支持如 Binance 的白名单钱包充值；GTR 路径自动报备，无需声明。 | Current Implementation |
| 结果页 | GTR 是否有与 WalletConnect 相同结果页未确认，见 ALL-GAP-009。 | Unknown |
| 异常闭环 | 非 Binance / 非本人账户 / 错误网络 / 错误地址 / 低于最小金额有风险，但后台与客服处理未确认，见 ALL-GAP-011。 | Unknown |

### 1.2 WalletConnect / Self-custodial Wallet 充值

| 层面 | 结论 | 状态 |
|---|---|---|
| 路径定义 | “From a Self-custodial Wallet”路径输入 Amount / Crypto / Network，通过 WalletConnect token、WebSocket、create_payment_intent、QR / deeplink 连接第三方钱包。 | Current Implementation |
| 自动加白 | 用户 Approved 后，DTC 自动添加发送地址到白名单；加白成功后才 send_payment。 | Current Implementation |
| 授权有效期 | AIX 对客授权有效期按 1 天；DTC 7 天是内部逻辑，不作为 AIX 对客口径。 | Current Implementation |
| Deeplink / QR | Deeplink 有效期 5 分钟；UI 倒计时 `Awaiting payment... 4:00 Min` 可配置。 | Current Implementation |
| 默认网络与默认币种 | 默认 Crypto 为 USDC；默认 Network 为 BSC，若币种不支持 BSC 则默认 ETH。 | Current Implementation |
| 结果页 | 明确 success / progressing / failed；Risk Withheld 不触发充值结果页，交易详情展示 under review。 | Current Implementation |
| Gas 提示 | 私有钱包必须有网络原生币支付 gas；Quick Deposit Check 提示链、币种和 Gas。 | Current Implementation |
| payment_info | payment_broadcasted 后每 5 秒查询一次，最多 5 分钟；payment_info success 理论触发资金流转账，实际可能有短延迟。 | Current Implementation |
| Deposit success 与 Wallet `COMPLETED` | 不得写死存在确定映射，见 ALL-GAP-016。 | Unknown |
| Travel Rule / 白名单边界 | Declare / Travel Rule / 白名单触发与展示边界未完整确认，见 ALL-GAP-044。 | Unknown |

### 1.3 Proposal：地址充值来源误用风控

| 层面 | 结论 | 状态 |
|---|---|---|
| 需求意图 | 在用户使用收款地址前确认转账来源：Binance 沿用现有支持流程；我的钱包 App 走白名单钱包地址；其他交易所明确不支持，以降低 Under Review。 | Proposal / PRD 编写中 |
| 流程设计 | 采用“资产网络优先，来源使用前确认”；新增白名单钱包地址需 DTC 支持性校验、添加并启用白名单。 | Proposal |
| 项目状态 | 需求批次 2026-05，需求状态“PRD 编写中”；项目计划中 UX、Tech Design、Development、QA 均未开始。 | Proposal |

## 2. 资产驻留位置

| 层面 | 结论 | 状态 |
|---|---|---|
| 托管 / 外部账户模型 | DTC 是外部供应商；DTC 存在 Master Account / Sub Account 账户模型，Sub Account 注册在 Master Account 下。 | Current Implementation |
| AIX 侧定位 | AIX 负责页面展示、调用、接收、展示、通知、告警、人工处理和记录边界，不维护 DTC 内部账户实现。 | Current Implementation |
| D-SUB-ACCOUNT-ID | DTC 请求 Header，表示 Master Account 下注册的 Sub Account ID，影响 WalletConnect、Wallet Account、Deposit、Balance、History 上下文。 | Current Implementation |
| WalletAccount | DTC WalletAccount 包含 id、clientId、status、currency、balance、label、createdDate、lastUpdatedDate 等字段，影响账户状态、余额、币种和可用性判断。 | Current Implementation |
| 账户映射 | AIX user 与 DTC Sub Account 是否一一对应未确认；`D-SUB-ACCOUNT-ID` 与 WalletAccount.clientId 是否等价未确认；Sub Account 创建时机与失败处理未确认。 | Unknown |
| WalletAccount.status 准入 | WalletAccount.status 与 AIX 能力准入映射未确认。 | Unknown |
| KYC 与账户创建 | KYC Approved 不一定代表 DTC Sub Account 已创建成功，也不一定代表所有 Wallet 能力可用。 | Unknown / boundary |

## 3. 稳定币 / Crypto 余额

| 层面 | 结论 | 状态 |
|---|---|---|
| 稳定币业务范围 | 当前钱包仅做稳定币业务：FDUSD、USDC、USDT、WUSD。 | Current Implementation |
| 资产首页 | My Assets 是钱包资产首页，展示 Total Asset、Stablecoin 列表、快捷入口和 Recent transaction。 | Current Implementation |
| 余额接口 | `GET /openapi/v1/wallet/balances` 查询全量币种余额；`GET /openapi/v1/wallet/balance/{currency}` 查询单币种余额。 | Current Implementation |
| Total Asset 计算 | Total Asset = USDT余额*Rate1 + USDC余额*Rate2 + WUSD余额*Rate3 + FDUSD余额*Rate4；各币按 USD 汇率折算，四舍五入保留 2 位后相加。 | Current Implementation |
| Fiat Balance | 每个稳定币有对应 USD Fiat Balance = Crypto Balance × Rate。 | Current Implementation |
| Fiat Balance 语义 | “Fiat Balance” 是稳定币余额的法币估算展示值，不是独立法币账户余额。 | Current Implementation |
| 排序与配置 | Stablecoin 列表固定排序，后端可配置展示币种；图标可配置。 | Current Implementation |
| 隐藏余额 | 眼睛图标控制总资产和稳定币余额显示/隐藏；隐藏时显示 `****`。 | Current Implementation |
| 前端枚举 | 代码可确认 `CryptoCurrency`：FDUSD、USDC、USDT、WUSD；`CryptoMainNet`：Ethereum、BSC、Base、Solana。 | Current Implementation |
| 余额字段边界 | 可用余额、冻结余额、总余额完整字段名未确认；排序与零余额规则未确认；查询失败处理未确认。 | Unknown |
| Card balance | Card balance 不写入 Wallet Assets 主事实；Card balance 与 Wallet balance 币种是否一致未确认。 | Unknown / boundary |

## 4. 购买力产生方式

| 层面 | 结论 | 状态 |
|---|---|---|
| 消费链路 | AIX Card 与 Wallet 组成当前消费链路：Card 承接卡消费；Wallet 承接余额、入金、转账和兑换。FAQ 解释为“充稳定币到 AIX Pay 账户后可直接消费”。 | Current Implementation / FAQ-layer evidence |
| Card 余额扣减 | 申卡成功实时扣制卡费；卡消费扣卡余额，退款按交易时汇率转成 USDT 等值金额后退回，仅退净商品金额，不含 FX 费用和 Transaction Fee。 | Current Implementation |
| 退款自动归集 | DTC 卡交易通知后，refund / reversal / deposit 类型触发查询卡余额；balance > 0 时 Transfer Balance to Wallet，amount = balance；失败告警并人工介入。 | Current Implementation |
| Card 余额驻留 | 卡余额属于 Card 资金，不等于 Wallet 主余额；归集到 Wallet 后才进入用户主可见余额。 | Current Implementation |
| Card → Wallet 对账 | Card Transaction 与 Wallet Transaction 是否一一对应未确认；关联字段未确认；DTC transfer 成功但 Wallet 未入账主要靠用户反馈发现。 | Unknown |
| Wallet ↔ Card 互转 | KB 未确认普通用户可把 Wallet 余额转入 Card 或从 Card 主动转出到 Wallet；文档只确认目标事件触发的自动归集。 | Unknown |

## 5. Rail 清单

| Rail | 当前状态 | 关键结论 |
|---|---|---|
| Card | Current Implementation | 支持 Virtual Card 与 Physical Card；Phase 1 支持地区 Philippines、Vietnam、Australia，后续可配置；最多 5 张卡（可配置），仅 1 张在途；Virtual USD 5、Physical USD 10；申卡前置钱包开通、DTC 渠道开户、KYC 验证通过、刷脸 Token 有效。 |
| Send | Current Implementation / runtime confirmation pending | KB 把 Send 拆分为 active 主事实，支持 Phone / Email / AIX Tag 向 AIX 平台存量用户发送同一币种稳定币；Send Now 触发刷脸 Token 校验；结果页 successful / processing / failure。注意：KB 索引仍保留“Swap / Send 当前是否上线待确认”，运行态需产品 / 后端核验。 |
| Swap | Current Implementation / runtime confirmation pending | KB 把 Swap 拆分为 active 主事实，支持同一用户不同稳定币之间兑换，如 USDT、USDC 等；OTC Rate / dtcQuoteId 一次性；支持 completed / processing / failed 结果页。注意：KB 索引仍保留“当前是否上线待确认”。 |
| Withdraw | 不支持 | 当前暂不支持，后续开放；App 隐藏 Withdraw 入口（ALL-GAP-071 resolved-by-user）。 |
| Fiat Deposit | Unknown | DTC 有 `FIAT_DEPOSIT=6` 分类，但 AIX 用户路径未见确认；不得写成已上线能力。 |
| Receive | Unknown | 独立 Receive 是否存在、与 Deposit 关系、页面与支持范围均未确认；交易历史有 Receive 类型但无独立入口路由（ALL-GAP-052 / 059 / 060 / 061 / 062）。 |
| QR / Transfer / P2P | Partially covered | QR 覆盖 GTR 收款地址和 WalletConnect 充值确认页；Send 覆盖 AIX 存量用户间转账；通用 P2P 余额划转未沉淀。 |

## 6. 地区与准入

| 层面 | 结论 | 状态 |
|---|---|---|
| Wallet / Crypto 充值支持国家 | 用户确认 2026-05-29：当前 Wallet / Crypto 充值支持国家为 Philippines（PH）。链 × 稳定币：BASE=USDC；BSC=FDUSD/USDC/USDT；ETHEREUM=FDUSD/USDC/USDT/WUSD；SOLANA=FDUSD/USDC/USDT。 | Current Implementation |
| Card Application Phase 1 | Phase 1 支持地区为 Philippines、Vietnam、Australia，后续可配置。 | Current Implementation |
| Wallet 与 Card 地区口径 | 本矩阵是充值链 × 稳定币清单，不等同 Card Phase 1 支持国家；两者范围不同，不得相互推导。 | Current Implementation / boundary |
| KYC 国家线 | KYC 以 Wallet Opening KYC PRD 国家线 / 居住国白名单为准；KB 未展开具体白名单。Archive 证据显示：国家线表中 VN、PH、AU 为 ✅；330 版本支持国家为 PH + SG；3.6 内测时 Phase 1 国家临时处理为 phase 2-waitlist，但 PH、AU、VN、SG 保持 Phase 1。该证据未在当前 KB 收口，只作为来源层证据。 | PRD-era evidence / Source conflict noted |
| Phase 1 / Phase 2 / Forbidden | KYC 国家选择按 Type 分 Phase 1、phase 2-waitlist、Forbiden；Forbiden 国家隐藏不可选；waitlist 用户不能继续 KYC。 | Current Implementation / PRD-era evidence |
| POA 校验 | POA 国家需与用户填报居住国匹配，申请国家需在白名单。 | Current Implementation |
| 充值资格 | 用户资格 / 准入仍以 KYC 居住国白名单为准。 | Current Implementation |
| KYC ↔ Deposit / Card 前置 | Account Opening / KYC 与 Card KYC 关系未确认；KYC 是否为 GTR / WalletConnect Deposit 前置未确认（ALL-GAP-030 / 031）。 | Unknown |
| Phone country code | 登录 / 注册国家区号部分存在删除线与待确认，不作为完整国家线沉淀。 | Unknown / non-fact |

## 7. 用户核心场景（文档可证明范围）

| 场景 | 文档证据 | 状态 |
|---|---|---|
| 从稳定币余额获得现实购买力 | FAQ 写明申请 AIX Pay 卡、充值稳定币到 AIX Pay 账户后即可消费；Card 消费扣卡余额。 | Current Implementation / FAQ-layer evidence |
| 充值 | Home / Wallet / 单币种入口进入 Deposit；选择 From an Exchange 或 From a Self-custodial Wallet；GTR / WalletConnect 分别生成地址或支付意图。 | Current Implementation |
| 资产查看 | My Assets 展示总资产、稳定币余额、法币估算、最近交易摘要；金额可隐藏。 | Current Implementation |
| 申卡 | 选择 Virtual / Physical、卡面、币种；填写 Billing / Mailing；支付制卡费；Face Auth 后提交；结果页 Approved / Under review / Unsuccessful。 | Current Implementation |
| 卡管理 | Lock / Unlock、PIN、敏感信息、实体卡激活；Recent Transactions 最近 3 条。 | Current Implementation |
| 卡交易 | Card History 展示 Payment / Cash withdrawal / Refund / Incremental Auth；REVERSAL 按退款展示；详情含 merchant / MCC / exchange rate。 | Current Implementation |
| 稳定币内部资金移动 | Send 给 Phone / Email / X-Tag 收款人；Swap 在稳定币之间兑换。 | Current Implementation |
| 交易可见性 | Transaction History / Detail 覆盖 Card / Crypto / OTC 来源；列表含类型与状态展示边界。 | Current Implementation |
| 争议 / 挂失 / 资金异常 | 客服答复卡要求转人工；争议、挂失、资金未入账内部流程未沉淀。 | Unknown |

## 8. 已有边界与规划边界

### 8.1 当前已有能力

- Deposit：GTR / Exchange 与 WalletConnect 两条稳定币入金子路径。
- Assets：稳定币资产首页与 USD 估算。
- Send：向 AIX 平台存量用户发送同一币种稳定币。
- Swap：同一用户不同稳定币之间兑换。
- Card：Virtual / Physical 卡申请、管理、消费、退款归集。
- KYC：Passport OCR、Face、POA、waitlist / 禁用国家处理。
- Account：注册 / 登录 / 忘记密码（SMS OTP）。
- Security：OTP、Face Auth、密码策略。
- 通知：KYC / Deposit / Card 相关通知边界。

### 8.2 当前不支持或隐藏

- Withdraw 当前暂不支持，后续开放；App 隐藏入口。
- 独立 Receive 未见确认入口。
- 法币入金用户路径未见确认。
- 非稳定币业务未见确认。
- 完整费用表（FX 加价、ATM、跨境、不活跃、Swap 价差、Send 链上 gas 等）未确认。
- 客服 SLA / 分级矩阵未确认。

### 8.3 PRD-defined 或 Proposal 中的规划

| 规划 | 状态 | 来源 |
|---|---|---|
| 地址充值来源误用风控 | Proposal / PRD 编写中 | `requirements/2026-05/wallet/deposit-address-misuse-risk-control.md` |
| 单币种首页（Single Currency Home） | PRD-era planning | 原始 PRD 修订记录说明 MVP 不做单币种首页，后续再迭代 |
| Card 首页点击跳转冲突处理 | Conflict | Home PRD 与 Card Application PRD 对部分首页卡片点击跳转存在差异，标 `CONFLICT` 待产品确认 |
| Google Wallet | Deferred / open | Card Home 记录 Android 入口方案待定 |
| Chat with us | Non-fact | FAQ 中章节删除线，不作为 confirmed runtime fact |

## 9. Unknown 与歧义清单

| 问题 | 影响 | 状态 / 引用 |
|---|---|---|
| GTR 是否使用 `FIAT_DEPOSIT=6` | 交易历史分类、法币入金判断 | Unknown / ALL-GAP-001 deferred |
| WalletConnect 是否使用 `CRYPTO_DEPOSIT=10` | 交易历史分类 | Unknown / ALL-GAP-002 deferred |
| KYC 是否为 GTR / WalletConnect Deposit 前置 | 资金进入漏斗入口 | Unknown / ALL-GAP-031 deferred |
| Deposit success 与 Wallet `state=COMPLETED` 映射 | 到账语义与余额可见时点 | Unknown / ALL-GAP-016 deferred |
| Risk Withheld 与 Wallet state / 冻结余额关系 | 风控状态下余额语义 | Unknown / ALL-GAP-008 deferred |
| Card / Wallet ID 串联与对账 | 退款归集可追踪性 | Unknown / ALL-GAP-017 / 018 deferred |
| AIX user ↔ DTC Sub Account 一一对应 | 账户模型 | Unknown / ALL-GAP-066 deferred |
| WalletAccount.status 与能力准入映射 | 资产 / 入金可用性 | Unknown / ALL-GAP-069 deferred |
| Receive 上线状态与范围 | 收款入口是否存在 | Unknown / ALL-GAP-052 / 059 / 060 / 061 / 062 deferred |
| 完整费用表 | Spend rail 成本结构 | Unknown / ALL-GAP-075 deferred |
| 客服 SLA / 分级矩阵 | 异常闭环时效 | Unknown / ALL-GAP-074 open |
| KYC 国家线版本口径 | 准入范围 | Unknown / GAP-KYC-COUNTRY-001；archive 显示 VN/PH/AU + 330 版本 PH+SG + 内测临时 PH/AU/VN/SG 证据 |
| Swap / Send 当前是否上线 | Rail 可用性 | KB 把独立 Send / Swap 文件标 active，但原始入口和 index 仍提示“当前是否上线待确认”；本轮按 KB 现状处理，最终运行态需产品 / 后端核验 |
| Wallet/Fiat Deposit 用户路径 | 资金进入形态 | Unknown / KB 无 Fiat Deposit 用户路径 |
| Website / Marketing 事实 | 对外宣传定位 | 不进入 runtime KB；不能用于 AIX 产品事实 |

## 10. 禁止写入或误读的风险

1. 不能把 `FIAT_DEPOSIT=6` / `CRYPTO_DEPOSIT=10` 直接等同 GTR / WalletConnect。
2. 不能把 Deposit success 写死为 Wallet `COMPLETED`。
3. 不能把 Risk Withheld 写死为 Wallet `REJECTED` / `PENDING` / `PROCESSING`。
4. 不能把通知成功等同资金到账。
5. 不能把 Wallet 余额等同于 Card 余额；Card balance 自动归集到 Wallet 的完整链路未确认。
6. 不能把 Phone country code / FAQ 推导成 KYC 国家线。
7. 不能把 Card Phase 1 支持国家直接扩展为 Wallet / KYC 全量支持国家。
8. 不能把 Withdraw 当前状态与后续开放时间表写成承诺。
9. 不能把市场推断、竞品定位、Job Family 当作 AIX 产品事实。
10. 不能把 FAQ / Website / Marketing 内容直接当作 runtime 事实。

## 11. Step 2 使用注意

1. 本卡片只提供“AIX 现状 + 设计意图 + 已知缺口”；不要把现状直接推成生态位结论。
2. 生态位定位应在 Step 2 / Step 5 中基于本卡片与竞品 / 市场证据分别验证；主次、优先级和战略判断不在此下结论。
3. 三个 Job Family 是市场分析层概念，不是 AIX 文档内事实；若 Step 2 使用，必须显式标注为市场推断，不是 AIX 现状。
4. 消费链路当前证据最充分；资金进入证据中等；提现 / 法币 / Receive 证据缺失。生态位评估需把“能力缺口”与“市场选择”分开，避免把合规或实现缺口误判为战略选择。
5. Step 3 竞品对比时，不要把 AIX 未确认项写成对比结论；先把 Unknown 转成核验问题。

## 12. 证据索引

### 现状 / 运行事实层（knowledge-base）

| 编号 | 路径 | 支持事实 |
|---|---|---|
| KB-01 | `knowledge-base/README.md` | knowledge-base 为已确认运行产品事实层；requirements 默认不是确认事实源 |
| KB-02 | `knowledge-base/_ai-query-router.md` | 当前产品范围、Deposit / Assets / Card / KYC 路由；Send / Swap 拆分后文件状态；Receive 独立能力不在 active 路由表 |
| KB-03 | `knowledge-base/_system-boundary.md` | AIX / DTC / AAI / KUN / WalletConnect / GTR / 区块链边界 |
| KB-04 | `knowledge-base/wallet/_index.md` | Wallet active 能力；Send / Withdraw / Swap 状态口径；稳定币 / 网络枚举 |
| KB-05 | `knowledge-base/wallet/assets.md` | 稳定币范围、网络枚举、余额接口、Total Asset / Fiat Balance、金额隐藏 |
| KB-06 | `knowledge-base/wallet/deposit.md` | GTR / WalletConnect 充值流程、网络矩阵、Travel Rule、结果页与状态边界 |
| KB-07 | `knowledge-base/wallet/send.md` | Send Crypto 收款人方式、余额校验、Face Token、结果页 |
| KB-08 | `knowledge-base/wallet/swap.md` | Swap 币种、OTC Rate、dtcQuoteId、结果页 |
| KB-09 | `knowledge-base/card/application.md` | Virtual / Physical、Phase 1 国家、费用、申卡资格、余额 / 支付 / 结果页 |
| KB-10 | `knowledge-base/card/transaction.md` | 卡交易通知后 refund / reversal / deposit 自动归集；退款费用边界 |
| KB-11 | `knowledge-base/card/transaction-detail.md` | Card History / Detail 展示范围、交易类型、状态、Exchange rate |
| KB-12 | `knowledge-base/transaction/history.md` | 全量交易来源、前端交易类型 / Receive 无独立入口路由、ActivityType 边界 |
| KB-13 | `knowledge-base/transaction/status-model.md` | Wallet state、Deposit success / Risk Withheld、Card 状态映射边界 |
| KB-14 | `knowledge-base/transaction/reconciliation.md` | Card → Wallet 对账与资金追踪缺口 |
| KB-15 | `knowledge-base/integrations/dtc/_index.md` | DTC Master / Sub Account、WalletAccount、Risk Withheld、ActivityType |
| KB-16 | `knowledge-base/integrations/walletconnect/_index.md` | WalletConnect 流程、自动加白、授权有效期、异常事件 |
| KB-17 | `knowledge-base/kyc/account-opening.md` | KYC 状态机、国家 / waitlist / forbidden、POA 校验、申卡前置 |
| KB-18 | `knowledge-base/_meta/countries-and-regions.md` | PH 充值支持国家、链 × 币矩阵、Card Phase 1 国家、不相互推导规则 |
| KB-19 | `knowledge-base/_meta/compliance-boundaries.md` | Withdraw 不支持 / 入口隐藏；waitlist / rejected KYC 拦截 |
| KB-20 | `knowledge-base/_meta/limits-and-rules.md` | 稳定币、卡费、Send / Swap / Deposit 关键有效期与限制 |
| KB-21 | `knowledge-base/common/cs-answer-cards.md` | 对客口径：稳定币、PH / 链矩阵、Withdraw 不支持、争议 / 挂失 / 资金问题转人工 |
| KB-22 | `knowledge-base/common/faq.md` | FAQ 解释层与边界；不能反推业务规则；Samsung Pay 证据边界 |
| KB-23 | `knowledge-base/changelog/knowledge-gaps.md` | ALL-GAP-001/002/008/016/030/031/037/044/052/055/059/066/069/071/074/075/077/078 等状态 |
| KB-24 | `knowledge-base/home/app-home.md` | Home 资产展示、申卡入口、核心交易入口、Withdraw 隐藏 |
| KB-25 | `knowledge-base/integrations/aai/_index.md` | KYC 身份验证外部依赖边界 |

### 历史源证据层（archive / legacy PRD）

| 编号 | 路径 | 支持事实 |
|---|---|---|
| SRC-01 | `archive/legacy-prd/kyc/wallet-opening/README.md` | 国家线表 VN/PH/AU ✅；330 版本支持 PH+SG；3.6 内测时 Phase 1 国家临时处理为 phase 2-waitlist，但 PH、AU、VN、SG 保持 Phase 1 |
| SRC-02 | `archive/legacy-prd/wallet/deposit-send-swap/README.md` | GTR / WalletConnect 充值流程、Binance-only 口径、Travel Rule 表述、WC 主流钱包示例 |
| SRC-03 | `reference-data/countries/countries-and-regions.csv` | 通用国家 / 电话代码数据；不得当作 KYC 支持国家白名单 |
| SRC-04 | `knowledge-base/non-runtime/website-phase-1.md` 与 `website-phase-2.md` | Website / Marketing 不进入 runtime KB，visual_only |

### PRD / Proposal 层（requirements）

| 编号 | 路径 | 支持事实 |
|---|---|---|
| PRD-01 | `requirements/2026-05/wallet/deposit-address-misuse-risk-control.md` | 地址充值来源误用风控：Binance / 我的钱包 App / 其他交易所来源分流，钱包地址白名单校验与启用；需求状态 PRD 编写中 |
| PRD-02 | `requirements/2026-05/account/change-email.md` | 账户侧在途迭代事实，不属于资金 / Card / 地区核心结论 |
| PRD-03 | `requirements/_index.md` | requirements 为新迭代 PRD 目录，默认不是确认运行事实源 |

### Step 1 / 仓内研究层

| 编号 | 路径 | 支持事实 |
|---|---|---|
| STEP-01 | `research/aix-market-positioning/01-market-overview-and-user-jobs.md` | Step 1 市场结论、Job Family、边界与“AIX 定位留待验证”问题 |
| STEP-02 | `research/aix-market-positioning/evidence/01-sources.md` | Step 1 证据口径与限制 |
| STEP-03 | `research/aix-market-positioning/TASK.md` | Step 2 需要独立 solution axes；玩家需分别验证资金位置、购买力产生、rail、可服务地区 |

## 13. 事实状态汇总

| 维度 | Current Implementation | PRD-defined / Proposal | Unknown |
|---|---|---|---|
| 资金进入 | GTR / Binance 地址充值、WalletConnect 自托管充值、PH 充值支持、稳定币 / 网络矩阵 | 地址充值来源误用风控 | KYC 前置、法币入金、结果页与异常闭环细节 |
| 资产驻留 | AIX 资产首页 / 余额展示、DTC 外部账户边界、退款自动归集 | 单币种首页规划 | Sub Account 映射、WalletAccount.status 准入、Card/Wallet 余额一致性 |
| 购买力 | Card 消费、退款回退、Send / Swap、交易可见性 | Google Wallet 方案待定 | 通用 Card/Wallet 主动互转、完整费用表 |
| 地区 | PH 充值、PH / VN / AU Card Phase 1、KYC waitlist / forbidden 机制 | 可配置扩展机制 | KYC 白名单权威清单与版本口径 |
| 边界 | Withdraw 不支持；Receive 未确认；完整费用表未确认 | 来源误用风控规划 | 客服 SLA、异常补偿入口、争议内部流程 |
