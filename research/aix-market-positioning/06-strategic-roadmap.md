# AIX Strategic Roadmap v1

> Date: 2026-08-30
> Status: Final / Accepted
> Review: AChatGPT GPT-5.6 Sol/high — PASS; P0=0; P1=0
> Market boundary: **`consumer crypto/stablecoin → real-world purchasing power`**

## Executive Decision

**Decision / Proposal.** The target proposal is **Stablecoin-native Everyday Money Account**.

- **Primary job:** J1 Global Money.
- **Secondary job:** J2 Crypto → Spend.
- **GTM wedge:** A6 Local Purchasing-Power Bridge.
- **Product form:** A3 Stablecoin Multi-rail Account.
- **Target account role:** A1 Money Account-first.
- **Proof-market candidate:** PH is the **current-evidence best-supported proof-market candidate only**. It is not a proven globally optimal market, a confirmed blue ocean, or a current-AIX anchor.
- **Positioning boundary:** Card is a purchasing-power rail, not the positioning itself.

**Decision.** A6 → A3 → A1 is one staged path, not three parallel products or three parallel strategies:

> **A6 GTM wedge → A3 product form → A1 target account role.**

**Guardrail.** J1 primary and the target account role are strategic choices and testable hypotheses. They must not be presented as proven market facts. The roadmap earns stronger claims through user behavior at each gate.

## Strategic Logic

### Strategic layers

| Layer | v1 position | Classification |
|---|---|---|
| Market boundary | Consumer crypto/stablecoin to real-world purchasing power | **Fact** |
| J1 Global Money | Primary job to validate | **Decision / target hypothesis** |
| J2 Crypto → Spend | Secondary job and initial purchasing-power wedge | **Decision** |
| A6 Local Purchasing-Power Bridge | Market entry and GTM wedge | **Decision** |
| A3 Stablecoin Multi-rail Account | Product form to validate after P1 | **Decision / Proposal** |
| A1 Money Account-first | Target account role earned only through recurring behavior | **Proposal / conditional target** |
| Card | One rail in the purchasing-power portfolio | **Decision** |
| PH | Best-supported proof-market candidate under current evidence | **Decision under uncertainty** |

**Inference.** A relationship in which funds remain available and are used repeatedly for purchasing power may be more durable than one-off card spend. This is a hypothesis to validate, not an established market fact.

**Decision.** AIX should use J2 to make the value immediately legible and use J1 as the relationship it ultimately tests. The roadmap therefore validates a money relationship first, adds local rails second, and considers the A1 account role only after recurring inflow and primary-account behavior are demonstrated.

**Scope guardrail.** Roadmap units are business capabilities, user relationships, product forms, and market validation. This document does not define pages, UI, copy, fields, APIs, state machines, PRD sections, or technical implementation.

## Current Baseline

This is a capability-level strategy overlay. Current AIX capability does not define the market boundary or prove the target account role.

| Area | Current overlay | Classification |
|---|---|---|
| Confirmed capabilities | Receive, Hold, Swap, and Card Spend are confirmed at capability level | **Fact** |
| Wallet / Card relationship | Wallet and Card are separate | **Fact** |
| Auto Debit | Partial runtime confidence | **Fact** |
| No runtime confirmation | Send; outbound Crypto Withdraw; Fiat bank/e-wallet cashout; Unified funding/balance | **Fact** |
| Strategic implication | Current capability must be treated as a baseline overlay, not as proof of a complete Money Account | **Decision** |

**Unknown.** The current baseline does not by itself establish whether users retain funds, return for repeat purchasing-power use, route recurring inflows, or treat AIX as a primary account.

## Roadmap Overview

| Stage | Business relationship / product form | Core validation | Gate or failure path |
|---|---|---|---|
| Current | Existing capability-level baseline | Establish the starting point without redefining the market by implementation | Enter P1 validation |
| Phase 1 — One Money Relationship | Focused purchasing-power relationship; not account feature completeness | Funds retained plus repeat purchasing-power relationship | **P1 Gate**; if failed, Stay Spend Feature / J2 |
| Phase 2 — Multi-rail Everyday Spend | A3 Stablecoin Multi-rail Account, entered through A6 and a proof-market candidate | One local high-frequency rail creates incremental frequency or scenario before a selective second rail | **P2 Gate**; if failed, return to P1 |
| Phase 3 — Everyday Money Account | A1 Money Account-first as an earned target account role | Recurring inflow/receive plus Receive/Hold/Send/Spend and primary-account behavior | **P3 Gate**; if failed, remain A3 multi-rail spend account |

## Phase 1 — One Money Relationship

### Business Goal

**Decision / Goal.** Validate whether AIX can create a relationship in which funds are retained and purchasing power is used repeatedly. Phase 1 does not attempt to prove account feature completeness.

### User Relationship

**Proposal.** A user keeps stablecoin-linked funds available in AIX and returns to use the relationship for real-world purchasing power across repeated occasions, rather than treating AIX as a one-off spend endpoint.

### Product Form

**Proposal.** A focused one-money relationship, deliberately narrower than a complete account. The initial form may remain a Spend Feature while the J2 purchasing-power use case is tested.

### Core Capabilities

**Capability scope.** Retain funds and make the existing purchasing-power capability useful enough to observe repeat use. The scope is a relationship-validation capability set, not a list of account features.

### Key Hypothesis

**Inference / Hypothesis.** If users retain funds in AIX and return for repeat purchasing-power use, AIX has a relationship beyond one-off card consumption and has a basis for testing broader everyday spend.

### Exit Gate

**P1 Gate.** Proceed only when evidence shows both:

- funds are retained alongside an active-relationship signal (repeat active use, renewed inflow, or actual spend); and
- users return for repeat purchasing-power use.

The gate is behavioral and relationship-based. It is not a completeness checklist for an account. Balance persistence alone may be trapped balance while Send/Withdraw runtime is unconfirmed; it does not constitute evidence that the P1 Gate has passed.

### Kill

**Kill rule.** If there is no funds retention or no repeat use, **Stay Spend Feature / J2**. Do not proceed to Phase 2 scale-up.

## Phase 2 — Multi-rail Everyday Spend

### Business Goal

**Decision / Goal.** After the P1 Gate is met, validate whether an everyday-spend relationship becomes stronger when one local high-frequency rail adds purchasing occasions or scenarios beyond the existing rail mix.

### User Relationship

**Proposal.** A user uses AIX for recurring everyday purchasing power across more than one relevant rail, with the local rail adding a reason, occasion, or frequency that card-only use does not provide.

### Product Form

**Decision / Proposal.** Phase 2 is the A3 **Stablecoin Multi-rail Account** form, entered through the A6 GTM wedge. PH may be investigated as the best-supported proof-market candidate, but discovery does not make PH a proven or exclusive market.

### Core Capabilities

**Capability scope.** Connect the purchasing-power relationship to one validated local high-frequency rail while preserving the existing spend rail. Add a second rail selectively only when evidence shows it is complementary. Card remains a rail among others, not the positioning.

### Key Hypothesis

**Inference / Hypothesis.** A local high-frequency rail can create incremental usage frequency or a new purchasing scenario, and a selective multi-rail relationship can deepen the value of retained funds.

### Exit Gate

**P2 Gate.** Scale Phase 2 only after the P1 Gate is accepted and evidence shows:

- one local high-frequency rail adds incremental frequency or a new scenario; and
- partner, compliance, and economics conditions support the rail relationship.

A second rail requires its own evidence of selective strategic fit. PH discovery may run before this gate, but PH scale-up remains conditional.

### Kill

**Kill rule.** If the local rail produces no increment, or economics, compliance, or partner conditions do not hold, **do not expand multi-rail**. Return to P1 and continue validating the one-money relationship.

## Phase 3 — Everyday Money Account

### Business Goal

**Decision / Goal.** Validate whether AIX can become part of users' recurring money flow and earn the A1 Money Account-first role through observed behavior.

### User Relationship

**Proposal.** Users receive recurring inflows into AIX, hold funds there, send and spend from the relationship, and treat it as a primary account for relevant money needs.

### Product Form

**Conditional target.** A1 **Money Account-first** is earned only if real behavior supports the account role. Until then, the product remains an A3 multi-rail spend account; the target must not be presented as proven.

### Core Capabilities

**Capability scope.** Validate the relationship-level bundle of **recurring inflow/receive + Receive + Hold + Send + Spend**, together with evidence of primary-account behavior. Availability of an individual capability is not sufficient to earn A1.

### Key Hypothesis

**Inference / Hypothesis.** Users with recurring money needs will direct recurring inflows to AIX and rely on it as a primary account when the relationship lets them receive, hold, send, and spend stablecoin-linked value in everyday contexts.

### Exit Gate

**P3 Gate.** Earn the A1 role only when evidence shows:

- recurring inflow/receive behavior; and
- primary-account behavior across the Receive/Hold/Send/Spend relationship.

The gate is based on real usage and relationship depth, not on the existence of an account-shaped product surface.

### Kill

**Kill rule.** If recurring inflow or primary-account behavior does not emerge, **do not upgrade to A1**. Remain an **A3 multi-rail spend account**.

## Execution Model

**Decision: Gate Serial, Discovery Parallel.**

| Work mode | Formal rule | v1 application |
|---|---|---|
| Gate serial | Scale the next phase only after the prior gate is met | P1 before P2 scale-up; P2 before P3 scale-up |
| Discovery parallel | Research may start before the gate it informs | P2 PH market/partner/compliance/economics discovery may run during P1; P3 J1 recurring-inflow demand research may start now |
| Scale discipline | Discovery does not equal commitment | Do not pre-build or scale the next stage before the previous gate is accepted |

This operating model separates learning speed from scale sequencing: discovery is parallel, while stage expansion is serial.

## Now / Parallel Discovery / Defer

### Now

- **P1 validation:** Test funds retained and repeat purchasing-power relationship.
- **J1 demand research:** Begin recurring-inflow demand research now as discovery for Phase 3; its results must not be written as proven demand before validation.
- **Baseline discipline:** Keep the current capability overlay separate from the target proposal and from market conclusions.

### Parallel Discovery

- **PH:** Continue market, partner, compliance, and economics discovery while P1 is running. PH remains a candidate only.
- **Local rail:** Identify and validate one local high-frequency rail that could add incremental frequency or a new scenario; do not commit to a broad rail portfolio.
- **P3 prerequisites:** Explore recurring-inflow use cases, primary-account jobs, and the conditions under which Receive/Hold/Send/Spend would be used together.

### Defer

- J3 collateral credit;
- self-custody;
- broad volatile crypto expansion;
- multi-region replication;
- complete multi-rail breadth.

These are deliberately deferred options, not hidden Phase 1–3 requirements.

## Strategic Metrics

**Decision.** v1 defines metric categories and evidence types only. It introduces no numerical thresholds.

| Validation layer | Metric categories |
|---|---|
| P1 relationship | Funds retained alongside repeat active use, renewed inflow, or actual spend; return/recurrence behavior; continuity of the money relationship |
| P2 rail and market | Incremental frequency, incremental scenarios, local-rail use, complementarity with existing spend, partner readiness, economics, compliance viability |
| P3 account role | Recurring inflow, Receive/Hold/Send/Spend relationship, primary-account behavior, relationship depth and continued reliance |
| Cross-phase | User retention, purchasing-power usefulness, failure reasons, evidence strength, and cost or constraint signals |

No metric category should be converted into a fabricated numerical gate in v1.

## Unknown / Risks

| Item | Classification | Boundary |
|---|---|---|
| Whether J1 is a sufficiently large or urgent primary job | **Unknown / target hypothesis** | J1 primary is a strategic choice to validate, not a proven market fact |
| Whether retained funds reflect an active money relationship rather than trapped balance | **Unknown** | With Send/Withdraw runtime unconfirmed, assess retained funds alongside repeat active use, renewed inflow, or actual spend; balance persistence alone is insufficient evidence for P1 |
| Whether PH is the right proof market in practice | **Unknown / candidate** | Current evidence supports PH as best-supported candidate only; it is not a confirmed blue ocean or global optimum |
| Which local rail adds real increment | **Unknown** | Rail selection follows observed frequency or scenario contribution |
| Partner, compliance, and economics viability | **Unknown** | These are P2 gate conditions, not assumed enablers |
| Whether recurring inflow and primary-account behavior will emerge | **Unknown** | Without both, A1 is not earned |
| Current missing runtime capabilities | **Fact / execution risk** | Send, outbound Crypto Withdraw, Fiat bank/e-wallet cashout, and Unified funding/balance currently have no runtime confirmation; the roadmap stays at capability level |
| A6, A3, and A1 collapsing into parallel strategies | **Decision risk** | Preserve the staged path and gate order |
| Stablecoin-primary drifting into fiat-native neobank or broad volatile-crypto positioning | **Decision risk** | Keep the market boundary and target proposal explicit; defer broad volatile crypto |

**Final boundary.** This roadmap formalizes a testable strategic sequence. It does not claim that the target, J1 primary, PH proof market, or A1 account role is already proven, and it does not authorize a feature list or implementation plan.
