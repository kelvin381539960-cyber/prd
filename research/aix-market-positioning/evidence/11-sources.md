# Evidence Sources — AIX Netbank Public Feasibility Closure (11)

> Traceability index for Strategic Validation 11. The source facts below are only the authoritative evidence supplied for this stage; no web browsing or new research was performed. Public evidence is not treated as AIX approval, partner willingness, approved commercial terms, or build authorization. This index remains at Strategy + Capability Level.

## Source register

### Vendor facts

#### S11-01 — Netbank international payment company support

**Source.** [Netbank International Payment Companies](https://netbank.ph/international-payment-companies/)

**Classification.** Vendor Fact.

**Fact used.** The page explicitly targets non-resident businesses. It states that non-resident money services businesses can establish a Philippine payment facility for local disbursements, cross-border transfers, FX, and stablecoin funding through a licensed local VASP partner; non-resident payment processors can open regulated local accounts; and Netbank's BaaS partner set includes fintechs, wallets, PSPs, remitters, and non-resident enterprises.

**Boundary.** This supports non-resident category fit only. It does not prove AIX-specific eligibility, approval, partner willingness, pooled retail settlement, or the complete stablecoin → PHP → QRPh merchant-spend path.

**Use.** Supports the `SUPPORTED AT CATEGORY LEVEL` closure and direct AIX eligibility validation.

#### S11-02 — Netbank products for non-resident payment processors

**Source.** [Netbank Products](https://netbank.ph/products/)

**Classification.** Vendor Fact.

**Fact used.** The products page lists `Non-resident Payment Processors` with Non-Resident Corporate Operating Accounts, Local Collect via VCA + QRPH, Local Disburse via Transfers, FX Services, and Cross-Border Transfers.

**Boundary.** The listing establishes relevant product-category evidence, not AIX approval or permission for a pooled account to fund multiple end-users' merchant payments.

**Use.** Supports category-level fit and the capability-level validation question about AIX/non-resident eligibility.

#### S11-03 — Netbank BaaS TPSP structure

**Source.** [Netbank BaaS License Agreement template](https://virtual.netbank.ph/attachment/Netbank-BaaS-License-Agreement-a00c1be8464e823aefbeff416f0967c217bd2b6b4cf0a560999bef3f871e893b.pdf)

**Classification.** Vendor Fact.

**Facts used.** The template does not hard-code a Philippine TPSP: its cover page leaves `<insert country>` for the TPSP organization. It states that the TPSP has its own End-Users and products, provides direct terms to End-Users, and may use BaaS components subject to Netbank approval.

**Boundary.** A template structure supports a non-resident TPSP category hypothesis; it does not establish that Netbank will approve AIX or accept the intended fund flow.

**Use.** Supports the category-level fit conclusion and the AIX-specific approval gap.

#### S11-04 — Settlement Account primitive

**Source.** [Netbank BaaS License Agreement template, Section 6](https://virtual.netbank.ph/attachment/Netbank-BaaS-License-Agreement-a00c1be8464e823aefbeff416f0967c217bd2b6b4cf0a560999bef3f871e893b.pdf)

**Classification.** Vendor Fact.

**Facts used.** Section 6 requires the TPSP to open a Netbank `Settlement Account`. Necessary BaaS debits/credits and fees may be debited/credited there, and sufficient balance must cover transaction requests. Rates may be set in the Partner Dashboard or a custom annex.

**Boundary.** This proves a TPSP settlement-account primitive, not that a single pooled account is approved for AIX retail end-user merchant payments.

**Use.** Supports the `SUPPORTED` infrastructure pattern and the `UNKNOWN` pooled-retail-permissibility boundary.

#### S11-05 — Payer-side corporate-account-funded QRPH primitive

**Source.** [Netbank QRPH documentation](https://virtual.netbank.ph/docs)

**Classification.** Vendor Fact.

**Fact used.** The public documentation exposes `Process QRPH disbursement`: it uses a decoded QRPH disburse ID, debits a specified Netbank Corporate Account, and transfers to the beneficiary in the QR.

**Boundary.** This proves a payer-side corporate-account-funded QRPH primitive. It does not prove that AIX may pool multiple end-users through one corporate account or that Netbank approves AIX's use case.

**Use.** Supports the pooled-settlement infrastructure hypothesis while preserving the retail P2M permissibility gap.

#### S11-06 — Stablecoin ↔ PHP partner-ecosystem leg

**Source.** [Netbank International Payment Companies](https://netbank.ph/international-payment-companies/)

**Classification.** Vendor Fact.

**Facts used.** The page explicitly states stablecoin funding for remittance companies: USDC/USDT → PHP conversion for local payouts via a licensed VASP partner. The account solution also mentions PHP → stablecoin.

**Boundary.** This proves a general stablecoin↔PHP funding/cross-border leg in the partner ecosystem, not the full stablecoin → PHP → QRPh consumer merchant-spend chain.

**Use.** Supports `SUPPORTED` for the stablecoin → PHP local-payout leg and keeps the full composition `UNKNOWN`.

#### S11-07 — BaaS responsibility facts

**Source.** [Netbank BaaS License Agreement template](https://virtual.netbank.ph/attachment/Netbank-BaaS-License-Agreement-a00c1be8464e823aefbeff416f0967c217bd2b6b4cf0a560999bef3f871e893b.pdf)

**Classification.** Vendor Fact.

**Facts used.** The TPSP puts terms and conditions directly with End-Users, provides direct support for its End-Users, is responsible for its Products and applicable-law compliance, and must secure end-user privacy consent where required. Netbank can authenticate End-Users/TPSP for relevant requests, need not grant UAT/PROD access unless satisfied with regulatory/security/privacy/end-user standards, and may audit TPSP usage.

**Boundary.** The public agreement contains no explicit AML/KYC responsibility split sufficient to assign complete AML/KYC, transaction-monitoring, or consumer-protection ownership.

**Use.** Supports the conclusion that material product-level responsibility remains with TPSP/AIX while the exact compliance allocation remains `UNKNOWN`.

### Regulatory fact

#### S11-08 — BSP OPS scope boundary

**Source.** [BSP OPS Registration FAQ](https://www.bsp.gov.ph/PaymentAndSettlement/FAQ_OPS_Registration.pdf)

**Classification.** Regulatory Fact.

**Facts used.** The FAQ states that foreign providers serving Philippine customers can be in scope for OPS registration. Partner-led integration does not automatically remove AIX regulatory obligations.

**Boundary.** The supplied fact does not assign AIX's exact classification, licenses, OPS status, or compliance ownership.

**Use.** Keeps AIX's regulatory role and required licenses/OPS status as direct validation questions.

### Accepted decision context

#### S11-09 — Stage 10 accepted status

**Source.** Accepted Stage 10 status supplied for this stage.

**Classification.** Decision context.

**Facts used.** Stage 10 accepted `Netbank-led payer-side discovery path / KEEP`; Netbank is a Tier-1 discovery candidate, not an approved vendor; pooled settlement is a Proposal; economics are `Unknown/commercial quote required`; the full stablecoin → QRPh path is `Unknown`; AIX's regulatory role is `Unknown`; P2 scale is blocked by P1; and the roadmap is unchanged.

**Use.** Provides continuity for the Stage 11 closure without treating Stage 10 as partner approval or changing roadmap order.

## Decision register

#### D11-01 — Public-evidence closure

**Type.** Decision.

**Decision.** `KEEP / stop public research`. Existing public evidence is sufficient to justify direct vendor/compliance/commercial validation; more public browsing is unlikely to resolve the remaining blockers.

**Support.** S11-01–S11-09.

#### D11-02 — Non-resident category fit

**Type.** Decision.

**Decision.** Netbank's non-resident partner fit is `SUPPORTED AT CATEGORY LEVEL`. `AIX-specific eligibility/approval` remains `UNKNOWN` until Netbank validates AIX's entity, licenses, business model, and intended fund flow.

**Support.** S11-01–S11-03, S11-08.

#### D11-03 — Pooled-settlement capability boundary

**Type.** Decision plus Proposal.

**Decision.** The pooled-settlement infrastructure pattern is `SUPPORTED`; AIX retail P2M permissibility is `UNKNOWN`.

**Proposal.** Validate partner-led pooled settlement first. The Settlement Account and corporate-account-funded QRPH primitives support a relevant capability hypothesis, not approval for one pooled account to fund multiple AIX end-users' merchant payments.

**Support.** S11-04–S11-05, S11-09.

#### D11-04 — Stablecoin funding boundary

**Type.** Decision.

**Decision.** The stablecoin → PHP leg is `SUPPORTED` for local payouts via a licensed VASP partner. The full `stablecoin → PHP → QRPh end-user merchant spend` path is `UNKNOWN`.

**Support.** S11-01, S11-06, S11-09.

#### D11-05 — Responsibility boundary

**Type.** Decision.

**Decision.** Material product-level responsibility remains with the TPSP/AIX, while Netbank retains approval, authentication, and audit roles. The exact AML/KYC/transaction-monitoring/consumer-protection allocation is `UNKNOWN` and requires direct compliance/contract confirmation.

**Support.** S11-07–S11-08.

#### D11-06 — Economics boundary

**Type.** Unknown / decision boundary.

**Decision.** Economics remain `UNKNOWN / commercial quote required`. No public evidence supplied for this stage confirms AIX payer-side QRPh pricing, FX spread, VASP cost, liquidity cost, settlement-account commitments, or minimums. No public generic price or merchant-acquiring percentage is used as AIX actual cost, and no threshold is invented.

**Support.** S11-04, S11-09.

#### D11-07 — Minimum next action

**Type.** Decision.

**Decision.** Vendor Validation is the minimum next action, not more public research. Ask only for AIX/non-resident eligibility; pooled corporate settlement for multiple end-users' QRPh merchant payments; USDC/USDT → PHP → QRPh composition; exact commercial quote/all-in economics; required licenses/OPS status; AML/KYC/transaction-monitoring/consumer-protection split; and whether the user-frequency/everyday-spend use case is acceptable.

**Boundary.** This is a capability-level confirmation package, not outreach drafting, contract negotiation wording, API requirements, or implementation design.

**Support.** D11-01–D11-06.

#### D11-08 — Decision trigger and fallback

**Type.** Decision.

**Decision.** If Netbank confirms eligibility, an acceptable pooled model, a credible stablecoin → PHP composition, acceptable regulatory burden, and viable all-in economics, the path becomes `PARTNER_VALIDATED_CANDIDATE` for P2 discovery. This is not build authorization and P2 scale remains blocked by P1. If the core conditions fail, downgrade Netbank and move to Tier-2 partner discovery.

**Support.** S11-09, D11-02–D11-07.

#### D11-09 — Roadmap impact

**Type.** Decision.

**Decision.** Roadmap remains `Current → P1 One Money Relationship → P2 Multi-rail Everyday Spend → P3 Everyday Money Account`; Gate Serial / Discovery Parallel is unchanged; P1 remains `NOT_YET_PASS`; P2 scale remains blocked.

**Support.** S11-09 and D11-08.

## Conclusion traceability

| Conclusion | Supporting evidence / decisions |
|---|---|
| Public research stops with `KEEP` | S11-01–S11-09, D11-01 |
| Netbank fits the non-resident category; AIX approval remains unknown | S11-01–S11-03, S11-08, D11-02 |
| Pooled infrastructure is supported; pooled AIX retail P2M is unknown | S11-04–S11-05, D11-03 |
| Stablecoin → PHP local-payout leg is supported; full merchant-spend composition is unknown | S11-01, S11-06, D11-04 |
| Material product-level responsibility remains with TPSP/AIX; exact compliance split is unknown | S11-07–S11-08, D11-05 |
| Economics require a commercial quote | D11-06 |
| Vendor Validation is the next action | D11-07 |
| Trigger, fallback, and roadmap remain constrained | S11-09, D11-08–D11-09 |
