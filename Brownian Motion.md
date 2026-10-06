# Brownian Motion

# Brownian Motion

Brownian motion, or a Wiener process $W_t$, is a continuous-time model of accumulated random shocks. It starts at zero, has independent increments, and for $s<t$, $W_t-W_s$ is normally distributed with mean zero and variance $t-s$. Its paths are continuous but almost surely nowhere differentiable.

A scaled increment over a short interval $\Delta t$ is represented as $\Delta W\approx\sqrt{\Delta t}Z$, where $Z\sim N(0,1)$. This scaling drives diffusion models and stochastic differential equations.

## Actuarial and financial use

Brownian motion is used to model continuous market fluctuations and as the noise term in mean-reverting interest-rate factors. By itself it does not model jumps, changing volatility, or all observed market behaviour.

## Connections

- [[Stochastic Processes]] — Random evolution through time
- [[Stochastic Calculus]] — Integrals and differential equations driven by Brownian motion
- [[Ornstein-Uhlenbeck Process]] — Gaussian mean-reverting process
- [[Hull-White Two-Factor Model]] — Correlated Brownian drivers for interest rates
- [[Merton Jump-Diffusion Model]] — Diffusion combined with jumps

