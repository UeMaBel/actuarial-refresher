---
aliases: [HW2F, Hull–White Two-Factor]
tags: [quantitative-finance, interest-rates, models]
---

# Hull-White Two-Factor Model

> An interest-rate model that uses two stochastic factors to generate movements in the yield curve.

Used within an Economic Scenario Generator for interest-rate scenarios, bond valuation, and the valuation of interest-sensitive guarantees.

## Intuition

A one-factor model ties movements at different maturities to a single source of randomness.

Two factors allow richer movements: short-term and long-term rates can respond differently, producing changes in the slope as well as the level of the curve.

The factors are mathematical drivers. They are not necessarily directly observable economic variables.

## Common Gaussian formulation

A widely used two-factor Gaussian representation, commonly called G2++, is:

$$
r_t = \phi(t) + x_t + y_t
$$

Under the money-market risk-neutral measure:

$$
dx_t = -a x_t\,dt + \sigma\,dW_{1,t}^{Q}
$$

$$
dy_t = -b y_t\,dt + \eta\,dW_{2,t}^{Q}
$$

$$
dW_{1,t}^{Q}\,dW_{2,t}^{Q} = \rho\,dt
$$

| Symbol | Meaning |
|---|---|
| $r_t$ | Instantaneous short rate |
| $\phi(t)$ | Deterministic shift fitting the initial yield curve |
| $x_t, y_t$ | Stochastic interest-rate factors |
| $a, b$ | Mean-reversion speeds |
| $\sigma, \eta$ | Factor volatilities |
| $\rho$ | Correlation between Brownian drivers |

“HW2F” can refer to different parameterisations. G2++ is a closely related standard representation; always check the equations used in a particular implementation.

## Mean reversion

Each factor tends back towards zero under the dynamics above.

- Higher mean reversion: shocks decay more quickly.
- Lower mean reversion: shocks persist for longer.
- Different mean-reversion speeds create different maturity sensitivities.

Mean reversion of the factors does not mean that the short rate reverts to a single constant: the deterministic shift also varies with time.

## From short rates to a yield curve

The model produces zero-coupon bond prices:

$$
P(t,T)
=
\mathbb{E}^{Q}\left[
e^{-\int_t^T r_s\,ds}
\mid \mathcal{F}_t
\right]
$$

The continuously compounded zero rate is:

$$
z(t,T) = -\frac{\ln P(t,T)}{T-t}
$$

Thus, the factors determine an entire yield curve at each simulation date, not just one interest rate.

## Calibration

For Risk-Neutral Scenarios:

- Fit the initial discount curve.
- Calibrate factor parameters to interest-rate option prices, often swaptions.
- Validate prices, curve reproduction, and simulation behaviour.

For Real-World Scenarios:

- Specify realistic interest-rate dynamics and risk premiums.
- Use historical evidence and economic assumptions.
- Do not assume that risk-neutral drifts are forecasts.

## Insurance applications

Under Solvency II, interest-rate paths affect:

- Discounted liability values
- Investment and reinvestment returns
- Minimum-return guarantees
- Profit sharing
- Surrender behaviour
- Asset–liability mismatches

They can also support market-dependent projections under IFRS.

## Strengths and limitations

**Strengths:** Tractable bond pricing, initial-curve fitting, richer curve dynamics than one factor, and efficient Gaussian simulation.

**Limitations:** Rates can be negative; Gaussian dynamics may poorly describe extreme events; a basic constant-parameter version cannot fit every feature of an option volatility surface.

Two factors do not capture every possible yield-curve movement.

## Source

- [QuantLib — G2 model implementation](https://github.com/lballabio/QuantLib/blob/master/ql/models/shortrate/twofactormodels/g2.hpp)

## Connections

- [[Ornstein-Uhlenbeck Process]] — Mean-reverting Gaussian factors
