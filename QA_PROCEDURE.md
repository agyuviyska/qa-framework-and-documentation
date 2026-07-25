# 🛡️ QUALITY ASSURANCE PROCEDURE (QA PROCEDURE) - v0.3

## 1. PURPOSE & SCOPE
This procedure defines the standards, stages, and responsibilities within the Quality Assurance (QA) process throughout the Software Development Life Cycle (SDLC). The primary objective is to minimize defects, enhance customer satisfaction, and ensure compliance with ISO 9001:2015 quality management principles. This procedure applies to all software development projects within the organization.

---

## 2. ROLES & RESPONSIBILITIES

| Role | Key Responsibilities |
| :--- | :--- |
| **QA Lead / Senior QA** | Manages the overall QA strategy, defines quality metrics, coordinates the QA team, approves test environments, and provides the final QA Sign-Off prior to production releases. |
| **QA Engineer** | Develops manual test cases and checklists, writes and maintains automated test scripts (API/UI), executes test sessions, registers defects (Bug Reports), and verifies bug fixes. |
| **Product Owner / Project Manager** | Accepts the defined testing scope, defines clear Acceptance Criteria, prioritizes defects within the project backlog, and assumes business ownership when releasing with known residual defects. |

---

## 3. SOFTWARE TESTING LIFE CYCLE (STLC STAGES)

1. **Requirement Analysis:** The QA team reviews specifications, epics, or User Stories to identify logical gaps, inconsistencies, or lack of testability before core development begins (Static Testing).
2. **Test Design & Automation:** Designing detailed Test Cases within the chosen Test Management Tool. In parallel, automated test scripts (Smoke & Regression suites) are developed for critical functionalities.
3. **Test Execution:** Performing Smoke testing (build verification), followed by comprehensive functional, integration, API, and UI testing. For every new build or release candidate, Regression testing is executed to guarantee the stability of existing features.
4. **Defect Management:** Upon identifying a discrepancy, a Bug Report is logged. Defects follow a strict lifecycle (`New` ➔ `In Progress` ➔ `Ready for QA` ➔ `In testing` ➔ `Verified` ➔ `Closed`) and are classified by Severity and Priority.
5. **Test Evaluation & Sign-Off:** Analyzing test execution results, assessing residual risks, and delivering an official release readiness report (QA Sign-Off).

---

## 4. QUALITY KEY PERFORMANCE INDICATORS (KPIs)

| Metric (KPI) | Target | Description |
| :--- | :---: | :--- |
| **Requirement Coverage** | `> 95%` | The percentage of business requirements and Acceptance Criteria directly covered by valid test scenarios. |
| **Defect Reopen Rate** | `< 5%` | The percentage of defects that must be reopened due to an unsuccessful or incomplete fix by the development team. |
| **Critical Escape Rate** | `0%` | The number of critical or blocking defects missed by the QA team and discovered by end-users in the Production environment. |
| **Automation Pass Rate** | `> 98%` | The percentage of successfully passed automated test cases within the CI/CD pipeline (excluding infrastructure or network fluctuations). |