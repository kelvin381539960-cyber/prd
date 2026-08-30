# Evidence Sources — AIX Strategic Validation Update 08

> Traceability index for the fixed synthesis. Sources are separated into AIX Data/Code Facts, Market/Vendor/Regulatory Facts, and Decisions. No raw user IDs or PII are included.

## AIX Data / Code Facts

### AIX-D1 — Production aggregate and cohort construction

**Source.** Archery instance `SG-AIX-AIXPAY-A-OB-MASTER-AWS`, database `aixpay_wallet`.

**Tables and filters recorded.**

- `crypto_transaction`: `transaction_type=1 (DEPOSIT)` and `status=200 (COMPLETED)`.
- `card_transaction`: `transaction_type=2 (PURCHASE)`; successful spend uses `status=221 (CAPTURED)`. Current production rows also include `status=301 (REVERSED)` and `status=900 (DENIED)`.
- `aixpay_app.users` and `test_user_info`: used to exclude explicit test users.
- Canonical backend code: used to map transaction enums.

**Aggregate outputs.**

| Output | Result |
|---|---:|
| Distinct card users overall | 92 |
| Completed Deposit transactions / users | 108 / 31 |
| Completed Deposit business transaction time | 2026-04-13 → 2026-08-28 |
| CAPTURED Purchase 221 transactions / users | 166 / 22 |
| REVERSED Purchase 301 transactions / users | 38 / 13 |
| DENIED Purchase 900 transactions / users | 187 / 19 |
| Purchase rows with status 200 | 0 |

Among the 31 completed-Deposit users: repeat Deposit ≥2 = 15; Deposit on ≥2 days = 11; Deposit across ≥2 months = 8; any captured Purchase = 21; captured Purchases ≥2 = 17; Purchase on ≥2 days = 15; Purchase across ≥2 months = 10; repeat Deposit + repeat Purchase = 10; both across ≥2 months = 6; later completed Deposit after first captured Purchase = 9; and full Deposit → Purchase → later Deposit → later Purchase loop = 7.

The 21 Deposit+Purchase users have active spans of 0–6d = 3, 7–29d = 8, 30–59d = 3, and 60d+ = 7. The mature cohort with first Deposit ≤2026-06-30 has 25 users: repeat Deposit 14, any captured Purchase 18, repeat Purchase 14, multi-month both 6, and full loops 6.

Excluding explicit test users does not change the counts.

**Limitations.** These are production aggregates only. They contain no raw user IDs or PII and are descriptive, not Gate thresholds. A Purchase status-200 assumption is invalid for the current data; status 221 is the captured-spend cohort.

### AIX-D2 — Geographic descriptive aggregate

**Filter.** Non-test users, grouped by phone-country, with the same Deposit and captured-Purchase definitions as AIX-D1.

| Phone-country | Deposit users | Purchase users | Repeat-both | Full-loop |
|---|---:|---:|---:|---:|
| PH | 22 | 14 | 4 | 2 |
| SG | 5 | 5 | 4 | 3 |
| HK | 2 | 2 | 2 | 2 |
| US | 2 | 0 | 0 | 0 |

PH-only outputs: 22 Deposit users; repeat Deposit 9; Purchase 14; repeat Purchase 10; repeat both 4; multi-month both 2; full loop 2.

**Limitation.** Sample sizes are small. These aggregates are descriptive and must not rank markets by rates or establish a market-priority conclusion.

### AIX-D3 — Retention and runtime-boundary facts

**Fact.** `transaction_balance_record` represents card balance auto-transfer / rollback evidence, not general Wallet retention history.

**Fact.** Wallet and Card are separate in the current implementation. Auto Debit has partial runtime confidence. Send, outbound Crypto Withdraw, Fiat bank/e-wallet cashout, and Unified funding/balance are not runtime-confirmed.

**Limitation.** A balance record alone cannot establish retained funds or a durable Wallet relationship. The missing evidence must link wallet balance or ledger-derived holding over time to captured spend, renewed inflow, and repeat active use while distinguishing retained funds from just-in-time funding.

## Market / Vendor / Regulatory Facts

### M1 — BSP QR Ph policy

**Source.** BSP Memorandum M-2023-005: <https://www.bsp.gov.ph/Regulations/Issuances/2023/M-2023-005.pdf>

**Fact used.** PSPs offering QR-enabled end-user payment services must adopt QR Ph; PSP merchant deployments require QR Ph; proprietary payment QR was disabled from 1 July 2023.

**Limitation.** This establishes the regulatory QR Ph context, not AIX-specific authorization, partner access, economics, or a build decision.

### M2 — BSP PPDD QR Ph scale

**Source.** BSP Payment and Settlement Systems quarterly/periodic bulletin: <https://www.bsp.gov.ph/PaymentAndSettlement/PPDD_Payments_Bulletin.pdf>

**Fact used.** The latest bulletin retrieved in June 2026 reports Jan–Jun 2026 QR Ph volume 2.5B, value PHP1.1T, 33 sender/receiver participants, 13 sender-only participants, 5 receiver-only participants, account penetration 81%, and 2,642,374 registered Merchant IDs as of 30 June 2026.

**Limitation.** Registered Merchant IDs are not unique merchants. Market scale does not establish incremental AIX frequency, partner willingness, or unit economics.

### M3 — Paleng-QR Ph Plus

**Source.** BSP Paleng-QR Ph Plus: <https://www.bsp.gov.ph/Pages/InclusiveFinance/PalengQR/PalengQRProgram.aspx?ID=2744>

**Fact used.** There were 1,566 enjoined/participating LGUs as of 31 July 2026. FSPs with QR Ph capability can participate in merchant and account onboarding.

**Limitation.** Program reach is not evidence of a named willing AIX partner, commercial terms, demand, or defensible differentiation.

### M4 — BSP merchant-acquisition capital and operating-role sources

**Sources.**

- BSP Circular 1198 FAQ: <https://www.bsp.gov.ph/Regulations/Issuances/2024/1198%20-%20FAQ.pdf>
- BSP MORPS: <https://www.bsp.gov.ph/Regulations/MORPS/MORPS.pdf>
- BSP M-2025-002: <https://www.bsp.gov.ph/Regulations/Issuances/2025/M-2025-002.pdf>

**Fact used.** The current FAQ states that OPS-MAL Category A, with average monthly collected funds transferred to merchants below PHP100m, has a PHP5m minimum capital; Category B, at or above PHP100m, has a PHP10m minimum capital. Exact AIX requirements remain Unknown because they depend on the operating role.

**Source-conflict resolution.** An earlier draft-derived note of PHP20m for the ≥PHP100m case is not carried forward. For this report, the current BSP Circular 1198 FAQ supersedes that earlier PHP20m note.

**Limitation.** The sources do not classify AIX’s eventual operating model. They do not by themselves establish whether AIX should use a partner-led, gateway/orchestration, direct, or hybrid access model.

### M5 — Coins.ph QRPH Stablecoin Payments

**Source.** Coins.ph support article: <https://support.coins.ph/hc/en-us/articles/57075258143001-QRPH-Stablecoin-Payments-Scan-and-Pay-with-Peso-Crypto-or-a-Mix-of-Both>

**Fact used.** Official QRPH Stablecoin Payments went live in April 2026 and supports payment with PHP, USDT, USDC, other supported crypto, or a mix.

**Limitation.** “First” and merchant-count statements are competitor claims, not BSP market totals. The live product means stablecoin-to-QRPH is not white space or a moat; it does not establish AIX demand or differentiation.

### M6 — BSP OFW / cross-border remittance flows

**Source.** BSP Table 11: <https://www.bsp.gov.ph/statistics/external/ofw2.aspx>

**Facts used.** Jan–Jun 2026 cash remittances were USD17.148609B versus USD16.753175B in Jan–Jun 2025. Jan–Jun 2026 source-country cash remittances were United States USD6.758828B, Singapore USD1.228317B, Saudi Arabia USD1.076501B, UAE USD0.750287B, and Malaysia USD0.344746B. Singapore is approximately 3.6× Malaysia by this period’s recorded flow.

**Limitation.** These are source-country recorded remittance flows. They do not by themselves prove AIX demand, user willingness to retain funds, or a global first corridor. They support Singapore as the primary ASEAN discovery sample and Malaysia as comparator by observed ASEAN scale only.

### M7 — World Bank corridor cost dispersion

**Sources.**

- Malaysia→Philippines: <https://remittanceprices.worldbank.org/corridor/Malaysia/Philippines>
- Singapore→Philippines: <https://remittanceprices.worldbank.org/corridor/SG/PH>

**Facts used.** Q3 2025 corridor pages display USD200 and USD500 baskets. Malaysia→Philippines reports averages of 3.92% and 2.53% across the two displayed baskets; Singapore→Philippines reports 3.16% and 2.09%; individual providers range lower and higher.

**Limitation.** These pages establish provider/cost heterogeneity and friction only. They do not prove stablecoin is cheaper, establish current user pain for AIX, or validate a remittance product.

### M8 — GCash component coverage

**Sources.**

- GCash fees and consumer ecosystem: <https://www.gcash.com/services/fees>
- GCash GCrypto: <https://www.gcash.com/services/gcrypto>

**Fact used.** GCash’s current consumer ecosystem includes bank transfer, overseas send-money, cash-in/out, GCrypto Peso↔crypto, and blockchain Send/Receive.

**Limitation.** Component coverage by an incumbent does not establish an integrated receive → hold → spend/send relationship, AIX demand, willingness to retain funds, or differentiation.

## Decisions and review references

### D1 — P1 Gate status

**Decision.** P1 changes from `NOT YET VALIDATED / DATA GAP` to **`NOT_YET_PASS — positive repeat-relationship signal proven; linked fund-retention evidence gap`**. It is neither FAIL nor PASS. P2 scale remains blocked.

**Independent challenge reference.** AChatGPT GPT-5.6 Luna/xhigh, job `job_01M19G49494NWP547AWCR7JV5G`, returned `P1_GATE = NOT_YET_PASS` with high confidence.

**Limitation.** The repeat relationship does not prove that funds were retained rather than deposited immediately before spending. No numerical Gate threshold is set.

### D2 — QR Ph discovery decision

**Decision.** QR Ph P2M remains **Priority Discovery Rail**, with close-out verdict **SUPPORTS PRIORITY DISCOVERY**.

**Review reference.** Job `job_01M19GCT3ZB9BWA6X0DB897W3P`.

**Limitation.** This is not build authorization, white space, or moat. Named partner, commercial and settlement economics, regulatory classification, incremental frequency, and defensible differentiation remain Unknown.

### D3 — Remittance discovery decision

**Decision.** OFW / cross-border remittance remains **Primary J1 Discovery Wedge** and **SUPPORTS PRIMARY J1 DISCOVERY** at the use-case level. Corridor priority is Singapore→Philippines primary ASEAN sample, Malaysia→Philippines comparator, US/Saudi scale benchmarks, and global first corridor Unknown.

**Limitation.** This does not prove a stablecoin remittance product direction. Direct user demand, willingness to receive and retain funds in AIX, willingness to spend/send from AIX, partner/regulatory access, and economics require research.

### D4 — Roadmap impact

**Decision.** Keep `Current → P1 One Money Relationship → P2 Multi-rail Everyday Spend → P3 Everyday Money Account`, `A6 → A3 → A1`, and `Gate Serial / Discovery Parallel`. Continue P2 and J1 discovery in parallel while closing P1 evidence; do not scale P2 before P1 acceptance.

**Boundary.** This update refines evidence and priority only. It does not specify pages, UI, APIs, fields, state machines, PRD, or implementation.
