> **PRE-CORRECTION / HISTORICAL AUDIT ONLY — generated before the authoritative route-first correction. Not an active Stage14 decision source; must not be used to select the differentiated route.**
> **AIX internal data is not used for Stage14 route selection.**

# Stage14 Deep Dive E — AIX observed behavior archive

## Source and semantics

This archive contains AIX-internal implementation and aggregate cohort evidence. The cohort is 31 unique users with completed deposits, representing 108 deposit transactions.

Current-code semantics are: `crypto_transaction.transaction_type=1` = `DEPOSIT`; `status=200` = `COMPLETED`; and card `transaction_type=21` = `CAPTURE`. The downstream filter `status=200`, `transaction_desc='1st Presentment Purchase'`, `indicator='debit'` is named the `successful purchase capture proxy`.

Semantic mappings use evidence class `Implementation + Data Fact`. Cohort metrics use evidence class `Observed AIX Behavior`.

## Aggregate observations

- The cohort contains 31 unique completed-deposit users and 108 deposits.
- USDT contributes 65 transactions across 22 users, with an aggregate amount of 760.54 USDT.
- USDC contributes 42 transactions across 13 users, with an aggregate amount of 1012.21 USDC.
- FDUSD contributes 1 transaction across 1 user, with an aggregate amount of 9.5 FDUSD.
- 21 of 31 users (67.7%) later meet the successful purchase capture proxy; this is the observed `Deposit → later Spend reuse proxy`.
- 15 of 31 users (48.4%) have at least two deposits; 15 of 31 (48.4%) have at least two later captures; 10 of 31 (32.3%) meet both repeated-activity conditions.

## Temporal reuse observations

- First later capture timing is: <1d, 0 users; 1-7d, 11 users (35.5% of the full cohort and 52.4% of the 21 later-capture users); 7-30d, 6 users (19.4%); and >=30d, 4 users (12.9%).
- Deposit activity spans at least 7d for 9 of 31 users (29.0%) and at least 30d for 7 of 31 (22.6%).
- Post-deposit successful purchase capture activity spans at least 7d for 9 of 31 users (29.0%) and at least 30d for 7 of 31 (22.6%). Both spans reach at least 30d for 6 of 31 users (19.4%).
- Deposits occur in at least two calendar months for 8 of 31 users (25.8%); later captures do so for 9 of 31 (29.0%); both event types do so for 6 of 31 (19.4%).

## Interpretation boundary

The supported statement is limited to `Observed AIX Behavior / Deposit → later Spend reuse proxy`. This evidence does not prove intermediate balance retention, salary or income source, stablecoin preference, market target, causality, or AIX right-to-win.

## Limitations

- The capture outcome is a downstream event proxy defined by the supplied implementation filter, not a direct measure of motivation or product-market fit.
- The evidence is aggregate and cohort-specific; it contains no PII and does not establish a comparison group or causal effect.
- Currency user counts can overlap, so they should not be added to estimate unique users.
- Timing, span, and calendar-month observations describe event reuse patterns only; they do not identify why behavior occurred.

## Decision impact

Use the observed deposit-to-later-spend pattern as directional strategy evidence for validation and prioritization of follow-up measurement. Do not use it alone to claim retention, income-source behavior, stablecoin preference, target-market fit, causality, or AIX right-to-win.

## What remains Unknown

- Whether users retain an intermediate balance between deposit and later capture.
- The source or nature of users' salary or income.
- Whether any stablecoin is preferred, and why.
- Which market or segment is represented, and whether it is strategically attractive.
- Whether deposit activity causes later spend, or merely co-occurs with it.
- Whether the observed proxy is a durable AIX advantage.

## Disconfirming evidence

The strategic interpretation would be weakened by a comparable cohort showing no later-capture lift after deposit, by controls for prior spending eliminating the relationship, or by validation showing that the filtered event is not a reliable purchase-reuse proxy.

## Recommended validation evidence

- A pre-registered cohort definition with event-linkage and timestamp quality checks.
- A comparator or matched analysis using users without the qualifying deposit.
- Ledger-level evidence for intermediate balances, kept separate from the capture proxy.
- Qualitative or consented research on income source, stablecoin choice, and market context.
- Replication across later cohorts and markets before making a strategy-level right-to-win claim.
