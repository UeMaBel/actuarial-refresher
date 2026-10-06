# Conditional Expectation

# Conditional Expectation

Conditional expectation is the expected value of a random variable given specified information. It is written $\mathbb{E}[X\mid\mathcal{F}]$, where $\mathcal{F}$ represents what is known. The result is itself a random variable: it can vary with the information observed.

## Key properties

- If $X$ is already known given $\mathcal{F}$, then $\mathbb{E}[X\mid\mathcal{F}]=X$.
- Linearity: $\mathbb{E}[aX+bY\mid\mathcal{F}]=a\mathbb{E}[X\mid\mathcal{F}]+b\mathbb{E}[Y\mid\mathcal{F}]$.
- Tower property: if $\mathcal{G}\subseteq\mathcal{F}$, then $\mathbb{E}[\mathbb{E}[X\mid\mathcal{F}]\mid\mathcal{G}]=\mathbb{E}[X\mid\mathcal{G}]$.

The tower property is the mathematical basis for updating projected values as information arrives over time.

## Insurance examples

Expected future claims conditional on age, policy status, or claims history can differ from an unconditional portfolio average. In a life-contingent contract, future benefits are valued conditional on the policyholder being alive and the contract remaining in force.

In pricing, valuation, and financial models, conditional expectations express values at a given date using the information available then.

## Connections

- [[Probability]] — Expectations and conditional probability
- [[Martingales]] — A process equal to its conditional expected future value
- [[Life Insurance Math]] — Benefits conditional on survival and policy status

