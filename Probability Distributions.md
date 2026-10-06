# Probability Distributions

A probability distribution describes the possible values of a random variable and their probabilities. These few distributions are common starting models in actuarial work. The choice is an assumption to check against the data and purpose, not an automatic truth.

## Discrete distributions

### Bernoulli

One trial with success probability $p$:

$$
P(X=x)=p^x(1-p)^{1-x},\quad x\in\{0,1\}.
$$

Mean $p$; variance $p(1-p)$. Can represent whether a policy has a claim in a fixed period, when at most one claim is possible.

### Binomial

Number of successes in $n$ independent Bernoulli trials with common success probability $p$:

$$
P(X=k)=\binom{n}{k}p^k(1-p)^{n-k},\quad k=0,\ldots,n.
$$

Mean $np$; variance $np(1-p)$. A possible model for claim counts across a fixed number of similar, independent policies, with at most one event per policy in the period.

### Poisson

Count of events over exposure $t$ at rate $\lambda$:

$$
P(N=k)=e^{-\lambda t}\frac{(\lambda t)^k}{k!},\quad k=0,1,2,\ldots
$$

Mean and variance are both $\lambda t$. Often used as a basic claim-frequency or jump-count model. The standard form assumes a stable rate and independent arrivals; see [[Poisson Process]].

## Continuous distributions

### Normal

A bell-shaped distribution with mean $\mu$ and standard deviation $\sigma$:

$$
f_X(x)=\frac{1}{\sigma\sqrt{2\pi}}\exp\left(-\frac{(x-\mu)^2}{2\sigma^2}\right),\quad -\infty<x<\infty.
$$

Mean $\mu$; variance $\sigma^2$. It is useful for measurement error and approximations, but its unbounded negative side makes it unsuitable for many raw claim amounts without adjustment.

### Exponential

A positive waiting time or loss amount with rate $\lambda>0$:

$$
f_X(x)=\lambda e^{-\lambda x},\quad x\geq0.
$$

Mean $1/\lambda$; variance $1/\lambda^2$. It has the memoryless property. It can serve as a simple severity or inter-arrival-time model, although its tail shape may not fit real claims well.

### Lognormal

A positive variable whose logarithm is normal: if $Y=\ln X\sim N(\mu,\sigma^2)$, then $X$ is lognormal with density

$$
f_X(x)=\frac{1}{x\sigma\sqrt{2\pi}}\exp\left(-\frac{(\ln x-\mu)^2}{2\sigma^2}\right),\quad x>0.
$$

Its mean is $e^{\mu+\sigma^2/2}$ and variance is $(e^{\sigma^2}-1)e^{2\mu+\sigma^2}$. It is a common positive, right-skewed severity model. Here $\mu$ and $\sigma$ describe the log amount, not the original amount.

## How to choose

- Claim counts are often modelled with Binomial or Poisson distributions.
- Positive claim amounts may use Exponential or Lognormal distributions.
- Normal distributions appear in approximations and many statistical procedures.
- Real portfolios may need over-dispersion, mixtures, truncation for deductibles and limits, or heavier tails.

A distribution gives a model for uncertainty; estimate its parameters from data and check fit and tail behaviour. See [[Statistical Estimation]] and [[Motor Insurance Math]] for applications.

## Connections

- [[Probability]] — Random variables, expectation, variance, and quantiles
- [[Poisson Process]] — Poisson event counts through time
- [[Statistical Estimation]] — Fitting distribution parameters
- [[Motor Insurance Math]] — Frequency and severity models
- [[Health Insurance Math]] — Claim counts and costs
- [[Merton Jump-Diffusion Model]] — Poisson arrivals and lognormal jump multipliers
