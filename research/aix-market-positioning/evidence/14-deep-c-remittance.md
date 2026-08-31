# Stage14 Deep Dive C — Remittance rail and retention boundary

> **Archive status:** Controller-verified evidence materialization; bounded package only.
>
> **Evidence class:** Remittance category cost, bounded sender-side academic evidence, and explanatory rail evidence. This is not global stablecoin adoption or recipient-balance retention proof.

## Question and scope

This deep dive tests remittance as an adjacent money movement job and records the boundary between a stablecoin-enabled rail and an end-user stablecoin balance. It does not treat the remittance category value as stablecoin addressable volume, and it does not convert a sender-side study into global adoption.

The machine-readable companion is [14-remittance-data.csv](data/14-remittance-data.csv). Existing public report archives remain under [source-files/14](source-files/14/); the ScienceDirect and Stripe explainer sources remain link-only in the manifest.

## Evidence ledger

### Category cost and scale

- World Bank Remittance Prices Worldwide covers 367 corridors and reports a 6.36% global average cost in the Stage14 package.
- Existing Stage14 evidence records approximately $685B for the LMIC remittance category and approximately $40B for the Philippines category.
- These figures establish the size and friction of a conventional category. They do not establish stablecoin adoption, reachable users, AIX demand, or retention.

### Bounded academic sender evidence

- The peer-reviewed Telematics & Informatics study covers 866 U.S.-based adults engaged in remittance.
- 26% of that bounded sample adopted stablecoins for remittance.
- Continuance is associated with satisfaction and usefulness in the reported study framing.
- This is sender-side, sample-bound evidence. It cannot be generalized to global senders, recipients, or retained balances.

### Stablecoin rail versus recipient money form

The Stripe explainer describes a stablecoin layer that may be visible to the user or hidden behind a fiat-facing experience. A recipient may cash out into local currency, hold the stablecoin for value protection, or spend it. The MoneyGram/Stellar example illustrates a cash-out path. Therefore, stablecoin rail volume is not equivalent to end-user stablecoin adoption or balance retention.

## Interpretation boundary

Remittance is a credible adjacent job because cross-border cost and speed matter, and a stablecoin rail can change settlement mechanics. But the strategic object to validate is the user outcome: whether the sender or recipient intentionally holds or spends stablecoin value, whether that behavior repeats, and whether it is preferable to conventional rails. A transfer that is cashed out immediately should not be counted as retained stablecoin value.

## Decision impact

Keep remittance as a strategy-level use-case hypothesis and a cost benchmark. Do not use the $685B, $40B, 367-corridor, or 26% figures as a stablecoin TAM, global adoption rate, or retention proxy. Any remittance positioning must distinguish rail efficiency from user-held digital-dollar value.

## What remains Unknown

- Whether the sender, recipient, or both are the target user and whether the stablecoin layer is visible.
- Recipient final form: cash-out, hold, or spend, and the duration of any hold.
- Repeat-transfer and cross-cycle behavior for the same users.
- Corridor-level adoption, economics, regulation, and competitive alternatives.
- Whether remittance is the primary money job or only an occasional transfer use case.

## Disconfirming evidence

- The 26% academic result is bounded to 866 U.S.-based remittance-engaged adults and may not represent other corridors or populations.
- A stablecoin-enabled transfer may end in local-currency cash-out, leaving no stablecoin balance to retain.
- Category-size estimates can be large while stablecoin share, target-user reachability, or willingness to switch remains small.
- Continuance drivers such as satisfaction and usefulness are not direct measurements of multi-cycle retention.

## Recommended validation evidence

At strategy level, validate selected corridors with linked sender-and-recipient research that records the rail used, final money form, hold duration, spend/cash-out outcome, repeat transfer behavior, and comparison with incumbent rails. Require a clean denominator before using remittance as a target segment or retained-balance opportunity.
