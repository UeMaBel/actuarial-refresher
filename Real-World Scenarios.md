---
aliases: [Physical-Measure Scenarios, P-Measure Scenarios]
tags: [actuarial, scenarios, risk-management]
---

# Real-World Scenarios

> Real-world scenarios model what might actually happen, with probabilities reflecting the modeller’s assumptions about the economy and markets.

They are generated under the physical probability measure, usually denoted P.

They are estimates, not objectively known future probabilities.

## Main uses

- Business planning
- Strategic asset allocation
- Asset–liability management
- Profit and liquidity projections
- ORSA under Solvency II
- Internal-model distributions of one-year losses

An Economic Scenario Generator supplies the paths; asset and liability models translate them into business results.

## Calibration

Real-world assumptions can draw on:

- Historical returns and dependencies
- Current economic conditions
- Forward-looking economic views
- Expected risk premiums
- Long-term equilibrium assumptions

Historical data alone may poorly represent future regimes or rare crises.

## Simple equity example

Under geometric Brownian motion:

$$
\frac{dS_t}{S_t}
=
\mu_P\,dt
+
\sigma\,dW_t^P
$$

Here, $\mu_P$ is the assumed expected price-growth rate. If the asset pays dividends, total expected return also includes them.

Unlike in Risk-Neutral Scenarios, the drift is not constrained to equal the risk-free rate minus dividend yield.

## Models versus probability measures

A model family does not automatically imply P or Q.

For example:

- Hull-White Two-Factor Model can be adapted to real-world interest-rate dynamics.
- Merton Jump-Diffusion Model can use real-world expected returns and jump assumptions.

Changing from P to Q can change drifts and, for jump models, jump intensity and jump-size distributions.

## Connection to Solvency II

In an internal model, real-world scenarios can describe how the insurer’s economic position changes over one year.

At the end of that year, remaining obligations may be valued using Risk-Neutral Scenarios.

This creates the distinction:

- **P:** Distribution of future economic states.
- **Q:** Valuation within a given state.

Standard-formula capital calculations instead use prescribed stresses and do not require a full real-world simulation.

## Validation questions

- Are expected returns and risk premiums defensible?
- Are dependencies plausible, particularly during stress?
- Are long-term paths economically reasonable?
- Are tail results sensitive to assumptions?
- Is simulation noise small enough for the intended decision?

More paths improve numerical precision, not the truth of the assumptions.


## Source

- [Broadie, Chernov and Johannes — Physical and risk-neutral dynamics](https://www.columbia.edu/~mnb2/broadie/Assets/EOR_20080618.pdf)

## Connections

- [[Probability Measures]] — The physical measure P
