# Health Insurance Math

> Mathematical foundations for pricing and valuing health insurance, from short-term claims to long-duration morbidity and ageing provisions.

## Frequency and severity

For a portfolio with claim count $N$ and claim amounts $X_i$, aggregate claims are

$$
S = \sum_{i=1}^{N} X_i.
$$

Under the usual independence assumptions, $\mathbb{E}[S]=\mathbb{E}[N]\mathbb{E}[X]$. Model claim frequency and severity separately, allowing for exposure, deductibles, limits, and benefit design.

## Morbidity and multi-state models

Long-duration health cover can be represented with states such as healthy, ill, disabled, and recovered. Transition intensities or probabilities determine expected time in each state and hence projected benefits, expenses, and premiums. Assumptions may vary by age, duration, and other rating factors.

## Trend and ageing

Project medical costs using health-specific assumptions for price inflation, utilisation, and treatment mix. For long-term contracts, combine morbidity and cost trends with survival, lapses, expenses, investment returns, and premium-adjustment rules. Ageing provisions depend on the product and jurisdiction; they are not simply a claim-frequency calculation.

## Valuation and risk

Expected discounted cash flows support pricing and liability valuation. Uncertainty comes from random claims, parameter estimation, trend, longevity, and policyholder behaviour. Short-tail portfolios emphasise annual frequency-severity pricing and claims development; life-like health business needs longer projections and biometric models.

## Connections

- [[Health Insurance]] — Product types, risks, and life-like versus non-life-like business
- [[Probability]] — Expected claim costs
- [[Statistics]] — Estimating morbidity and claim assumptions
- [[Poisson Process]] — A possible model for claim arrivals
- [[Solvency II - Pillar I - Quantitative Requirements]] — Health underwriting risk and technical provisions
- [[IFRS]] — Measurement of health insurance contracts

## Further methods

- [[Survival Models and Life Tables]] — Survival and multi-state foundations for long-duration health business.
- [[Insurance Pricing and GLMs]] — Claim frequency and severity for shorter-duration health business.
- [[Claims Reserving]] — Existing claims and development.

