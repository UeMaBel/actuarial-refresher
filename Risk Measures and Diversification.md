# Risk Measures and Diversification

> A best estimate summarizes the centre of a loss distribution. A risk measure asks how much loss could occur in adverse outcomes.

## From a loss distribution to a number

Let $L$ be a loss over a specified horizon. Expected loss $\mathbb{E}[L]$ is a mean. Value-at-Risk at level $\alpha$ is a loss quantile:

$$
\operatorname{VaR}_{\alpha}(L)=\inf\{l:P(L\leq l)\geq\alpha\}.
$$

A 99% VaR is a threshold exceeded with probability at most about 1% under the model. It says little about the size of losses beyond the threshold. Expected shortfall summarizes losses in the worst tail; for continuous distributions it is the mean loss conditional on exceeding VaR. The exact definition for distributions with atoms needs care.

## Diversification and concentration

Aggregate loss $L=L_1+L_2$ depends on the joint behaviour of its components. Independence, ordinary correlation, and stressed dependence lead to different tail results. Diversification can reduce aggregate risk, but shared events, common economic drivers, and extreme dependence can make that benefit smaller than expected.

## Solvency application

Solvency II calibrates the SCR to a 99.5% Value-at-Risk of basic own funds over one year. That is a regulatory capital standard, not a complete description of every risk or every future year. An internal model may simulate one-year economic and underwriting outcomes, revalue liabilities, and obtain a distribution of changes in own funds. Standard-formula calculations use prescribed stresses and aggregation rules.

## Model questions

- What exactly counts as a loss, and over what horizon?
- Are data and assumptions adequate for the chosen tail level?
- Do dependencies and risk mitigation behave differently in stress?
- How sensitive is the result to parameter uncertainty and model choice?

## Connections

- [[Probability]] — Quantiles, expectation, and variance
- [[Correlation and Dependence]] — Joint risk and aggregation
- [[Monte Carlo Simulation]] — Estimating loss distributions
- [[Claims Reserving]] — Uncertainty in existing claims
- [[Real-World Scenarios]] — Distributions of possible future states
- [[Solvency II - Pillar I - Quantitative Requirements]] — SCR and capital
- [[ORSA]] — Insurer-specific risk and solvency assessment

## Further reading

- [EIOPA Solvency II Directive, Article 101](https://www.eiopa.europa.eu/rulebook/solvency-ii-single-rulebook/article-2188_en)
