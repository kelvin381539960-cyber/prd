# Step 4 Agent G2 收口｜非卡替代 Rails（Non-Card Substitute-Rails）证据卡

> 状态：Step 4 Agent G2 CLOSEOUT（2026-08-30）。只收口已采集缓存，不再浏览。
> 类型：Step 4 输入证据卡 / rail-level 固定稿；固化「crypto / stablecoin 不经 Visa/Mastercard 卡轨而变成现实购买力」的市场证据。不替代 Step 4 主文档 `04-competition-map.md` 的 R1–R5 分类。
> 数据边界：只使用 `/private/tmp/agent-g-evidence/` 已采集缓存（2026-08-30 访问）与 Step 1–3 已评审定义/结论。**未联网、未补抓、未新增 URL。**
> AIX 纪律：AIX 仅是未来进入者（future-entrant）。本卡不以 AIX 为比较锚点、不定义 AIX 当前/目标生态位；AIX 不参与任何本卡市场级判断。

---

## 0. 范围与不纳入

**本卡覆盖（非卡 Rails）**：

- **Direct at-merchant**：消费发生时直接用 stablecoin / crypto 余额支付，不经卡（Visa/Mastercard），例如 Coins.ph QR Ph stablecoin payment。
- **Two-step e-wallet**：crypto 先转回环境内 PHP / e-wallet 余额，再用 QR / bills / load 消费，例如 GCash GCrypto → GCash Wallet → QR/GBills。
- **Voucher / top-up bridge**：crypto 购买礼品卡、话费、eSIM、e-wallet voucher，再形成本地购买力，例如 Bitrefill → GCash Voucher。
- **Peso stablecoin layer**：本地法币锚定稳定币（Coins.ph PHPC，BSP sandbox）可买入/卖出/转账；与支付 rail 的衔接按缓存证据区分。
- **Merchant acceptance rails**：商户侧直接接受 crypto/stablecoin 的支付框架（Solana Pay、OpenNode）。
- **Legacy cash-out rails（context）**：PHP 从平台出来的 InstaPay / PESONet / OTC cash pickup，作为「crypto→PHP→取现/转出」的非卡通道。

**不纳入 / 不作为证据**：

- `azteco.html`：抓到的是美国佐治亚州 Valdosta 的 "Azteco-SEO" 棉花糖/小吃摊位网站，**不是** bitcoin cash voucher 服务商 Azteco；不得引用。
- `moneygram-crypto.html`：Angular 空壳，HTML 73KB 但 `<body>` 可见文本为 0 字符（未渲染 shell）；无 MoneyGram crypto 事实。
- `coinbase-commerce.html` / `cb-commerce2.html`：Cloudflare challenge；无内容。
- `strike.html`：CloudflareBotBlock（403）；无内容。
- `bitrefill-ph.html`：Clopudflare challenge；Bitrefill 实时 PH 页不可用，PH 目录仅能以搜索页+官方文档作 secondary 证据。
- `wb-bitrefill-ph.html` / `wb-bitrefill-ph-gc.html`：Wayback "has not archived that URL"；无档案页。
- `solanapay-learn.html`：404。
- `gcash-crypto.html`：GCash 官网 "Not Found"；GCash 依据使用 Zendesk JSON 缓存。
- `coinsph-search1/2/3.json`、`gcash-search*.json`：Zendesk "Not found"；无搜索结果事实。
- 所有 404 / 空壳缓存不产生「不存在」的否定结论，只标记当前缓存不可用。

---

## 1. 缓存证据清单（/private/tmp/agent-g-evidence，2026-08-30 访问）

| 缓存文件 | 来源 / canonical（缓存内提取） | 内容状态 | 有效性 |
|---|---|---|---|
| `coinsph.html` | https://www.coins.ph/en-ph | 主页：QRPh 600k+ stores、Pay bills、Send、Trade、USDT→PHP remittance、BSP-regulated、5M+ users / $20B 2025 品牌声明 | ✅ 有效（品牌营销数字不进入资格判定） |
| `coinsph-help.html` | https://support.coins.ph/hc/en-us | Help Center 壳 | ✅ 有效（导航索引） |
| `coinsph-sections.json` | Zendesk sections API | 全部分区索引（含 Scan & Pay、QR Ph、Cash Out、PHPC、Crypto、Western Union 等） | ✅ 有效 |
| `coinsph-sec-202591667.json` | Zendesk cash-out 分区 | 含 How to Cash Out、Cash Out Options、InstaPay/PESONet/Remittance Center 文章列表 | ✅ 有效 |
| `coinsph-sec-13216784335897.json` | Zendesk QR Ph 分区 | **QRPH Stablecoin Payments**、What is QR Ph、Pay with QR 等 | ✅ 有效 |
| `coinsph-sec-36152938993305.json` | Zendesk "All about PHPC" 分区 | PHPC 发行/转换/网络/沙箱文章 | ✅ 有效 |
| `coinsph-sec2-900000592806.json` | Zendesk crypto 分区 | Supported Tokens、Deposit/Withdraw、Send Crypto 系列 | ✅ 有效（列表索引） |
| `coinsph-art-*.json` / `coinsph-art3-*.json` | 各 article JSON（URL 内含 `coinsph.zendesk.com/...`） | 文章正文：QRPH stablecoin、Cash Out、PHPC、USDC、send/receive | ✅ 有效 |
| `coinsph-sec2-*.json` | 分区文章列表 | Load / Cash In / Bills / Crypto 文章名列表 | ✅ 有效（部分正文未抓） |
| `gcash-*.json`（art/art2/sec/cats） | https://help.gcash.com Zendesk API | GCrypto、Pay QR、GBills、Cash In/Out、Send/Receive crypto section 索引 | ✅ 有效（部分正文未抓） |
| `maya-crypto.html` | https://www.maya.ph/crypto（HubSpot 页） | Maya Crypto：buy/sell、convert to cash、send/receive "still being built" | ✅ 有效 |
| `bitrefill-docs.html` | https://docs.bitrefill.com/docs/api-overview（dateModified 2026-03-26） | API 文档：gift cards / top-ups / eSIMs；crypto payment 方式 | ✅ 有效（一手） |
| `ddg-bitrefill.html` | DuckDuckGo 搜索页 | Bitrefill PH 站点 meta + GCash Voucher / GrabMart 商品标题 | ⚠️ Secondary（搜索页证据） |
| `bitrefill-ph.html` | https://www.bitrefill.com/ph/en/ | Cloudflare challenge | ❌ 不可用 |
| `wb-bitrefill-ph*.html` | archive.org | "has not archived that URL" | ❌ 不可用 |
| `solanapay.html` | https://solanapay.com | Solana Pay 主页：Shopify integration 声明 | ✅ 有效（一手，但见 Shopify 冲突） |
| `solanapay-docs.html` | https://docs.solanapay.com/ | 协议/参考实现、支持钱包、POS | ⚠️ 2023 Copyright，版本陈旧；current 状态未知 |
| `shopify-solanapay.html` | https://apps.shopify.com/solana-pay | "This app is not currently available on the Shopify App Store"（开发者 Helio Fintech Ltd） | ✅ 有效（与 Solana Pay 主页冲突） |
| `opennode.html` | https://www.opennode.com | Bitcoin/Lightning merchant processing、本地法币结算 | ✅ 有效（一手） |
| `bsp-2025.txt` / `bsp-2025-epayments.pdf` / `bsp-2025-report.pdf` | BSP 2025 Report on E-Payments Measurement（bsp-report-page.html 指向最新 2025 PDF） | 全文：数字支付份额、QR Ph 增长、商户支付 | ✅ 有效（官方统计；与 crypto 无关） |
| `bsp-report-page.html` | https://www.bsp.gov.ph 报告页 | 标题 + 最新 2025 PDF 链接 | ✅ 有效 |
| `bsp-press.html` | BSP 页面壳 | 仅导航，无正文 | ⚠️ 无内容可取 |
| `azteco.html` | 错误站点（非目标品牌） | 无关 | ❌ 排除 |
| `moneygram-crypto.html` | Angular 壳（73KB，body 可见文本 0 字符） | 无事实 | ❌ 排除 |
| `coinbase-commerce.html` / `cb-commerce2.html` | Cloudflare | challenge | ❌ 排除 |
| `strike.html` | CloudflareBotBlock | 403 | ❌ 排除 |

---

## 2. Rail 证据卡

### 2.1 Coins.ph：PH 直接 stablecoin/crypto QR Ph 消费（本卡最强 direct 样本）

**缓存依据**：`coinsph.html`、`coinsph-sec-13216784335897.json`（含 `coinsph-art-57075258143001.json`）、`coinsph-sec-202591667.json`、`coinsph-sec-36152938993305.json`。

已固化事实：

- **主页（品牌口径，营销数字不进入资格门）**："BSP-regulated e-wallet for Filipinos. Pay bills, Use QRPH at 600k+ stores, send money home in seconds, buy & sell crypto in pesos"；"Convert your local currency to USDT, then to pesos with live rates and no hidden fees. Funds can reach your family in the Philippines in seconds"；自称 5M+ verified users、$20B total volume 2025、BSP-regulated since 2014、26 licenses。
- **QRPH Stablecoin Payments（官方 Help Center，updated 2026-08-09）**："With Coins.ph, you can now scan QRPH and pay using your stablecoins or crypto assets! You can directly scan and pay a QR and select from your available assets to pay easily. There's no need to sell your assets for PHP separately before paying."
  - 支付类型：PHP Only / Crypto Only / Combined Payment（PHP + 一个 crypto 资产）。
  - 流程：扫描 QRPH → 确认金额 → 选择可用资产余额 → 查看当前 PHP 汇率 → "Confirm convert and pay" → MFA 安全校验。
  - 即：**在支付点发生汇率确认 + 转换 + 付款**；这是「不先卖成 PHP、直接以 crypto 完成商户支付」的 evidence。
- **QR Ph 定义/费用**：国家 QR 标准，基于 EMV 框架，BSP Circular 1055 / PPMI 批准；商户支付实时处理、当前商户 QR 支付免费；个人间 QR 转账可能收费；要求 ID + Selfie 验证、绑定手机号、余额/限额足够。
- **Cash-out / 转出 rails（crypto→PHP→钱包/银行/现金）**：InstaPay（实时/10 分钟内，支持 GCash、Maya/PayMaya、GrabPay 及多家银行；How to Cash Out 表列 flat ₱5）；PESONet（批处理，Coins 表列零平台费）；Remittance Center / OTC cash pickup（M Lhuillier、Cebuana、Palawan、Pera Hub、Villarica、LBC、RD、Bayad Center；min ₱1,000）；Coins→GrabPay cash in。
- **PHPC peso stablecoin（updated 2026-08-25）**：1 PHPC 目标 = 1 PHP；由 Coins.ph（自述 licensed VASP + EMI）发行；BSP Regulatory Sandbox 试点；Polygon + Ronin；PHP⇄PHPC、BTC/ETH/USDT-PHPC convert pairs；单笔 0.01–250,000 PHP；沙箱期结束有兑换义务。**缓存未说明 PHPC 可直接用于 QRPH stablecoin payment**——该衔接保持 Unknown。

**读数**：PH 存在**已证实的「crypto/stablecoin 在商户支付点直接转化并完成非卡付款」轨道**（QR Ph 国家商户轨 + Coins.ph 应用内转换）。这是本缓存集中最直接的 card-substitute rail 证据。

### 2.2 GCash / GCrypto：两步路径（crypto → PHP wallet → QR / bills / load）

**缓存依据**：`gcash-art-47624429776025.json`、`gcash-art-31304830152089.json`、`gcash-art-9781218166041.json`、`gcash-sec-360004657934.json`、`gcash-sec-360004696173.json`、`gcash-sections.json`。

已固化事实：

- GCrypto："lets you buy, sell, and manage cryptocurrency in the GCash app… powered by PDAX"；GCrypto Trading Wallet 是独立交易钱包，需先从 GCash Wallet Top Up，再购买。
- 提现："Withdrawing from your GCrypto Trading Wallet moves your crypto funds to your GCash Wallet."；限额表（Fully Verified / GCash Plus，daily/monthly）。
- 币种/网络列表（updated 2026-08-28）：USDT、USDC、BTC、ETH、SOL、XRP 等，含多网络（TRC20、ERC20、Solana、Avalanche 等）。
- Pay QR："Pay QR powers cashless payments… scan a merchant's QR code or have others scan their personal QR code for instant transfers… in the Philippines and at select international merchants through Alipay+ partnership."
- GBills："pay their bills online to over 2,000+ billers nationwide"（fee examples：Meralco ₱0、Manila Water ₱6、PLDT/SMART ₱7 等）。
- `gcash-sections.json` 索引存在 **"Send and Receive Crypto with GCrypto"（section 31272577173785）**，但对应文章正文**未在本缓存中**。

**读数**：缓存中 **没有**「GCash 直接用 crypto 余额扫 QR/付账单」的证据；GCash 的非卡消费路径是 **GCrypto → GCash Wallet（PHP）→ QR/GBills/load 两步转换**。与 Coins.ph 的直接路径必须区分，不能合并为同一种 rail。

### 2.3 Maya：买卖 + 转现金，无直接 crypto 消费 rail 证据

**缓存依据**：`maya-crypto.html`。

已固化事实：

- Maya Crypto：buy/sell BTC、ETH、SOL、QNT 等；"Convert your crypto to cash in your Maya Wallet"；最低 ₱100 起步营销口径。
- FAQ："Can I send and receive crypto on Maya? This capability is still being built…"（缓存页状态）。
- 地区："Crypto not available in your location" 页面提示仅 PH 设备/位置可用（首次访问需设备位置在 PH）。
- Maya 生态本身有 bills / QR / load / send money / Maya Card（导航），但**缓存未提供 crypto 余额直接用于这些 rail 的证据**。

**读数**：Maya 在缓存中仅是 crypto 买卖 + 转现金（PHP）通道，send/receive 未上线、无直接 crypto 支付 rail 证据。

### 2.4 Bitrefill：crypto 礼品卡 / 话费 / eSIM / PH GCash voucher 桥

**缓存依据**：`bitrefill-docs.html`（一手）、`ddg-bitrefill.html`（secondary）、`bitrefill-ph.html`（blocked）。

已固化事实：

- 官方 API 文档（dateModified 2026-03-26）："The Bitrefill API lets you programmatically purchase gift cards, mobile top-ups, and eSIMs"；"Browse products — Search and filter gift cards, eSIMs, and mobile top-ups across 170+ countries"；"Pay with crypto or balance — Use Bitcoin, Lightning, Ethereum, USDC, USDT, or your account balance."；Business API 面向 crypto exchange / wallet 集成。
- 搜索页局部证据（Bitrefill PH 站点 meta + 商品标题）："Bitrefill (Philippines) - Shop for Gift Cards, eSIMs, and Mobile Recharges with BTC, ETH, USDT, USDC, and more. Pay online with crypto in over 186 countries"；含 **"Buy GCash Voucher with Bitcoin & Crypto"（`/ph/en/gift-cards/gcash-php/`）**、**"Buy GrabMart Gift Card with Bitcoin, ETH, USDT or Crypto"**。
- 实时 PH 页面被 Cloudflare 拦截；"170+ / 186 countries" 是营销口径，不进入区域/资格判定；GCash Voucher 商品存在性目前为 **secondary 证据**（搜索页标题）。

**读数**：Bitrefill 提供「crypto → 礼品卡/话费/eSIM → 本地消费或 e-wallet 余额」的非卡桥；在 PH 局部证据下尤其出现 **crypto → GCash Voucher → GCash PHP 余额 → QR/bills/load** 的两步路径。这是 GCash 路径的 voucher 变体。

### 2.5 Solana Pay / Shopify：stablecoin merchant checkout rail（含当前状态冲突）

**缓存依据**：`solanapay.html`、`solanapay-docs.html`、`shopify-solanapay.html`。

已固化事实：

- Solana Pay 主页："Solana Pay, an open, free-to-use payments framework built on Solana, is available to millions of businesses as an approved app integration on Shopify."；"direct merchant-to-consumer payment rail"；接受 USDC 或 SPL token；即时结算、near-zero fee。
- Docs：开放标准 + reference implementations；支持 Phantom/Solflare/Glow/Decaf/Espresso/Ottr/Ultimate/Tiplink；提供 web SDK 与 in-person POS；**版权 2023，属陈旧快照**。
- Shopify App Store 当前页："This app is not currently available on the Shopify App Store. If you have support questions, contact Helio Fintech Ltd directly."（开发者 Helio Fintech Ltd）。
- `solanapay-learn.html` 404。

**读数**：Solana Pay 是「商户直接接受 USDC/SPL」的支付框架，但 **Solana Pay 官方“approved Shopify integration”声明与 Shopify App Store 当前“not currently available”存在来源冲突**；本卡保留冲突，不把 Shopify availability 写成 current。

### 2.6 OpenNode：Bitcoin / Lightning merchant acceptance rail

**缓存依据**：`opennode.html`。

已固化事实：

- "We offer a complete processing solution for bitcoin-powered payments and payouts"；"Accept bitcoin and receive bitcoin or local currencies like EUR, GBP, USD and more"；"Process and settle bitcoin payments instantly through the Lightning Network"；"Automatically convert bitcoin to local currencies at the time of payment."；提供 hosted checkout / payment button / API / payouts。
- 缓存无 PH 专属资格/商户列表；"bitcoin & local currencies+" 为平台能力描述。

**读数**：OpenNode 证明「商户侧接受 BTC/LN 即形成现实购买力」的轨道路线存在（商家接受 crypto 的直接通道），但其证据是 merchant-side 能力，不是消费者钱包 rail；PH 覆盖 Unknown。

### 2.7 BSP 2025 E-Payments：PH 非卡零售轨背景（不含 crypto 拆分）

**缓存依据**：`bsp-2025.txt`（PDF 提取）、`bsp-2025-epayments.pdf`、`bsp-report-page.html`。

已固化事实（2025 报告）：

- 数字支付占零售交易量 **64.69%**（2024 为 57.45%），占价值 **53.32%**（**2024 价值份额在报告内存在 58.98% vs 59.98% 两处不一致**——保留冲突，不取单值）。
- QR Ph 交易量 **2.47B**（2025），较 2024 的 174.34M **+1,315.94%**；交易值 **PHP 1.16T**，较 PHP 227.47B **+408.32%**。
- QR Ph 参与机构 **48 家**；注册商户 ID **2.29M**（end-2025）。
- 商户支付占电子支付交易 **74.31%**；P2M 交易量 **2.93B**（+33.22%）。
- Paleng-QR Ph Plus 覆盖 1,435 城市；支付受理终端 **316,795**（mPOS 168,565 / POS 148,230）。
- **报告全程未提及 crypto / stablecoin / virtual asset**：只作「PH 零售非卡商户轨已是主流且高速扩张」的官方背景。

---

## 3. 非卡替代轨道的市场读数（AIX-independent）

1. **已证实 direct at-merchant 样本**：Coins.ph QR Ph Stablecoin Payments（官方 Help Center，2026-08-09 更新）是目前缓存中唯一「支付点直接用 stablecoin/crypto + 转换 + 完成商户付款」的 consumer rail；BSP 官方 QR Ph 统计证实该商户轨在 PH 是主流零售轨（2.47B 笔 / 2.29M 商户 / 48 机构）。
2. **两步转换是 PH 主要替代形态**：GCash（GCrypto → PHP wallet → QR/GBills/load）与 Maya（crypto → cash in wallet）都需先转成 PHP 再消费；Bitrefill→GCash Voucher 提供间接 voucher 变体。**direct 与 two-step 不得合并成一种机制。**
3. **商户侧接受 rails 独立存在**：Solana Pay（USDC/SPL，Shopify 状态冲突）与 OpenNode（BTC/Lightning，本地法币结算）证明商户直接接受 crypto 的基础设施路线，但两者都没有 PH 消费者覆盖证据。
4. **Peso stablecoin 层**：Coins.ph PHPC（BSP sandbox）是 PH 本地法币锚定稳定币，但其与 QRPH 支付的衔接在缓存中 Unknown；不等同于「PHPC 可直接扫 QR 消费」。
5. **不做替代量化**：BSP 数据不含 instrument 拆分，不能推导非卡 rails 对卡 rails 的替代比例；非卡 rails 也未达到任何 R1–R5 判定（本卡不做竞争分类）。

---

## 4. Unknown / 待决（Step 4 主文档 / 后续输入）

1. Coins.ph QRPH stablecoin payment 的**可用资产清单**（哪些 stablecoin / crypto 资产可直付）未在缓存文章中枚举；PHPC 是否可直接用于 QRPH 直付 Unknown。
2. Solana Pay "approved Shopify integration" 与 Shopify App Store "not currently available" 的冲突未裁决；Solana Pay docs 为 2023 快照，current 状态需重采集。
3. Bitrefill 实时 PH 页被拦截；PH GCash Voucher / GrabMart 商品只以搜索页标题为 secondary 证据；"170+ / 186 countries" 为营销口径。
4. GCash "Send and Receive Crypto with GCrypto" 正文未缓存（仅 section 索引）。
5. Maya send/receive 上线时点 Unknown（缓存页 "still being built" 无日期）。
6. OpenNode / Solana Pay 的 PH / VN / AU 商户覆盖 Unknown。
7. OpenNode 等 merchant-side rail 是否进入 Step 5 图谱（本卡不判）。
8. BSP 报告 2024 数字支付价值份额存在 58.98% / 59.98% 内部冲突，引用 2024 对比值时需注明。

---

## 5. 约束自检

- ✅ 未联网、未补抓、未新增 URL；全部事实来自 `/private/tmp/agent-g-evidence/` 缓存。
- ✅ AIX 仅以 future-entrant 纪律出现；未以 AIX 定义、过滤、升级或降级任何玩家/rail。
- ✅ direct at-merchant 与 two-step / voucher 路径严格分开，未合并机制。
- ✅ 无效缓存（Azteco 错站点、MoneyGram 空壳、Coinbase Commerce/Strike 拦截、Bitrefill live 拦截、Wayback 未归档、Solana Pay learn 404）明确排除，不产生事实。
- ✅ 来源冲突保留为 conflicts：Solana Pay/Shopify、BSP 2024 价值份额。
- ✅ 营销数字（600k+ stores、170+/186 countries、5M+、$20B、2,000+ billers 等）只作为品牌/宣传记录，不进入资格或密度判定。
- ✅ Unknown ≠ No：Bitrefill PH 商品、GCash send/receive、PHPC→QR、Maya 上线、merchant rails PH 覆盖全部保持 Unknown。
- ✅ 本卡不做 R1–R5 竞争分类，不替代 `04-competition-map.md`。

---

## 6. 来源映射（仅本地证据文件）

| 本卡内容 | 来源 |
|---|---|
| Coins.ph 主页品牌/营销声明 | `coinsph.html`（canonical https://www.coins.ph/en-ph） |
| QRPH Stablecoin Payments 直付流程 | `coinsph-sec-13216784335897.json` / `coinsph-art-57075258143001.json`（updated 2026-08-09） |
| QR Ph 定义/费用/要求 | `coinsph-sec-13216784335897.json` |
| InstaPay / PESONet / Remittance / GrabPay cash-out | `coinsph-sec-202591667.json`、`coinsph-art-202398194.json` |
| PHPC stablecoin | `coinsph-sec-36152938993305.json`、`coinsph-art-33977644340121.json` |
| GCrypto 买卖/提现/币种网络 | `gcash-art-47624429776025.json`、`gcash-art-31304830152089.json`、`gcash-art-9781218166041.json`、`gcash-sec-31268521864217.json` |
| GCash Pay QR / GBills / Alipay+ | `gcash-sec-360004657934.json`、`gcash-sec-360004696173.json`、`gcash-art-360017563034.json`、`gcash-art-900004373166.json` |
| GCash Send/Receive crypto section 索引 | `gcash-sections.json`（section 31272577173785） |
| Maya Crypto | `maya-crypto.html` |
| Bitrefill API / 支付方式 | `bitrefill-docs.html`（dateModified 2026-03-26） |
| Bitrefill PH / GCash Voucher / GrabMart secondary | `ddg-bitrefill.html` |
| Solana Pay 主页 / Docs / Shopify 冲突 | `solanapay.html`、`solanapay-docs.html`、`shopify-solanapay.html` |
| OpenNode | `opennode.html` |
| BSP 2025 E-Payments 统计 | `bsp-2025.txt`、`bsp-2025-epayments.pdf`、`bsp-report-page.html` |

---

## 7. 输出 JSON

```json
{
  "outcome": "PASS",
  "summary": "Step 4 Agent G2 materialized the non-card substitute-rail evidence card from /private/tmp/agent-g-evidence caches only (no browsing, no new URLs, no AIX positioning). Strongest direct evidence: Coins.ph QRPH Stablecoin Payments (official Help Center, updated 2026-08-09) lets PH users scan QR Ph and pay with stablecoins/crypto or a PHP+crypto mix, with rate confirmation and 'Confirm convert and pay' at the point of sale; BSP 2025 E-Payments report confirms the underlying QR Ph rail is PH mainstream (2.47B transactions, PHP 1.16T value, 48 FIs, 2.29M merchant IDs) while containing no crypto/stablecoin split. Two-step paths kept separate: GCash GCrypto only withdraws to the PHP GCash wallet before QR/GBills/load spend; Maya only converts crypto to cash in the Maya wallet, with send/receive still being built; Bitrefill provides a crypto-funded voucher/top-up bridge including a PH GCash Voucher listing (secondary search-page evidence) but its live PH page was Cloudflare-blocked. Merchant-side rails captured with conflicts: Solana Pay claims approved Shopify integration while the current Shopify App Store page says the app is not available; OpenNode shows Bitcoin/Lightning merchant acceptance with local-currency settlement. PHPC is recorded as a BSP-sandbox peso stablecoin but its direct use for QRPH payment remains Unknown. Invalid captures (Azteco wrong-site, MoneyGram empty shell, Coinbase Commerce/Strike blocked, Wayback not archived, Solana Pay learn 404) are explicitly excluded; no R1-R5 classification was attempted.",
  "changedFiles": [
    "research/aix-market-positioning/evidence/04-agent-g2-non-card-substitute-rails-evidence-card.md"
  ],
  "tests": [
    "every cited cache file exists under /private/tmp/agent-g-evidence and supports the quoted fact (spot-checked coinsph.html, coinsph-sec-13216784335897, coinsph-sec-202591667, coinsph-sec-36152938993305, gcash art/sec JSON, maya-crypto.html, bitrefill-docs.html, ddg-bitrefill.html, solanapay.html, shopify-solanapay.html, opennode.html, bsp-2025.txt)",
    "exact-quote verification via rg/python extraction: QRPH 'Confirm convert and pay', GCrypto 'moves your crypto funds to your GCash Wallet', Maya 'still being built', Bitrefill 'Use Bitcoin, Lightning, Ethereum, USDC, USDT', Shopify 'not currently available', BSP '64.69%'/'2.47 billion'/'1,315.94%'",
    "invalid-capture audit: azteco (wrong business), moneygram (Angular shell with zero visible body text), coinbase-commerce/cb-commerce2 (Cloudflare), strike (403), bitrefill-ph (Cloudflare), wayback (not archived), gcash-crypto (404), solanapay-learn (404), coinsph-search/gcash-search (Not found) marked non-evidence",
    "direct-vs-two-step discipline: Coins.ph direct crypto-at-payment QR vs GCash/Maya crypto-to-PHP conversion vs Bitrefill voucher bridge kept as distinct mechanisms",
    "source-conflict checks: Solana Pay Shopify claim vs current Shopify App Store 'not currently available'; BSP 2024 value share 58.98% vs 59.98% preserved as unresolved",
    "marketing-number guardrail: 600k+ stores, 170+/186 countries, 5M+ users, $20B volume, 2,000+ billers not used as issuance/eligibility gates",
    "Unknown discipline: PHPC-to-QRPH direct spend, Bitrefill PH catalog, GCash send/receive article body, Maya launch timing, merchant-rail PH coverage all remain Unknown",
    "AIX guardrail scan: AIX appears only in the future-entrant discipline note; no AIX fact filtered, upgraded, or downgraded any rail/player",
    "scope check: card performs no R1-R5 classification and does not replace 04-competition-map.md",
    "JSON block at end of the card parses as valid JSON"
  ],
  "commands": [
    "ls -la /private/tmp/agent-g-evidence to inventory the 76-file cache set",
    "python3 HTML extraction over coinsph/maya/bitrefill/solanapay/opennode/bsp caches to verify every cited fact against cache text",
    "python3 Zendesk JSON body extraction over coinsph-*/gcash-* to verify help-article quotes and updated_at dates",
    "rg -n -i 'QRPH Stablecoin Payments|Confirm convert and pay|GCrypto Trading Wallet|crypto to cash in your Maya Wallet|Bitcoin, Lightning, Ethereum, USDC, USDT|not currently available|64.69%|2.47 billion|1,315.94%' /private/tmp/agent-g-evidence",
    "git status --short to confirm only the new evidence card was added"
  ],
  "decisionsRequired": [
    "Decide whether Coins.ph QRPH Stablecoin Payments is entered as an independent non-card direct-spend mode (and which stablecoin/crypto assets are eligible) in Step 4 competition mapping; PHPC-to-QRPH direct use is still unknown",
    "Adjudicate the Solana Pay 'approved Shopify integration' claim against the current Shopify App Store 'not currently available' page before any merchant-rail availability statement",
    "Decide whether Bitrefill PH GCash Voucher/GrabMart listings (currently secondary search-page evidence, live page blocked) need re-collection for PH voucher-bridge density",
    "Decide whether GCash 'Send and Receive Crypto with GCrypto' and its direct-vs-two-step handling need the article body fetched before Step 4 usage",
    "Determine whether merchant-side rails (Solana Pay, OpenNode) are in scope for Step 5 or remain infrastructure context only",
    "Resolve BSP 2024 digital-payment value-share internal conflict (58.98% vs 59.98%) before citing 2024 comparisons",
    "Keep excluding AIX current facts from non-card rail edits; any AIX entry decision belongs to the Step 5 positioning agent"
  ],
  "requiresGptReview": true
}
```
