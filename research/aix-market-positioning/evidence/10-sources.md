# Evidence Sources — AIX QR Ph Partner Operating Model & Economics Discovery (10)

> Traceability index for the QR Ph named-partner, operating-model, and economics discovery materialization. The source facts below are the authoritative evidence supplied for this stage; no browsing was performed. Public evidence is not treated as partner willingness, AIX acceptance, or approved commercial terms. This index remains at Strategy + Capability Level and contains no implementation design.

## Source register

### Vendor / Market facts

#### S10-01 — BSP QR Ph P2M participant roles

**Source.** [BSP QR Ph P2M Participants](https://www.bsp.gov.ph/PaymentAndSettlement/QR%20Ph%20P2M%20Participants.pdf)

**Fact used.** The latest supplied participant document lists Netbank (A Rural Bank), Inc., Maya Philippines, and PayMongo Payments as QR Ph P2M Sender/Receiver participants.

**Source conflict / boundary.** Retrieval showed a date-render mismatch: parsed metadata for the current file says 31 Jul 2026, while the screenshot render showed 31 May 2026. The exact date is not used as a decision driver; the stable fact used here is participant role. Participant status does not establish partner willingness, AIX eligibility, or approved terms.

**Use.** Supports naming Netbank as a Tier-1 discovery candidate and Maya/PayMongo as Tier-2 backups.

#### S10-02 — Netbank BSP OPS registration

**Source.** [BSP Certificate of Registration](https://www.bsp.gov.ph/PaymentAndSettlement/COR.pdf)

**Fact used.** Netbank is BSP-registered as an Operator of Payment System, registration `OPSCOR-2023-0026`.

**Use.** Supports regulated-partner fit discovery; it does not determine AIX's own regulatory classification.

#### S10-03 — Netbank public payer-side QRPH capability evidence

**Source.** [Netbank Virtual API Documentation](https://virtual.netbank.ph/docs)

**Fact used.** The supplied public documentation exposes QRPH decode, Generate QRPH for P2P/P2M, and `Process QRPH disbursement`, which debits a specified Netbank Corporate Account and transfers to the beneficiary encoded by the QR.

**Use.** Establishes unusually relevant payer-side capability evidence for discovery, distinct from generic merchant acceptance. It does not prove a white-label AIX arrangement or commercial approval.

#### S10-04 — Netbank end-user merchant-spending use case

**Source.** [Netbank Cash Lenders](https://netbank.ph/cash-lenders/)

**Fact used.** Netbank explicitly markets a payer-side end-user use case in which users can spend issued loan/credit directly with merchants via QRPh.

**Use.** Supports infrastructure fit for an end-user merchant-spend pattern; it does not establish stablecoin funding support.

#### S10-05 — Netbank BaaS settlement-account requirement

**Source.** [Netbank BaaS License Agreement](https://virtual.netbank.ph/attachment/Netbank-BaaS-License-Agreement-a00c1be8464e823aefbeff416f0967c217bd2b6b4cf0a560999bef3f871e893b.pdf)

**Fact used.** The BaaS agreement requires the TPSP to maintain a Netbank Settlement Account sufficient to cover API transaction requests and fees. Commercial rates may be in the Partner Dashboard or a custom annex.

**Use.** Supports validating pooled settlement and confirms that actual terms require commercial discovery.

#### S10-06 — Netbank international payment-company support

**Source.** [Netbank International Payment Companies](https://netbank.ph/international-payment-companies/)

**Fact used.** Netbank publicly mentions support for international/non-resident payment companies, local QR Ph collections, local payouts, FX/cross-border activity, and stablecoin fund transfers through a licensed local VASP partner.

**Boundary.** This does not publicly prove stablecoin → PHP → QRPh consumer merchant payment or that AIX is an accepted partner.

**Use.** Supports Tier-1 discovery fit and the question of whether a VASP/FX component is needed.

#### S10-07 — Netbank generic disbursement price benchmark

**Source.** [Netbank Business Disburse-to-Account](https://virtual.netbank.ph/business-disburse-to-account)

**Fact used.** Standard public generic interbank `Disburse-to-Account` pricing is PHP10 per transaction; for the stated simple engagement, no minimum monthly invoice, fixed monthly fee, or ADB is listed.

**Boundary.** This is a pricing benchmark only, not the confirmed QRPh payer-side price for AIX.

#### S10-08 — Public merchant-acceptance pricing benchmarks

**Sources.** [Maya Business Pricing](https://www.maya.ph/business/pricing); [PayMongo Pricing](https://www.paymongo.com/pricing); [Xendit Philippines Pricing Calculator](https://www.xendit.co/en-ph/pricing-calculator-ph/)

**Facts used.** The supplied public benchmarks are approximately 1.0% for Maya QRPh, 1.34% for PayMongo in-store QRPh, and 1.40% or PHP15 with VAT shown in the Xendit calculator.

**Boundary.** These are merchant-acceptance benchmarks, not AIX payer-side rail costs and not an AIX pass threshold.

#### S10-09 — Xendit QRPh acceptance product

**Source.** [Xendit QRPH](https://www.xendit.co/en-my/payment-channel/qrph/)

**Facts used.** The supplied public page describes PHP settlement, T+1 working-day settlement, no refunds, and an acceptance/payment-method product.

**Use.** Provides acceptance and operating/economics context; it is not evidence of payer-side white-label scan-to-pay capability for AIX.

#### S10-10 — PayMongo and Maya public QRPh acceptance boundary

**Sources.** [PayMongo QR Ph Payment Acceptance](https://docs.paymongo.com/docs/payment-acceptance-qr-ph); Maya public QRPh business pages supplied for this stage.

**Fact used.** The obtained public materials focus on Dynamic/Static QR merchant acceptance. No payer-side white-label AIX capability is established by these materials.

**Use.** Keeps Maya and PayMongo as Tier-2 backups rather than elevating them to the first payer-side discovery path.

### Regulatory facts

#### S10-11 — BSP OPS scope boundary

**Source.** [BSP OPS Registration FAQ](https://www.bsp.gov.ph/PaymentAndSettlement/FAQ_OPS_Registration.pdf)

**Facts used.** An OPS can include an entity maintaining a platform enabling payments/fund transfers or providing a system that processes payments on behalf of a person. Payment facilitators/gateways engaged by BSFIs may still need OPS registration when performing OPS activities, and foreign providers serving Philippine customers can also be in scope.

**Use.** Establishes that partner-led integration does not automatically eliminate AIX regulatory obligations. Exact AIX classification remains `Unknown` until role and fund flow are confirmed.

### Accepted roadmap context

#### S10-12 — P1 Gate and roadmap dependency

**Sources.** [`TASK.md`](../TASK.md), [`09-p1-gate-closure.md`](../09-p1-gate-closure.md), and [`evidence/09-sources.md`](09-sources.md)

**Facts used.** The current strategy remains `Current → P1 One Money Relationship → P2 Multi-rail Everyday Spend → P3 Everyday Money Account`; P1 is `NOT_YET_PASS`; P2 discovery may continue, but P2 scale remains blocked.

**Use.** Constrains this stage to P2 discovery materialization without changing roadmap order or Gate status.

## Decision register

#### D10-01 — Named QR Ph path

**Type.** Decision.

**Decision.** Upgrade QR Ph P2M from generic `Priority Discovery Rail` to **`Netbank-led payer-side discovery path / KEEP`**.

**Support.** S10-01–S10-06.

**Boundary.** This is discovery, not build authorization, partner approval, a white-space claim, or a moat claim.

#### D10-02 — Netbank Tier-1 candidate

**Type.** Decision.

**Decision.** Netbank is the Tier-1 discovery candidate because the supplied evidence combines participant role, payer-side QRPh capability evidence, BaaS settlement context, and international payment-company support.

**Support.** S10-01–S10-06.

**Boundary.** Fit evidence is not evidence of willingness or approved commercial terms.

#### D10-03 — Maya / PayMongo Tier-2 backups

**Type.** Decision.

**Decision.** Maya Philippines and PayMongo Payments remain Tier-2 backups. Their participant status is confirmed, but the public materials obtained here establish merchant acceptance rather than white-label payer-side AIX capability; payer-side partner capability is `Unknown`.

**Support.** S10-01 and S10-10.

#### D10-04 — Xendit and Coins.ph positioning

**Type.** Decision.

**Decision.** Xendit is an acceptance/economics benchmark, not the first-priority payer-side rail candidate on the supplied evidence. Coins.ph remains a competitor/market precedent rather than the preferred partner path.

**Support.** S10-08–S10-09 plus accepted market context.

#### D10-05 — Preferred operating-model hypothesis

**Type.** Proposal.

**Proposal.** Validate partner-led pooled settlement first: AIX preserves the user-facing stablecoin / One Money Relationship; Netbank provides regulated PHP settlement and the QRPh sender rail; a licensed VASP/FX component is used only if needed.

**Support.** S10-03–S10-06 and S10-11.

**Boundary.** Pooled settlement, the role split, VASP/FX need, and AIX responsibility are not confirmed.

#### D10-06 — Why pooled settlement is preferred

**Type.** Strategic rationale.

**Decision.** Pooled settlement is the first hypothesis to validate because it has the best strategic chance of preserving a stablecoin-native relationship without forcing a visible pre-funded PHP account.

**Support.** D10-05.

**Boundary.** BSP OPS rules mean the AIX regulatory/compliance burden may remain; exact classification is `Unknown`.

#### D10-07 — Fallback model

**Type.** Proposal.

**Proposal.** Use per-user Netbank Account-as-a-Service / white-label accounts only if pooled settlement is not allowed or regulatory separation requires it.

**Trade-off.** It may introduce an additional fiat balance/account relationship and weaken the One Money Relationship unless abstracted successfully.

#### D10-08 — Direct AIX route

**Type.** Decision.

**Decision.** Do not prioritize a direct AIX OPS / merchant-acquisition route for the next discovery. Keep it as an Unknown/later option only if partner-led economics or compliance fail and the strategic upside justifies it.

#### D10-09 — Economics status

**Type.** Unknown / decision boundary.

**Decision.** Economics are **`Unknown / commercial quote required`**. Do not use the public PHP10 generic disbursement benchmark or 1.0–1.4% merchant-acceptance benchmarks as AIX actual cost, and do not invent a pass threshold.

**Support.** S10-05, S10-07–S10-10.

#### D10-10 — Capability-level validation questions

**Type.** Next discovery scope.

**Questions.** Confirm payer-side QRPh P2M eligibility for AIX/non-resident fintech; pooled Settlement Account permissibility for end-user merchant payments; whether stablecoin-to-PHP funding/FX can be supported directly or through a licensed VASP; all-in per-transaction/FX/liquidity/settlement costs; minimums/commitments; regulatory/KYC/AML/consumer-protection responsibility split; and high-level settlement/refund/reversal capability boundaries.

**Boundary.** These remain capability-level commercial/regulatory questions, not API, field, state, workflow, or PRD requirements.

#### D10-11 — Disconfirmers

**Type.** Decision guardrail.

**Disconfirmers.** Netbank cannot support payer-side end-user merchant spend for AIX; pooled settlement requires a per-user visible PHP account that materially breaks the target relationship; all-in economics make low-ticket everyday spend unattractive; AIX regulatory obligations remain too heavy even partner-led; no stablecoin-to-PHP funding path; or no user-frequency lift.

#### D10-12 — Roadmap impact

**Type.** Decision.

**Decision.** P2 discovery becomes more concrete, but P2 scale remains blocked by the P1 Gate. Roadmap order remains unchanged: `Current → P1 → P2 → P3`.

**Support.** S10-12.

## Conclusion traceability

| Conclusion | Supporting evidence / decisions |
|---|---|
| QR Ph becomes a named Netbank-led discovery path | S10-01–S10-06, D10-01–D10-02 |
| Netbank is Tier-1; Maya/PayMongo are Tier-2 backups | S10-01, S10-03–S10-06, S10-10, D10-02–D10-03 |
| Preferred model is pooled settlement, still a Proposal | S10-05–S10-06, S10-11, D10-05–D10-06 |
| Per-user account model is fallback only | D10-07 |
| Direct AIX OPS/acquisition route is not next discovery | S10-11, D10-08 |
| Economics are Unknown and require commercial quote | S10-05, S10-07–S10-10, D10-09 |
| AIX regulatory role and complete stablecoin-to-PHP-to-QRPh path remain Unknown | S10-06, S10-11, D10-05, D10-09–D10-10 |
| P2 discovery is more concrete; P2 scale remains blocked; roadmap unchanged | S10-12, D10-12 |
