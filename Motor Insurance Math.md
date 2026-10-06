# Motor Insurance Math

> Mathematical foundations for motor insurance pricing, claims reserving, and aggregate loss risk.

## Frequency-severity model

Let $N$ be the number of claims in a period and $X_1,\ldots,X_N$ their severities. Aggregate loss is

$$
S = \sum_{i=1}^{N} X_i.
$$

If claim count and severities are independent and severities are identically distributed,

$$
\mathbb{E}[S] = \mathbb{E}[N]\mathbb{E}[X], \qquad
\operatorname{Var}(S)=\mathbb{E}[N]\operatorname{Var}(X)+\operatorname{Var}(N)\mathbb{E}[X]^2.
$$

This separates expected claim cost into frequency and severity. Exposure, rating characteristics, deductibles, limits, and claim inflation affect the inputs.

## Pricing and risk

A technical premium starts with expected claims, then allows for expenses and other required loads. Portfolio pricing also considers uncertainty, reinsurance, competition, and capital. Correlation and accumulation matter when many vehicles can be affected by the same event.

## Reserving

For claims already incurred, development data can be arranged by accident period and development age. Methods such as chain ladder project ultimate losses from observed development; Bornhuetter–Ferguson blends an a priori expected loss with observed emergence. Assumptions should reflect claim reporting delays, settlement patterns, inflation, and long-tail liability claims.

## Connections

- [[Motor Insurance]] — Coverages, risks, and reserving context
- [[Probability]] — Aggregate loss expectations and distributions
- [[Statistics]] — Fitting frequency and severity models
- [[Poisson Process]] — A possible claim-arrival model
- [[Correlation and Dependence]] — Shared events and portfolio accumulation
- [[Solvency II - Pillar I - Quantitative Requirements]] — Premium, reserve, and catastrophe risk
- [[IFRS]] — Remaining coverage and incurred-claims measurement


## Further methods

- [[Insurance Pricing and GLMs]] — Exposure-based frequency and severity pricing.
- [[Claims Reserving]] — Development triangles and outstanding claims.

