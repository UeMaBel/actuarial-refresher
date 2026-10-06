# Poisson Process

# Poisson Process

A Poisson process $N_t$ counts events over time. With constant intensity $\lambda$, the number of events in an interval of length $t$ has distribution

$$
\Pr(N_t=k)=e^{-\lambda t}\frac{(\lambda t)^k}{k!}, \qquad k=0,1,2,\ldots
$$

It has independent increments; the expected count and variance over length $t$ are both $\lambda t$. The waiting times between events are independent exponential variables with rate $\lambda$.

## Actuarial use

A Poisson process can model claim arrivals or jump times. In compound models, each event has a random size, and total loss is the sum of event severities. A constant-intensity process assumes a stable rate and independent arrivals; exposure changes, seasonality, clustering, and common causes may require richer models.

## Connections

- [[Stochastic Processes]] — Counting process as a time-evolving random process
- [[Motor Insurance Math]] — Claim frequency and aggregate losses
- [[Health Insurance Math]] — A possible short-term claim-arrival model
- [[Merton Jump-Diffusion Model]] — Arrivals of asset-price jumps

