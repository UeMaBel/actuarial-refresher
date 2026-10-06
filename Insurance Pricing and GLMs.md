# Insurance Pricing and GLMs

> Insurance pricing connects exposure, expected claims, expenses, and risk. A generalized linear model (GLM) helps estimate how claim experience varies across policy characteristics.

## Start with exposure and loss cost

An exposure unit measures time or amount at risk, such as one insured vehicle-year. Claim frequency is claims divided by exposure; severity is claim cost divided by claim count. Under suitable assumptions,

$$
\text{expected loss cost per exposure}=\text{frequency}\times\text{severity}.
$$

For example, 0.08 claims per vehicle-year at €2,000 per claim imply €160 expected claims per vehicle-year before expenses, reinsurance, and other loads. The price actually charged also depends on product design, regulation, commercial constraints, and the pricing objective.

## What a GLM adds

A GLM relates a distribution's mean to predictors through a link function. For claim counts, a Poisson GLM with a log link can use exposure $e_i$ as an offset:

$$
\log \mathbb{E}[N_i]=\log e_i+\beta_0+\beta_1x_{i1}+\cdots.
$$

Exponentiating a coefficient gives a multiplicative relativity for its predictor, conditional on the other variables. A separate severity model can use a positive distribution and log link. The Poisson variance equals its mean, so excess variation may require a different model or variance treatment.

## Interpret with care

Check exposure definitions, claim development, inflation, policy mix, missing data, and whether rating factors are permitted and appropriate. A predictive relationship does not automatically imply a causal effect. Small groups may need credibility adjustments. Compare predicted and observed experience on data outside the fitting sample.

## Connections

- [[Motor Insurance Math]] — Aggregate losses and motor pricing
- [[Health Insurance Math]] — Utilisation and claim-cost models
- [[Probability Distributions]] — Count and severity distributions
- [[Statistical Estimation]] — Parameter uncertainty and diagnostics
- [[Claims Reserving]] — Developed claims as a pricing input

## Further reading

- [CAS monograph on insurance rating plans using GLMs](https://www.casact.org/monograph/cas-monograph-no-5)
