# 🛡️ QUALITY ASSURANCE PROCEDURE (QA PROCEDURE)


## Document Control & Revision History

| Version | Date       | Author        | Change Description                             |
|:--------|:-----------|:--------------|:-----------------------------------------------|
| 1.2.0   | 02-08-2026 | An. Gyuviyska | Changed "version" structure; added new section |

---

## 1. PURPOSE & SCOPE
This procedure defines the standards, stages, and responsibilities within the Quality Assurance (QA) process throughout the Software Development Life Cycle (SDLC). The primary objective is to minimize defects, enhance customer satisfaction, and ensure compliance with ISO 9001:2015 quality management principles. This procedure applies to all software development projects within the organization.

---

## 2. ROLES & RESPONSIBILITIES

| Role                                | Key Responsibilities                                                                                                                                                                             |
|:------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **QA Lead / Senior QA**             | Manages the overall QA strategy, defines quality metrics, coordinates the QA team, approves test environments, and provides the final QA Sign-Off prior to production releases.                  |
| **QA Engineer**                     | Develops manual test cases and checklists, writes and maintains automated test scripts (API/UI), executes test sessions, registers defects (Bug Reports), and verifies bug fixes.                |
| **Product Owner / Project Manager** | Accepts the defined testing scope, defines clear Acceptance Criteria, prioritizes defects within the project backlog, and assumes business ownership when releasing with known residual defects. |

---

## 3. SOFTWARE TESTING LIFE CYCLE (STLC STAGES)

1. **Requirement Analysis:** The QA team reviews specifications, epics, or User Stories to identify logical gaps, inconsistencies, or lack of testability before core development begins (Static Testing).
2. **Test Design & Automation:** Designing detailed Test Cases within the chosen Test Management Tool. In parallel, automated test scripts (Smoke & Regression suites) are developed for critical functionalities.
3. **Test Execution:** Performing Smoke testing (build verification), followed by comprehensive functional, integration, API, and UI testing. For every new build or release candidate, Regression testing is executed to guarantee the stability of existing features.
4. **Defect Management:** Upon identifying a discrepancy, a Bug Report is logged following the strict lifecycle (`New` ➔ `In Progress` ➔ `Ready for QA` ➔ `In testing` ➔ `Verified` ➔ `Closed`).
    * **Severity (Technical Impact - Set by QA):**
        * `Blocker`: Prevents further testing or development; blocks the entire application or execution of test suites.
        * `Critical`: Severe breakdown of a core feature or data corruption with no available workaround.
        * `Major`: Significant functionality issue, but a reasonable workaround exists.
        * `Minor`: Secondary feature issue or minor functionality flaw.
        * `Cosmetic`: UI misalignment, formatting errors, typos, or aesthetic issues with no functional impact.
    * **Priority (Business Urgency - Set by Product Owner / PM):**
        * `High`: Must be fixed immediately in the current sprint or hotfix.
        * `Medium`: Fix should be planned for the next regular release.
        * `Low`: Optional fix, to be resolved when time permits.
5. **Test Evaluation & Sign-Off:** Analyzing test execution results, assessing residual risks, and delivering an official release readiness report (QA Sign-Off).

---

## 4. WORK ITEM TYPES & QA SCOPE

| Work Item Type               | Primary Focus                                 | QA Responsibility & Scope                                                                                                                               |
|:-----------------------------|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **User Story** *(Parent)*    | Business value & user functionality           | Review Acceptance Criteria, design E2E scenarios, and perform final acceptance testing. Verify that all linked child tasks are complete before closing. |
| **Technical Task** *(Child)* | Implementation details (DB, API, Refactoring) | Perform targeted component/technical testing (e.g., Postman for API endpoints, DB checks). Verifies individual technical criteria.                      |
| **Bug Report**               | Defect / Discrepancy from specs               | Log detailed reproduction steps, classify Severity/Priority, attach logs/screenshots, verify fixes, and perform regression checks.                      |

---

## 5. QUALITY KEY PERFORMANCE INDICATORS (KPIs)

| Metric (KPI)             | Target  | Description                                                                                                                              |
|:-------------------------|:-------:|:-----------------------------------------------------------------------------------------------------------------------------------------|
| **Requirement Coverage** | `> 95%` | The percentage of business requirements and Acceptance Criteria directly covered by valid test scenarios.                                |
| **Defect Reopen Rate**   | `< 5%`  | The percentage of defects that must be reopened due to an unsuccessful or incomplete fix by the development team.                        |
| **Critical Escape Rate** |  `0%`   | The number of critical or blocking defects missed by the QA team and discovered by end-users in the Production environment.              |
| **Automation Pass Rate** | `> 98%` | The percentage of successfully passed automated test cases within the CI/CD pipeline (excluding infrastructure or network fluctuations). |

---

## 6. RELATED QA ARTEFACTS & TEMPLATES

| Document / Template              | Description & Purpose                                                             | Location / Link                                 |
|:---------------------------------|:----------------------------------------------------------------------------------|:------------------------------------------------|
| **Bug Report Template**          | Standardized template for logging defects via Issues.                             | `docs/templates/BUG_REPORT_TEMPLATE.md`         |
| **Test Plan Template**           | Standard structure for defining testing strategy, scope, risks, and test design.  | `docs/templates/TEST_PLAN_TEMPLATE.md`          |
| **QA Metrics & KPIs**            | Comprehensive framework tracking defect leakage, pass rates, and quality metrics. | `docs/QA_METRICS_AND_KPIS.md`                   |
| **Documentation Procedure**      | Guidelines and standards for maintaining QA project documentation.                | `docs/DOCUMENTATION_PROCEDURE.md`               |
| **Test Report Example**          | Practical example of an executed test evaluation and release readiness report.    | `docs/TEST_REPORT_EXAMPLE.md`                   |