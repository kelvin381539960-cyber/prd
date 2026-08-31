# Stage15 WS1 — Route Normalization & Falsifier Registry

> **Status:** `Materialized workstream; Stage15 bounded research package completed; route validation remains unresolved`.
> **Stage15 final review:** Included in AChatGPT GPT-5.6 Sol/high `CLEAN PASS` (Job `job_01M1BMP3V2YG5KB2SVWFGS2X70`); this workstream's route/Gate status remains as stated below.
> **Purpose:** Normalize H1, H2, H0, and the H3 dimension before interpreting country or cohort evidence.
> **Evidence boundary:** Mechanical record derived from the Stage15 architecture and evidence register. It adds no new source claim.

## 1. Scope check

| Question | WS1 answer |
|---|---|
| Strategic question | Are the candidate routes being compared at the same money-relationship and user-outcome level? |
| Capability level | Route definition, evidence boundary, and falsifier only. |
| In scope | User Job/Outcome, starting money, relationship depth, Current Alternative Stack, cell identity, and pre-registered falsifiers. |
| Out of scope | Feature backlog, page or UX design, API/schema, implementation, vendor/partner choice, launch-market choice, and AIX internal data. |

## 2. Canonical route matrix

| Route label | User Job / Outcome | Starting money | Required relationship depth | Current Alternative Stack | Initial status |
|---|---|---|---|---|---|
| **H1** | Digital-dollar value continuity into country-specific local everyday purchasing-power depth, rather than only one-off cash-out or card spend. | Digital-dollar or stablecoin value held or received before local use. | Repeated digital-dollar → local-use continuity with meaningful everyday depth. | KAST; RedotPay / Bitget / ether.fi / Oobit; Wise; Deel / Stripe / Remote; relevant local wallets; combined status quo. | `NOT_YET_PASS` |
| **H2** | Destination-side retained digital-dollar relationship after cross-border income/remittance, rather than immediate liquidity or transport only. | Cross-border income/remittance value received on the destination side, with the digital-dollar relationship explicitly tested. | Repeated receive → retain/manage → local reuse. | KAST; outcome-relevant card/direct-spend alternatives; Wise; Deel / Stripe / Remote as applicable/context-only; relevant local wallets; combined status quo. | `NOT_YET_PASS` |
| **H0 / Null** | Existing alternatives sufficiently solve the relevant outcome; no differentiated Primary route is selected. | The same starting-money context as the matched H1/H2 comparison. | No distinct AIX relationship is required if the alternatives sufficiently solve the outcome. | The full same-cell Current Alternative Stack. | `NOT_SELECTED` |
| **H3 dimension** | Recurring global income as a source-of-funds / relationship-anchor dimension that may strengthen H1 or H2. | Recurring global income; wage currency and payout provider are not assumed. | Compare whether receipt, retention, management, and local reuse are stronger in the cohort. | Upstream payout/distribution context plus the same outcome-level alternatives. | `NOT_INDEPENDENTLY_PROMOTABLE` |

H3 is never treated as a third same-level route. It may stratify an H1 or H2 cell, but it cannot independently become Primary.

## 3. Minimum validation cell

The canonical unit is:

`Route × Country × Cohort × Job/Outcome × Current Alternative Stack`

Each accepted evidence record must also preserve the starting-money context, denominator, observed behavior, residual-gap interpretation, relationship-depth interpretation, reachability, date, source, and limitations. Evidence from different countries, cohorts, or outcomes cannot be stitched into a Gate PASS.

`Missing / inaccessible / non-comparable / incomplete` evidence remains `NOT_YET_PASS`. It is not a falsifier.

## 4. Pre-registered falsifier registry

| Route | Falsifier to seek in the same cell | Decision boundary |
|---|---|---|
| H1 | The Job is sparse or low-value; users mainly cash out or spend once; alternatives sufficiently solve the outcome; or a simple rail/feature bundle closes the gap without independent continuity/depth. | May produce `FALSIFIED_IN_CELL` for the affected expression/cell. It does not turn missing relationship evidence into a global H1 kill. |
| H2 | Recipients mainly cash out or use ordinary local money; stablecoin is only invisible transport; no repeated retained/managed/reused relationship appears; or alternatives sufficiently solve the outcome. | May produce `FALSIFIED_IN_CELL` for the affected expression/cell. It does not turn missing recipient evidence into a global H2 kill. |
| H0 | H0 is disconfirmed only when a candidate shows matched residual pain, a switching/parallel-use reason, and clears the required gates. | Insufficiency alone cannot select H0. |
| H3 | The recurring-global-income cohort does not strengthen a matched H1/H2 relationship. | Remove H3 as a promotion argument; do not independently kill or promote H1/H2 from H3 alone. |

## 5. WS1 output

- H1 remains `Leading Discovery Candidate / NOT_YET_PASS`.
- H2 remains `Secondary Discovery Candidate / NOT_YET_PASS`.
- H0 remains a baseline and is not selected solely from evidence insufficiency.
- H3 remains a source-of-funds / relationship-anchor dimension.
- `Primary strategic route = NOT_YET_SELECTED`.
- `AIX Right-to-win = Unknown`.
- `P1 = NOT_YET_PASS`; `P2 scale = BLOCKED_BY_P1`.
- Roadmap remains `Current → P1 One Money Relationship → P2 Multi-rail Everyday Spend → P3 Everyday Money Account`.

This is a route-normalization record, not a route decision or review result.
