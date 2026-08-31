# Stage14 Deep Dive A — Worker payout → hold/spend overlap

> **Archive status:** Controller-verified evidence materialization; bounded package only.
>
> **Evidence class:** External worker, contractor, and provider evidence. This is not a same-user longitudinal cohort and is not an AIX market-size estimate.

## Question and scope

This deep dive tests whether global-worker payout evidence is directionally consistent with a job that extends from receiving money into holding or spending dollar value. It does not claim that the same worker is present in every source, that a payout user retains a balance, or that the source populations are additive.

The machine-readable companion is [14-worker-overlap-data.csv](data/14-worker-overlap-data.csv). It records one claim per row, with the available sample or denominator, method, and explicit non-support boundary.

## Evidence ledger

### Stripe worker survey

- The survey covers more than 2,300 independent workers across 20 countries.
- 57% would accept stablecoin payouts if offered. This is willingness, not adoption.
- 18% of independent workers in emerging markets currently receive stablecoin payouts. The denominator is the survey subgroup; the subgroup size is not established in the supplied package.
- In Latin America, one-third say stablecoins could protect against currency volatility. Argentina and Colombia are named examples. This is a hedge-value motivation and is not linked to the 18% current-use subgroup.
- In Sub-Saharan Africa, 72% receive payouts to a digital wallet and 38% say receiving payouts is the primary stablecoin use case. These figures are wallet/use-case context, not a same-user overlap measure.

### Stripe / Remote provider case

- Stablecoin payouts are available in 60+ countries.
- Contractors requested the payout option to hold and spend USD while avoiding local-currency swings and FX fees.
- The operator reports an estimate of 2–3 days faster payout and more than 1% of payout value saved by avoiding FX conversion.
- The named markets include Argentina, Mexico, Colombia, and Ghana.
- This is the strongest same-job directional evidence in the package because payout and hold/spend motive are linked in one provider case. It has no clean user denominator and no longitudinal retained-balance measurement. The correct label is `directional same-job / not longitudinally proven`.

### Deel labor-market context

- The 2025 dataset covers more than 1,000,000 active worker contracts, 37,000+ companies, and 150+ countries.
- Contractors in high-inflation markets frequently choose USD or stablecoins; Argentina is reported at 84.6% choosing USD over local currency.
- The reported stablecoin contractor-adoption ranking includes Argentina, Cameroon, South Korea, Türkiye, Vietnam, and Tajikistan.
- USD preference is not stablecoin preference. Ranking or co-location is not a same-user retention result.

### Provider-linked and crypto-engaged context

- BVNK/Deel reports more than 10,000 contractors in more than 100 markets opting into stablecoin pay. This is a provider-linked Known Floor.
- BVNK/YouGov reports on 4,658 crypto-engaged current, former, or intended users across 15 countries; 39% report getting paid in stablecoins. The category includes professional and family/friends contexts and is not a clean salary denominator.

## Interpretation boundary

The evidence supports a coherent discovery hypothesis: some globally paid workers may value a payout rail together with dollar-value holding or spending. It does not support multiplying the Stripe, Remote, Deel, BVNK, or labor-market denominators, nor converting willingness, provider availability, USD preference, or current-use shares into a stablecoin worker TAM.

No source in this package measures the intersection of a worker’s payout receipt, retained balance, and later spend across multiple pay cycles. The target evidence therefore remains an overlap hypothesis, not a proven cohort.

## Decision impact

Keep worker payout → hold/spend as a strategy-level discovery direction and a candidate job to validate. Use Argentina, Colombia, Ghana, and comparable high-pressure markets as hypothesis contexts rather than ranked market sizes. Do not use this file as proof of primary money status, recurring income retention, or an AIX right-to-win.

## What remains Unknown

- Same-user intersection between receiving stablecoin or USD-denominated pay and holding a balance.
- Whether held value survives until the next pay cycle and whether the user spends from that balance.
- Clean worker-only denominators, country-level prevalence, and reachable AIX population.
- Whether the motive is currency protection, payout speed, FX cost, access, or a combination of jobs.
- Relative switching intent and differentiation versus fiat and stablecoin-native alternatives.

## Disconfirming evidence

- The 57% Stripe willingness figure could materially overstate actual use because it is a hypothetical offer response.
- The 18% current-use figure is subgroup-bound and has no publicly established subgroup n in this package.
- Deel’s 84.6% Argentina USD preference could reflect fiat USD demand without stablecoin demand.
- BVNK/YouGov’s crypto-engaged sample and mixed payment category could fail to represent independent workers or salary recipients.
- The Remote case could be concentrated provider-specific behavior and does not show balance persistence.

## Recommended validation evidence

Run a strategy-level, worker-specific validation that links the same respondent or customer across payout receipt, dollar-value holding, and subsequent spend, with explicit country, worker type, pay-cycle, and alternative-rail comparisons. The decision gate should require a clean denominator and repeat-cycle evidence before treating the overlap as a target segment or durable retention opportunity.
