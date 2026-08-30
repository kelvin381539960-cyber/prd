# AIX P1 Gate Closure — Strategic Validation

> Date: 2026-08-30
> Scope: Business Strategy / Product Strategy / Strategic Roadmap validation at Capability Level.
> Stage meaning: this closes the evidence-validation stage; it does not mean that the P1 Gate passed.
> Evidence basis: authoritative evidence supplied for this stage plus accepted repository context. No new browsing, production query, or code investigation was performed.
> Boundary: this artifact contains no feature, PRD, page, API, state-machine, schema, instrumentation, or implementation design.

## Executive conclusion

**P1 remains `NOT_YET_PASS — positive repeat-relationship signal proven; linked fund-retention evidence gap`.**

The evidence confidence is upgraded from a generic relationship data gap to a bounded conclusion:

- the repeat relationship is proven;
- temporal persistence proxies are now positive; and
- direct linked historical fund-retention evidence remains unproven.

The P1 Gate therefore remains open. P2 scale remains blocked, the roadmap order is unchanged, and discovery may continue in parallel. No numerical Gate threshold is introduced.

## Evidence carried forward and added

### Accepted P1 baseline

Update 08 established the accepted baseline of 31 completed Deposit users and already-positive repeat-relationship signals. Before this stage, P1 was:

`NOT_YET_PASS — positive repeat-relationship signal proven; linked fund-retention evidence gap`

This stage tests whether the added temporal evidence closes the remaining direct fund-retention gap. It does not reset the baseline or reinterpret it as a negative result.

### Production aggregates

The stage-supplied production aggregates are descriptive and contain no raw user IDs or PII.

| Cohort / filter | Aggregate |
|---|---:|
| Successful card TOP_UP: `card_transaction.transaction_type=1`, `status=200` | 198 transactions / 23 users |
| Explicit `test_user_info` contamination among those TOP_UP users | 0 |
| Successful card TOP_UP business transaction window | 2026-04-13 → 2026-08-28 |
| Captured Purchase: `card_transaction.transaction_type=2`, `status=221` | 166 transactions / 22 users |

The TOP_UP and captured-Purchase aggregates provide the stated non-test population for temporal relationship analysis. They do not, by themselves, establish a wallet holding history.

### Temporal persistence proxies

**Retention-proxy A — card-side pre-funding persistence.** For each captured Purchase, the most recent successful card TOP_UP before that Purchase was selected, avoiding intervening-TOP_UP confounding. Each user was then classified by their maximum observed lag:

| Maximum observed lag | Users |
|---|---:|
| `<1d` | 14 |
| `1–6d` | 4 |
| `7–29d` | 4 |
| `30d+` | 0 |

This is a positive card-side temporal persistence signal, but it is not wallet fund-retention history.

**Retention-proxy B — cross-balance temporal relationship.** For each successful card TOP_UP, the most recent completed crypto Deposit before that TOP_UP was selected, avoiding intervening-Deposit confounding. Among the 22 non-test users with this chain, maximum observed lag was classified as:

| Maximum observed lag | Users |
|---|---:|
| `<1d` | 3 |
| `1–6d` | 0 |
| `7–29d` | 10 |
| `30d+` | 9 |

This is a positive cross-balance temporal relationship signal only. It does not prove that the later card TOP_UP was funded from the earlier wallet Deposit, and it does not prove that the same funds remained continuously in AIX.

All distributions above are descriptive evidence, not Gate thresholds.

## Direct fund-retention evidence boundary

The current implementation does not provide a usable direct historical wallet-balance source in the evidence supplied for this stage:

- `WalletPO` has only `id`, `created_time`, and `updated_time`; it has no balance field.
- Current wallet balance is fetched live through `WalletRemoteRepository#getWalletBalances` → DTC `GET /openapi/v1/wallet/balances`. The current implementation exposes a current snapshot, not persisted history.
- `WalletBalanceHistoryRequest` / `WalletBalanceHistoryResponse` DTOs exist, but repository search found no client endpoint or actual usage. `WalletActivityTypeEnum` explicitly contains placeholder values based on a PDF whose full list was not provided. These classes are therefore not usable evidence of a functioning historical wallet-balance source.
- `transaction_balance_record` is card-side only (`balance_type=CARD`), not a wallet-balance history source; this is consistent with the accepted fact base.

The result is a direct evidence gap, not evidence that users do not retain funds. The two proxies improve confidence in temporal relationship behavior while leaving fund provenance and continuous wallet retention unresolved.

## Strategic decision

| Question | Decision |
|---|---|
| P1 One Money Relationship | **Remain `NOT_YET_PASS`**. Repeat relationship is proven; temporal persistence proxies are positive; direct linked historical fund-retention remains unproven. |
| P1 evidence confidence | **Upgrade** from generic data-gap confidence to a bounded, proxy-supported conclusion. |
| P2 scale | **Blocked** until P1 is accepted. |
| Gate thresholds | **None added.** Existing qualitative Gate discipline is preserved. |

At Capability Level, this supports continued validation of the One Money Relationship. It does not create a new capability decision, authorize scale, or justify a feature-level workstream.

## Minimum next evidence

**Status: `Unknown / downstream validation required`.**

The minimum next evidence remains a non-PII linked historical balance/ledger-derived holding-duration aggregate tied to repeat active use, sufficient to distinguish retained funds from just-in-time funding. This artifact does not design the source, schema, instrumentation, query, API, or implementation needed to obtain it.

## Roadmap impact and handoff

The roadmap remains:

`Current → P1 One Money Relationship → P2 Multi-rail Everyday Spend → P3 Everyday Money Account`

The staged relationship remains `A6 → A3 → A1`, with **Gate Serial / Discovery Parallel** execution. P2 and other approved discovery work may remain parallel, but P2 scale does not start before P1 acceptance.

The next strategic step is to resolve the direct fund-retention evidence gap. If that evidence is unavailable, retain `Unknown / downstream validation required`; do not convert the positive proxies into a Gate pass.

## Capability-level closure

This stage is complete as an evidence-validation materialization, with independent review still separate. The hardened guardrail remains in force: future work in this task may assess strategic assumptions, capability priority, evidence sufficiency, constraints, and Roadmap Gates, but must stop before page/UI/CTA/copy, field/API mapping, state machines, error flows, schema/instrumentation, PRD requirements, or implementation design.
