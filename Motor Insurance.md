---
aliases: [Car Insurance, Auto Insurance, Kfz-Versicherung]
tags: [actuarial, insurance, non-life]
---

# Motor Insurance

> Motor insurance covers liabilities and losses arising from the ownership or use of vehicles.

It belongs to non-life insurance, also called property and casualty insurance.

## Main coverages

| Coverage | German term | Main protection |
|---|---|---|
| Third-party liability | Kfz-Haftpflicht | Injury and property damage caused to others |
| Partial comprehensive | Teilkasko | Specified risks such as theft, glass damage, or natural hazards |
| Comprehensive collision cover | Vollkasko | Additional cover for damage to the insured vehicle, subject to policy terms |

Exact coverage depends on the jurisdiction and contract.

## Core actuarial model

A basic aggregate claim model is:

$$
S = \sum_{i=1}^{N} X_i
$$

where:

- $N$ is the number of claims.
- $X_i$ is the amount of claim $i$.
- $S$ is aggregate claim cost.

Under standard independence assumptions:

$$
\mathbb{E}[S]
=
\mathbb{E}[N]\mathbb{E}[X]
$$

This gives the basic pricing idea:

**Expected claim cost = claim frequency Ã— average claim severity.**

Premiums must also cover expenses, reinsurance, capital costs, and profit.

## Main risks

- **Frequency risk:** More accidents or claims than expected.
- **Severity risk:** Claims cost more than expected.
- **Reserve risk:** Existing claims ultimately settle above current estimates.
- **Inflation risk:** Repairs, replacement parts, wages, or injury compensation become more expensive.
- **Catastrophe and accumulation risk:** One event damages many vehicles.
- **Legal and behavioural change:** Liability rules, litigation, fraud, or driving patterns change.

## Short coverage does not mean short liabilities

Policies often provide approximately one year of coverage.

However, serious bodily injury claims can take many years to settle and may generate long-term periodic payments.

Motor damage is generally shorter-tail than motor bodily injury liability.

## Reserving

At a valuation date, obligations include:

- Reported claims not yet fully settled
- Claims incurred but not yet reported â€” IBNR
- Future claim-handling expenses

Common reserving methods include chain ladder and Bornhuetterâ€“Ferguson, supplemented by individual claim assessments and other models.

## Role of economic scenarios

Economic scenarios are usually less central than for guaranteed savings life insurance, but still matter through:

- Claims inflation
- Discounting of long-tail claims
- Investment performance
- Assetâ€“liability management
- Economic effects on claim behaviour

Real-World Scenarios support planning and risk analysis. Financial valuation assumptions must follow the applicable framework.

An Economic Scenario Generator does not replace frequency, severity, or reserving models.

## Solvency II connection

Under Solvency II, motor business contributes to non-life premium and reserve risk, relevant catastrophe risks, and other applicable risks.

Market, counterparty, and operational risks also apply to the insurer.

## IFRS 17 connection

Under IFRS, many annual motor contracts qualify for the Premium Allocation Approach.

This simplifies remaining-coverage measurement. Incurred claims still require fulfilment cash-flow measurement, including a Risk Adjustment and discounting where required.

## Actuarial mathematics

- [[Motor Insurance Math]] â€” Frequency-severity pricing, aggregate losses, and reserving



## Follow the actuarial workflow

- [[Insurance Pricing and GLMs]] — Price new coverage using exposure and expected claims.
- [[Claims Reserving]] — Estimate the cost of claims already incurred.

