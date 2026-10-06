---
aliases: [ESG, Economic Scenarios, Capital Market Scenarios]
tags: [actuarial, quantitative-finance, simulation]
---

# Economic Scenario Generator

> An Economic Scenario Generator (ESG) simulates financial and economic paths used for valuation, risk measurement, and planning.

Here, ESG means **Economic Scenario Generator**, rather than environmental, social, and governance.`r`n`r`n## Start here`r`n`r`nThis is the bridge between financial mathematics and insurance applications. First compare [[Real-World Scenarios]] with [[Risk-Neutral Scenarios]]: they answer different questions. Then follow [[Financial Models]] to the interest-rate and equity models, and [[Monte Carlo Simulation]] to how paths become estimates. For the broader actuarial foundations, start at [[Mathematics Refresher]]; for the regulatory application, start at [[Solvency II]].

## What it generates

An ESG can simulate:

- Interest rates and yield curves
- Equity prices and returns
- Credit spreads and defaults
- Property values
- Inflation
- Exchange rates

Dependencies between these variables matter: an insurer needs coherent joint scenarios, not isolated simulations of individual markets.

## Where it fits

The ESG supplies economic paths to an integrated assetâ€“liability model:

1. Generate financial and economic scenarios.
2. Project asset returns, defaults, and reinvestment.
3. Project premiums, claims, expenses, and policyholder behaviour.
4. Apply management actions, such as bonus decisions.
5. Calculate liability values, profits, risk measures, and capital needs.

The ESG is the economic input layer. Insurance contract rules and company behaviour are represented in the downstream models.

## Two types of scenarios

### Real-World Scenarios

**Question:** What might actually happen?

Also called **physical-measure** or **P-measure** scenarios.

They incorporate assumptions about expected returns, risk premiums, and economic developments.

Typical uses:

- Business planning
- Strategic asset allocation
- Assetâ€“liability management
- ORSA and forward-looking solvency planning
- Real-world risk distributions in internal models

### Risk-Neutral Scenarios

**Question:** What is a future payoff worth today, consistently with market prices?

Also called **Q-measure** scenarios.

They are calibrated for pricing rather than forecasting. Risk-neutral probabilities generally differ from real-world probabilities.

Typical uses:

- Valuation of financial options and guarantees
- Market-consistent insurance liability valuation under Solvency II - Pillar I - Quantitative Requirements
- Valuation of market-dependent cash flows under IFRS

Risk-neutral does not mean risk-free: these scenarios still contain uncertainty, volatility, and potentially severe losses.

## Example models

### HW2F â€” Hullâ€“White Two-Factor

An interest-rate model with two stochastic factors.

The factors allow richer yield-curve dynamics than a one-factor model, including different movements across maturities.

In a common Gaussian formulation, the short rate is represented as:

$$
r_t = \phi(t) + x_t + y_t
$$

The factors are correlated mean-reverting processes; the deterministic function allows the model to fit the initial yield curve.

Typical role in an ESG:

- Simulating interest rates and yield curves
- Pricing interest-rate-sensitive guarantees
- Providing discount factors and bond values

The exact specification and calibration depend on the implementation. A modelâ€™s name alone does not determine whether its scenarios are real-world or risk-neutral.

### Merton Jump-Diffusion Model

An asset-price model combining:

- Continuous Brownian fluctuations
- Discrete jumps arriving through a Poisson process

Jump sizes are commonly modelled as lognormal multipliers.

Typical role in an ESG:

- Simulating equity or other asset prices
- Representing sudden market moves
- Producing return distributions richer than a pure diffusion
- Pricing options when calibrated under a pricing measure

Distinguish this from the **Merton structural credit-risk model**, which is a different model.

In a market with jump risk, risk-neutral calibration requires assumptions about how jump risk is priced; historical jump estimates alone do not determine pricing parameters.

## Why many paths are needed

Guarantees, options, profit sharing, and policyholder behaviour produce nonlinear results:

$$
f(\mathbb{E}[X]) \neq \mathbb{E}[f(X)]
$$

Running an insurance model on an average market path generally does not give the average result across many market paths.

Thousands of paths can help estimate these effects.

More paths reduce Monte Carlo noise. They do not fix poor assumptions or missing risk factors.

## Calibration and validation

**Calibration:** Choose model parameters to fit relevant market observations or real-world assumptions.

**Validation:** Check whether the resulting scenarios behave consistently with their intended purpose.

Examples:

- Initial yield-curve reproduction
- Market-price reproduction for pricing scenarios
- Martingale tests under the appropriate pricing measure
- Plausibility of real-world returns and dependencies
- Numerical convergence and simulation stability

## Connection to my former work

My capital-market scenario work supplied the financial input layer for actuarial valuation, assetâ€“liability modelling, planning, and solvency calculations.

It connected quantitative-finance models such as Hull-White Two-Factor Model and Merton Jump-Diffusion Model to practical insurance applications.

## Connections

- [[Real-World Scenarios]] â€” Planning and risk measurement
- [[Risk-Neutral Scenarios]] â€” Market-consistent valuation
- [[Financial Models]] â€” Models generating the financial paths
- [[Monte Carlo Simulation]] â€” Simulation precision and convergence


## Guided refresher

- [[Actuarial Refresher]] — Where scenarios fit in the overall actuarial workflow.
- [[Time Value of Money]] — Discount factors and yield curves used in scenario valuation.
