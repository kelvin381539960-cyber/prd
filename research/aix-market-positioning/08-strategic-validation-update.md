# AIX Strategic Validation Update 08

> Scope: mechanical materialization of the fixed synthesis. This update refines evidence and discovery priority; it does not add research or define implementation.

## Executive update

**Decision.** The roadmap is unchanged:

`Current → P1 One Money Relationship → P2 Multi-rail Everyday Spend → P3 Everyday Money Account`

The strategic sequence remains `A6 → A3 → A1`, with **Gate Serial / Discovery Parallel** execution.

| Area | Current position | Boundary |
|---|---|---|
| P1 One Money Relationship | **`NOT_YET_PASS — positive repeat-relationship signal proven; linked fund-retention evidence gap`** | Not FAIL and not PASS. |
| P2 QR Ph P2M | **Priority Discovery Rail**; close-out verdict: **SUPPORTS PRIORITY DISCOVERY** | Not build authorization, white space, or moat. |
| P3/J1 OFW / cross-border remittance | **Primary J1 Discovery Wedge**; discovery remains supported | Not a proven AIX product direction. |

An independent P1 challenge by AChatGPT GPT-5.6 Luna/xhigh, job `job_01M19G49494NWP547AWCR7JV5G`, returned `P1_GATE = NOT_YET_PASS` with high confidence.

The QR Ph P2M close-out job is `job_01M19GCT3ZB9BWA6X0DB897W3P`. Its verdict is **SUPPORTS PRIORITY DISCOVERY**.

For remittance discovery, **Singapore→Philippines = primary ASEAN discovery sample; Malaysia→Philippines = ASEAN comparator; US/Saudi = scale benchmarks; global first corridor = Unknown**. This corridor choice is not inferred from current AIX countries.

## P1 Data Facts — production aggregate

**Fact.** The production aggregate is from Archery instance `SG-AIX-AIXPAY-A-OB-MASTER-AWS`, database `aixpay_wallet`. `aixpay_app.users` and `test_user_info` were used to exclude explicit test users. The output contains no raw user IDs or PII. Canonical backend code supplied the transaction-enum mapping.

### Population and transaction filters

| Population or filter | Aggregate output |
|---|---:|
| Distinct card users overall | 92 users |
| Completed crypto Deposit: `crypto_transaction.transaction_type=1 (DEPOSIT)` and `status=200 (COMPLETED)` | 108 transactions / 31 users |
| Completed Deposit business transaction time | 2026-04-13 → 2026-08-28 |

**Fact.** Current production Purchase rows use captured status `221` for the successful-spend cohort:

| `card_transaction` filter | Meaning | Aggregate output |
|---|---|---:|
| `transaction_type=2 (PURCHASE)`, `status=221` | CAPTURED | 166 transactions / 22 users |
| `transaction_type=2 (PURCHASE)`, `status=301` | REVERSED | 38 transactions / 13 users |
| `transaction_type=2 (PURCHASE)`, `status=900` | DENIED | 187 transactions / 19 users |

There are no status-200 Purchase rows in the current data. P1 therefore uses status `221`, not status `200`, for captured Purchase.

### Deposit and captured-Purchase relationship

**Fact.** Among the 31 completed-Deposit users:

| Signal | Users |
|---|---:|
| Repeat Deposit, at least 2 | 15 |
| Deposit on at least 2 days | 11 |
| Deposit activity across at least 2 months | 8 |
| At least 1 captured Purchase | 21 |
| At least 2 captured Purchases | 17 |
| Purchase activity on at least 2 days | 15 |
| Purchase activity across at least 2 months | 10 |
| Repeat Deposit + repeat Purchase | 10 |
| Repeat Deposit + repeat Purchase, both across at least 2 months | 6 |
| A later completed Deposit after first captured Purchase | 9 |
| Deposit → Purchase → later Deposit → later Purchase | 7 |

Among the 21 Deposit+Purchase users, active-span distribution is descriptive only:

| Active span | Users |
|---|---:|
| 0–6 days | 3 |
| 7–29 days | 8 |
| 30–59 days | 3 |
| 60 days+ | 7 |

No span is a Gate threshold.

The mature cohort with first Deposit on or before 2026-06-30 contains 25 users: 14 repeat Deposit users, 18 users with any captured Purchase, 14 repeat-Purchase users, 6 with multi-month Deposit and Purchase activity, and 6 full loops. These are descriptive outputs, not pass thresholds.

Excluding explicit test users does not change the counts.

### Geographic descriptive signal

**Fact.** Non-test phone-country aggregates are descriptive and small; they must not be used to rank markets by rate.

| Phone-country group | Deposit users | Purchase users | Repeat-both | Full-loop |
|---|---:|---:|---:|---:|
| PH | 22 | 14 | 4 | 2 |
| SG | 5 | 5 | 4 | 3 |
| HK | 2 | 2 | 2 | 2 |
| US | 2 | 0 | 0 | 0 |

The PH-only cohort has 22 Deposit users: repeat Deposit 9, Purchase 14, repeat Purchase 10, repeat both 4, multi-month both 2, and full loop 2. Sample sizes are small.

## P1 interpretation and Gate

### Proven — Fact

A positive repeated purchasing-power relationship exists for a subset of users: repeat Deposits, repeat captured Purchases, renewed inflow after Purchase, multi-period activity, and complete Deposit → Purchase → Deposit → Purchase loops. P1 is no longer a generic `DATA GAP`.

### Unproven — Unknown

- There is no linked evidence that funds remain in AIX over time rather than users making just-in-time Deposits before spending.
- A general Wallet balance history or holding-duration source sufficient to link retention with active use has not been obtained.
- `transaction_balance_record` is card balance auto-transfer / rollback evidence, not general Wallet retention history.
- Wallet and Card remain separate in the current implementation. Auto Debit has partial runtime confidence. Send, outbound Crypto Withdraw, Fiat cashout, and Unified funding are not runtime-confirmed. Balance persistence alone therefore cannot be treated as retention.

### Gate decision — Decision

P1 does not pass yet. P2 scale remains blocked.

Minimum next P1 evidence is a non-PII production aggregate that links per-user wallet balance or ledger-derived holding over time to captured spend, renewed inflow, and repeat active use, sufficiently distinguishing retained funds from just-in-time funding. No numerical threshold is invented; evidence sufficiency must be explicit before a negative or positive Gate decision.

## QR Ph P2M discovery

### Latest official and vendor facts

- **Market / Regulatory Fact [M1].** BSP M-2023-005 requires PSPs offering QR-enabled end-user payment services to adopt QR Ph. PSP merchant deployments require QR Ph, and proprietary payment QR was disabled from 1 July 2023.
- **Market Fact [M2].** The latest BSP PPDD bulletin retrieved in June 2026 reports Jan–Jun 2026 QR Ph volume of 2.5B and value of PHP1.1T; 33 sender/receiver participants, 13 sender-only participants, and 5 receiver-only participants; account penetration of 81%; and 2,642,374 registered Merchant IDs as of 30 June 2026. Merchant IDs are not unique merchants.
- **Market Fact [M3].** Paleng-QR Ph Plus had 1,566 enjoined/participating LGUs as of 31 July 2026. FSPs with QR Ph capability can participate in merchant and account onboarding.
- **Regulatory Fact [M4].** The current merchant-acquisition source is BSP Circular 1198 / MORPS / FAQ. OPS-MAL Category A, where average monthly collected funds transferred to merchants are below PHP100m, has a PHP5m minimum capital; Category B, at or above PHP100m, has a PHP10m minimum capital. The exact AIX requirement remains Unknown because it depends on the operating role.
- **Vendor Fact [M5].** Coins.ph official QRPH Stablecoin Payments went live in April 2026 and supports QRPH payment with PHP, USDT, USDC, other supported crypto, or a mix. Claims such as “first” and merchant count remain competitor claims.

### Decision and boundaries

**Decision.** QR Ph P2M **SUPPORTS PRIORITY DISCOVERY**.

Plausible access-model proposals are:

- partner-led bank, EMI, acquirer, or PSP access;
- gateway / technology orchestration with a licensed partner owning acceptance and settlement;
- direct or hybrid access only as an Unknown requiring a separate compliance and operating-model assessment.

This is not build authorization, white space, or moat. Coins.ph already demonstrates that stablecoin-to-QRPH payment is live.

**Unknown.** A named willing partner, commercial terms, MDR, settlement and reconciliation economics, FX / conversion / liquidity economics, AIX-specific regulatory classification, incremental AIX user demand or frequency, and defensible differentiation remain unproven.

**Disconfirmers.** No credible partner path; negative unit economics; unacceptable capital, compliance, or operational burden; no incremental frequency or scenario; or no differentiation beyond current competitors.

## OFW / cross-border remittance J1 discovery

### Official market and vendor facts

- **Market Fact [M6].** BSP Table 11 reports Jan–Jun 2026 cash remittances of USD17.148609B versus USD16.753175B in Jan–Jun 2025.
- **Market Fact [M6].** Jan–Jun 2026 source-country cash remittances were: United States USD6.758828B; Singapore USD1.228317B; Saudi Arabia USD1.076501B; UAE USD0.750287B; and Malaysia USD0.344746B. These are source-country recorded remittance flows and do not by themselves prove AIX demand.
- **Decision from market scale [M6].** Singapore’s flow is approximately 3.6× Malaysia’s in Jan–Jun 2026, so Singapore is the stronger ASEAN discovery sample by observed remittance scale. This is not a global first-market conclusion.
- **Market Fact [M7].** World Bank Q3 2025 corridor pages show provider and cost dispersion, with USD200 and USD500 baskets. Malaysia→Philippines reports corridor averages of 3.92% and 2.53% across the two displayed baskets; Singapore→Philippines reports 3.16% and 2.09%, with individual providers ranging lower and higher. Use this only to establish cost heterogeneity and friction; do not claim stablecoin is cheaper.
- **Vendor Fact [M8].** GCash’s current consumer ecosystem includes bank transfer, overseas send-money, cash-in/out, GCrypto Peso↔crypto, and blockchain Send/Receive. Incumbents therefore cover many component Jobs; the evidence strengthens the need to prove an integrated receive → hold → spend/send relationship, not merely crypto access.

### Decision, research jobs, and disconfirmers

**Decision.** OFW / cross-border remittance **SUPPORTS PRIMARY J1 DISCOVERY** at the use-case level. It is not a proven stablecoin remittance product direction.

**Corridor decision:** **Singapore→Philippines = primary ASEAN discovery sample; Malaysia→Philippines = comparator; US/Saudi = scale benchmarks; global first corridor = Unknown** pending user access, partner and regulatory feasibility, and direct demand evidence.

**User research jobs:** recurring family support / income receipt; current provider pain across fee, FX, speed, trust, and cashout; willingness to receive into AIX; willingness to retain some funds instead of immediate cashout; willingness to spend or send directly from AIX; and trust / compliance expectations.

**Disconfirmers:** immediate cashout remains dominant; existing digital remittance is good enough with no incremental value; users reject stablecoin-linked holding; partner, regulatory, or economics conditions fail; or an integrated AIX loop does not deepen the relationship.

## Roadmap impact

**Decision.** Roadmap and stage order are unchanged.

- P1 is `NOT_YET_PASS`; P2 discovery continues, but P2 scale is blocked.
- QR Ph remains supported as the priority discovery rail.
- Remittance J1 discovery remains supported; corridor research is more precise but not globally fixed.
- Next formal work is to close the P1 fund-retention evidence gap, identify a named QR partner with economics and operating model, and conduct direct remittance user discovery on the Singapore→Philippines primary ASEAN sample with Malaysia as comparator and US/Saudi as benchmarks.
- No numeric Gate thresholds are fabricated.

**Final boundary.** This update refines evidence and priority only. It contains no pages, UI, APIs, fields, state machines, PRD, or implementation plan.
