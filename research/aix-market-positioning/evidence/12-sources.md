# Evidence Sources — AIX Strategic Validation 12: Netbank Internal Relationship Validation Route

> Traceability index for Strategic Validation 12. The source of truth for the new relationship claims is internal Lark Organization / Collaboration Facts supplied for this stage, together with the accepted Stage 11 context. No web browsing or new external research was performed. This index remains at Strategy + Capability Level.
>
> The artifact intentionally contains no raw transaction IDs, account numbers, amounts, customer/user IDs, personal names, raw API payloads, screenshots, or other user-level operational details. Group names, dates, sanitized fact summaries, message IDs, and the supplied internal document URL are retained only for traceability.

## Source register

### Internal Organization / Collaboration Facts

#### S12-01 — Existing wider-group Netbank operating relationship

**Source.** Cross-chat Lark search for `Netbank`; multiple current 2026 internal threads.

**Classification.** Internal Organization/Collaboration Fact.

**Fact used.** Atome/Advance group teams already operate live Philippine Netbank integrations. The current threads cover Savings/Transfer operational flows, production incident handling, Netbank service degradation/downtime handling, callback/status reconciliation, and direct channel verification with Netbank.

**Boundary.** This establishes an active wider-group vendor relationship and an operating route. It does not establish AIX-specific approval, eligibility, willingness, contract reuse, commercial reuse, technical reuse, or QRPh P2M permission for AIX.

**Use.** Supports group-level relationship status `EXISTING_ACTIVE` and the conclusion that vendor-access risk is `REDUCED_NOT_ELIMINATED` (reduced, not eliminated).

#### S12-02 — Netbank-hosted Savings activation

**Source.** `业务产品群`, 2026-08-12; message IDs `om_x100b68f417f9eca4e2e7166c69dc819` and `om_x100b68f425e2fca0e192786b3da19c1`.

**Classification.** Internal Organization/Collaboration Fact.

**Fact used.** Savings activation is performed on Netbank's page and proceeds through Netbank-hosted activation.

**Boundary.** Only the existence of a live group integration is used. No detailed user flow, user data, or account-level information is reproduced.

**Use.** Supports the active wider-group relationship conclusion.

#### S12-03 — Production transfer operations and Netbank incident coordination

**Source.** `支付sentry报警群` and `Atome Product x Tech x Data`, Jul–Aug 2026; message IDs `om_x100b688925f690a4e2bf1381096c16e`, `om_x100b68a342ce14b0e10c617020d3116`, `om_x100b67e0b899b8a8e19209fcd1836ce`, and `om_x100b67cf0e287c68e2ca8ad2a7df665`.

**Classification.** Internal Organization/Collaboration Fact.

**Fact used.** Internal production discussions show transfer requests/callbacks involving Netbank, direct channel verification of inconsistent states, incident handling, and planned backend degraded-mode handling for Netbank outages.

**Boundary.** No transaction IDs, account numbers, names, amounts, raw payloads, PII, or other user/transaction details are used or reproduced.

**Use.** Supports group-level operational maturity, direct vendor communication capability, and reduced cold-start access risk. It does not prove AIX technical asset reuse or AIX approval.

#### S12-04 — Planned expansion of wider-group Netbank collaboration

**Source.** `Card Data Request` thread, 2026-08-07; message ID `om_x100b686107f20ca0e2d087a24e2b119`.

**Classification.** Internal Organization/Collaboration Fact.

**Fact used.** A PH-market Netbank Cash product is planned and described as a direct-integration/referral-style product with end-to-end reporting planning.

**Boundary.** This supports active expansion of wider-group collaboration only. It does not prove AIX scope, QRPh P2M scope, commercial reuse, contract reuse, or AIX approval.

**Use.** Supports the conclusion that the group relationship extends beyond a single existing flow.

#### S12-05 — Current Savings analytics relationship

**Source.** `Card Data Request`, 2026-08-20; message ID `om_x100b67531338d0a0e1206974333751d`; linked internal document: <https://advancegroup.sg.larksuite.com/docx/HG5udBfChoBaQKxlAvpl91Pgg9c>.

**Classification.** Internal Organization/Collaboration Fact.

**Fact used.** Current Savings KYC analytics explicitly distinguishes `submit to netbank`. The linked internal document contains sections for Savings KYC volume and application-path analysis.

**Boundary.** Only the existence of a live Netbank Savings relationship is used. No user-level data, metrics, names, or application details are copied into this artifact.

**Use.** Supports group-level relationship status `EXISTING_ACTIVE`.

#### S12-06 — Lark Gateway search coverage limitation

**Source.** Search attempts for more specific terms in the internal Lark environment during this stage.

**Classification.** Evidence coverage limitation.

**Fact used.** More specific searches were intermittently blocked by Lark Gateway upstream errors.

**Boundary.** Search instability limits coverage. It must not be converted into a claim that no AIX-specific approval, contract, owner, or other evidence exists.

**Use.** Preserves the distinction between `not found in available search coverage` and `does not exist`; keeps unresolved claims as `UNKNOWN`.

### Accepted Stage 11 context

#### S12-07 — Accepted Stage 11 status and guardrails

**Source.** Accepted Stage 11 context supplied for this stage.

**Classification.** Decision context.

**Facts used.** Public research is closed with `KEEP / stop public research`; Netbank current status is `DISCOVERY_CANDIDATE_NOT_APPROVED`; non-resident fit is `SUPPORTED_CATEGORY_LEVEL`; pooled infrastructure is `SUPPORTED` while AIX retail P2M permissibility is `UNKNOWN`; the stablecoin→PHP local-payout leg is `SUPPORTED` while the full stablecoin→PHP→QRPh end-user merchant path is `UNKNOWN`; compliance split is `UNKNOWN`; economics are `UNKNOWN / commercial quote required`; the next action was Vendor Validation; `PARTNER_VALIDATED_CANDIDATE` is future conditional only; P1 remains `NOT_YET_PASS`; P2 scale is blocked; and the roadmap is unchanged.

**Boundary.** This context remains the baseline. New internal relationship evidence does not upgrade any AIX-specific status, authorize build, or change the P1/P2 dependency.

**Use.** Constrains Stage 12 to an internal relationship/access-route upgrade and preserves all Stage 11 Unknowns and decision triggers.

## Decision register

#### D12-01 — Group-level Netbank relationship

**Type.** Decision.

**Decision.** The wider Atome/Advance group-level Netbank relationship is **`EXISTING_ACTIVE`**.

**Support.** S12-01–S12-05.

**Boundary.** This is a group relationship decision, not AIX partner approval, QRPh P2M approval, contract reuse, commercial reuse, or technical reuse.

#### D12-02 — AIX partner status remains unchanged

**Type.** Decision.

**Decision.** AIX remains **`DISCOVERY_CANDIDATE_NOT_APPROVED`**. Group usage must not be used as a proxy for AIX-specific approval, eligibility, partner willingness, or approved terms.

**Support.** S12-01, S12-06–S12-07.

#### D12-03 — Vendor-access risk is `REDUCED_NOT_ELIMINATED`

**Type.** Decision.

**Decision.** Vendor-access risk is **`REDUCED_NOT_ELIMINATED`** (reduced, not eliminated): existing operational channels and group-vendor experience reduce cold-start risk, but the risk is not eliminated. Exact owner identity and whether the existing route can sponsor AIX onboarding were not established in this stage.

**Support.** S12-01, S12-03, S12-06.

#### D12-04 — Internal owner handoff before AIX-specific Vendor Validation

**Type.** Proposal / next-action decision.

**Decision.** Refine the next action to **`INTERNAL_OWNER_HANDOFF_THEN_AIX_VENDOR_VALIDATION`** (internal owner handoff, then AIX vendor validation). First identify the existing internal Netbank vendor/commercial/compliance owner path; then run the Stage 11 capability-level validation questions.

**Boundary.** This is an execution-route refinement, not a completed handoff, message draft, contact action, vendor validation result, or partner approval.

**Support.** S12-01–S12-07.

#### D12-05 — Contract/commercial reuse remains Unknown

**Type.** Unknown / decision boundary.

**Decision.** Existing Savings, Cash, and Transfer collaboration does not prove that the same agreement, pricing, settlement setup, licenses, or compliance responsibilities can be reused for AIX QRPh P2M. Contract/commercial reuse remains **`UNKNOWN`**.

**Support.** S12-01, S12-04–S12-07.

#### D12-06 — Technical capability reuse remains Unknown

**Type.** Unknown / decision boundary.

**Decision.** Existing live integrations prove organizational experience and operational maturity, but do not establish that current Atome Netbank integration assets/components are reusable by AIX. Technical capability reuse remains **`UNKNOWN`**.

**Boundary.** No code, API, endpoint, or component analysis is performed in this stage.

**Support.** S12-01, S12-03, S12-07.

#### D12-07 — AIX QRPh business-case Unknowns remain unchanged

**Type.** Decision.

**Decision.** The group relationship evidence does not resolve pooled multi-end-user retail P2M permissibility, the complete stablecoin→PHP→QRPh composition, AIX-specific approval/licensing, AML/KYC/transaction-monitoring/consumer-protection split, all-in economics, or intended use-case acceptance.

**Support.** S12-06–S12-07; D12-02, D12-05–D12-06.

#### D12-08 — No cold outreach or contact action

**Type.** Decision / scope guardrail.

**Decision.** No internal or external message is drafted or sent, no employee names are exposed, and no contact action is initiated in this stage. The recommendation is only to reuse the existing relationship route when an authorized future validation activity begins.

**Support.** D12-04 and the stage scope boundary.

#### D12-09 — Decision trigger and roadmap remain unchanged

**Type.** Decision.

**Decision.** Only AIX-specific confirmation of eligibility, an acceptable pooled model, credible stablecoin→PHP composition, acceptable regulatory burden, and viable all-in economics can produce the future conditional status `PARTNER_VALIDATED_CANDIDATE`. This is not build authorization. P1 remains `NOT_YET_PASS`, P2 scale remains blocked by P1, and the roadmap remains `Current → P1 One Money Relationship → P2 Multi-rail Everyday Spend → P3 Everyday Money Account` with Gate Serial / Discovery Parallel.

**Support.** S12-07; D12-02, D12-04, D12-07.

#### D12-10 — Failed AIX-specific Vendor Validation fallback

**Type.** Decision boundary.

**Decision.** If AIX-specific Vendor Validation fails one or more core conditions—eligibility, acceptable pooled model, credible stablecoin→PHP composition, acceptable regulatory burden, or viable all-in economics—**downgrade Netbank and resume Tier-2 partner discovery**. Roadmap order, the P1 Gate, the P2 scale block, and **Gate Serial / Discovery Parallel** remain unchanged. AIX remains `DISCOVERY_CANDIDATE_NOT_APPROVED`; `PARTNER_VALIDATED_CANDIDATE` is not reached in this branch.

**Support.** S12-07; D12-02 and D12-09.

## Conclusion traceability

| Conclusion | Supporting evidence / decisions |
|---|---|
| Wider-group Netbank relationship is `EXISTING_ACTIVE` | S12-01–S12-05; D12-01 |
| Internal relationship reduces access risk but does not validate AIX | S12-01, S12-03, S12-06–S12-07; D12-02–D12-04 |
| Contract/commercial reuse is Unknown | S12-01, S12-04–S12-07; D12-05 |
| Technical capability reuse is Unknown | S12-01, S12-03, S12-07; D12-06 |
| Stage 11 QRPh, compliance, economics, and approval Unknowns remain unchanged | S12-06–S12-07; D12-02, D12-05–D12-07 |
| No cold outreach or contact action occurs in this stage | D12-04, D12-08 |
| Future trigger, P1/P2 constraints, and roadmap are unchanged | S12-07; D12-09 |
| Failed validation of any core condition downgrades Netbank and resumes Tier-2 partner discovery without changing roadmap order, P1 Gate, P2 scale block, or Gate Serial / Discovery Parallel | S12-07; D12-10 |

## Redaction and coverage controls

- Raw transaction IDs, account numbers, amounts, customer/user IDs, personal names, raw API payloads, screenshots, and other user-level operational details are excluded.
- The included message IDs are Lark message references supplied for traceability, not transaction or account data.
- The one included URL is the supplied internal Lark document reference; its contents are not copied into this artifact.
- Lark Gateway search instability is recorded as a coverage limitation. Failed or blocked searches do not establish non-existence.
- No external source, public-market claim, contract interpretation, code fact, API fact, or new research result is added.
