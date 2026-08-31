# AIX Strategic Validation 13 — Netbank Internal Owner Route Identification

> Date: 2026-08-31
> Scope: Business Strategy / Product Strategy / Strategic Roadmap validation at Strategy + Capability Level.
> Internal owner route status: `PARTIALLY_IDENTIFIED`.
> Group-level relationship status: `EXISTING_ACTIVE`.
> AIX-specific partner status: `DISCOVERY_CANDIDATE_NOT_APPROVED`.
> Vendor-access risk: `REDUCED_NOT_ELIMINATED`.
> Owner sponsorship: `UNKNOWN`.
> Evidence basis: fixed, sanitized internal Lark facts supplied for this stage. No new research, message drafting, sending, or contact action was performed.
> Boundary: this artifact does not identify or expose employee names, infer approval, define contract or commercial terms, analyze code or APIs, or design features, UX, PRD, state machines, schemas, or implementation flows.

## Executive conclusion

The internal owner route is **`PARTIALLY_IDENTIFIED`**, not fully identified.

The evidence supports the following role/team chain as the starting route for a future authorized handoff:

`PH Savings/Product → existing Netbank integration/operations → vendor/commercial/compliance sponsor`

This is a **role/team path**, not named-person ownership. The exact vendor/commercial/compliance sponsor and that sponsor's authority to sponsor AIX onboarding remain **`UNKNOWN`**. Current evidence and search coverage do not establish either point. The search limitation is a coverage limitation, not proof that no sponsor or authority exists.

Stage 13 therefore only refines **where the internal handoff should start**. The next route remains:

`INTERNAL_OWNER_HANDOFF_THEN_AIX_VENDOR_VALIDATION`

The wider-group relationship remains **`EXISTING_ACTIVE`**, vendor-access risk remains **`REDUCED_NOT_ELIMINATED`**, and AIX-specific partner status remains **`DISCOVERY_CANDIDATE_NOT_APPROVED`**. Owner sponsorship remains **`UNKNOWN`**.

## Canonical stage states

| Strategic item | Canonical state | Interpretation |
|---|---|---|
| Internal owner route | **`PARTIALLY_IDENTIFIED`** | The role/team chain is supported, but the authorized sponsor is not fully identified. |
| Supported route chain | **`PH Savings/Product → existing Netbank integration/operations → vendor/commercial/compliance sponsor`** | A role/team handoff path only; it is not named-person ownership. |
| Exact sponsor identity and authority | **`UNKNOWN`** | Current evidence/search coverage does not establish the exact sponsor or authority to sponsor AIX onboarding. |
| Wider-group relationship | **`EXISTING_ACTIVE`** | The existing group relationship remains active. |
| Vendor-access risk | **`REDUCED_NOT_ELIMINATED`** | Existing relationship and operating route reduce cold-start risk, but do not remove authorization uncertainty. |
| AIX partner status | **`DISCOVERY_CANDIDATE_NOT_APPROVED`** | No AIX approval, willingness, eligibility, or build authorization is inferred. |
| Owner sponsorship | **`UNKNOWN`** | Sponsorship must be established through an authorized future validation step. |
| Minimum next route | **`INTERNAL_OWNER_HANDOFF_THEN_AIX_VENDOR_VALIDATION`** | Stage 13 only narrows the starting point for the handoff. |

## Evidence-supported route chain

### PH Savings/Product as the informed internal entry point

The current PH Savings/Product discussion in `业务产品群` directly references Netbank-hosted activation. This supports PH Savings/Product as an informed internal entry point for locating the existing route. It does **not** establish ownership, sponsor authority, AIX approval, or vendor/commercial responsibility. [S13-01]

### Existing Netbank integration/operations as the middle route

Current Savings BE/FE operational coordination in `Atome Product x Tech x Data` covers Netbank availability and degraded handling. This supports an existing Netbank integration/operations route. It does **not** establish vendor/commercial/compliance authority or an authorized AIX sponsor. [S13-02]

### Vendor/commercial/compliance sponsor as unresolved final route node

The role/team chain points to a vendor/commercial/compliance sponsor as the required next ownership layer. The exact sponsor and authority to sponsor AIX onboarding remain **`UNKNOWN`**. The supplied search coverage does not close this gap. [S13-04]

The planned PH Netbank Cash API/referral product and cross-functional reporting follow-up support broader PH product collaboration, but do not establish AIX scope or commercial sponsorship. [S13-03]

## Capability-level interpretation

| Capability / strategic assumption | Current classification | What Stage 13 supports | What remains outside the evidence |
|---|---|---|---|
| Internal owner route | **`PARTIALLY_IDENTIFIED`** — Decision | A role/team chain begins at PH Savings/Product, passes through existing Netbank integration/operations, and points to a vendor/commercial/compliance sponsor. | Exact authorized sponsor identity and sponsorship authority. |
| AIX onboarding sponsorship | **`UNKNOWN`** — Unknown | The route is sufficiently localized for a future authorized handoff to start in the informed internal path. | Whether any identified role/team can sponsor AIX onboarding; no approval is inferred. |
| Wider-group Netbank relationship | **`EXISTING_ACTIVE`** — Unchanged | Existing group relationship remains the context for the route. | No AIX-specific partner validation or approval. |
| Vendor-access risk | **`REDUCED_NOT_ELIMINATED`** — Unchanged | Existing relationship and operations route reduce cold-start access risk. | Authorization, sponsor identity, and AIX-specific validation. |
| Contract/commercial reuse | **`UNKNOWN`** — Unchanged | The route makes future validation more targeted. | Reusable agreement, pricing, settlement arrangement, licenses, or compliance allocation. |
| Technical capability reuse | **`UNKNOWN`** — Unchanged | Existing operations route does not itself establish reuse. | Reusable code, API, integration component, or technical asset; no code/API analysis is performed. |
| AIX retail QRPh P2M permissibility | **`UNKNOWN`** — Unchanged | The route may support asking the capability question later. | Permission for the AIX pooled multi-end-user model. |
| Complete stablecoin → PHP → QRPh composition | **`UNKNOWN`** — Unchanged | No Stage 13 evidence closes the end-to-end composition gap. | AIX-specific complete consumer merchant-spend chain. |
| AIX-specific approval/licensing, compliance split, economics, and use-case acceptance | **`UNKNOWN`** — Unchanged | These remain downstream Vendor Validation questions. | Required licenses/OPS status; AML/KYC/transaction-monitoring/consumer-protection split; exact quote/all-in economics; and acceptance of the intended user-frequency/everyday-spend use case. |

## Minimum next route

The next route remains:

`INTERNAL_OWNER_HANDOFF_THEN_AIX_VENDOR_VALIDATION`

Stage 13 refines only the starting point for that handoff:

1. Start with the informed **PH Savings/Product** role/team entry point.
2. Follow the existing **Netbank integration/operations** route.
3. Establish the authorized **vendor/commercial/compliance sponsor** and that sponsor's authority to sponsor AIX onboarding.
4. Only after an authorized sponsor is established, run the Stage 11/12 AIX-specific Vendor Validation questions at Strategy + Capability Level.

This materialization does not execute the handoff, draft or send an internal/external message, initiate contact, or expose employee names.

If the internal route cannot identify an authorized sponsor, record **`INTERNAL_OWNER_UNRESOLVED`** and stop. Do not infer AIX approval, partner willingness, authorization, or sponsorship from the role/team chain.

The downstream Vendor Validation questions remain unchanged:

- AIX/non-resident eligibility;
- pooled corporate settlement for multiple end-users' QRPh merchant payments;
- USDC/USDT → PHP → QRPh composition;
- exact commercial quote and all-in economics;
- required licenses/OPS status;
- AML/KYC/transaction-monitoring/consumer-protection split; and
- whether the user-frequency/everyday-spend use case is acceptable.

## Decision trigger and fallback

Only AIX-specific Vendor Validation confirming **eligibility + acceptable pooled model + credible stablecoin→PHP composition + acceptable regulatory burden + viable all-in economics** can move Netbank to the future conditional state **`PARTNER_VALIDATED_CANDIDATE`** for P2 discovery. That state is not build authorization.

If later AIX-specific Vendor Validation fails one or more of those core conditions, **downgrade Netbank and resume Tier-2 partner discovery**. AIX remains **`DISCOVERY_CANDIDATE_NOT_APPROVED`** in that branch. The role/team route does not change this fallback.

## Unchanged strategic constraints

Stage 13 does not change any Stage 11/12 AIX-specific QRPh Unknowns. Contract/commercial reuse and technical capability reuse remain **`UNKNOWN`**. The following remain unresolved:

- pooled multi-end-user retail P2M permissibility;
- complete stablecoin → PHP → QRPh composition;
- AIX-specific approval/licensing;
- AML/KYC/transaction-monitoring/consumer-protection split;
- all-in economics and commercial quote; and
- intended user-frequency/everyday-spend use-case acceptance.

P1 remains **`NOT_YET_PASS`**. P2 scale remains blocked by P1. The roadmap remains:

`Current → P1 One Money Relationship → P2 Multi-rail Everyday Spend → P3 Everyday Money Account`

**Gate Serial / Discovery Parallel** remains unchanged.

## Scope stop

This stage stops at Strategy + Capability Level. It does not enter internal/external message drafting or sending, contact execution, employee identification, contract negotiation, pricing design, code or API analysis, implementation-level fund-flow diagrams, feature design, UX, PRD, state machine, error handling, schema, or code. If the authorized sponsor remains unresolved, record **`INTERNAL_OWNER_UNRESOLVED`** and stop without inferring approval.

## Traceability

| Conclusion | Supporting evidence / decisions |
|---|---|
| Internal owner route is `PARTIALLY_IDENTIFIED`, not fully identified | S13-01–S13-04; D13-01 |
| Supported route is `PH Savings/Product → existing Netbank integration/operations → vendor/commercial/compliance sponsor` | S13-01–S13-03; D13-01 |
| Exact sponsor identity and authority remain `UNKNOWN` | S13-02, S13-04; D13-02 |
| AIX status, group relationship, vendor-access risk, and owner sponsorship remain canonical | D13-03 |
| Minimum next route remains `INTERNAL_OWNER_HANDOFF_THEN_AIX_VENDOR_VALIDATION` | D13-04 |
| Unresolved authorized sponsor produces `INTERNAL_OWNER_UNRESOLVED` and a stop; no approval is inferred | D13-05 |
| Contract/commercial reuse, technical capability reuse, and Stage 11/12 AIX-specific QRPh Unknowns remain unchanged | D13-06 |
| Vendor Validation failure downgrades Netbank and resumes Tier-2 partner discovery | D13-07 |
| P1/P2, roadmap, and Gate Serial / Discovery Parallel remain unchanged | D13-08 |

No review file is created in this stage.
