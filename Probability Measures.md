# Probability Measures

# Probability Measures

A probability measure assigns probabilities to events in a sample space. In modelling, the same possible outcomes can be evaluated under different probability measures, which assign different weights to those outcomes.

## Physical and pricing measures

The physical or real-world measure is commonly denoted $P$. It represents assumptions about how outcomes occur and is used for forecasting and risk distributions. The pricing measure is commonly denoted $Q$. In an arbitrage-free financial model, it supports valuation by discounted expected payoffs, relative to a chosen numeraire.

For a payoff $H_T$ and money-market account $B_t$, a basic pricing relation is

$$
V_t = B_t\,\mathbb{E}^{Q}\left[\frac{H_T}{B_T}\mid\mathcal{F}_t\right].
$$

The choice of measure does not change the observed market today; it changes the probability weights used in the model. In incomplete markets there may be multiple pricing measures, so additional modelling or calibration assumptions are needed.

## Actuarial distinction

Use $P$ scenarios to ask what may happen and to assess distributions of future outcomes. Use $Q$ scenarios to value market-linked cash flows consistently with traded prices. Non-financial insurance risks still require actuarial assumptions; a financial pricing measure alone does not specify mortality, expenses, or policyholder behaviour.

## Connections

- [[Real-World Scenarios]] — Uses of the physical measure
- [[Risk-Neutral Scenarios]] — Pricing under a risk-neutral measure
- [[Change of Measure]] — How probability weights transform
- [[Conditional Expectation]] — Expectations conditional on current information

