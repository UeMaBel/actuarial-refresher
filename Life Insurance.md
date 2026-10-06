---
aliases: [Life Assurance, Lebensversicherung]
tags: [actuarial, insurance, life]
---

# Life Insurance

> Life insurance covers financial consequences of death, survival, and sometimes disability. Many products also include savings and investment features.

## Main products

| Product | Main benefit |
|---|---|
| Term life — Risikolebensversicherung | Payment if the insured dies during the coverage period |
| Endowment — Kapitallebensversicherung | Payment on death or survival to a specified date |
| Annuity — Rentenversicherung | Regular payments, often for the remaining lifetime |
| Unit-linked — Fondsgebundene Versicherung | Benefits linked to investment funds, sometimes with guarantees |
| Disability — Berufsunfähigkeitsversicherung | Income or benefits following qualifying disability |

Product names do not by themselves determine the precise accounting or regulatory classification.

## Main actuarial risks

- **Mortality:** Deaths exceed expectations, increasing death benefits.
- **Longevity:** People live longer than expected, increasing lifetime annuity payments.
- **Disability and morbidity:** More insured people become disabled or ill.
- **Lapse:** Policyholders surrender or discontinue contracts differently from expectations.
- **Expense:** Administration costs exceed assumptions.
- **Market:** Investment returns, interest rates, or asset values move adversely.

The direction of risk depends on the product: higher mortality harms term-life business but can reduce payments on lifetime annuities.

## Cash-flow modelling

Models project:

- Premiums
- Death and survival benefits
- Annuity payments
- Expenses
- Surrender payments
- Policyholder bonuses

These depend on demographic assumptions, contract terms, economic conditions, policyholder behaviour, and management actions.

## Why financial scenarios matter

Life contracts can last decades.

Interest rates affect liability discounting, reinvestment returns, guarantees, and surrender incentives.

An Economic Scenario Generator provides financial paths. Risk-Neutral Scenarios support market-consistent valuation of financial guarantees; Real-World Scenarios support planning and risk measurement.

The Hull-White Two-Factor Model can supply interest-rate paths. The Merton Jump-Diffusion Model can supply equity paths.

## Asset–liability interaction

For participating business, investment performance can affect policyholder bonuses.

In poor markets, guarantees may remain payable even when asset returns are insufficient. In favourable markets, some gains may be shared with policyholders.

This creates nonlinear cash flows and makes stochastic modelling important.

## Solvency II connection

Under Solvency II, life underwriting risks include mortality, longevity, disability/morbidity, lapse, expense, revision, and catastrophe risk.

Market and counterparty risks are assessed separately but interact economically with the insurance obligations.

## IFRS 17 connection

Under IFRS, the General Measurement Model commonly applies to long-duration contracts.

The Variable Fee Approach applies where contracts meet the direct-participation criteria. It does not apply automatically to every participating or unit-linked contract.

## Key distinction

**Protection business:** Primarily transfers biometric risk.

**Savings and annuity business:** Often combines biometric risk with significant financial risk.

## Actuarial mathematics

- [[Life Insurance Math]] — Survival models, expected present values, premiums, and reserves


## Further foundation

- [[Survival Models and Life Tables]] — Survival and mortality probabilities behind the cash flows.
- [[Time Value of Money]] — Discounting long-term benefits and premiums.

