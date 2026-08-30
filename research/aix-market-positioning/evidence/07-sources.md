# Strategic Validation v1 — Evidence Index

> Date: 2026-08-30
> Purpose: Evidence used to prioritize P1 validation, the Phase 2 local-rail discovery order, and the Phase 3/J1 discovery order.
> Discipline: Market rail scale ≠ stablecoin adoption; competitor claim ≠ market total; population size ≠ stablecoin demand; discovery priority ≠ committed build.

## AIX Data / Internal Evidence

### AIX current capability and P1 data query

**Supports**
- Current capability baseline: Receive/Hold/Swap/Card Spend confirmed; Wallet/Card separate; Auto Debit partial runtime confidence; Send/outbound Crypto Withdraw/Fiat bank-e-wallet cashout/Unified funding-balance have no runtime confirmation.
- AIX Data catalog reported `anchor_status=drift_detected`, with `review_required_fields` limited to `card.card_status`; this P1 relationship analysis does not depend on that field.
- `txn_type` aggregation returned PURCHASE=68, TOP_UP=27, REVERSAL=63, REVERSAL_TO_ACCOUNT=4, ACCOUNT_VERIFICATION=12, CAPTURE=6, REFUND=7.
- UDP metadata located `c_aix_com_aix_x.x_dwd_aix_trx_crypto_deposit_completed_di` and `x_dwd_aix_trx_card_transaction_auth_approval_di`.

**Limitations**
- Transaction-type counts do not establish same-user repeat behavior or retention.
- `udp_get_physical_table_detail` was unavailable upstream.
- Custom Archery query was blocked by `Instance does not exist`; the anonymous cohort evidence required for P1 remains unavailable.
- Balance persistence cannot be treated as positive retention while Send/Withdraw runtime is unconfirmed.

## PH Local Rail

### 1. BSP — PPDD Payments Bulletin
URL: https://www.bsp.gov.ph/PaymentAndSettlement/PPDD_Payments_Bulletin.pdf

**Supports**
- QR Ph P2M Jan–Dec 2025 volume 2.5B and value PHP 1.2T.
- Dec-2025 volume 431.2M and value PHP 179.4B.
- 2,289,106 registered Merchant IDs at 31 Dec 2025.
- QR Ph P2M participant account penetration 78%.
- InstaPay QR Jan–Dec 2025 volume 183.3M and value PHP 926.1B.

**Limitations**
- Merchant IDs are not unique merchants.
- Payment-rail scale does not prove stablecoin/crypto usage share.
- This source does not prove AIX demand or incremental usage.

### 2. Coins.ph Support — QRPH Stablecoin Payments
URL: https://support.coins.ph/hc/en-us/articles/57075258143001-QRPH-Stablecoin-Payments-Scan-and-Pay-with-Peso-Crypto-or-a-Mix-of-Both

**Supports**
- QRPH Stablecoin Payments is live in 2026.
- Users can scan QRPH and pay using PHP, USDT, USDC/other supported crypto, or a mix.

**Limitations**
- A competitor product proves feasibility/current competition, not AIX demand or moat.

### 3. Coins.ph Blog — QRPH Stablecoin integration
URL: https://www.coins.ph/en-ph/blog/pay-with-peso-crypto-or-both-coins-ph-pioneers-stablecoin-payment-utility-in-the-philippines-with-first-of-its-kind-qrph-integration

**Supports**
- Coins.ph states that the integration launched in April 2026.
- Coins.ph describes itself as the first Philippine e-wallet with this integration and cites nearly 700,000 merchants.

**Limitations**
- “First” and “nearly 700,000 merchants” are competitor claims, not BSP market totals.
- The source does not establish QR Ph as white space or a defensible moat.

### 4. BSP Memorandum M-2025-031 — VASP moratorium
URL: https://www.bsp.gov.ph/Regulations/Issuances/2025/M-2025-031.pdf

**Supports**
- Moratorium on issuance of new VASP licenses continues from 1 September 2025.
- BSP cites consumer-protection and cybercrime concerns and retains the ability to reassess.

**Limitations**
- Does not establish that a specific future AIX operating model necessarily needs a new VASP license.

### 5. BSP — Active VASP List
URL: https://www.bsp.gov.ph/Lists/Directories/Attachments/19/VASP.pdf

**Supports**
- Current active VASP list includes players such as Coins.ph, Maya and PDAX.

**Limitations**
- Presence on the list does not define AIX's future regulatory classification or partner structure.

## J1 / Recurring Inflow

### 6. BSP Media Release — 2025 Remittances
URL: https://www.bsp.gov.ph/Media_And_Research/Media%20Releases/2026_03/news-03132026a1.aspx

**Supports**
- 2025 personal remittances USD 39.619B.
- 2025 cash remittances through the banking system USD 35.634B.

**Limitations**
- Market flow size does not prove demand for AIX or stablecoin-based remittance.

### 7. BSP — OFW Remittance Statistics
URL: https://www.bsp.gov.ph/statistics/external/ofw2.aspx

**Supports**
- 2026 Jan–Jun cash remittances USD 17.149B versus USD 16.753B in 2025 Jan–Jun.

**Limitations**
- Does not establish user willingness to receive, hold, send or spend through AIX.

### 8. World Bank — Remittance Prices Worldwide
URL: https://remittanceprices.worldbank.org/

**Supports**
- Global average remittance cost of 6.36% in the Q3/Sep-2025 context.
- Remittance cost remains a measurable friction.

**Limitations**
- Global average is not a specific corridor or provider price.
- Does not prove stablecoin is cheaper.

### 9. World Bank — Malaysia to Philippines Corridor
URL: https://remittanceprices.worldbank.org/corridor/Malaysia/Philippines

**Supports**
- The corridor contains both lower-cost digital providers and higher-cost traditional options.

**Limitations**
- Cost is heterogeneous; no blanket “remittance is expensive” or “stablecoin is cheaper” conclusion is supported.

### 10. PSA — Digital Economy 2025
URL: https://psa.gov.ph/content/digital-economy-contributes-98-percent-philippine-economy-2025

**Supports**
- 2025 digital-economy employment 10.39M, 21.2% of total employment.

**Limitations**
- Employment size does not prove stablecoin payroll or freelancer-payment demand.

### 11. PSA — December 2025 Labor Force
URL: https://psa.gov.ph/content/number-unemployed-persons-december-2025-increased-226-million-filipinos-aged-15-years-and

**Supports**
- Wage and salary workers were 64.2% of the workforce in Dec-2025.

**Limitations**
- Large payroll population does not establish willingness to receive payroll in stablecoin or through AIX.

## Evidence Discipline

1. P1 remains `NOT YET VALIDATED / DATA GAP`; transaction existence is not relationship validation.
2. QR Ph P2M is a `Priority Discovery Rail`, not a committed build, white space, or moat.
3. Coins.ph proves live stablecoin→QRPh competition; its own scale claims remain competitor claims.
4. BSP rail statistics prove rail maturity/scale, not stablecoin adoption.
5. VASP moratorium/list prove regulated-access constraints, not AIX-specific license requirements.
6. OFW/cross-border remittance is a `Primary J1 Discovery Wedge`, not a proven AIX product direction.
7. Remittance cost friction does not prove stablecoin is always cheaper.
8. Payroll/digital-employment population does not prove stablecoin payroll demand.
9. Roadmap order remains unchanged; Gate Serial / Discovery Parallel.
10. No fabricated numerical Gate or Kill threshold is introduced.

End with one JSON object containing outcome, summary, changedFiles, tests, commands, decisionsRequired and requiresGptReview.
