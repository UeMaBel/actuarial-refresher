# Probability

> First stop for the mathematical refresher: learn how to summarize uncertainty before moving to statistical estimation or stochastic models.

## 1. Outcomes, events, and random variables

A random experiment has possible outcomes in a sample space $\Omega$. An event is a set of outcomes. A probability $P(A)$ lies between 0 and 1; $P(\Omega)=1$, and probabilities of mutually exclusive events add.

A random variable $X$ assigns a number to each outcome. Its distribution describes the probabilities of its possible values. For a discrete variable use the probability mass function $P(X=x)$; for a continuous variable use a density $f_X(x)$, where probabilities are areas under the density. In the continuous case, $P(X=x)=0$ for any one exact value.

The cumulative distribution function is

$$
F_X(x)=P(X\leq x).
$$

It works for both discrete and continuous variables and is useful for probabilities and quantiles.

## 2. Expected value — Erwartungswert

The expected value is the probability-weighted average of a random variable over repeated outcomes. For discrete $X$,

$$
\mathbb{E}[X]=\sum_x xP(X=x).
$$

For continuous $X$ with density $f_X$,

$$
\mathbb{E}[X]=\int_{-\infty}^{\infty} x f_X(x)\,dx.
$$

Example: a claim count $N$ is 0, 1, or 2 with probabilities 0.2, 0.5, and 0.3. Then $\mathbb{E}[N]=0(0.2)+1(0.5)+2(0.3)=1.1$. This is a long-run average, not a possible outcome that must occur in any one period.

Linearity is especially useful:

$$
\mathbb{E}[aX+bY+c]=a\mathbb{E}[X]+b\mathbb{E}[Y]+c.
$$

It holds whether or not $X$ and $Y$ are independent.

## 3. Variance and standard deviation — Varianz und Standardabweichung

Variance measures the expected squared distance from the mean:

$$
\operatorname{Var}(X)=\mathbb{E}[(X-\mathbb{E}[X])^2]
=\mathbb{E}[X^2]-\mathbb{E}[X]^2.
$$

For the example above, $\mathbb{E}[N^2]=0+0.5+4(0.3)=1.7$, so $\operatorname{Var}(N)=1.7-1.1^2=0.49$. The standard deviation is $\sqrt{0.49}=0.7$ claims. Variance is in squared units; standard deviation is in the original units.

Adding a constant does not change variance, and scaling by $a$ multiplies it by $a^2$:

$$
\operatorname{Var}(aX+b)=a^2\operatorname{Var}(X).
$$

## 4. Covariance and sums

Covariance measures how two variables move together:

$$
\operatorname{Cov}(X,Y)=\mathbb{E}[(X-\mathbb{E}X)(Y-\mathbb{E}Y)].
$$

For a sum,

$$
\operatorname{Var}(X+Y)=\operatorname{Var}(X)+\operatorname{Var}(Y)+2\operatorname{Cov}(X,Y).
$$

If $X$ and $Y$ are independent, their covariance is zero. The converse is not generally true. Positive dependence increases the variance of a sum; negative dependence reduces it. Correlation is covariance divided by the product of standard deviations and is unitless.

## 5. Conditional probability and expectation

Conditional probability updates an event probability using information that another event occurred:

$$
P(A\mid B)=\frac{P(A\cap B)}{P(B)}, \qquad P(B)>0.
$$

Conditional expectation $\mathbb{E}[X\mid\mathcal{F}]$ is the expected value given currently available information. For now, think of it as updating a projection when age, policy status, claims history, or market information is known. See [[Conditional Expectation]] for the deeper treatment.

## 6. Quantiles and tail probabilities

A quantile $q_\alpha$ is a threshold such that the probability of being at or below it is approximately $\alpha$. For a loss variable $L$, the 99th percentile is a loss level exceeded with probability about 1% (subject to the quantile convention). Quantiles describe the distribution's tail and connect probability models to capital measures such as Value-at-Risk.

## Actuarial interpretation

- Expected claim cost supports pricing and best-estimate cash flows.
- Variance and tail probabilities describe uncertainty around that expected cost.
- Dependence affects portfolio aggregation and diversification.
- A model's parameters are estimated from data; uncertainty about them is part of the next step, [[Statistics]].

## Continue from here

1. [[Conditional Expectation]] — Expectations given information and over time.
2. [[Probability Measures]] — Different probability weights for forecasting and pricing.
3. [[Statistics]] — Describing data and learning model assumptions.
4. [[Motor Insurance Math]] — Apply expectation and variance to claim counts and aggregate losses.

## Connections

- [[Mathematics Refresher]] — The route through the mathematical foundations
- [[Statistics]] — Estimation and dependence
- [[Correlation and Dependence]] — Joint outcomes and portfolio aggregation
- [[Conditional Expectation]] — Conditional averages
- [[Probability Measures]] — Probability frameworks

## Common distributions

Start with [[Probability Distributions]] for Bernoulli, Binomial, Poisson, Normal, Exponential, and Lognormal models, including their parameters, means, variances, and actuarial uses.


## Continue into valuation and risk

- [[Time Value of Money]] — Discount uncertain future cash flows.
- [[Risk Measures and Diversification]] — Use quantiles and dependence to assess adverse losses.

