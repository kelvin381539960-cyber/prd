# Stage15 WS4 — Relationship Depth Register

> **Status:** `Materialized working artifact; money-relationship depth remains NOT_YET_PASS`.
> **Stage15 final review:** Included in AChatGPT GPT-5.6 Sol/high `CLEAN PASS` (Job `job_01M1BMP3V2YG5KB2SVWFGS2X70`); this workstream's route/Gate status remains as stated below.
> **Purpose:** Distinguish one-off transport or spend from repeated digital-dollar continuity or destination-side retained use.
> **Evidence boundary:** Mechanical classification of the existing Stage15 source records. No internal data, schema, instrumentation, or implementation is introduced.

## 1. Scope check

| Question | WS4 answer |
|---|---|
| H1 relationship test | Repeated digital-dollar → local-use continuity with meaningful everyday depth and value retained until use. |
| H2 relationship test | Repeated receive → retain/manage → local reuse on the destination side. |
| Not sufficient | Sender adoption, transfer volume, a product capability, a one-off spend, a one-time cash-out, or a transport event. |
| Out of scope | Balance schema, ledger query, event instrumentation, API, feature design, or implementation plan. |

## 2. Cell-level relationship evidence

| Route × country cell | What is actually observed in the current package | Relationship-depth status |
|---|---|---|
| H1 × Argentina | belo, Lemon, KAST, and other provider pages document possible hold/use or digital-dollar-to-local-use paths. The Argentina WS2 cards do not show same-user repeated retention, local-use frequency/value, or post-use reuse. | `Insufficient / NOT_YET_PASS` for normalized H1; broad rail-bundle expression is separately disconfirmed in-cell. |
| H1 × Philippines | Card/direct-spend, QR, local-wallet, and cash-out routes establish alternative outcome coverage pressure. They do not show repeated hold-until-use behavior by the same cohort. | `Insufficient / NOT_YET_PASS` for normalized H1. |
| H2 × Philippines | Local wallets, QR, cards, remittance, and cash-out alternatives establish transport/local-liquidity pressure. Destination-side repeated retain/manage/reuse is not observed. | `Insufficient / NOT_YET_PASS` for normalized H2. |
| H2 × Mexico | Remittance and payout records establish a possible destination-side context, but no same-recipient digital-dollar retention or repeated local reuse is recorded. | `Insufficient / NOT_YET_PASS` for normalized H2. |

## 3. Relationship-depth adjudication rules

| Evidence pattern | Allowed conclusion |
|---|---|
| Provider says users can hold and spend | Capability-level possibility only; not observed retention or repeated use. |
| Sender, payout, or transfer volume is present | Source-of-funds or transport context only; not destination retention. |
| One successful local payment or conversion is present | One-off outcome coverage only; not a Primary money relationship. |
| Repeated same-cell receive → retain/manage → local reuse | Candidate-supporting evidence for H2, still subject to DR-1..DR-4 and the alternative comparison. |
| Repeated same-cell digital-dollar → local-use continuity with meaningful everyday depth | Candidate-supporting evidence for H1, still subject to DR-1..DR-4 and the alternative comparison. |
| Same-cell behavior is mainly immediate cash-out / one-off spend / transport | Direct falsifier for the corresponding relationship expression; downgrade to utility or transport evidence. |

## 4. Gate status

| Gate | Status | Reason |
|---|---|---|
| DR-5 Money relationship depth | `NOT_YET_PASS` | No complete same-country + same-cohort repeated retain/manage/reuse or continuity record is present. |
| DR-1 Job/Target | `NOT_YET_PASS` | Relationship depth cannot substitute for a defined, observed Job and denominator. |
| DR-2 Differentiated outcome | `NOT_YET_PASS` | A retained relationship must still show residual pain and a reason to switch or use in parallel. |
| DR-3 Defensibility | `NOT_YET_PASS` | Depth is not proven merely because a product has a unified account or multiple rails. |

## 5. Decision boundary

The current records do not support a positive H1 or H2 relationship-depth conclusion. They also do not support a global kill based solely on missing behavior. `H1 = NOT_YET_PASS`, `H2 = NOT_YET_PASS`, and `Primary strategic route = NOT_YET_SELECTED` remain unchanged.
