# AIX Strategic Validation 11 — Netbank Public Feasibility Closure

> Date: 2026-08-31
> Scope: Business Strategy / Product Strategy / Strategic Roadmap validation at Strategy + Capability Level.
> Status: `KEEP / stop public research`.
> Evidence basis: only the authoritative evidence and decisions supplied for this stage (A–I); no web browsing or new research was performed.
> Boundary: this artifact does not draft partner outreach, contract wording, API endpoints, implementation-level fund-flow diagrams, feature design, UX, PRD, state machine, error handling, schema, or code.

## Executive conclusion

**Public-evidence closure: `KEEP / stop public research`.** The supplied public evidence is now sufficient to justify direct vendor, compliance, and commercial validation. More public browsing is unlikely to resolve the remaining blockers: AIX-specific approval, pooled retail P2M permissibility, the exact responsibility split, and all-in economics.

Netbank is **`SUPPORTED AT CATEGORY LEVEL`** for a non-resident partner fit. Its public materials explicitly cover non-resident payment processors/remittance companies, and the BaaS structure accommodates a TPSP organized in another country. This does **not** establish `AIX-specific eligibility/approval`; that remains **`UNKNOWN`** until Netbank validates AIX's entity, licenses, business model, and intended fund flow.

The capability closure is:

- the **pooled-settlement infrastructure pattern is `SUPPORTED`**, while **AIX retail P2M permissibility is `UNKNOWN`**;
- the **stablecoin → PHP leg is `SUPPORTED` for local payouts via a licensed VASP partner**, while the complete **`stablecoin → PHP → QRPh end-user merchant spend`** path is `UNKNOWN`;
- the public agreement places material product-level terms, support, compliance, and privacy duties with the TPSP/AIX, while the exact **AML/KYC/transaction-monitoring/consumer-protection split is `UNKNOWN`**; and
- economics remain **`UNKNOWN / commercial quote required`**.

This is a public-evidence closure and a direct-validation handoff, not partner approval, build authorization, or P2 scale acceptance. P2 scale remains blocked by P1, and the roadmap is unchanged.

## What public evidence upgraded

| Classification | Evidence-supported upgrade | Capability boundary |
|---|---|---|
| **Vendor Fact** | Netbank explicitly targets non-resident businesses, including non-resident payment processors and remittance companies. Its products page lists non-resident corporate operating accounts, local collect via VCA + QRPH, local disburse via transfers, FX, and cross-border transfers. | This supports category-level fit and a named validation path; it does not approve AIX. [S11-01–S11-02] |
| **Vendor Fact** | The BaaS template leaves the TPSP country open, describes the TPSP's own End-Users and products, and allows BaaS components subject to Netbank approval. | This supports a cross-border TPSP structure; it does not establish AIX eligibility or partner willingness. [S11-03] |
| **Vendor Fact** | The Settlement Account requirement and `Process QRPH disbursement` establish relevant primitives: a TPSP settlement-account relationship and a payer-side QRPH operation funded from a specified Netbank Corporate Account. | These primitives do not prove that one pooled account may fund merchant payments for multiple AIX end-users. [S11-04–S11-05] |
| **Vendor Fact** | Netbank publicly describes USDC/USDT → PHP conversion for local payouts through a licensed local VASP partner, and also mentions PHP → stablecoin. | This supports the stablecoin↔PHP funding/cross-border leg in the partner ecosystem; it does not prove the complete consumer merchant-spend chain. [S11-06] |
| **Vendor / Regulatory Fact** | The agreement assigns direct End-User terms/support, product and applicable-law compliance, and privacy-consent duties to the TPSP; Netbank retains approval, authentication, and audit roles. The BSP OPS FAQ keeps foreign providers serving Philippine customers potentially in scope. | Partner-led integration does not automatically remove AIX obligations. The exact allocation of AML/KYC, transaction monitoring, and consumer protection remains unknown. [S11-07–S11-08] |
| **Decision** | The public-research stage is closed at `KEEP`; the minimum next action is direct Vendor Validation. | No further public browsing is required to make the next capability-level decision. [S11-09 and D11-01] |

## What remains unknown

The following are not resolved by the supplied public evidence:

- **Unknown — AIX-specific eligibility/approval:** whether Netbank will accept AIX's entity, licenses, business model, and intended fund flow.
- **Unknown — pooled retail P2M permissibility:** whether a single TPSP pooled corporate settlement account may fund QRPh merchant payments for multiple AIX end-users.
- **Unknown — complete funding composition:** whether the supported stablecoin → PHP leg can be composed with payer-side QRPh P2M for AIX consumers.
- **Unknown — regulatory and responsibility allocation:** required licenses/OPS status and the complete AML/KYC/transaction-monitoring/consumer-protection split.
- **Unknown — partner willingness and terms:** public evidence does not establish approval, willingness, or contract terms.
- **Unknown — economics:** payer-side QRPh pricing, FX spread, VASP cost, liquidity cost, settlement-account commitments, minimums, and other all-in commercial terms.
- **Unknown — use-case acceptability:** whether the user-frequency/everyday-spend use case is acceptable to the partner.

No public generic price or benchmark is converted into an AIX cost, threshold, or Gate requirement. No numeric threshold is added.

## Strategic decisions and proposals

### Decision — public-evidence closure

**`KEEP / stop public research`.** Existing public evidence is sufficient to move to direct vendor/compliance/commercial validation. More public research is unlikely to resolve the decision blockers above.

### Decision — non-resident partner fit

Netbank is **`SUPPORTED AT CATEGORY LEVEL`** for the non-resident partner category. `AIX-specific eligibility/approval` remains **`UNKNOWN`** until Netbank validates AIX's entity, licenses, business model, and intended fund flow.

### Proposal — pooled settlement as the first capability hypothesis

Validate **partner-led pooled settlement** first. The Settlement Account and corporate-account-funded QRPH primitives make the pattern relevant, but they do not prove that pooled retail P2M is permitted for AIX. A per-user account pattern is not elevated by this stage.

### Decision — stablecoin funding boundary

The stablecoin → PHP leg is **`SUPPORTED` for local payouts via a licensed VASP partner**. The full **`stablecoin → PHP → QRPh end-user merchant spend`** chain remains **`UNKNOWN`**.

### Decision — responsibility burden

The public agreement shows that the TPSP/AIX carries material product-level responsibilities for End-User terms, support, product and applicable-law compliance, and privacy consent, while Netbank retains approval, authentication, and audit roles. The exact AML/KYC/transaction-monitoring/consumer-protection allocation is **`UNKNOWN`** and requires direct compliance and contract confirmation.

### Decision — economics

Economics remain **`UNKNOWN / commercial quote required`**. Public evidence does not confirm AIX payer-side QRPh pricing, FX spread, VASP cost, liquidity cost, settlement-account commitments, or minimums. No public generic PHP10 or merchant-acquiring percentage is treated as AIX's actual cost, and no threshold is invented.

### Decision — next action

**Vendor Validation is now the minimum next action, not more public research.** The confirmation package remains capability-level and asks only for:

- AIX/non-resident eligibility;
- pooled corporate settlement for multiple end-users' QRPh merchant payments;
- USDC/USDT → PHP → QRPh composition;
- the exact commercial quote and all-in economics;
- required licenses/OPS status;
- the AML/KYC/transaction-monitoring/consumer-protection split; and
- whether the user-frequency/everyday-spend use case is acceptable.

These are validation questions, not API or implementation requirements.

## Decision trigger and roadmap impact

If Netbank confirms **eligibility + an acceptable pooled model + a credible stablecoin → PHP composition + acceptable regulatory burden + viable all-in economics**, the path becomes **`PARTNER_VALIDATED_CANDIDATE`** for P2 discovery.

That trigger is **not build authorization**. P2 scale remains blocked by the P1 Gate, which remains `NOT_YET_PASS`.

If the core conditions fail, downgrade Netbank and move to Tier-2 partner discovery. The roadmap order does not change:

`Current → P1 One Money Relationship → P2 Multi-rail Everyday Spend → P3 Everyday Money Account`

Execution remains **Gate Serial / Discovery Parallel**. P1 remains `NOT_YET_PASS`; discovery may continue, but P2 scale does not receive authorization from this closure.

## Scope stop

This stage stops before partner outreach message drafting, contract negotiation wording, API endpoints, implementation-detailed fund-flow diagrams, feature design, UX, PRD, state machine, error handling, schema, or code. If capability-level validation remains unresolved, record **`Unknown / downstream validation required`** and stop at this boundary.

## Traceability

| Conclusion | Support |
|---|---|
| Public research closes with `KEEP` | S11-01–S11-08; D11-01 |
| Non-resident category fit is supported; AIX approval is unknown | S11-01–S11-03; D11-02 |
| Pooled infrastructure pattern is supported; pooled AIX retail P2M remains unknown | S11-04–S11-05; D11-03 |
| Stablecoin → PHP leg is supported for local payouts; complete QRPh merchant-spend chain remains unknown | S11-06; D11-04 |
| TPSP/AIX has material product-level burden; exact responsibility split remains unknown | S11-07–S11-08; D11-05 |
| Economics require a commercial quote | D11-06 |
| Vendor Validation is the minimum next action | D11-07 |
| P2 trigger, fallback, and unchanged roadmap | S11-09; D11-08–D11-09 |

No review file is created in this stage.
