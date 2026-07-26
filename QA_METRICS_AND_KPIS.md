#QA Metrics & Key Performance Indicators (KPIs)


## Document Control & Revision History

| Version | Date       | Author        | Change Description                             |
|:--------|:-----------|:--------------|:-----------------------------------------------|
| 1.0.2   | 25-07-2026 | An. Gyuviyska | Changed "version" structure; added new section |

---

## 1. Overview
This document defines the core Quality Assurance metrics, their mathematical formula formulas, and the calculation methodologies used to assess product quality and test process efficiency throughout the Software Development Life Cycle (SDLC).

---

## 2. Metric Calculations

### 1. Requirement Coverage (RC)
Measures the percentage of defined business requirements or Acceptance Criteria covered by executed test scenarios.

* Formula:

$$
\text{Requirement Coverage (\%)} = \left( \frac{\text{Executed Requirements}}{\text{Total Planned Requirements}} \right) \times 100
$$

* Target: `> 95%`
* Example:
  If a sprint includes 10 User Stories and test cases were executed for 9 of them:
  $$\left( \frac{9}{10} \right) \times 100 = 90\% \quad \text{(Below Target)}$$
---

### 2. Defect Reopen Rate (DRR)
Tracks the stability of developer fixes by measuring how many resolved defects failed QA verification.

* Formula:
* Target: `< 5%`
* Example:

---
### 3. Critical Escape Rate (CER)
Measures the proportion of severe/blocking defects missed during internal QA testing that reached the Production environment.

* Formula: 
* Target: ` 0%`
* Example:

---
### 4. Automation Pass Rate (APR)
Evaluates the health and reliability of automated test execution within continuous integration pipelines.

* Formula:
* Target: `> 98%`
* Example:

---
## 3. Usage & Decision-Making
* Release gate:
* Process Improvement:
