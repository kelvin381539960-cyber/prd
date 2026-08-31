# Stage15 WS6 — Competitor / Red-Team & Defensibility Register

> **Status:** `WS6 bounded package complete; included in Stage15 final Sol/high CLEAN PASS; normalized route validation remains unresolved`.
> **Date:** 2026-08-31
> **Purpose:** Attack H1 and H2 with the strongest realistic incumbent, local-wallet, and combined-status-quo alternatives. This workstream is not an AIX advantage search.
> **Evidence boundary:** Prior publicly sourced Stage14 evidence and reviewed competitor/rail cards are re-recorded against the Stage15 cell rules. No AIX internal data, vendor selection, implementation design, or launch-market decision is used.

## 1. Scope check

| Question | WS6 answer |
|---|---|
| Strategic question | Do incumbents or local wallets already close the H1/H2 outcome, and is any remaining difference independent of a simple rail/feature bundle? |
| Capabilities under attack | H1: repeated digital-dollar continuity into country-specific everyday purchasing power. H2: destination-side receive → retain/manage → local reuse. |
| Level | Strategy + Capability. The analysis compares outcome coverage, relationship depth, and defensibility. |
| Explicitly outside scope | Pages, UX, fields, APIs, state machines, implementation, vendors/partners, owners, commercial terms, regulatory operating models, launch selection, and any AIX capability recommendation. |

## 2. Red-team method

The attacker treats the user's **combined current alternative stack** as the competitor, not a single branded product. The attack sequence is:

1. **Outcome closure:** Can the alternative already produce the same local purchasing-power or destination-money outcome?
2. **Starting-money match:** Is the comparison actually about a digital-dollar/stablecoin starting balance, or only a fiat substitute?
3. **Relationship-depth match:** Is there evidence of repeated hold/retain/reuse, or only one-off spend, conversion, payout, or cash-out?
4. **Fast-follow test:** If the claimed difference is card, QR, e-wallet, auto-convert, cashback, or multi-rail breadth, can an incumbent or local wallet supply the same outcome without owning a new relationship?

The status rule is deliberately asymmetric:

- `Disconfirming / falsifier triggered` is used only when the market evidence directly shows that the proposed bundle already exists **inside a locked country + cohort + outcome cell**. The current package meets that bar for the PH H1 rail-only expression.
- `Competitive disconfirmation / NOT_YET_PASS` records strong incumbent or alternative pressure when the bundle is already available but the record does not lock one matched country + cohort + outcome cell. The current H2 transport-only attack remains in this class.
- The normalized H1/H2 core remains `Insufficient` unless the same country + cohort + outcome cell contains user behavior, residual pain, and relationship-depth evidence.
- Missing country eligibility, cohort linkage, user behavior, or retention data is not relabeled as a falsifier.

## 3. Strongest alternative stack

| Alternative stack | Outcome it already pressures | Attack on H1 | Attack on H2 | Boundary |
|---|---|---|---|---|
| **KAST global money account** | Receive salary/invoices or transfers, hold digital dollars, send, and spend from a unified account; the broad digital-dollar money-account proposition is already occupied. [S15-RT-01] | Attacks any broad `hold digitally → spend locally` claim. | Attacks a generic receive → hold → spend relationship where KAST is available. | KAST country-level PH eligibility is Unknown; provider proposition and scale are not retention or same-cohort proof. |
| **RedotPay / Bitget / ether.fi / Oobit** | PH stablecoin-starting card/direct-spend outcomes already have multiple current samples. [S15-RT-02] | Directly attacks card, auto-convert, self-custody spend, acceptance, and cashback as differentiation. | Attacks a receive-and-spend or transport utility that never demonstrates retained value. | Product overlap is strong for spend; repeated hold-until-use and destination retention are not observed. |
| **Coins.ph** | PH local e-wallet, QRPh direct stablecoin/crypto payment, and cash-out / bank / remittance routes. [S15-RT-03] | The local purchasing-power endpoint is not empty; Coins.ph combines local network access with a direct at-merchant path. | Recipient can use or cash out locally without a new digital-dollar relationship. | The source does not prove user frequency, retained balances, or a unified stablecoin money account. |
| **GCash / Maya / Bitrefill bridge** | Crypto can be converted to PHP wallet value, then used for QR, bills, load, or vouchers; Maya also documents crypto-to-cash. [S15-RT-04] | A two-step local-wallet path may be sufficient even if it is not direct stablecoin spend. | A recipient seeking local liquidity may prefer a familiar wallet or voucher rather than retain digital dollars. | Direct and two-step mechanisms remain separate; direct stablecoin QR for GCash/Maya is not claimed. |
| **Wise and conventional fiat rails** | Mature cross-border receive/hold/spend, local settlement, and speed. [S15-RT-06] | If users accept conversion to fiat, local purchasing power is already well served. | Strong substitute for transport and immediate destination liquidity. | Different starting money; this is a conditional substitute, not proof that stablecoin continuity is unnecessary. |
| **Deel / Stripe / Remote** | Upstream global-income distribution and, in Deel's case, a stablecoin wallet that moves toward hold/spend. [S15-RT-07] | Compresses the post-payout gap and may own the user's income relationship. | Attacks receipt/distribution as a wedge; destination retention remains unmeasured. | Upstream or provider-reported evidence is context-only for destination-side retention. |
| **Combined status quo** | A user can combine a payout provider, a stablecoin wallet/card, and a local wallet or cash-out rail. | A new rail may add convenience without creating an independent relationship. | Immediate cash-out plus local wallet may solve the actual recipient job. | Same-user overlap, primary-vs-secondary use, and repeat behavior remain Unknown. |

## 4. Candidate-specific red-team register

The cells below are the minimum Stage15 unit. `PH hard-baseline` is used only as a country context; it does not select the H2 diagnostic market or a launch market.

| ID | Candidate cell | Red-team attack | Strongest alternative(s) | Evidence status | Gate impact / interpretation |
|---|---|---|---|---|---|
| **RT-H1-01** | H1 × PH × stablecoin-starting users seeking everyday local purchasing power × J5 | A card or direct-spend bundle is already available: stablecoin deposit/top-up, auto-convert or direct deduction, and real-world acceptance are not new. | RedotPay, Bitget, ether.fi Direct Pay, Oobit; Coins.ph QRPh. [S15-RT-02][S15-RT-03] | **Disconfirming / falsifier triggered — H1-as-rail-bundle only** | DR-3 cannot pass from rail count, card access, or conversion convenience. This falsifies the rail-only expression, not the deeper H1 continuity/depth hypothesis. |
| **RT-H1-02** | H1 × PH × stablecoin-starting users seeking everyday local purchasing power × J5 | The local outcome may already be closed by a native wallet and the dominant merchant rail; a new overlay could be redundant even if its mechanism is different. | Coins.ph; GCash; Maya; BSP QRPh ecosystem. [S15-RT-03][S15-RT-04][S15-RT-05] | **Insufficient** | Strong DR-2 pressure, but no linked same-cohort user evidence, frequency/value, switching reason, or proof that users reject the existing local stack. H1 core remains NOT_YET_PASS rather than falsified. |
| **RT-H1-03** | H1 × PH or other eligible market × digital-dollar holders/receivers × J5 | A broad `receive/hold/spend digital dollars` account may already supply continuity; the proposed country-depth gap could be a coverage/eligibility gap, not a user-outcome gap. | KAST; Oobit; relevant local-wallet stack. [S15-RT-01][S15-RT-02] | **Insufficient** | KAST PH eligibility and same-cohort behavior are not established. No DR-2/DR-5 conclusion can be drawn from provider proposition alone. |
| **RT-H1-04** | H1 × context-only × digital-dollar holders who may accept fiat conversion × J5 | A user may simply use a mature fiat cross-border product after conversion; continuity may be a preference with no value large enough to sustain a separate relationship. | Wise; local bank/e-wallet; combined status quo. [S15-RT-06] | **Insufficient / context-only** | Starting money does not match cleanly and there is no same-cell hold-until-use behavior. This is a valid falsifier to test, not a current H1 kill. |
| **RT-H2-01** | H2 × PH hard-baseline × destination-side cross-border recipients with digital-dollar receipt × J6 | If the destination job is local liquidity, local wallets, QR, bills, bank transfer, and cash-out already solve it; retaining digital dollars may be unnecessary. | Coins.ph; GCash; Maya; conventional remittance/local cash-out. [S15-RT-03][S15-RT-04][S15-RT-05] | **Insufficient** | Strong attack on H2's assumed recipient preference, but no recipient-level denominator, retention duration, or repeat-use observation is present. DR-2 and DR-5 remain NOT_YET_PASS. |
| **RT-H2-02** | H2 × PH hard-baseline × remittance recipients × J6 | A transport/payout provider can deliver local currency quickly; a stablecoin layer may be invisible and create no retained relationship. | Wise; fiat remittance; Deel/Stripe/Remote where upstream/context-only; local wallet. [S15-RT-06][S15-RT-07][S15-RT-08] | **Insufficient** | Existing sources show category and alternative pressure, but sender-side adoption is not recipient-side retention. No H2 falsifier is claimed without same-cell recipient evidence. |
| **RT-H2-03** | H2 × context-only × recipients who might want to hold digital dollars × J6 | KAST and crypto wallets already describe receive/hold/send/spend; a new destination account may be a duplicated relationship rather than an unmet one. | KAST; RedotPay; Coins.ph; relevant local wallets. [S15-RT-01][S15-RT-02][S15-RT-03] | **Insufficient / context-only** | Country eligibility, same-cohort linkage, and repeated retention are missing. The attack blocks promotion; it does not turn missing evidence into a kill. |
| **RT-H2-04** | H2 × PH or other eligible market × recipients × J6 | If H2 is reduced to `receive → convert/cash out → spend`, existing rails already provide it and the bundle is easy to reproduce or source locally. | Coins.ph; GCash/Maya; remittance and bank/e-wallet rails; crypto cards. [S15-RT-02][S15-RT-03][S15-RT-04] | **Competitive disconfirmation / NOT_YET_PASS — H2-as-transport/rail-bundle only** | Strong alternative coverage is recorded, but this record is not one locked country + cohort + outcome cell; it does not produce `FALSIFIED_IN_CELL`. The normalized H2 retained/manage/reuse claim remains NOT_YET_PASS because behavior is not measured. |
| **RT-H0-01** | H0 × the same PH or future matched market cell × same cohort/outcome | The user's combined incumbent/local-wallet stack may already be good enough, leaving no reason to switch or use a second relationship. | Full alternative stack above. | **Insufficient** | H0 has high red-team pressure but is not formally selected: same-cell satisfaction, residual pain, and switching/parallel-use evidence are absent. |

## 5. Defensibility verdict

| Claimed difference | Red-team result | Defensibility reading |
|---|---|---|
| Stablecoin top-up / deposit | Already supplied by several wallets and cards. | **Low** as a standalone differentiator. |
| Auto-convert or direct deduction at payment | Already commercialized by custodial and self-custody alternatives. | **Low**; mechanism is an entry condition, not a moat. |
| Card acceptance, virtual/physical card, Apple/Google Pay, cashback | Repeated across the sampled PH spend set and inherited from card networks/issuer relationships. | **Low**; fast-followable or network-provided. |
| Card + QR + bank/e-wallet + voucher breadth | Local incumbents already own the destination networks; a bundle can be assembled by multiple players. | **Low as an independent moat**. Integration effort may be real, but it is not a proven user relationship. |
| Local merchant network, license, settlement, and trusted wallet distribution | Strong structural position for the incumbent that owns the network. | **Potentially high for incumbents**, but not portable evidence for a new overlay and not a route decision. |
| Unified receive/hold/send/spend account | KAST already occupies the broad proposition; a unified balance can create switching cost if it becomes primary. | **Medium-high structural potential**, not unique and not proven in a matched target cohort. |
| Repeated digital-dollar hold-until-use / destination retention and reuse | This is the only part not closed by a feature list, but no same-cell evidence currently demonstrates it. | **Potentially defensible, currently unproven**. It is the required hypothesis, not a declared moat. |
| Payout or remittance corridor ownership | Deel/Stripe/Remote and conventional remittance providers already have distribution relationships. | **Incumbent advantage**; upstream distribution is not an open differentiation by default. |
| Price, spread, fee waiver, or cashback | Can be matched and subsidized. | **Low** and unsuitable as the sole route defense. |

### Fast-follow conclusion

The attack succeeds against any positioning whose substance is:

> `stablecoin balance + card/QR/e-wallet rails + auto-convert + local cash-out`.

That is already a market pattern, and its components can be supplied by incumbents, local wallets, or a combined user stack. It is not a defensible route merely because the components are assembled in one product.

The attack does **not yet prove** that every target user has no residual need for repeated digital-dollar continuity or destination-side retention. It shows that this is the only unresolved relationship-level question; current evidence cannot answer it.

## 6. WS6 impact on candidates and gates

| Item | WS6 result | Status after WS6 |
|---|---|---|
| H1 rail-only expression | Falsified by existing PH spend/direct-payment coverage. | Do not promote or repackage as a new route. |
| H1 normalized route | Competitor coverage creates strong DR-2/DR-3 pressure; same-cell continuity, residual pain, and repeat depth are not observed. | `Leading Discovery Candidate / NOT_YET_PASS`; no promotion. |
| H2 transport/rail-only expression | Strong competitive disconfirmation from local-wallet, cash-out, and remittance alternatives, but `RT-H2-04` is not one locked country + cohort + outcome cell. | `Competitive disconfirmation / NOT_YET_PASS`; no cell-level falsifier or promotion. |
| H2 normalized route | Recipient retention/manage/reuse is unobserved; existing alternatives may be sufficient, but the same-cell falsifier is not yet recorded. | `Secondary Candidate / NOT_YET_PASS`; no promotion. |
| H0 | The combined status quo is a credible attacker and may win in a matched cell. | Not formally selected because same-cell behavior and sufficiency evidence are missing. |
| DR-1 / DR-4 | Not adjudicated by WS6. | Remain `NOT_YET_PASS`. |
| DR-2 / DR-3 / DR-5 | WS6 blocks any PASS based on rail breadth; no normalized-candidate PASS evidence exists. | Remain `NOT_YET_PASS`; the PH H1 rail-only falsifier and H2 transport-only competitive disconfirmation are recorded above. |
| Stage15 state | WS6 bounded public-evidence workstream complete and included in final review. | `Stage15 research package = Completed`; `Primary = NOT_YET_SELECTED`; normalized H1/H2 remain `NOT_YET_PASS`. |

## 7. What would be required to overturn the attack

Only a same-country + same-cohort + same-outcome validation can reopen the normalized H1/H2 claims. It would need to show, at Strategy + Capability level:

- repeated digital-dollar → local-use continuity for H1, or repeated receive → retain/manage → local reuse for H2;
- a material residual pain after the full incumbent/local-wallet stack is considered;
- a reason to switch or use the relationship in parallel; and
- evidence that the relationship depth is not explained by simply adding another rail.

If the matched cell instead shows immediate cash-out, one-off spend, transport-only behavior, or adequate incumbent/local-wallet coverage with no residual pain, the registered falsifier should be triggered and H0 / no Primary selected. Until that evidence exists, the correct state is `NOT_YET_PASS`, not a forced H0 win.

No further generic feature/rail inventory is warranted for WS6. Downstream vendor, partner, implementation, UX, or launch-market work remains out of scope.

## 8. Source mapping

| Stage15 source ID | Source basis | Reused reviewed evidence |
|---|---|---|
| **S15-RT-01** | KAST global money-account proposition: receive, hold, send, spend, unified balance; PH eligibility remains Unknown. | `evidence/04-agent-a-j1-global-money-card.md`; `evidence/14-deep-d-market-alternatives.md` |
| **S15-RT-02** | RedotPay plus Bitget, ether.fi Direct Pay, and Oobit PH spend/direct-rail pressure. | `evidence/03-agent-a-redotpay-kast.md`; `evidence/03-agent-b-custodial-cards.md`; `evidence/04-agent-c-self-custody-wallet-native-evidence-card.md`; `evidence/05-agent-c-white-space-defensibility.md` |
| **S15-RT-03** | Coins.ph QRPh stablecoin payment, local e-wallet, and cash-out routes. | `evidence/04-agent-g2-non-card-substitute-rails-evidence-card.md`; `evidence/14-sources.md` |
| **S15-RT-04** | GCash/Maya two-step conversion and Bitrefill voucher bridge; direct vs two-step kept separate. | `evidence/04-agent-g2-non-card-substitute-rails-evidence-card.md` |
| **S15-RT-05** | BSP QRPh / PH digital-payment network context; no crypto-specific volume inference. | `evidence/04-agent-g2-non-card-substitute-rails-evidence-card.md`; `evidence/14-sources.md` |
| **S15-RT-06** | Wise mature fiat cross-border alternative. | `evidence/14-deep-d-market-alternatives.md`; `evidence/14-sources.md` |
| **S15-RT-07** | Deel, Stripe, and Remote payout/distribution and post-receipt wallet pressure. | `evidence/14-deep-a-worker-overlap.md`; `evidence/14-deep-d-market-alternatives.md`; `evidence/14-sources.md` |
| **S15-RT-08** | World Bank / bounded academic remittance evidence and recipient-form limitation. | `evidence/14-deep-c-remittance.md`; `evidence/14-sources.md` |

## 9. WS6 conclusion

The strongest real-world attack **provides strong competitive disconfirmation against the proposed rails**: card, QR, e-wallet, auto-convert, cash-out, and multi-rail breadth are already solved or readily assembled by incumbents and local wallets. They cannot be used as H1/H2 differentiation.

The attack **does not grant H1 or H2 a positive pass**. It leaves only a narrow, unproven relationship-level question: whether a specific cohort repeatedly retains digital-dollar value and reuses it locally in a way that the combined alternative stack does not adequately serve. H1 and H2 therefore remain `NOT_YET_PASS`; H0 is not declared the winner solely from evidence insufficiency; `Primary strategic route = NOT_YET_SELECTED`; `AIX Right-to-win = Unknown`; and the P1/P2/roadmap state is unchanged. The PH H1 rail-only expression is the only PH rail-level falsifier in this register; H2 transport-only remains `Competitive disconfirmation / NOT_YET_PASS` until a single matched cell is established.
