# Documentation Management Procedure (BA Workflow)

## 1. Document Control & Revision History

| Version | Date       | Author        | Change Description |
|:--------|:-----------|:--------------|:-------------------|
| 1.1.3   | 25.07.2026 | An. Gyuviyska | Added new section  |

---

## 2. Objective
The purpose of this procedure is to define a standardized lifecycle for creating, reviewing, approving, and maintaining project documentation (e.g., Business Requirements, QA Test Plans, Procedures, Release Notes, Guidelines, etc...). This ensures all artifacts maintain consistent structure, clear version control, and high technical quality.

---

## 3. Scope
This procedure applies to all project documentation created within the repository, including:
- Business Requirements & User Stories
- QA Process & Procedure Guidelines
- Test Plans & Test Execution Strategy Templates
- Realise Notes
- System Architecture & README References

---

## 4. Documentation Lifecycle Statuses

| Status Name     | Stage Category | Description                                                                          |
|:----------------|:---------------|:-------------------------------------------------------------------------------------|
| **Backlog**     | Discovery      | Idea or requrement identified; logged for future prioritization and grooming.        |
| **To do**       | Planning       | Task identified and queued; work has not started yet.                                |
| **In Progress** | Drafting       | Initial draft is actively being researched and written.                              |
| **In Review**   | Validation     | Draft is complete and under peer review for missing details, versioning, and layout. |
| **Approved**    | Sign-off       | Feedback is applied and the document is ready for release.                           |
| **Done**        | Publishing     | Document is merged into main branch and published.                                   |

---

## 5. Standard Operating Procedure (SOP)

### Phase 1: Backlog & Backlog Grooming (`Backlog`)
1. Identify missing documentation, technical debt, or future scope requirements.
2. Create a Project Issue titled `[DOC] Name of Document` with initial context.
3. Keep the item in the **Backlog** column until prioritized for an upcoming iteration.


### Phase 2: dentification & Planning (`To do`)
1. Identify missing documentation or required updates.
2. Create a Project Issue titled `[DOC] Name of Document`.
3. Assign the item to the **To Do** column on the GitHub Board.

### Phase 3: Drafting & Authoring (`In Progress`)
1. Move the issue to **In Progress**.
2. Create or edit the target Markdown file in a feature branch.
3. Ensure the standard header template is present (Title, Revision History, Scope, etc.).

### Phase 4: Review & Quality Check (`In Review`)
1. Open a Pull Request (PR) and move the issue to **In Review**.
2. Perform the following checks:
    - **Versioning:** Ensure the Revision History table is updated.
    - **Completeness:** Check for missing technical requirements or edge cases.
    - **Formatting:** Verify Markdown header hierarchy, tables, and code blocks.
    - **Language:** Ensure professional technical English is used throughout.

### Phase 5: Approval (`Approved`)
1. Address and incorporate all reviewer feedback.
2. Re-request review if changes were made.
3. Once all discussions are resolved, obtain official approval (PR status becomes **Approved**).

### Phase 6: Publishing & Closure (`Done`)
1. Merge the approved Pull Request into the `main` branch.
2. Delete the temporary working branch.
3. Close the associated Issue and update its board status to **Done**.

---

## 6. Key Quality Indicators (KPIs)

- **Review Lead Time:** Average time a document stays in *In Review* before PR approval.
- **Accuracy Rate:** Absence of outdated references or missing steps in published artifacts.
- **Version Alignment:** 100% adherence to Semantic Versioning (`Major.Minor.Patch`) across all repository documents.(see [Section 7](#7-document-versioning-guidelines-semantic-versioning)).

## 7. Document Versioning Guidelines (Semantic Versioning)

All documentation artifacts must strictly follow **Semantic Versioning (SemVer)** using the `MAJOR.MINOR.PATCH` format (e.g., `1.0.0`).

| Version Type | Format  | When to Increment                                                                               | Example            |
|:-------------|:--------|:------------------------------------------------------------------------------------------------|:-------------------|
| **MAJOR**    | `X.0.0` | Complete overhaul of the document, process restructuring, or breaking changes.                  | `1.0.0` ➔ `2.0.0` |
| **MINOR**    | `1.X.0` | Addition of new sections, new workflow statuses, or guidelines without removing existing logic. | `1.0.0` ➔ `1.1.0` |
| **PATCH**    | `1.0.X` | Small fixes: typo corrections, translation of comments/text, layout fixes, or link updates.     | `1.0.0` ➔ `1.0.1` |

> **Rule:** Every published document starts at `1.0.0`. Small edits (like translating comments to English) should bump the **PATCH** version (e.g., to `1.0.1`).