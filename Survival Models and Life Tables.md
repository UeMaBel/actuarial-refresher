# Survival Models and Life Tables

> A life table turns mortality experience into survival probabilities. Those probabilities, combined with discount factors, value life-contingent cash flows.

## Read a life table

Let $l_x$ be the number of a hypothetical cohort alive at exact age $x$. Let $d_x=l_x-l_{x+1}$ be deaths between ages $x$ and $x+1$. Then

$$
q_x=\frac{d_x}{l_x}, \qquad p_x=1-q_x=\frac{l_{x+1}}{l_x}.
$$

For example, if $l_{60}=90{,}000$ and $l_{61}=89{,}100$, then $q_{60}=0.01$ and $p_{60}=0.99$. The probability that a life aged $x$ survives $n$ whole years is ${}_np_x=l_{x+n}/l_x$ under the table's assumptions.

## Lifetime and mortality intensity

Future lifetime $T_x$ is random. Its survival function is ${}_tp_x=P(T_x>t)$. The force of mortality $\mu_{x+t}$ is an instantaneous rate conditional on survival; under suitable smoothness,

$$
{}_tp_x=\exp\left(-\int_0^t\mu_{x+s}\,ds\right).
$$

It is a rate, not a probability. Annual $q_x$ and continuous $\mu_{x+t}$ must not be interchanged without a within-year assumption.

## From survival to present value

For a unit benefit at time $n$ only if the person is alive, expected present value is $D(0,n){}_np_x$. For a unit benefit at the end of the year of death, a term assurance over $n$ years has value

$$
\sum_{k=0}^{n-1}D(0,k+1){}_kp_xq_{x+k}.
$$

The payment timing is part of the product definition. A life annuity instead weights each payment by the probability of being alive on its payment date. See [[Life Insurance Math]] for the continuous formulas.

## Practical assumptions

Observed rates need suitable exposure denominators and may require graduation or smoothing. Mortality can differ by product, underwriting, age, sex where permitted, calendar year, and selection. **Longevity improvement** means future survival can exceed what a static table suggests. Disability, recovery, and lapse require multiple-state or competing-decrement models.

## Connections

- [[Life Insurance Math]] — Death benefits, annuities, and reserves
- [[Health Insurance Math]] — Morbidity and multiple-state models
- [[Statistics]] — Estimating mortality from experience
- [[Time Value of Money]] — Discounting contingent payments
- [[Stochastic Processes]] — Transitions through time

## Further reading

- [IFoA CM1 syllabus, life tables and contingent cash flows](https://actuaries.org.uk/media/yfnkmkbq/cm1_syllabus-2026-_final-proof.pdf)
