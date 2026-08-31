# AIX Strategic Validation 12 — Netbank Internal Relationship Validation Route

> Date: 2026-08-31
> Scope: Business Strategy / Product Strategy / Strategic Roadmap validation at Strategy + Capability Level.
> Group-level relationship status: `EXISTING_ACTIVE`.
> AIX-specific partner status: `DISCOVERY_CANDIDATE_NOT_APPROVED`.
> Evidence basis: internal Lark Organization / Collaboration Facts supplied for this stage plus accepted Stage 11 context. No web browsing or new external research was performed.
> Boundary: this artifact does not draft or send outreach, identify or expose employee names, initiate contact, define contract terms, analyze code or APIs, or design features, UX, PRD, state machines, schemas, or implementation flows.

## Executive conclusion

**The wider Atome/Advance group already has an `EXISTING_ACTIVE` Netbank operating relationship in the Philippines.** Current internal collaboration evidence shows live group Netbank integrations across Savings and Transfer-related operations, production incident coordination, service degradation handling, callback/status reconciliation, and direct channel verification.

This is a **Strategy + Capability-level execution-route upgrade**, not AIX partner validation. It changes the recommended access path from a potential cold-start assumption to **reuse of the group's existing internal Netbank relationship and owner path first**. Vendor-access risk is therefore **`REDUCED_NOT_ELIMINATED`** (reduced, not eliminated).

The AIX decision remains bounded exactly as accepted in Stage 11:

- AIX-specific partner status remains **`DISCOVERY_CANDIDATE_NOT_APPROVED`**. Group usage does not imply AIX approval, eligibility, willingness, or approved terms.
- The minimum next action becomes **`INTERNAL_OWNER_HANDOFF_THEN_AIX_VENDOR_VALIDATION`** (internal owner handoff, then AIX vendor validation). This is an execution-route refinement, not vendor validation itself.
- If AIX-specific Vendor Validation fails one or more core conditions—eligibility, acceptable pooled model, credible stablecoin→PHP composition, acceptable regulatory burden, or viable all-in economics—**downgrade Netbank and resume Tier-2 partner discovery**. Roadmap order, the P1 Gate, the P2 scale block, and **Gate Serial / Discovery Parallel** remain unchanged; AIX remains `DISCOVERY_CANDIDATE_NOT_APPROVED`.
- Contract/commercial reuse and technical capability reuse are both **`UNKNOWN`**. Existing Savings, Cash, and Transfer collaboration does not prove reusable agreements, pricing, settlement arrangements, licenses, compliance allocations, code, or components for AIX QRPh P2M.
- The AIX QRPh business-case Unknowns remain unchanged: pooled multi-end-user retail P2M permissibility; complete stablecoin → PHP → QRPh composition; AIX-specific approval/licensing; AML/KYC/transaction-monitoring/consumer-protection split; all-in economics; and use-case acceptance.
- No cold outreach or contact action is taken in this stage. The recommendation is to identify the existing internal Netbank vendor/commercial/compliance owner path before any AIX-specific validation.
- `P1 NOT_YET_PASS`, P2 scale blocked by P1, and the roadmap remain unchanged.

## What changed vs Stage 11

| Stage 11 baseline | Stage 12 internal evidence | Strategic impact |
|---|---|---|
| Public research closed at `KEEP`; Netbank was a named discovery candidate, but the access route was not established by public evidence. | Internal Lark facts show an active wider-group Netbank relationship and recurring operational coordination in the Philippines. | Group-level relationship status becomes **`EXISTING_ACTIVE`**. |
| Minimum next action: `Vendor Validation`. | Existing internal relationship and owner path should be located before direct validation. | Minimum execution route becomes **`INTERNAL_OWNER_HANDOFF_THEN_AIX_VENDOR_VALIDATION`**. |
| Vendor-access uncertainty remained an execution risk. | Existing channels and operating processes reduce cold-start access risk. | Vendor-access risk is **`REDUCED_NOT_ELIMINATED`** (reduced, not eliminated). |
| AIX eligibility, pooled retail P2M, complete funding composition, responsibility split, economics, and use-case acceptance were Unknown. | The internal facts do not answer those AIX-specific questions. | All Stage 11 business-case Unknowns remain unchanged. |
| `PARTNER_VALIDATED_CANDIDATE` was future conditional only; P1/P2 and roadmap were unchanged. | No evidence supplied here establishes AIX approval, reusable terms, or reusable technical assets. | The conditional trigger, `P1 NOT_YET_PASS`, P2 scale block, and roadmap remain unchanged. |

## Internal Organization / Collaboration Facts

The following are sanitized organizational facts. They are not user-level, transaction-level, account-level, or implementation evidence.

### Fact — existing group Netbank operating relationship

**Internal Organization/Collaboration Fact.** Multiple current 2026 Lark threads show Atome/Advance group teams already operating live Philippine Netbank integrations. The evidence covers Savings/Transfer operational flows, production incident handling, Netbank service degradation/downtime handling, callback/status reconciliation, and direct channel verification with Netbank. [S12-01, S12-03]

**Boundary.** This establishes an active wider-group vendor relationship and operating route. It does not establish AIX-specific eligibility, approval, contract reuse, commercial reuse, technical reuse, or QRPh P2M permission for AIX.

### Fact — live Savings relationship

**Internal Organization/Collaboration Fact.** Messages in `业务产品群` on 2026-08-12 state that Savings activation is performed on Netbank's page and proceeds through Netbank-hosted activation. [S12-02]

**Boundary.** This is used only to prove a live group integration relationship; no additional user-flow detail is inferred.

### Fact — operational communication and incident capability

**Internal Organization/Collaboration Fact.** Jul–Aug 2026 messages in `支付sentry报警群` and `Atome Product x Tech x Data` show production transfer requests/callbacks involving Netbank, direct channel verification of inconsistent states, incident handling, and planned backend degraded-mode handling for Netbank outages. [S12-03]

**Boundary.** This supports group-level operational maturity and communication capability. It does not prove that any AIX technical asset or integration component can be reused.

### Fact — collaboration expansion beyond one flow

**Internal Organization/Collaboration Fact.** A 2026-08-07 `Card Data Request` thread describes a PH-market Netbank Cash product as a planned direct-integration/referral-style product with end-to-end reporting planning. [S12-04]

**Boundary.** This supports active expansion of wider-group Netbank collaboration. It does not prove AIX scope, QRPh P2M scope, commercial reuse, contract reuse, or AIX approval.

### Fact — current Savings analytics relationship

**Internal Organization/Collaboration Fact.** A 2026-08-20 `Card Data Request` message distinguishes `submit to netbank` for current Savings KYC analytics. The linked internal document contains sections for Savings KYC volume and application-path analysis. [S12-05]

**Boundary.** Only the existence of a live Netbank Savings relationship is used. No user-level data, metrics, names, or operational details are reproduced.

### Coverage limitation

**Evidence limitation.** Lark Gateway searches for more specific terms were intermittently blocked by upstream errors. The resulting coverage limitation means that missing search results must **not** be treated as proof that a fact or approval does not exist. [S12-06]

## Capability-level interpretation

| Capability / strategic assumption | Current classification | What the internal evidence supports | What remains outside the evidence |
|---|---|---|---|
| Wider-group Netbank relationship | **`EXISTING_ACTIVE`** — Decision | Live group integrations, recurring operational coordination, and direct vendor-channel verification exist. | No conclusion about AIX entity or product approval. |
| Internal vendor-access and operating route | **Evidence present; access risk `REDUCED_NOT_ELIMINATED`** — Decision | The group has people/processes capable of operational communication and production issue coordination with Netbank. | Exact owner identity and sponsorship route for AIX were not established. |
| AIX/non-resident eligibility and approval | **`UNKNOWN`** — Stage 11 context | Group usage provides a route to ask the question through an informed internal path. | Netbank acceptance of AIX entity, licenses, business model, and intended fund flow. |
| Contract/commercial reuse | **`UNKNOWN`** — Unknown | Existing collaboration makes internal reuse worth validating first. | Same agreement, pricing, settlement setup, licenses, or compliance responsibilities for AIX QRPh P2M. |
| Technical capability reuse | **`UNKNOWN`** — Unknown | Existing integrations show organizational experience and operational maturity. | Reusability of current Atome Netbank integration assets/components by AIX; no code/API analysis is performed. |
| Pooled multi-end-user retail QRPh P2M | **Infrastructure pattern `SUPPORTED`; AIX permissibility `UNKNOWN`** — Stage 11 context | The internal relationship may make the capability question easier to route. | Permission for a pooled model, AIX-specific operating role, and complete end-user payment composition. |
| Stablecoin → PHP → QRPh merchant spend | **Stablecoin → PHP local-payout leg `SUPPORTED`; full chain `UNKNOWN`** — Stage 11 context | No new internal fact closes the composition gap. | AIX-specific end-to-end composition and acceptance. |
| Compliance allocation and economics | **`UNKNOWN`** — Stage 11 context | An internal owner path may identify the correct validation route. | Required licenses/OPS status, AML/KYC/transaction-monitoring/consumer-protection split, exact quote, and all-in economics. |

## Strategic decisions and proposals

### Decision — group-level relationship status

Set the wider Atome/Advance group-level Netbank relationship to **`EXISTING_ACTIVE`**. The evidence is sufficient to conclude that Netbank is an active operating vendor relationship for the wider group, not merely a public-market-fit candidate. [S12-01–S12-05]

This decision is explicitly **not** an AIX approval or partner-validation decision.

### Decision — AIX partner status remains unchanged

AIX remains **`DISCOVERY_CANDIDATE_NOT_APPROVED`**. Atome/Advance group usage must not be used as a proxy for AIX entity eligibility, product approval, QRPh P2M permission, partner willingness, or approved commercial terms. [S12-07]

### Decision — vendor-access risk is reduced, not eliminated

The existing group relationship reduces the likelihood of a cold-start vendor-access problem. It does not remove the need to confirm the AIX-specific owner, entity, product, contract, compliance, and commercial path. Exact vendor/commercial/compliance owner identity was not established in this stage. [S12-01, S12-03, S12-06]

### Proposal — internal owner handoff before AIX-specific validation

The minimum next route is:

`INTERNAL_OWNER_HANDOFF_THEN_AIX_VENDOR_VALIDATION`

First locate the existing internal Netbank vendor/commercial/compliance owner path. Then run the Stage 11 capability-level validation package. This is a sequencing proposal, not a completed handoff, outreach instruction, or partner validation result.

### Unknown — contract and commercial reuse

Existing Savings, Cash, and Transfer collaboration does **not** prove that AIX can reuse the same agreement, pricing, settlement setup, licenses, or compliance responsibilities for a pooled QRPh P2M path. Contract/commercial reuse remains **`UNKNOWN`** and requires AIX-specific confirmation.

### Unknown — technical capability reuse

Live group integrations prove organizational experience and operational maturity, but do **not** establish that current Atome Netbank integration assets or components are reusable by AIX. Technical capability reuse remains **`UNKNOWN`**. This stage does not inspect code, APIs, endpoints, or integration components.

### Decision — AIX business-case Unknowns remain unchanged

The internal relationship evidence does not resolve any of the following Stage 11 Unknowns:

- pooled multi-end-user retail P2M permissibility;
- complete stablecoin → PHP → QRPh composition;
- AIX-specific approval/licensing;
- AML/KYC/transaction-monitoring/consumer-protection allocation;
- all-in economics and commercial quote;
- acceptance of the intended user-frequency/everyday-spend use case.

### Decision — no cold outreach or contact action in this stage

No internal or external message is drafted or sent, no employee names are exposed, and no contact action is initiated. The strategic recommendation is only to reuse the existing relationship route when the next authorized validation activity begins.

## Minimum next action: capability-level validation package

After the internal owner path is identified through an authorized future step, the AIX-specific validation questions remain the Stage 11 package:

- AIX/non-resident eligibility;
- pooled corporate settlement for multiple end-users' QRPh merchant payments;
- USDC/USDT → PHP → QRPh composition;
- exact commercial quote and all-in economics;
- required licenses/OPS status;
- AML/KYC/transaction-monitoring/consumer-protection split; and
- whether the user-frequency/everyday-spend use case is acceptable.

These questions remain at Strategy + Capability Level. They are not outreach copy, contract negotiation wording, API requirements, or implementation design.

## Decision trigger and roadmap impact

The decision trigger is unchanged. Only after AIX-specific Vendor Validation confirms **eligibility + acceptable pooled model + credible stablecoin→PHP composition + acceptable regulatory burden + viable all-in economics** may the status become **`PARTNER_VALIDATED_CANDIDATE`** for P2 discovery.

If AIX-specific Vendor Validation fails one or more core conditions—eligibility, acceptable pooled model, credible stablecoin→PHP composition, acceptable regulatory burden, or viable all-in economics—**downgrade Netbank and resume Tier-2 partner discovery**. In this failed-validation branch, roadmap order, the P1 Gate, the P2 scale block, and **Gate Serial / Discovery Parallel** remain unchanged; AIX remains `DISCOVERY_CANDIDATE_NOT_APPROVED`.

That status remains future conditional only. It is not build authorization. P2 scale remains blocked by P1, and P1 remains **`NOT_YET_PASS`**.

The roadmap remains:

`Current → P1 One Money Relationship → P2 Multi-rail Everyday Spend → P3 Everyday Money Account`

Execution remains **Gate Serial / Discovery Parallel**. The internal relationship upgrade does not change roadmap order, P1 acceptance, or P2 scale authorization.

## Scope stop

This stage stops at Strategy + Capability Level. It does not proceed into internal/external message drafting, contact execution, employee identification, contract negotiation, pricing design, code or API analysis, implementation-level fund-flow diagrams, feature design, UX, PRD, state machine, error handling, schema, or code. If AIX-specific validation remains unresolved, record **`Unknown / downstream validation required`** and stop at this boundary.

## Traceability

| Conclusion | Supporting evidence / decisions |
|---|---|
| Wider-group Netbank relationship is `EXISTING_ACTIVE` | S12-01–S12-05; D12-01 |
| Group relationship improves the route but does not validate AIX | S12-01–S12-07; D12-02–D12-03 |
| Vendor-access risk is `REDUCED_NOT_ELIMINATED` (reduced, not eliminated) | S12-01, S12-03, S12-06; D12-03 |
| Minimum route is `INTERNAL_OWNER_HANDOFF_THEN_AIX_VENDOR_VALIDATION` | D12-04 |
| Contract/commercial and technical reuse remain `UNKNOWN` | S12-01, S12-04–S12-07; D12-05–D12-06 |
| Stage 11 AIX business-case Unknowns remain unchanged | S12-07; D12-07 |
| No cold outreach or contact action occurs in this stage | D12-08 |
| Conditional trigger, P1/P2 constraints, and roadmap are unchanged | S12-07; D12-09 |
| Failed validation of any core condition downgrades Netbank and resumes Tier-2 partner discovery without changing roadmap order, P1 Gate, P2 scale block, or Gate Serial / Discovery Parallel | S12-07; D12-10 |

No review file is created in this stage.
