# Evidence Sources — AIX Strategic Validation 13: Netbank Internal Owner Route Identification

> Traceability index for Strategic Validation 13. This register uses only the fixed, sanitized facts supplied for this stage. No new research, message drafting, sending, or contact action was performed. The register remains at Strategy + Capability Level.
>
> No sender names, mentioned employee names, user-level data, raw message content, transaction details, account details, credentials, or implementation artifacts are reproduced.

## Source register

### Internal Organization / Collaboration Facts

#### S13-01 — PH Savings/Product as informed internal entry point

**Source.** `业务产品群` message `om_x100b68f425e2fca0e192786b3da19c1`.

**Classification.** Internal Organization/Collaboration Fact.

**Fact used.** The message shows a current PH Savings/Product discussion directly referencing Netbank-hosted activation.

**Boundary.** This supports PH Savings/Product as an informed internal entry point, but does not establish ownership, named-person responsibility, vendor/commercial/compliance authority, AIX approval, or sponsorship authority.

**Use.** Supports the first node in the role/team route: `PH Savings/Product`.

#### S13-02 — Existing Netbank integration/operations route

**Source.** `Atome Product x Tech x Data` message/thread root `om_x100b68a342ce14b0e10c617020d3116`.

**Classification.** Internal Organization/Collaboration Fact.

**Fact used.** The message/thread root shows current Savings BE/FE operational coordination for Netbank availability and degraded handling.

**Boundary.** This supports an existing Netbank integration/operations route, but does not establish vendor/commercial/compliance authority, an authorized AIX sponsor, technical reuse, or AIX approval.

**Use.** Supports the middle node in the role/team route: `existing Netbank integration/operations`.

#### S13-03 — Broader PH product collaboration

**Source.** `Card Data Request` message `om_x100b686107f20ca0e2d087a24e2b119`.

**Classification.** Internal Organization/Collaboration Fact.

**Fact used.** The message describes a planned PH Netbank Cash API/referral product and cross-functional reporting follow-up.

**Boundary.** This supports broader PH product collaboration, but does not establish AIX scope, QRPh P2M scope, vendor/commercial/compliance sponsorship, contract/commercial reuse, or AIX approval.

**Use.** Provides supporting context for the broader PH collaboration route without identifying a sponsor.

#### S13-04 — Search coverage limitation for sponsor evidence

**Source.** Repeated Lark cross-chat/workspace search attempts for Netbank commercial/contract/owner terms.

**Classification.** Evidence coverage limitation.

**Fact used.** The repeated search attempts returned retryable upstream errors.

**Boundary.** Missing owner evidence is a coverage limitation, not proof that the exact sponsor or sponsorship authority does not exist. The result cannot establish approval, non-approval, or absence of an owner.

**Use.** Keeps exact vendor/commercial/compliance sponsor identity and authority as **`UNKNOWN`**, and prevents the route from being treated as fully identified.

## Decision register

#### D13-01 — Internal owner route is partially identified

**Type.** Decision.

**Decision.** The internal owner route is **`PARTIALLY_IDENTIFIED`**, not fully identified. The supported role/team chain is:

`PH Savings/Product → existing Netbank integration/operations → vendor/commercial/compliance sponsor`

This is a role/team path, not named-person ownership.

**Support.** S13-01–S13-03.

#### D13-02 — Exact sponsor and authority remain Unknown

**Type.** Unknown / decision boundary.

**Decision.** The exact vendor/commercial/compliance sponsor and that sponsor's authority to sponsor AIX onboarding remain **`UNKNOWN`** because current evidence/search coverage does not establish them.

**Support.** S13-02, S13-04.

#### D13-03 — Canonical relationship and status states remain unchanged

**Type.** Decision.

**Decision.** AIX partner status remains **`DISCOVERY_CANDIDATE_NOT_APPROVED`**; the group relationship remains **`EXISTING_ACTIVE`**; vendor-access risk remains **`REDUCED_NOT_ELIMINATED`**; and owner sponsorship remains **`UNKNOWN`**.

**Support.** S13-01–S13-04 and accepted Stage 11/12 context.

#### D13-04 — Route remains internal handoff before AIX validation

**Type.** Proposal / next-action decision.

**Decision.** The next route remains **`INTERNAL_OWNER_HANDOFF_THEN_AIX_VENDOR_VALIDATION`**. Stage 13 only refines where that handoff should start: PH Savings/Product, then existing Netbank integration/operations, then the vendor/commercial/compliance sponsor role/team.

**Boundary.** This is a route refinement, not an executed handoff, message draft, contact action, sponsor identification, vendor validation result, partner approval, or build authorization.

**Support.** D13-01–D13-03.

#### D13-05 — Authorized sponsor unresolved branch

**Type.** Decision boundary.

**Decision.** If the internal route cannot identify an authorized sponsor, record **`INTERNAL_OWNER_UNRESOLVED`** and stop. Do not infer approval or sponsorship from the role/team chain.

**Support.** D13-01–D13-02.

#### D13-06 — Reuse and AIX-specific QRPh Unknowns remain unchanged

**Type.** Decision.

**Decision.** Contract/commercial reuse and technical capability reuse remain **`UNKNOWN`**. Stage 11/12 AIX-specific QRPh Unknowns remain unchanged: pooled multi-end-user retail P2M permissibility; complete stablecoin → PHP → QRPh composition; AIX-specific approval/licensing; AML/KYC/transaction-monitoring/consumer-protection split; all-in economics; and intended user-frequency/everyday-spend use-case acceptance.

**Support.** S13-01–S13-04 and accepted Stage 11/12 context.

#### D13-07 — Failed AIX-specific Vendor Validation fallback

**Type.** Decision boundary.

**Decision.** If later AIX-specific Vendor Validation fails one or more core conditions—eligibility, acceptable pooled model, credible stablecoin→PHP composition, acceptable regulatory burden, or viable all-in economics—**downgrade Netbank and resume Tier-2 partner discovery**. AIX remains `DISCOVERY_CANDIDATE_NOT_APPROVED` in that branch.

**Support.** Accepted Stage 11/12 context; D13-03.

#### D13-08 — P1, P2, roadmap, and execution mode remain unchanged

**Type.** Decision.

**Decision.** P1 remains **`NOT_YET_PASS`**; P2 scale remains blocked by P1; the roadmap remains `Current → P1 One Money Relationship → P2 Multi-rail Everyday Spend → P3 Everyday Money Account`; and **Gate Serial / Discovery Parallel** remains unchanged.

**Support.** Accepted Stage 11/12 context; D13-03 and D13-07.

## Conclusion traceability

| Conclusion | Supporting evidence / decisions |
|---|---|
| Internal owner route is `PARTIALLY_IDENTIFIED`, not fully identified | S13-01–S13-04; D13-01 |
| Role/team route is `PH Savings/Product → existing Netbank integration/operations → vendor/commercial/compliance sponsor` | S13-01–S13-03; D13-01 |
| Exact sponsor identity and authority are `UNKNOWN` | S13-02, S13-04; D13-02 |
| AIX status, group relationship, vendor-access risk, and owner sponsorship remain canonical | D13-03 |
| Next route remains `INTERNAL_OWNER_HANDOFF_THEN_AIX_VENDOR_VALIDATION` | D13-04 |
| Unresolved authorized sponsor produces `INTERNAL_OWNER_UNRESOLVED` and a stop | D13-05 |
| Contract/commercial reuse, technical capability reuse, and Stage 11/12 AIX-specific QRPh Unknowns remain unchanged | D13-06 |
| Failed AIX-specific Vendor Validation downgrades Netbank and resumes Tier-2 partner discovery | D13-07 |
| P1/P2, roadmap, and Gate Serial / Discovery Parallel remain unchanged | D13-08 |

## Redaction and coverage controls

- Only sanitized role/team descriptions, supplied message references, and supplied coverage facts are included.
- No sender names, mentioned employee names, user-level data, raw message content, transaction details, account details, credentials, or implementation artifacts are included.
- Retryable upstream search errors are recorded as a coverage limitation and are not converted into proof of absence.
- No internal or external message is drafted or sent, and no contact action is initiated.
