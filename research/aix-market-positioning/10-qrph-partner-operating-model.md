# AIX QR Ph Partner Operating Model & Economics Discovery — Strategic Validation

> Date: 2026-08-30
> Scope: Business Strategy / Product Strategy / Strategic Roadmap validation at Capability Level.
> Stage meaning: this materializes a named partner path and an operating-model/economics discovery hypothesis; it is not build authorization, partner approval, or P2 scale acceptance.
> Evidence basis: authoritative evidence supplied for this stage plus accepted repository context. No browsing, production query, or code investigation was performed.
> Boundary: this artifact contains no feature, PRD, page, UI, API, state-machine, schema, instrumentation, or implementation design. Partner willingness and commercial terms are not inferred.

## Executive conclusion

**Decision: upgrade QR Ph P2M from generic `Priority Discovery Rail` to `Netbank-led payer-side discovery path / KEEP`.**

This is a concrete discovery path, not a committed build, a moat claim, or evidence that Netbank has accepted AIX. Netbank is the **Tier-1 discovery candidate** because the supplied public evidence uniquely combines:

- QR Ph P2M Sender/Receiver participant status;
- public payer-side QRPh decode / pay capability evidence;
- a BaaS settlement-account model; and
- support for international payment companies.

Maya Philippines and PayMongo Payments remain **Tier-2 backup candidates** because the supplied public evidence confirms QRPh Sender/Receiver status but their obtained public materials establish merchant acceptance, not white-label payer-side capability for AIX. Xendit is an acceptance/economics benchmark, not the first-priority payer-side candidate. Coins.ph remains a competitor and market precedent, not the preferred partner path.

The operating-model hypothesis to validate first is **partner-led pooled settlement**: AIX preserves the user-facing stablecoin / One Money Relationship; Netbank provides regulated PHP settlement and the QRPh sender rail; a licensed VASP/FX component is used only if needed. This is a **Proposal**, not a confirmed operating arrangement. It is preferred because it has the best strategic chance of preserving a stablecoin-native relationship without forcing a visible pre-funded PHP account. The regulatory/compliance burden on AIX may nevertheless remain; AIX's exact role and OPS classification are **Unknown** until role and fund flow are confirmed.

The fallback is per-user Netbank Account-as-a-Service / white-label account only if pooled settlement is not permitted or regulatory separation requires it. Its strategic downside is an additional fiat balance/account relationship that may weaken the One Money Relationship unless successfully abstracted; this document does not design that experience. A direct AIX OPS / merchant-acquisition route is **not recommended for the next discovery** and remains an Unknown/later option only if partner-led economics and compliance fail and the strategic upside justifies it.

Economics are **Unknown / commercial quote required**. Public PHP10 generic interbank disbursement pricing and roughly 1.0–1.4% merchant-acceptance benchmarks are not AIX payer-side QRPh costs and must not be used as an AIX pass threshold. P2 discovery is now more concrete, while P2 scale remains blocked by the P1 Gate. The roadmap remains:

`Current → P1 One Money Relationship → P2 Multi-rail Everyday Spend → P3 Everyday Money Account`

## Stage scope check

### Strategic question

Can a named partner-led QR Ph P2M path plausibly provide the high-level **everyday PHP spend capability** while preserving AIX's stablecoin-native One Money Relationship, with an operating model and economics that merit downstream validation?

### Capabilities and strategic assumptions judged

- **Payer-side QR Ph P2M Spend capability:** whether AIX can reach everyday merchant-spend outcomes through a partner rail.
- **Regulated PHP settlement capability:** whether a partner can provide the settlement role needed for the spend outcome.
- **Stablecoin-to-PHP funding / FX capability:** whether the conversion and funding role can be supported directly or through a licensed VASP/FX component.
- **Partner-led operating model:** whether pooled settlement is strategically preferable to a per-user fiat-account model.
- **Low-ticket everyday-spend economics:** whether the all-in cost structure is commercially viable; no pass threshold is invented here.

### Explicitly outside this stage

This stage does not decide QR scanning or confirmation UX, pages, CTA/copy, fields, API contracts, state machines, errors, refunds/reversals workflows, limits, frequency rules, instrumentation, PRD requirements, or implementation design.

## Evidence classification

### Vendor / Market / Regulatory Facts

The following are facts or evidence boundaries from the supplied sources, not AIX decisions:

| Classification | Supplied fact | Strategic boundary |
|---|---|---|
| Vendor / Market Fact | The latest supplied BSP QR Ph P2M participant document lists Netbank (A Rural Bank), Inc., Maya Philippines, and PayMongo Payments as Sender/Receiver participants. | Participant role supports candidate naming; it does not establish partner willingness, AIX eligibility, or commercial approval. |
| Regulatory / Vendor Fact | Netbank is BSP-registered as an Operator of Payment System, registration `OPSCOR-2023-0026`. | This supports regulated-partner discovery; it does not determine AIX's own classification. |
| Vendor Fact | Netbank public QRPH materials expose QRPH decode, QR generation for P2P/P2M, and a QRPh disbursement capability that debits a specified Netbank Corporate Account and transfers to the beneficiary encoded by the QR. | This is public payer-side capability evidence, unlike generic merchant-acceptance evidence; it is not proof of a white-label AIX arrangement. |
| Vendor Fact | Netbank markets a payer-side end-user use case in which users spend issued loan/credit directly with merchants via QRPh. | This supports infrastructure fit for an end-user merchant-spend pattern, not stablecoin funding support. |
| Vendor Fact | Netbank's BaaS agreement requires a TPSP to maintain a Netbank Settlement Account sufficient for API transaction requests and fees; rates may be in the Partner Dashboard or a custom annex. | This supports investigating pooled settlement and confirms that actual rates require commercial validation. |
| Vendor / Market Fact | Netbank publicly mentions international/non-resident payment companies, local QR Ph collections, local payouts, FX/cross-border support, and stablecoin fund transfers through a licensed local VASP partner. | It does not publicly prove stablecoin → PHP → QRPh consumer merchant payment or that AIX is an accepted partner. |
| Vendor Pricing Fact | Netbank's standard public generic interbank `Disburse-to-Account` price is PHP10/transaction, with no minimum monthly invoice, fixed monthly fee, or ADB for the stated simple engagement. | Benchmark only; it is not the confirmed QRPh payer-side price. |
| Market Pricing Fact | Public merchant-acceptance benchmarks supplied for Maya, PayMongo, and Xendit are approximately 1.0%, 1.34%, and 1.40% or PHP15 with VAT shown in the Xendit calculator. | These are merchant-acquirer acceptance benchmarks, not AIX payer-side rail costs. |
| Market Fact | Xendit public QRPh materials describe PHP settlement, T+1 working day settlement, no refunds, and an acceptance/payment-method product. PayMongo and Maya materials obtained here likewise focus on merchant acceptance. | None of these public materials establishes payer-side white-label scan-to-pay capability for AIX. |
| Regulatory Fact | BSP's OPS FAQ states that an OPS can include an entity maintaining a payment/fund-transfer platform or processing payments on behalf of a person; payment facilitators/gateways engaged by BSFIs may still need OPS registration, and foreign providers serving Philippine customers can be in scope. | Partner-led integration does not automatically remove AIX regulatory obligations; exact AIX classification is Unknown until role and fund flow are confirmed. |

**Source conflict note.** The supplied BSP participant PDF has a date-render mismatch: parsed metadata says 31 Jul 2026 while the screenshot render showed 31 May 2026. The exact date is not used as a decision driver; only the stable participant role is used.

### Proposal / Decision / Unknown

| Type | Stage position |
|---|---|
| Decision | **`Netbank-led payer-side discovery path / KEEP`** is the named QR Ph path for the next capability-level discovery. |
| Decision | Netbank is **Tier-1**; Maya and PayMongo are **Tier-2 backups**; Xendit is an acceptance/economics benchmark; Coins.ph is a competitor/market precedent. |
| Proposal | Validate **partner-led pooled settlement** first: AIX preserves the stablecoin / One Money Relationship; Netbank supplies regulated PHP settlement and the QRPh sender rail; licensed VASP/FX is added only if needed. |
| Rationale | Pooled settlement has the best strategic chance of preserving a stablecoin-native relationship without forcing a visible pre-funded PHP account. This is a strategic preference, not a confirmed partner or regulatory outcome. |
| Fallback Proposal | Use per-user Netbank Account-as-a-Service / white-label account only if pooled settlement is not allowed or regulatory separation requires it. |
| Decision | Do not prioritize a direct AIX OPS / merchant-acquisition route in the next discovery. Keep it as an Unknown/later option if partner-led economics or compliance fail and the strategic upside justifies it. |
| Unknown | Partner willingness, AIX/non-resident eligibility, approved commercial terms, pooled-settlement permissibility for end-user merchant payments, stablecoin-to-PHP funding/FX path, AIX regulatory classification, responsibility split, and all-in economics remain unconfirmed. |
| Unknown | No public source supplied here proves a stablecoin-to-PHP-to-QRPh consumer merchant payment path or user-frequency lift. |

## Operating-model hypotheses

### Preferred hypothesis — partner-led pooled settlement

**Proposal:** AIX remains the user-facing stablecoin and One Money Relationship; Netbank provides the regulated PHP settlement role and QRPh sender rail; a licensed VASP/FX component is involved only if the stablecoin-to-PHP leg requires it.

Strategic reasons to validate this first:

- it best preserves the intended stablecoin-native relationship;
- it may avoid a visible pre-funded PHP account for each user; and
- it keeps the next question at capability level: whether the combined partner roles can make everyday PHP spend feasible.

This model does not imply that AIX avoids regulatory or consumer-protection responsibilities. BSP's OPS framing means the AIX role must be assessed from the actual role and fund flow.

### Fallback hypothesis — per-user account model

**Proposal:** Use Netbank Account-as-a-Service / white-label accounts per user only if pooled settlement is not permitted or a regulated separation requires it.

**Strategic downside:** an additional fiat balance/account relationship may weaken the One Money Relationship and stablecoin-native positioning unless it can be abstracted successfully. Whether that abstraction is possible is not decided here.

### Deferred option — direct AIX OPS / merchant acquisition

**Decision:** Do not make this the next discovery path. It remains an Unknown/later option, contingent on partner-led economics and compliance failing and the strategic upside still justifying the additional burden.

## Capability and economics status

| Capability / constraint | Status | Meaning for the next decision |
|---|---|---|
| QR Ph P2M payer-side everyday spend | **Candidate / Discovery** | A named path now exists, but no build authorization follows. |
| Netbank-led PHP settlement and sender rail | **Fit evidence / feasibility Unknown** | Public evidence is unusually relevant, but AIX eligibility and terms are not confirmed. |
| Stablecoin → PHP funding / FX | **Unknown** | Netbank's public VASP/cross-border statements do not prove the complete consumer merchant-payment path. |
| Pooled Settlement Account for end-user merchant payments | **Unknown** | BaaS settlement-account language supports a validation question, not approval. |
| AIX regulatory / KYC / AML / consumer-protection role | **Unknown** | Partner-led integration does not automatically eliminate AIX obligations. |
| All-in everyday-spend economics | **Unknown / commercial quote required** | Validate per-transaction, FX, liquidity, settlement, minimums, commitments, and other commercial components together. |
| Low-ticket economics pass threshold | **Not set** | Public benchmarks are context only; this stage invents no numeric threshold. |

## Capability-level commercial validation questions

The next discovery should confirm, at a high level:

- whether payer-side QRPh P2M is available to AIX and/or a non-resident fintech in the proposed role;
- whether a pooled Netbank Settlement Account can support end-user merchant payments;
- whether stablecoin-to-PHP funding and FX can be supported directly or through a licensed VASP;
- the all-in per-transaction, FX, liquidity, and settlement cost structure;
- minimums, volume commitments, or other commercial commitments;
- the regulatory, KYC/AML, and consumer-protection responsibility split; and
- high-level feasibility boundaries for settlement, refunds, and reversals.

These are discovery questions, not API, field, state, workflow, or PRD requirements.

## Disconfirmers

The named path or preferred operating-model hypothesis should be reconsidered if any of the following is established:

- Netbank cannot support payer-side end-user merchant spend for AIX;
- pooled settlement is unavailable and the required per-user visible PHP account materially breaks the target relationship;
- all-in economics make low-ticket everyday spend unattractive;
- AIX regulatory obligations remain too heavy even under a partner-led model;
- no stablecoin-to-PHP funding path can be supported; or
- the capability produces no user-frequency lift.

These are disconfirmers, not quantitative pass/fail thresholds.

## Roadmap and Gate impact

P2 discovery becomes more concrete through a named Netbank-led path and an explicit operating-model/economics hypothesis. **P2 scale remains blocked by the P1 Gate**, which is still `NOT_YET_PASS`; this stage does not change the P1 conclusion, authorize build, or add a numerical Gate threshold.

The roadmap remains:

`Current → P1 One Money Relationship → P2 Multi-rail Everyday Spend → P3 Everyday Money Account`

Discovery may continue in parallel, but the order and Gate Serial / Discovery Parallel discipline remain unchanged.

## Capability-level closure

This stage is materialized as a strategic validation artifact. Its next step is partner/commercial/regulatory discovery at Capability Level, followed by separate review when requested. The hardened guardrail remains in force: do not turn the named path into page, UI, API, field, state-machine, exception, schema, instrumentation, PRD, or implementation decisions.
