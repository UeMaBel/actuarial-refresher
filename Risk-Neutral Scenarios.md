---
aliases: [Q-Measure Scenarios, Pricing Scenarios]
tags: [actuarial, scenarios, valuation]
---

# Risk-Neutral Scenarios

> Risk-neutral scenarios are used to value future payoffs consistently with market prices. They are not forecasts of actual outcomes.

They are generated under a pricing measure, usually denoted Q.

The pricing measure depends on the chosen numeraire. The formulas below use the money-market account.

## Basic pricing principle

For a payoff $H_T$:

$$
V_t
=
\mathbb{E}^{Q}\left[
e^{-\int_t^T r_s\,ds}H_T
\mid\mathcal{F}_t
\right]
$$

The value today is the Q-weighted expectation of the discounted future payoff.

For insurance contracts, actuarial assumptions for non-financial risks are also needed: a financial pricing measure alone does not determine mortality, expenses, or policyholder behaviour.

## What “risk-neutral” means

Under the appropriate pricing measure, suitably discounted traded-asset gains are martingales.

For a non-dividend-paying asset and money-market account:

$$
B_t = e^{\int_0^t r_s\,ds}
$$

$$
\mathbb{E}^{Q}\left[
\frac{S_T}{B_T}
\mid\mathcal{F}_t
\right]
=
\frac{S_t}{B_t}
$$

For dividend-paying assets, the martingale condition must include dividends.

Risk-neutral does not mean:

- No volatility
- No crashes
- No defaults
- Investors actually being indifferent to risk

Risk is reflected in market prices and the pricing probabilities.

## Simple equity example

Under geometric Brownian motion:

$$
\frac{dS_t}{S_t}
=
(r_t-q)\,dt
+
\sigma\,dW_t^Q
$$

Here, $q$ is the continuous dividend yield.

Compare Real-World Scenarios, where the drift reflects an assumed real-world expected return.

## Calibration

Typical inputs include:

- Current discount curves
- Option prices or implied volatilities
- Relevant market dependencies
- Product-specific market information

Useful checks include:

- Initial yield-curve reproduction
- Option-price reproduction
- Martingale tests
- Numerical convergence

Passing a martingale test is necessary for many pricing implementations, but does not by itself prove that the model fits all relevant market prices.

## Models

- Hull-White Two-Factor Model: Interest-rate paths, bond prices, and interest-rate options.
- Merton Jump-Diffusion Model: Asset paths with jumps and option valuation.

In incomplete markets, such as those with unhedgeable jump risk, absence of arbitrage alone may not identify a unique pricing measure. Additional calibration or risk-pricing assumptions are needed.

## Insurance applications

Under Solvency II, risk-neutral scenarios support market-consistent valuation of market-dependent benefits, especially financial options and guarantees.

Under IFRS, related modelling can support market-dependent insurance cash-flow valuation, subject to IFRS-specific measurement rules.

The ESG supplies financial scenarios. The insurance model adds contract terms, mortality, expenses, lapses, bonuses, and management actions.

## Why the average path is insufficient

For nonlinear payoffs:

$$
f(\mathbb{E}^{Q}[X])
\neq
\mathbb{E}^{Q}[f(X)]
$$

A guarantee can be valuable even when it would never pay out along the average path.

Stochastic valuation captures the range of outcomes and their pricing weights.


## Sources

- [EIOPA — Stochastic valuation under Solvency II](https://www.eiopa.europa.eu/publications/peer-review-supervision-stochastic-valuation-under-solvency-ii_en)
- [Broadie, Chernov and Johannes — Pricing measures and risk premiums](https://www.columbia.edu/~mnb2/broadie/Assets/EOR_20080618.pdf)

## Connections

- [[Change of Measure]] — Pricing measure Q and risk premiums
- [[Martingales]] — Discounted traded-asset gains
