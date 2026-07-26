#QA Metrics & Key Performance Indicators (KPIs)


## Document Control & Revision History

| Version | Date       | Author        | Change Description                             |
|:--------|:-----------|:--------------|:-----------------------------------------------|
| 1.2.2   | 25-07-2026 | An. Gyuviyska | Changed "version" structure; added new section |

---

## 1. Overview
This document defines the core Quality Assurance metrics, their mathematical formula formulas, and the calculation methodologies used to assess product quality and test process efficiency throughout the Software Development Life Cycle (SDLC).

---

## 2. Metric Calculations

### 1. Requirement Coverage (RC)
Measures the percentage of defined business requirements or Acceptance Criteria covered by executed test scenarios.

* Formula:
  $$\text{Requirement Coverage (%)} = \left( \frac{\text{Executed Requirements}}{\text{Total Planned Requirements}} \right) \times 100$$

* Target: `> 95%`
* Example:  If a sprint includes 10 User Stories and test cases were executed for 9 of them:
  $$\left( \frac{9}{10} \right) \times 100 = 90\% \quad \text{(Below Target)}$$
---

### 2. Defect Reopen Rate (DRR)
Tracks the stability of developer fixes by measuring how many resolved defects failed QA verification.

* Formula:
  $$\text{Defect Reopen Rate (%)} = \left( \frac{\text{Reopened Defects}}{\text{Total Resolved Defects Tested}} \right) \times 100$$

* Target: `< 5%`
* Example:  If 20 defects were marked as `Ready for QA` by developers, and 1 failed verification:
  $$\left( \frac{1}{20} \right) \times 100 = 5\% \quad \text{(On Target)}$$

---
### 3. Critical Escape Rate (CER)
Measures the proportion of severe/blocking defects missed during internal QA testing that reached the Production environment.

* Formula:
  $$\text{Critical Escape Rate (%)} = \left( \frac{\text{Production Critical Bugs}}{\text{Total Critical Bugs (Internal + Production)}} \right) \times 100$$

* Target: ` 0%`
* Example:  If 5 critical bugs were found in QA testing and 0 were reported by end-users on Production:
  $$\left( \frac{0}{5} \right) \times 100 = 0\% \quad \text{(Target Achieved)}$$

---
### 4. Automation Pass Rate (APR)
Evaluates the health and reliability of automated test execution within continuous integration pipelines.

* Formula:
$$\text{Automation Pass Rate (%)} = \left( \frac{\text{Passed Automated Tests}}{\text{Total Executed Automated Tests}} \right) \times 100$$

* Target: `> 98%`
* Example:  If an automated Postman collection executes 150 test assertions and 149 pass:
  $$\left( \frac{149}{150} \right) \times 100 = 99.33\% \quad \text{(Target Achieved)}$$

---
## 3. Usage & Decision-Making
* Release gate:
* Process Improvement:
