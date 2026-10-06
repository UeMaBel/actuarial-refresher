# Stochastic Calculus



## Topics

- [[Martingales]] â€” Conditional-expectation structure
- [[Change of Measure]] â€” Changing probability weights

# Stochastic Calculus

Stochastic calculus extends calculus to processes with random, non-smooth paths, especially Brownian motion. Its central tool in many financial models is the Itô integral and Itô's formula.

## Itô's formula

If $dX_t=\mu_tdt+\sigma_tdW_t$ and $f$ is sufficiently smooth, then

$$
df(t,X_t)=\left(f_t+\mu_tf_x+\tfrac12\sigma_t^2f_{xx}\right)dt+\sigma_tf_xdW_t.
$$

The second-derivative term appears because Brownian increments have variance proportional to $dt$. This is the key difference from ordinary chain-rule calculus.

Stochastic differential equations describe model dynamics. Numerical schemes such as Euler-Maruyama approximate their paths; discretization error and simulation error are separate considerations.

## Why actuaries use it

It underpins continuous-time asset and interest-rate models, derivative pricing, and risk-neutral valuation. It helps derive how transformed quantities such as asset prices, discount factors, or option values evolve.

## Connections

- [[Brownian Motion]] — Source of continuous random shocks
- [[Martingales]] — Conditional expectation and fair-game property
- [[Change of Measure]] — Transforming dynamics between probability measures
- [[Ornstein-Uhlenbeck Process]] — A stochastic differential equation
- [[Hull-White Two-Factor Model]] — Interest-rate factor dynamics
- [[Merton Jump-Diffusion Model]] — Diffusion plus jump dynamics

