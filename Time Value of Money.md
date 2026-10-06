# Time Value of Money

> A euro received later is valued using a discount factor. This is the common language behind premiums, reserves, bonds, and insurance liabilities.

## Accumulation and discounting

At a constant effective annual interest rate $i$, one unit grows to $(1+i)^t$ after $t$ years. Its present value is

$$
v^t=(1+i)^{-t}, \qquad v=(1+i)^{-1}.
$$

For example, €100 payable in two years at 5% is worth $100/(1.05)^2=€90.70$ today. The discount rate, payment date, and compounding convention must be stated together.

With a continuous force of interest $\delta$, the discount factor is $e^{-\delta t}$ and $\delta=\ln(1+i)$ for an equivalent constant annual rate.

## Cash flows and annuities

For cash flows $C_t$ paid at times $t$, present value is $\sum_t C_t v(t)$, where $v(t)$ is the discount factor to time $t$. A level annuity of 1 paid at the **end** of each year for $n$ years has value

$$
a_{\overline{n}|}=\sum_{k=1}^{n}v^k=\frac{1-v^n}{i}, \qquad i\ne0.
$$

Payments at the **start** of each year have value $\ddot a_{\overline{n}|}=(1+i)a_{\overline{n}|}$. An annuity certain pays regardless of survival; a life annuity also needs survival probabilities.

## Term structure and bonds

Real valuations usually use a discount curve rather than one rate. Let $D(0,t)$ be the price today of one unit paid at $t$. Then $PV=\sum_t C_tD(0,t)$. A zero rate $z_t$ may be defined by $D(0,t)=e^{-z_tt}$ under continuous compounding. Different maturities can have different rates.

A fixed coupon bond is the present value of its coupon payments and redemption amount. Its price and yield move in opposite directions. **Duration** summarizes first-order sensitivity to a small parallel yield change; it does not fully describe large or nonparallel curve moves.

## Why the basis matters

Pricing, planning, Solvency II, and IFRS may use different discounting assumptions for different purposes. Match the currency, timing, and characteristics of the cash flows to the chosen basis. In stochastic valuation, discount factors can vary by scenario and may be dependent on the benefit cash flows.

## Connections

- [[Life Insurance Math]] — Discounted death benefits, annuities, and reserves
- [[Health Insurance Math]] — Long-duration benefit and premium projections
- [[Motor Insurance Math]] — Discounting long-tail claims
- [[Hull-White Two-Factor Model]] — Stochastic interest rates and discount factors
- [[Solvency II - Pillar I - Quantitative Requirements]] — Economic valuation
- [[IFRS]] — Insurance contract discounting

## Further reading

- [IFoA actuarial mathematics curriculum](https://actuaries.org.uk/qualify/curriculum/actuarial-mathematics)
