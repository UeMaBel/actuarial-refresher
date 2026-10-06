# Life Insurance Math

> Mathematical foundations for mortality, survival benefits, annuities, and long-term life insurance cash flows.

## Survival and mortality

Let $T_x$ be the future lifetime of a life aged $x$. The survival function is

$$
{}_tp_x = \Pr(T_x > t),
$$

and the probability of death within $t$ years is $q_x(t)=1-{}_tp_x$. In a discrete annual model, $p_x+q_x=1$. A force of mortality $\mu_{x+t}$ gives the instantaneous death rate conditional on survival to age $x+t$.

## Present values

With discount factor $v(t)$, an expected present value is the probability-weighted value of benefits and premiums over possible lifetimes. For example, a continuous life annuity paying at rate 1 while the insured is alive has value

$$
a_x = \int_0^\infty v(t)\,{}_tp_x\,dt.
$$

A term assurance paying 1 at death during $[0,n]$ has value

$$
A_{x:\overline{n}|} = \int_0^n v(t)\,{}_tp_x\,\mu_{x+t}\,dt.
$$

Payment timing and discrete versus continuous conventions change the formulas.

## Premiums and reserves

The equivalence principle sets the expected present value of premiums equal to that of benefits and expenses under the chosen assumptions. Prospective policy reserves are the expected present value of future outgo less future premiums, conditional on the policy being in force. Practical valuation also accounts for expenses, lapses, guarantees, and the applicable reporting framework.

## Multiple decrements and financial risk

Disability, lapse, and death can be modelled as competing transitions. Investment-linked benefits and guarantees add economic scenarios and may require stochastic valuation because the payoff is nonlinear in market paths.

## Connections

- [[Life Insurance]] — Products, risks, and cash-flow applications
- [[Probability]] — Survival probabilities and expectations
- [[Statistics]] — Estimating mortality, lapse, and expense assumptions
- [[Stochastic Processes]] — Lifetime and state-transition models
- [[Economic Scenario Generator]] — Financial paths for guarantees and participating business
- [[Solvency II - Pillar I - Quantitative Requirements]] — Technical provisions and life underwriting risk
- [[IFRS]] — Insurance contract measurement and profit recognition

## Foundations to revisit

- [[Time Value of Money]] — Discounting certain and contingent payments.
- [[Survival Models and Life Tables]] — Mortality, survival, and life-table notation.

