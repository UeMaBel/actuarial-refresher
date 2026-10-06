---
tags: [actuarial, insurance, solvency, valuation]
---

# Solvency II - Pillar I - Quantitative Requirements

> Value the economic balance sheet and determine the capital required to absorb adverse developments.


## Economic balance sheet

Assets and liabilities are valued on an economic, market-consistent basis.

For most insurance obligations:

$$
\text{Technical provisions}
=
\text{Best Estimate}
+
\text{Risk Margin}
$$

**Best Estimate:** Probability-weighted present value of future benefits and expenses minus premiums within the contract boundary, using the relevant risk-free term structure and applicable adjustments.

**Risk Margin:** An additional amount based on the cost of capital required to support the remaining obligations in a hypothetical transfer to another insurer.

**Own funds:** Broadly, the excess of assets over liabilities, with regulatory adjustments. Eligibility rules and tier limits determine what can cover capital requirements.

The Risk Margin is part of the liability valuation. It is not the capital requirement.

## Capital requirements

### SCR — Solvency Capital Requirement

Calibrated to a **99.5% Value-at-Risk of basic own funds over one year**.

It covers market, counterparty default, underwriting, and operational risks, recognising diversification and relevant loss-absorbing effects.

Calculation approaches:

- Standard formula
- Approved internal model
- Approved partial internal model

The calibration is model-based, not a guarantee of survival.

### MCR — Minimum Capital Requirement

A lower capital threshold whose breach triggers stronger supervisory intervention.

Breaching the SCR also requires action.

### Coverage ratio

$$
\text{SCR coverage ratio}
=
\frac{\text{Eligible own funds}}{\text{SCR}}
$$

Eligible own funds of 150 million and an SCR of 100 million give 150% coverage.

## Economic scenario generators

An Economic Scenario Generator supplies financial paths to asset and insurance liability models.

Risk-Neutral Scenarios support market-consistent valuation, particularly where obligations contain material financial options and guarantees.

Relevant financial models include:

- Hull-White Two-Factor Model for interest rates
- Merton Jump-Diffusion Model for asset prices with jumps

These are possible modelling choices, not models prescribed by Solvency II.

## Valuation versus risk measurement

**Valuation:** Determine what the remaining obligations are worth in a particular economic state.

**Risk measurement:** Determine how the economic balance sheet could deteriorate over one year.

An internal model may use:

1. Outer Real-World Scenarios to generate one-year economic states.
2. Inner risk-neutral simulations to value remaining obligations in those states.
3. The resulting distribution of changes in own funds to calculate capital.

The standard formula instead uses prescribed stresses and does not require this full outer simulation.

## Insurance applications

- Life Insurance: Mortality, longevity, lapse, guarantees, and participating benefits.
- Motor Insurance: Premium, reserve, catastrophe, and long-tail claims risks.
- Health Insurance: Morbidity, expenses, ageing, and life-like or non-life-like obligations.

## Relationship to accounting

IFRS and Solvency II can share actuarial modelling infrastructure, but their objectives and measurement rules differ.

IFRS 17 includes a Risk Adjustment and CSM; Solvency II uses a Risk Margin and sets capital requirements.

## Connections

- [[Economic Scenario Generator]] — Financial inputs for valuation and capital modelling
- [[Insurance Types]] — Underwriting risks by insurance branch
- [[IFRS]] — Comparison with accounting valuation

## Further foundation

- [[Time Value of Money]] — Discounting future obligations.
- [[Risk Measures and Diversification]] — Loss distributions, VaR, and aggregation.
- [[Claims Reserving]] — Existing non-life claims and reserve risk.

