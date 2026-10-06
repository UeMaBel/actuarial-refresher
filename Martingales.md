# Martingales

# Martingales

A process $M_t$ is a martingale relative to information $\mathcal{F}_t$ if it is integrable, adapted to that information, and

$$
\mathbb{E}[M_t\mid\mathcal{F}_s]=M_s \quad (s\leq t).
$$

In plain terms, given what is known now, the expected future value is the current value. A martingale is not necessarily constant and can still be volatile.

## Financial interpretation

Under an appropriate pricing measure, discounted traded-asset values (including relevant gains and dividends) are martingales. This links no-arbitrage pricing to conditional expectations. Which quantities are martingales depends on the chosen numeraire and measure.

Martingale conditions are useful model checks, but passing them does not prove calibration quality or realism under the physical measure.

## Connections

- [[Conditional Expectation]] — Defining conditional expectation property
- [[Stochastic Calculus]] — Continuous-time martingales and stochastic integrals
- [[Change of Measure]] — Pricing measures and martingale dynamics
- [[Risk-Neutral Scenarios]] — Discounted asset gains and valuation

