# Stage14 Deep Dive B — Country signals

> **Archive status:** Controller-verified evidence materialization; bounded package only.
>
> **Evidence class:** Macro, network-activity, provider co-location, and public financial-inclusion context. These are prioritization signals, not country-level stablecoin adoption or retention proof.

## Question and scope

This deep dive records why Argentina, Colombia, Türkiye, Vietnam, Cameroon, and Tajikistan remain plausible strategy-level country contexts for further validation. It keeps four evidence classes separate:

1. IMF consumer-price inflation as structural macro pressure.
2. Chainalysis transaction and exchange activity as market activity.
3. Deel’s reported stablecoin contractor ranking as provider co-location.
4. World Bank Global Findex variables as financial-inclusion and digital-payment context.

The machine-readable companion is [14-country-signals-data.csv](data/14-country-signals-data.csv). The official World Bank CSV and glossary, plus the official IMF API response, are archived under [source-files/14](source-files/14/). The Findex labels were verified against the glossary before retaining the supplied values: `account.t.d`, `mobileaccount.t.d`, `save.any.t.d`, `g20.received`, `g20.made`, and `g20.any`.

## Evidence ledger

### Structural macro pressure — IMF

The archived annual consumer-price inflation values are:

| Country | 2024 | 2025 | 2026 |
|---|---:|---:|---:|
| Argentina | 219.9 | 41.9 | 30.4 |
| Türkiye | 58.5 | 34.9 | 28.6 |
| Colombia | 6.6 | 5.1 | 5.9 |
| Vietnam | 3.6 | 3.3 | 4.9 |
| Cameroon | 4.5 | 3.4 | 3.5 |
| Tajikistan | 3.5 | 3.4 | 4.0 |

These values can support structural currency-value and purchasing-power pressure hypotheses. They cannot establish stablecoin use, willingness, balance holding, or user-level retention. The 2026 API values are preserved as returned; this archive does not reclassify their vintage or status.

### Network activity — Chainalysis

- LATAM recorded nearly $1.5T of crypto volume from July 2022 to June 2025, with Argentina receiving $93.9B in the reported network measure.
- Stablecoin purchases represented more than half of exchange purchases denominated in COP, ARS, and BRL from July 2024 to June 2025 in the cited order-book dataset.
- The 2024 comparison reports Argentina at 61.8% and Brazil at 59.8% stablecoin transaction share versus a 44.7% global average.

These are transaction or order-book activity measures. The order-book dataset is not comprehensive of all centralized-exchange activity, and none of these figures is a people count or retained-balance measure.

### Provider co-location — Deel

The reported stablecoin contractor-adoption ranking includes Argentina, Cameroon, South Korea, Türkiye, Vietnam, and Tajikistan. The list is useful as a directional co-location signal with contractor activity. It has no country-level denominator in the supplied package and does not show that the same users also hold or spend a stablecoin balance.

### Financial-inclusion context — World Bank Global Findex 2025

The archive retains the supplied 2024 all-adult country rows for adult population, account access, mobile-money account use, saving any money, and the three G20 digital-payment indicators. The glossary definitions establish these as age-15-plus financial-inclusion or digital-payment variables. They do not measure stablecoins, contractor status, remittance purpose, or retained digital-dollar balances.

The Findex values are stored as proportions from 0 to 1, with a mechanically derived percentage column for readability. Adult population is stored as the `pop_adult` count. The country labels follow the controller package while preserving official country codes; the downloaded source uses `Turkiye` and `Viet Nam` as row names.

## Interpretation boundary

Country signals can support a sequence of validation hypotheses: macro pressure may create value-protection motivation; network activity may indicate an active crypto market; provider co-location may indicate worker-related presence; and financial inclusion may affect rail accessibility. These signals are not interchangeable and must not be multiplied into a country TAM or used as a proxy for same-user behavior.

## Decision impact

Use the six countries as a bounded country-validation set, with different reasons for inclusion rather than a single “best market” score. Prioritize country-specific validation of worker payout, remittance, and hold/spend jobs. Keep macro, network, provider, and Findex values as separate evidence classes in strategy materials.

## What remains Unknown

- Country-level stablecoin adoption and user counts for the target worker or remittance populations.
- Whether the reported contractor activity and macro pressure occur in the same people.
- Whether stablecoin value is held, spent, cashed out, or merely traded.
- Country-specific legal, payout, FX, card, and competitive constraints.
- Reachable AIX population, acquisition economics, and repeat-cycle behavior.

## Disconfirming evidence

- High inflation can coexist with low stablecoin use or with use concentrated in trading rather than money storage.
- Chainalysis transaction share can rise because of a small number of high-volume actors and does not identify people.
- Deel ranking membership has no public denominator and may reflect provider mix rather than national prevalence.
- Findex account, saving, and digital-payment indicators are not stablecoin indicators and cannot be used as substitutes for them.

## Recommended validation evidence

At strategy level, run country-stratified research that links the same target person’s income or remittance receipt, stablecoin exposure, holding duration, spend/cash-out outcome, and repeat cycle. Require country-specific denominators and competitor/rail comparisons before promoting any country from a directional hypothesis to a target-market decision.
