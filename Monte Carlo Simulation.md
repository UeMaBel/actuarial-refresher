# Monte Carlo Simulation

# Monte Carlo Simulation

Monte Carlo simulation estimates quantities by generating random samples from a model. For independent outcomes $Y_1,\ldots,Y_n$ with mean $\mu$, the sample average

$$
\hat\mu=\frac{1}{n}\sum_{i=1}^{n}Y_i
$$

estimates $\mu$. Its standard error is approximately $s/\sqrt{n}$, where $s$ is the sample standard deviation. Increasing the number of independent simulations reduces sampling error at a square-root rate.

## Actuarial uses

Simulation can estimate expected claims, tail risk, option and guarantee values, and distributions of future solvency outcomes. In a stochastic valuation, each economic path is passed through asset and liability cash-flow models, then results are averaged or summarized according to the chosen measure and objective.

## Practical checks

Use enough paths for stable results, report Monte Carlo error where useful, and distinguish sampling error from parameter uncertainty and model risk. More paths do not repair biased assumptions, a misspecified model, or omitted dependencies. Variance reduction methods can improve precision for a fixed computational budget.

## Connections

- [[Economic Scenario Generator]] — Generates economic paths for downstream models
- [[Risk-Neutral Scenarios]] — Monte Carlo valuation under a pricing measure
- [[Real-World Scenarios]] — Simulated distributions for planning and risk
- [[Solvency II - Pillar I - Quantitative Requirements]] — Stochastic valuation and internal-model risk
- [[Life Insurance Math]] — Nonlinear guarantees and contingent benefits

