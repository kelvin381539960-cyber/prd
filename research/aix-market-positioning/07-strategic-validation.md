# AIX Strategic Validation v1

> Date: 2026-08-30
> Scope: Business Strategy / Product Strategy / Strategic Roadmap Validation
> Roadmap: Current → Phase 1 One Money Relationship → Phase 2 Multi-rail Everyday Spend → Phase 3 Everyday Money Account
> Execution: Gate Serial / Discovery Parallel

## Executive Decision

本轮不改变 AIX 战略主线，只收敛并行 Discovery 的优先级。

| Item | Decision | Classification |
|---|---|---|
| Target | Stablecoin-native Everyday Money Account | **Decision / Proposal** |
| J1 Global Money | Primary Job to validate | **Decision / Hypothesis** |
| J2 Crypto → Spend | Secondary Job | **Decision** |
| P1 | **NOT YET VALIDATED / DATA GAP** | **Unknown / Data Gap** |
| P2 first discovery rail | **QR Ph P2M — Priority Discovery Rail** | **Decision under uncertainty** |
| P3/J1 first discovery wedge | **OFW / cross-border remittance — Primary J1 Discovery Wedge** | **Decision under uncertainty** |

**Boundary.** QR Ph P2M is not a committed build. OFW/remittance is not a proven product direction. Roadmap phase order is unchanged.

## P1 Validation Status — One Money Relationship

**Decision: `NOT YET VALIDATED / DATA GAP`.** Current evidence is insufficient to pass or fail the P1 Gate.

### Known facts

**Data Fact.** Current capability baseline:
- Receive / Hold / Swap / Card Spend: confirmed at capability level.
- Wallet / Card: separate.
- Auto Debit: partial runtime confidence only.
- Send / outbound Crypto Withdraw / Fiat bank-e-wallet cashout / Unified funding-balance: no runtime confirmation.

**Data Fact.** AIX Data semantic catalog reports `anchor_status=drift_detected`; the only `review_required_fields` item is `card.card_status`, which is not used in this relationship validation.

**Data Fact.** Current semantic transaction aggregation returned:

| txn_type | count |
|---|---:|
| PURCHASE | 68 |
| TOP_UP | 27 |
| REVERSAL | 63 |
| REVERSAL_TO_ACCOUNT | 4 |
| ACCOUNT_VERIFICATION | 12 |
| CAPTURE | 6 |
| REFUND | 7 |

These counts prove only that these transaction types exist. They do **not** prove same-user repeat Deposit/Receive, repeat Spend, renewed inflow, cross-period active use, or a One Money Relationship.

**Data Fact.** UDP metadata located:
- `c_aix_com_aix_x.x_dwd_aix_trx_crypto_deposit_completed_di` — crypto Deposit completed transaction fact.
- `x_dwd_aix_trx_card_transaction_auth_approval_di` — card Auth approval transaction fact.

`udp_get_physical_table_detail` was unavailable upstream. A custom Archery query attempt was blocked by `Instance does not exist`. Therefore the anonymous cohort analysis needed for P1 could not be completed in this run.

### Required evidence

**Decision.** Next P1 evidence must examine anonymous cohort behavior across:
- repeat Deposit / Receive;
- repeat Spend;
- renewed inflow;
- cross-period active use.

Because Send/Withdraw runtime is not confirmed, **balance persistence alone is not retention evidence**. Retained funds must be interpreted together with voluntary active behavior such as repeat use, renewed inflow, or actual spend.

No numerical Gate threshold is set in this version.

## P2 Priority Discovery Rail — QR Ph P2M

### Why it is first

**Market Fact.** BSP 2025 payment data:
- QR Ph P2M Jan–Dec volume: **2.5B**;
- QR Ph P2M Jan–Dec value: **PHP 1.2T**;
- Dec 2025 volume: **431.2M**;
- Dec 2025 value: **PHP 179.4B**;
- registered Merchant IDs at 31 Dec 2025: **2,289,106**, not a unique-merchant count;
- participant account penetration: **78%**;
- InstaPay QR Jan–Dec 2025 volume: **183.3M**;
- InstaPay QR Jan–Dec 2025 value: **PHP 926.1B**.

**Market Fact.** Coins.ph launched QRPH Stablecoin Payments in April 2026. Users can scan QRPH and pay using PHP, USDT, USDC/other supported crypto, or a combination without a separate manual sell-to-PHP step. Coins.ph describes itself as the first Philippine e-wallet with this integration and cites nearly 700,000 merchants; those are **competitor claims**, not BSP market totals.

### Strategic decision

**Decision.** Promote **QR Ph P2M** to `Priority Discovery Rail` for Phase 2. The purpose is to test whether it creates **incremental frequency or a new purchasing scenario** beyond Card. This does not authorize a build.

**Decision.** InstaPay and other local rails remain second-wave discovery. AIX should not expand rails to maximize rail count.

### Boundaries / disconfirmers

QR Ph should not proceed to scale if it adds no incremental frequency/scenario, or if partner, economics, compliance or regulatory conditions are not viable.

**Market Fact.** BSP continued the moratorium on new VASP licenses from 1 September 2025, and its active VASP list includes players such as Coins.ph, Maya and PDAX. This establishes a meaningful regulated-access constraint around crypto-asset activity in PH.

**Unknown.** This does **not** establish that a specific future AIX model necessarily requires a new VASP license. That depends on the eventual operating model and requires separate fact-checking.

**Boundary.** Coins.ph already proves stablecoin→QRPh is live. QR Ph itself is therefore **not** a white space or moat.

## P3 / J1 Discovery Wedge — OFW / Cross-border Remittance

### Why it moves first

**Market Fact.** BSP reported:
- 2025 personal remittances: **USD 39.619B**;
- 2025 cash remittances through the banking system: **USD 35.634B**;
- 2026 Jan–Jun cash remittances: **USD 17.149B**;
- 2025 Jan–Jun cash remittances: **USD 16.753B**.

This is a large, recurring, cross-border money flow aligned with the J1 Global Money problem space.

**Market Fact.** World Bank Remittance Prices Worldwide reported a global average remittance cost of **6.36%** in the Q3/Sep-2025 context. The Malaysia→Philippines corridor contains both low-cost digital operators and higher-cost traditional options.

**Boundary.** This supports that remittance friction exists and varies by corridor/provider. It does **not** prove that stablecoin is necessarily cheaper.

### Strategic decision

**Decision.** Promote **OFW / cross-border remittance** to `Primary J1 Discovery Wedge`. It becomes the first J1 use case to research deeply for recurring inflow and primary-account behavior. This does not mean the market has already proven AIX should build a remittance product.

**Decision.** Payroll and freelancer invoice remain secondary J1 research tracks.

**Market Fact.** PSA reported 2025 Philippine digital-economy employment of **10.39M**, or **21.2%** of total employment, and Dec-2025 wage/salary workers at **64.2%** of the workforce.

**Boundary.** These figures establish a large wage/payroll population. They do not demonstrate demand for stablecoin payroll, so Payroll does not outrank remittance in the current discovery order.

### Disconfirmers

Remittance should lose priority if target users do not want recurring inflows to land in/remain in AIX, still need immediate cashout, existing digital remittance options remove the pain, or economics/partner/regulatory access makes the proposition unattractive.

## Roadmap Update

The Roadmap does **not** change stage order.

```text
Current
  ↓
Phase 1 — One Money Relationship
  Gate status: NOT YET VALIDATED / DATA GAP
  ↓
Phase 2 — Multi-rail Everyday Spend
  Parallel discovery priority: QR Ph P2M
  ↓
Phase 3 — Everyday Money Account
  Parallel J1 discovery priority: OFW / cross-border remittance
```

**Decision.** Keep `Gate Serial / Discovery Parallel`:
- P2 QR Ph discovery can continue while P1 evidence is completed, but P2 scale does not start before P1 Gate acceptance.
- P3/J1 remittance research can start now, but A1 is not earned before recurring inflow plus Receive/Hold/Send/Spend plus primary-account behavior are observed.

## Kill / Disconfirmers

| Strategic line | What would disconfirm it |
|---|---|
| P1 One Money Relationship | After sufficient cohort coverage and observation, evidence shows no voluntary repeat relationship behavior; apparent retention is explainable by trapped balance or one-off use. Insufficient evidence remains DATA GAP, not a negative result. |
| P2 QR Ph priority | No incremental frequency/scenario, or partner/economics/compliance conditions fail. |
| P3 Remittance discovery | Users do not route/retain recurring inflow in AIX, current alternatives remove the pain, or economics/partner/regulatory access fails. |

No fabricated numerical kill threshold is introduced in v1.

## Evidence Gaps

**Unknown / Data Gap.** P1 anonymous cohort evidence is still missing because the current data path did not expose the required user-linked aggregate query.

**Unknown.** QR Ph incremental value for AIX users, AIX-specific partner access, economics and exact regulatory model are unproven.

**Unknown.** OFW/remittance user willingness to receive into AIX, retain value, continue spending/sending from AIX, and switch from existing providers is unproven.

**Unknown.** Stablecoin payroll and freelancer-invoice demand remain insufficiently evidenced.

## Next Strategic Work

1. Close the P1 anonymous cohort data gap; do not substitute balance persistence for active retention.
2. Run QR Ph P2M discovery around incremental user scenario/frequency, partner access, economics and compliance feasibility.
3. Run OFW/cross-border remittance J1 discovery around recurring-inflow Jobs, current alternatives, pain, trust and willingness to keep/use funds in AIX.
4. Keep Payroll and freelancer invoice as secondary research tracks until direct demand evidence improves.

**Final boundary.** This document prioritizes what AIX should validate next. It does not define pages, UI, fields, APIs, state machines, PRD requirements, or technical implementation.
