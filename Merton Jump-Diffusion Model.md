---
aliases: [Merton Jump Diffusion, MJD]
tags: [quantitative-finance, equities, models]
---

# Merton Jump-Diffusion Model

> An asset-price model combining continuous fluctuations with sudden jumps.

It extends geometric Brownian motion by adding a compound Poisson jump process.

Used within an Economic Scenario Generator, commonly for equity scenarios and option valuation.

## Intuition

Two mechanisms move the price:

1. **Diffusion:** Continuous fluctuations driven by Brownian motion.
2. **Jumps:** Sudden changes at random event times.

The classic model allows both upward and downward jumps.

It is different from the Merton structural credit-risk model.

## Risk-neutral dynamics

For constant parameters, a common formulation is:

$$
\frac{dS_t}{S_{t-}}
=
(r-q-\lambda\kappa)\,dt
+
\sigma\,dW_t^{Q}
+
(J-1)\,dN_t^{Q}
$$

At each jump, a fresh independent multiplier $J$ is drawn:

$$
\ln J \sim N(m,\delta^2)
$$

Therefore:

$$
\kappa = \mathbb{E}^{Q}[J-1]
= e^{m+\delta^2/2}-1
$$

| Symbol | Meaning |
|---|---|
| $S_t$ | Asset price |
| $S_{t-}$ | Price immediately before time $t$ |
| $r$ | Risk-free rate |
| $q$ | Continuous dividend yield |
| $\sigma$ | Diffusion volatility |
| $N_t^Q$ | Poisson counting process |
| $\lambda$ | Expected number of jumps per unit time |
| $J$ | Price multiplier at a jump |
| $m,\delta$ | Mean and standard deviation of log jump size |

If $J=0.8$, the price falls by 20% at that jump.

## Why subtract the jump compensator?

The jumps contribute an expected return of $\lambda\kappa$.

Subtracting it from the continuous drift ensures that total expected price growth under Q is $r-q$.

Without this adjustment, the expected jump return would be counted in addition to the required risk-neutral growth rate.

## Simulation

For a time step $\Delta t$ with constant parameters:

$$
K \sim \operatorname{Poisson}(\lambda\Delta t)
$$

Draw independent jump log sizes:

$$
Y_j \sim N(m,\delta^2)
$$

Then:

$$
S_{t+\Delta t}
=
S_t
\exp\left[
(r-q-\lambda\kappa-\tfrac12\sigma^2)\Delta t
+
\sigma\sqrt{\Delta t}\,Z
+
\sum_{j=1}^{K}Y_j
\right]
$$

where $Z\sim N(0,1)$ and is independent of the jumps.

## Real-world versus risk-neutral parameters

For Real-World Scenarios, a compensated formulation replaces $r-q$ with an assumed expected price-growth rate under P and uses P-measure jump parameters.

For Risk-Neutral Scenarios, parameters are chosen for market-consistent pricing, commonly using option prices.

Jump intensity and jump-size distributions can differ between P and Q. Historical estimates alone do not determine how jump risk is priced.

## Insurance applications

Equity jumps can affect:

- Investment losses
- Equity-linked guarantees
- Policyholder bonuses
- Capital requirements
- Hedging performance

These effects matter in Solvency II and in market-dependent insurance valuations under IFRS.

## Strengths and limitations

**Strengths:** Represents sudden market moves and produces non-normal returns. It can generate option smiles or skews.

**Limitations:** The classic model has constant diffusion volatility and independent Poisson arrivals, so it does not naturally capture volatility clustering or clustered crises.

Its return tails are richer than those of pure geometric Brownian motion, but are not automatically realistic for every risk application.

## Sources

- [MathWorks — Merton jump-diffusion model](https://www.mathworks.com/help/finance/merton.html)
- [Broadie, Chernov and Johannes — Understanding Index Option Returns](https://www.columbia.edu/~mnb2/broadie/Assets/EOR_20080618.pdf)

## Connections

- [[Poisson Process]] — Random jump arrivals
