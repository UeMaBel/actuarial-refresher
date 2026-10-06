# Change of Measure

# Change of Measure

A change of measure changes the probability weights assigned to outcomes while keeping the modelled events themselves. In financial mathematics, it connects physical dynamics used for forecasting with pricing dynamics used for valuation.

## Radon–Nikodym density

If measure $Q$ is absolutely continuous with respect to $P$, a positive density process $Z_t$ relates conditional expectations:

$$
\mathbb{E}^{Q}[X\mid\mathcal{F}_t]
=\frac{\mathbb{E}^{P}[Z_T X\mid\mathcal{F}_t]}{Z_t},
\qquad Z_t=\mathbb{E}^{P}[Z_T\mid\mathcal{F}_t].
$$

Intuitively, outcomes that are more heavily weighted under $Q$ receive greater pricing weight. The density must satisfy appropriate integrability and consistency conditions.

## Brownian drift adjustment

Girsanov's theorem gives conditions under which a Brownian motion under one measure becomes a Brownian motion with an adjusted drift under another. Thus, changing measure typically changes process drifts; in jump models, intensity and jump-size weighting may also change.

The physical measure $P$ supports real-world scenario assumptions. A pricing measure $Q$ is selected and calibrated so discounted traded-asset gains have the required martingale property. In incomplete markets, that property may not determine a unique $Q$.

## Connections

- [[Probability Measures]] — Physical and pricing measures
- [[Martingales]] — Martingale property under a pricing measure
- [[Risk-Neutral Scenarios]] — Market-consistent valuation
- [[Real-World Scenarios]] — Forecasting and risk distributions
- [[Stochastic Calculus]] — Dynamics under transformed measures

