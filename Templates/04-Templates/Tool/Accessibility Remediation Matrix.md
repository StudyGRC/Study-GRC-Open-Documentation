### Accessibility Remediation Matrix

| Document Control | |
| :--- | :--- |
| **Document ID** | ACC-TOL-001 |
| **Document Type** | Tool / Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | VP of Education & Training |
| **Classification** | Public |

### 1. Purpose
The purpose of this **Accessibility Remediation Matrix** is to provide a standardized framework for categorizing, prioritizing, and scheduling the remediation of digital accessibility barriers found within Study GRC Inc.’s ecosystem.

In accordance with **Bylaws Article I, Section 1.3**, which commits the Organization to "removing barriers," and **Article IX**, which governs data and policy, this tool ensures that accessibility defects are triaged based on their impact on user experience and civil rights compliance (ADA, Section 508, WCAG 2.2). This matrix eliminates subjectivity in the bug-tracking process, ensuring that "Blockers" affecting Assistive Technology (AT) users are treated with the same urgency as functional system outages.

### 2. Scope
This matrix applies to all digital assets owned, developed, or maintained by Study GRC Inc., including but not limited to:
*   Public-facing websites and marketing materials.
*   The Learning Management System (LMS) and educational curriculum.
*   Internal tools used by employees and volunteers.
*   Third-party integrations where configuration controls exist.
*   PDFs, documents, and multimedia content.

**Exclusions:** Legacy archived content explicitly labeled as non-conforming and not currently in active use for educational certification.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **WCAG 2.2** | Web Content Accessibility Guidelines, the international standard for web accessibility. |
| **Assistive Technology (AT)** | Software or hardware used by people with disabilities to interact with digital content (e.g., screen readers, switch devices, screen magnifiers). |
| **Critical Path** | The sequence of steps a user must take to complete a core function (e.g., registering for a course, donating, logging in). |
| **Blocker** | A defect that prevents a user from completing a task entirely; no workaround exists. |
| **Remediation** | The process of fixing code, design, or content to meet accessibility standards. |

### 4. Remediation Prioritization Logic

All identified accessibility issues must be scored using the **Impact Severity Scale** (4.1) and assigned a **Remediation Service Level Agreement (SLA)** (4.2).

#### 4.1 Impact Severity Scale

| Severity Level | Classification | Impact Description | WCAG Alignment |
| :--- | :--- | :--- | :--- |
| **Level 1** | **Critical (Blocker)** | **User cannot access content or complete a core task.** The barrier renders a feature unusable for specific groups (e.g., keyboard-only users, screen reader users). No reasonable workaround exists. <br><br>*Examples: Keyboard trap, missing form labels on registration, video without captions, flashing content (seizure risk).* | **Level A** (Non-conformance) |
| **Level 2** | **High (Major)** | **User can complete the task, but with significant difficulty or frustration.** A workaround exists but is difficult to discover or perform. The experience is unequal compared to non-disabled users. <br><br>*Examples: Poor focus order, low contrast on essential text, missing headings structure, non-descriptive link text ("Click Here").* | **Level AA** (Non-conformance) |
| **Level 3** | **Medium (Minor)** | **User is annoyed or confused, but task completion is not impeded.** The issue causes minor inconvenience or requires extra steps but does not stop progress. <br><br>*Examples: Inconsistent navigation styles, minor HTML validation errors that don't break parsing, decorative images with redundant alt text.* | **Level AA** (Technical non-conformance) |
| **Level 4** | **Low (Cosmetic)** | **Does not affect functionality or understanding.** Issues are primarily aesthetic or related to best practices rather than strict compliance failures. <br><br>*Examples: Layout shifts that do not obscure content, contrast issues on non-essential decorative elements.* | **Level AAA** (Target) or Best Practice |

#### 4.2 Remediation SLA (Service Level Agreement)

Once a Severity Level is assigned, the issue must be scheduled for remediation according to the following timelines.

| Priority Code | Severity Level | Required Action | Remediation Timeline |
| :--- | :--- | :--- | :--- |
| **P0** | **Critical** | **Immediate Hotfix.** Stop the line. If the issue is on a live production environment affecting the Critical Path, it must be addressed immediately. | **< 48 Hours** (or immediate rollback of deployment) |
| **P1** | **High** | **Next Sprint.** Must be prioritized in the immediate backlog. New features cannot be released until P1 issues in that feature are resolved. | **< 14 Days** (Next scheduled release) |
| **P2** | **Medium** | **Scheduled Backlog.** To be addressed during standard maintenance cycles or "tech debt" sprints. | **< 90 Days** (Quarterly) |
| **P3** | **Low** | **Backlog / Won't Fix.** Addressed only if resources allow or during a major redesign/refactor. | **Discretionary** |

#### 4.3 Youth Protection & Education Multiplier
Pursuant to the Organization's focus on K-12 education and **Bylaws Article I** (Educational Purposes), any defect found in **educational materials intended for minors** or **safety reporting mechanisms** is automatically escalated by one Priority Code (e.g., a P2 Medium issue in a youth course becomes a P1 High priority).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Product Owner / Project Manager** | Responsible for assigning the Priority Code (P0-P3) in the ticketing system (e.g., Jira/GitHub) based on this matrix. Ensures P0/P1 items are not de-prioritized for new features. |
| **QA / Accessibility Specialist** | Identifies the defect and assigns the initial Severity Level (1-4). Verifies the fix meets WCAG criteria before closing the ticket. |
| **Developers / Content Creators** | Responsible for executing the remediation within the timeline defined by the SLA. |
| **Executive Director** | Final authority on accepting risk for any P1 or P2 items that exceed the SLA timeline due to resource constraints. |

### 6. Compliance and Enforcement
Failure to adhere to this matrix, particularly the willful ignoring of **Level 1 (Critical)** barriers in production environments, constitutes a violation of the **Digital Accessibility Policy** and the **Code of Ethics**.

*   **Launch Blocking:** The VP of Education & Training or the CISO has the authority to block any release that contains known **P0** accessibility defects.
*   **Audit Trail:** All decisions to defer remediation of P1 or P2 issues must be documented in the risk register with a rationale and a target resolution date.

### 7. References
*   **ACC-POL-001:** Digital Accessibility Policy
*   **GOV-CHT-002:** Bylaws of Study GRC Inc. (Article I & IX)
*   **W3C Recommendation:** Web Content Accessibility Guidelines (WCAG) 2.2
*   **Regulation:** Americans with Disabilities Act (ADA) Title III

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Compliance Architect | Initial release of remediation matrix and SLA definitions. |