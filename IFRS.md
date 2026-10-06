---
tags: [actuarial, insurance, accounting]
---

# IFRS

> Core question: How should an entity report its financial position and performance, including when it recognises profit?

**IFRS — International Financial Reporting Standards** are international accounting standards.

For insurers, two particularly important standards are:

- **IFRS 17:** Insurance contracts
- **IFRS 9:** Financial instruments, including many investments

Compare Solvency II: prudential regulation focuses on policyholder protection and capital adequacy.

## 1. IFRS 17: insurance contracts

IFRS 17 replaced IFRS 4 and applies to annual reporting periods beginning on or after 1 January 2023.

Its central ideas are:

- Measure insurance obligations using current cash-flow estimates.
- Allow explicitly for uncertainty from non-financial risk.
- Recognise profit as insurance contract services are provided.
- Recognise expected losses on onerous groups promptly.

## 2. Main valuation components

In the general measurement model:

$$
\text{Fulfilment cash flows}
=
\text{Expected discounted net outflows}
+
\text{Risk Adjustment}
$$

The carrying amount also includes a **Contractual Service Margin — CSM**, where applicable. Detailed measurement distinguishes remaining coverage from incurred claims.

### Expected discounted net outflows

Expected benefits and expenses minus premiums within the contract boundary.

Discount rates reflect the characteristics of the cash flows, including:

- Timing
- Currency
- Liquidity

### Risk Adjustment

The compensation the insurer requires for bearing uncertainty from **non-financial risk**, such as:

- Mortality and longevity
- Claim frequency and severity
- Expenses
- Policyholder lapses

It is not the same as the Solvency II Risk Margin.

### CSM — Contractual Service Margin

The CSM represents **unearned profit relating to future insurance contract services**.

It prevents expected future profit from being recognised immediately when a profitable contract group is first recorded.

The CSM is subsequently recognised in profit or loss as services are provided, using coverage units.

> The key new accounting idea is that expected profit and earned profit are different.

## 3. Simple example

Assume a new profitable group has:

| Item | Present value |
|---|---:|
| Future premiums | 100 |
| Future benefits and expenses | 85 |
| Risk Adjustment | 5 |
| CSM | 10 |

Expected net outflows:

$$
85 - 100 = -15
$$

Fulfilment cash flows:

$$
-15 + 5 = -10
$$

The CSM of +10 offsets this initial gain.

**No day-one profit is recognised.** The CSM is earned through future services.

This simplified example ignores additional initial-recognition adjustments.

For an onerous group of issued insurance contracts, the expected loss is recognised immediately. Its CSM cannot become negative. Reinsurance held has separate rules.

## 4. Subsequent measurement

Over time, the insurer updates assumptions and recognises actual experience.

Depending on the measurement model and the nature of the change:

- Changes relating to future service generally adjust the CSM, subject to exceptions.
- Changes relating to current or past service generally affect current profit or loss.
- Certain insurance finance effects may be presented in other comprehensive income, depending on the accounting policy.

The actuarial task therefore includes both projecting cash flows and explaining movements between reporting dates.

## 5. Three measurement approaches

| Approach | Typical application |
|---|---|
| General Measurement Model — GMM | Default approach |
| Variable Fee Approach — VFA | Contracts meeting the direct-participation criteria |
| Premium Allocation Approach — PAA | Optional simplified approach for eligible contracts, often short-duration coverage |

The PAA mainly simplifies the measurement of remaining coverage; incurred claims still require their own measurement.

## 6. Connection to economic scenario generators

Economic scenario generators can support projections of market-dependent insurance benefits, financial guarantees, and contractual options.

Some modelling infrastructure can be shared with Solvency II:

- Economic scenarios
- Asset models
- Insurance cash-flow models
- Policyholder behaviour
- Management actions

However, the frameworks can differ in:

- Contract boundaries
- Discounting
- Risk allowances
- Contract grouping
- Profit recognition
- Presentation and disclosure

Shared models do not imply identical reported liabilities.

## 7. IFRS 17 versus Solvency II

| | IFRS 17 | Solvency II |
|---|---|---|
| Objective | Financial reporting and profit recognition | Policyholder protection and capital adequacy |
| Risk allowance | Risk Adjustment for non-financial risk | Risk Margin based on cost of capital |
| Future profit | Deferred through the CSM | No equivalent CSM component |
| Capital requirement | Does not set an SCR | SCR and MCR |

An insurer can therefore have different equity figures under IFRS accounting and Solvency II.

## 8. What IFRS 1–16 mean

The numbers identify separate standards covering different subjects. They are not earlier versions of IFRS 17.

Older **IAS — International Accounting Standards** also remain part of the framework where applicable.

| Standard | Subject |
|---|---|
| IFRS 1 | First-time adoption of IFRS |
| IFRS 2 | Share-based payment |
| IFRS 3 | Business combinations |
| IFRS 4 | Insurance contracts — superseded by IFRS 17 |
| IFRS 5 | Non-current assets held for sale and discontinued operations |
| IFRS 6 | Exploration for and evaluation of mineral resources |
| IFRS 7 | Financial instruments: disclosures |
| IFRS 8 | Operating segments |
| IFRS 9 | Financial instruments |
| IFRS 10 | Consolidated financial statements |
| IFRS 11 | Joint arrangements |
| IFRS 12 | Disclosure of interests in other entities |
| IFRS 13 | Fair value measurement |
| IFRS 14 | Regulatory deferral accounts |
| IFRS 15 | Revenue from contracts with customers |
| IFRS 16 | Leases |

This is a reference to IFRS 1–16, not a complete list of all IFRS standards.

## Sources

- [IFRS Foundation — IFRS 17](https://www.ifrs.org/issued-standards/list-of-standards/ifrs-17-insurance-contracts/)
- [IFRS Foundation — IFRS 17 key terms](https://www.ifrs.org/supporting-implementation/supporting-materials-by-ifrs-standards/ifrs-17/key-terms/)
- [IFRS Foundation — Standards navigator](https://www.ifrs.org/issued-standards/list-of-standards/)
