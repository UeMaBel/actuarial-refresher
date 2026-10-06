# Claims Reserving

> Claims reserving estimates the future cost of claims that have already occurred. It links claims data to insurance liabilities and reserve risk.

## What is being estimated?

For an accident period, **ultimate claims** are the final total cost after all claims are settled. Outstanding claims equal ultimate claims less claims paid to date. Estimates include future payments on reported claims and incurred but not reported claims (IBNR), with claim-handling expenses as required by the valuation basis.

Paid and incurred claims tell different stories: incurred data include case estimates on reported claims; paid data reflect actual settlement. Changes in case reserving or settlement speed can distort development patterns.

## Development triangles and chain ladder

A triangle arranges cumulative claims by accident period and development age. Chain ladder uses observed age-to-age development factors to project less mature periods to ultimate.

If cumulative paid claims for one accident year are 100 at 12 months and the selected factor from 12 months to ultimate is 1.40, projected ultimate is 140 and the implied future paid amount is 40. This is only a simple illustration; a full analysis estimates factors from multiple periods and checks their stability.

## Bornhuetter–Ferguson

The Bornhuetter–Ferguson idea combines an independent expected ultimate amount with the portion of claims not yet expected to have emerged. With expected ultimate $U_0$ and estimated reported proportion $r$:

$$
\text{Ultimate estimate}=\text{reported to date}+(1-r)U_0.
$$

It can be useful when early development is volatile, but it relies on a credible prior expectation and development pattern.

## Review the assumptions

Check exposure and portfolio mix, claims inflation, large claims, catastrophes, legal changes, reporting delays, and settlement speed. Reserve estimates are uncertain; one selected ultimate value does not describe the range of outcomes. Discounting and explicit risk allowances depend on the reporting framework.

## Connections

- [[Motor Insurance Math]] — Frequency, severity, and long-tail motor claims
- [[Health Insurance Math]] — Reserving for shorter-duration health business
- [[Statistical Estimation]] — Parameter and model uncertainty
- [[Risk Measures and Diversification]] — Reserve risk and tail outcomes
- [[Solvency II - Pillar I - Quantitative Requirements]] — Technical provisions and reserve risk
- [[IFRS]] — Liability for incurred claims

## Further reading

- [IFoA actuarial mathematics curriculum, non-life reserving](https://actuaries.org.uk/qualify/curriculum/actuarial-mathematics)
- [CAS monograph on stochastic loss reserving](https://www.casact.org/monograph/cas-monograph-no-3)
