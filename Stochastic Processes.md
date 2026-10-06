# Stochastic Processes



## Topics

- [[Brownian Motion]] â€” Continuous Gaussian noise
- [[Poisson Process]] â€” Counting random events
- [[Ornstein-Uhlenbeck Process]] â€” Gaussian mean reversion
- [[Stochastic Calculus]] â€” Integration and stochastic differential equations

# Stochastic Processes

A stochastic process is a collection of random variables indexed by time, written $\{X_t:t\geq0\}$. It models how an uncertain quantity evolves. A filtration $\{\mathcal{F}_t\}$ represents information available through time; a model should respect that information when describing future changes.

## Common process types

- **Discrete-time or continuous-time:** Whether observations or evolution occur at steps or continuously.
- **Discrete-state or continuous-state:** Whether values are counts/states or real-valued quantities.
- **Diffusion:** Continuous paths with random fluctuations, commonly driven by Brownian motion.
- **Counting process:** Increases by jumps as events occur, such as claims or market jumps.

A process model specifies both its transition behaviour and assumptions such as stationarity, independence, and parameter stability.

## Actuarial applications

Mortality and morbidity can be modelled as transitions between states. Claims and financial jumps can be represented by counting processes. Market variables such as interest rates can use diffusions or mean-reverting processes. The chosen process should match the question, data, and timescale.

## Connections

- [[Brownian Motion]] — Continuous Gaussian noise
- [[Poisson Process]] — Counting random events
- [[Ornstein-Uhlenbeck Process]] — Gaussian mean reversion
- [[Stochastic Calculus]] — Calculus for continuous-time random models
- [[Life Insurance Math]] — Lifetime and state-transition cash flows
- [[Economic Scenario Generator]] — Joint economic paths

