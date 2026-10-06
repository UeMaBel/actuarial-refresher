# Ornstein-Uhlenbeck Process



## Topics

- [[Brownian Motion]] â€” Driving noise

# Ornstein-Uhlenbeck Process

The Ornstein-Uhlenbeck (OU) process is a continuous-time Gaussian process that mean-reverts. A standard form is

$$
dX_t=\kappa(\theta-X_t)\,dt+\sigma\,dW_t,
$$

where $\theta$ is the long-run mean, $\kappa>0$ is the speed of mean reversion, and $\sigma$ controls random variation. The drift pulls $X_t$ toward $\theta$ while Brownian motion adds shocks.

Over a time interval $h$, its exact conditional distribution is normal with mean $\theta+(X_t-\theta)e^{-\kappa h}$ and variance $\frac{\sigma^2}{2\kappa}(1-e^{-2\kappa h})$. This is useful for simulation and shows how shocks decay over time.

## Interest-rate models

OU factors are used in Gaussian interest-rate models. In Hull-White two-factor formulations, two correlated mean-reverting factors are combined with a deterministic shift to fit the initial yield curve. The OU form describes the factors; the complete interest-rate model includes additional specification and calibration.

## Connections

- [[Brownian Motion]] — Random driving noise
- [[Stochastic Calculus]] — Stochastic differential equations
- [[Hull-White Two-Factor Model]] — Mean-reverting interest-rate factors

