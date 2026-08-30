# Evidence Sources — AIX P1 Gate Closure (09)

> Traceability index for the P1 Gate Closure materialization. It uses only the authoritative evidence supplied for this stage and accepted repository context. No raw user IDs or PII are included. This index records evidence boundaries; it is not a schema, API, instrumentation, or implementation design.

## Source register

### Accepted repository context

#### S09-01 — Update 08 P1 baseline

**Source.** [`08-strategic-validation-update.md`](../08-strategic-validation-update.md), especially the P1 production aggregate and Gate sections; corroborated by [`evidence/08-sources.md`](08-sources.md).

**Accepted fact used.** The baseline contains 31 completed Deposit users with already-positive repeat-relationship signals. Before this stage, P1 was:

`NOT_YET_PASS — positive repeat-relationship signal proven; linked fund-retention evidence gap`

**Use.** Establishes the prior state that this stage updates without replacing or weakening it.

#### S09-02 — Existing card-side balance boundary

**Source.** Accepted fact base recorded in [`evidence/08-sources.md`](08-sources.md#aix-d3--retention-and-runtime-boundary-facts).

**Accepted fact used.** `transaction_balance_record` is card-side only (`balance_type=CARD`) and represents card balance auto-transfer / rollback evidence, not general Wallet retention history.

**Use.** Prevents card-side balance records from being treated as a wallet-balance history source.

### Stage-supplied production code evidence

The following sources are the authoritative evidence supplied in this stage. No repository source path was supplied for these code facts, so this index does not infer one.

#### S09-03 — Wallet persistence and current-balance boundary

**Source.** Stage-supplied authoritative evidence, item 2.

**Facts used.** `WalletPO` has only `id`, `created_time`, and `updated_time`, with no balance field. Current wallet balance is fetched live through `WalletRemoteRepository#getWalletBalances` → DTC `GET /openapi/v1/wallet/balances`; the implementation exposes a current snapshot, not persisted history.

**Use.** Establishes why the current balance path cannot close the direct historical fund-retention gap.

#### S09-04 — Unusable wallet-history DTO evidence

**Source.** Stage-supplied authoritative evidence, item 3.

**Facts used.** `WalletBalanceHistoryRequest` / `WalletBalanceHistoryResponse` exist, but no client endpoint or actual usage was found. `WalletActivityTypeEnum` contains placeholder values based on a PDF whose full list was not provided.

**Use.** Establishes that class existence is not evidence of a functioning historical wallet-balance source.

### Stage-supplied production and temporal evidence

#### S09-05 — Successful card TOP_UP aggregate

**Source.** Stage-supplied authoritative evidence, item 5.

**Filter.** `card_transaction.transaction_type=1,status=200`.

**Result.** 198 successful card TOP_UP transactions across 23 users, 2026-04-13..2026-08-28. Explicit `test_user_info` contamination among those 23 users is 0.

**Use.** Defines the non-test TOP_UP population used by the temporal proxy evidence.

#### S09-06 — Captured Purchase aggregate

**Source.** Stage-supplied authoritative evidence, item 6.

**Filter.** `card_transaction.transaction_type=2,status=221`.

**Result.** 166 captured Purchase transactions across 22 users.

**Use.** Defines the captured-spend cohort used by Retention-proxy A.

#### S09-07 — Retention-proxy A

**Source.** Stage-supplied authoritative evidence, item 7.

**Construction.** Each captured Purchase is paired to the most recent successful card TOP_UP before it, avoiding intervening-TOP_UP confounding. Each user's maximum observed lag is then classified.

**Result.** 22 non-test users:

| Maximum observed lag | Users |
|---|---:|
| `<1d` | 14 |
| `1–6d` | 4 |
| `7–29d` | 4 |
| `30d+` | 0 |

**Use.** Supports a positive card-side pre-funding persistence signal. It does not prove wallet fund retention.

#### S09-08 — Retention-proxy B

**Source.** Stage-supplied authoritative evidence, item 8.

**Construction.** Each successful card TOP_UP is paired to the most recent completed crypto Deposit before it, avoiding intervening-Deposit confounding. Each user's maximum observed lag is then classified.

**Result.** 22 non-test users with this chain:

| Maximum observed lag | Users |
|---|---:|
| `<1d` | 3 |
| `1–6d` | 0 |
| `7–29d` | 10 |
| `30d+` | 9 |

**Use.** Supports a positive cross-balance temporal relationship signal only. It does not prove funding provenance or continuous retention of the same funds in AIX.

#### S09-09 — Interpretation boundary

**Source.** Stage-supplied authoritative evidence, item 9.

**Facts used.** Proxy B does not prove that the later card TOP_UP was funded from the earlier wallet Deposit and does not prove that the same funds remained continuously in AIX. Proxy A shows some pre-funding persistence on the card side but does not establish wallet fund-retention history.

**Use.** Controls the strategic interpretation of both proxies.

## Decision register

#### D09-01 — P1 status and evidence-confidence update

**Source.** Stage-supplied authoritative evidence, items 1 and 10, read with S09-01 and S09-07–S09-09.

**Decision.** P1 remains **`NOT_YET_PASS — positive repeat-relationship signal proven; linked fund-retention evidence gap`**. Evidence confidence is upgraded: repeat relationship is proven, temporal persistence proxies are positive, and direct linked historical fund-retention remains unproven.

**Boundary.** This is neither a P1 PASS nor a P1 FAIL. No numerical Gate threshold is introduced.

#### D09-02 — Roadmap impact

**Source.** Stage-supplied authoritative evidence, item 11, read with accepted roadmap context.

**Decision.** P2 scale remains blocked, the roadmap order is unchanged, and discovery may remain parallel.

#### D09-03 — Minimum next evidence

**Source.** Stage-supplied authoritative evidence, item 12.

**Decision.** The minimum next evidence is a non-PII linked historical balance/ledger-derived holding-duration aggregate tied to repeat active use, sufficient to distinguish retained funds from just-in-time funding.

**Status.** `Unknown / downstream validation required` in this stage. No source, schema, API, instrumentation, or implementation design is specified here.

## Conclusion traceability

| Conclusion | Supporting evidence |
|---|---|
| P1 remains `NOT_YET_PASS` | S09-01, S09-07, S09-08, S09-09, D09-01 |
| Repeat relationship is proven | S09-01 and accepted Update 08 baseline |
| Temporal persistence proxies are positive | S09-05–S09-08 |
| Direct linked historical fund-retention remains unproven | S09-02–S09-04, S09-09 |
| P2 scale remains blocked and roadmap order is unchanged | D09-02 |
| Next evidence is `Unknown / downstream validation required` | D09-03 |
