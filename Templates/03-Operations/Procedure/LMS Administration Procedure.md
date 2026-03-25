### LMS Administration Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-013 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | VP of Education & Training |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish the standards and operational steps for the administration, maintenance, and security of the Study GRC Inc. Learning Management System (LMS). This procedure ensures that the delivery of educational resources aligns with the Organization’s mission to provide "zero-cost, open-source resources" (Bylaws Article I, Section 1.3) while maintaining strict data privacy, system availability, and content integrity.

### 2. Scope
This procedure applies to all Study GRC Inc. personnel, volunteers, and contractors who have administrative or instructor-level access to the LMS.
*   **In Scope:** User account management, course publishing workflows, system patching, data backup, and plugin management.
*   **Out of Scope:** The pedagogical design of curriculum (refer to *Curriculum Development Procedure*) and end-user (learner) technical support, unless escalated to system administration.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **LMS** | Learning Management System; the software application used to administer, document, track, report, and deliver educational courses. |
| **RBAC** | Role-Based Access Control; restricting system access to authorized users based on their role within the organization. |
| **PII** | Personally Identifiable Information; any data that could potentially identify a specific individual. |
| **SCORM/xAPI** | Technical standards for eLearning software products. |
| **Maintenance Window** | A pre-defined period during which system changes are permitted, potentially causing service interruption. |

### 4. Procedures

#### 4.1 User Account Management & Access Control
To maintain the integrity of the educational platform, access is granted on a Principle of Least Privilege basis.

1.  **Role Assignment:**
    *   **Learner:** Default role for public registrants. Read-only access to published content.
    *   **Instructor:** Assigned only to individuals vetted per the *Instructor Qualification Standard*. Can grade assessments and view roster data for their specific courses only.
    *   **Content Creator:** Can draft and upload content but cannot publish live to the catalog.
    *   **LMS Administrator:** Full system access. Limited to the VP of Education & Training and designated IT staff.
2.  **Privileged Access Review:**
    *   The CISO and VP of Education & Training must review all Administrator and Instructor accounts quarterly.
    *   Accounts belonging to inactive volunteers must be deprovisioned within 24 hours of their departure.
3.  **Authentication:**
    *   All Administrator and Instructor accounts must enforce Multi-Factor Authentication (MFA) in accordance with *IS-POL-005 (Master Information Security Policy)*.

#### 4.2 Course Publishing Workflow
To ensure quality and legal compliance regarding Intellectual Property (Bylaws Article IX, Section 9.3).

1.  **Staging:** Content Creators must upload course materials (videos, text, quizzes) to the "Staging" or "Draft" environment.
2.  **QA Review:** The VP of Education & Training (or designee) must review the course for:
    *   Technical functionality (broken links, video playback).
    *   Accessibility compliance (WCAG 2.2 AA standards).
    *   Alignment with the *Code of Ethics*.
3.  **IP Verification:** The reviewer must confirm that all materials are either original works owned by Study GRC Inc. or properly licensed open-source materials.
4.  **Publication:** Only the VP of Education & Training or a designated LMS Administrator may toggle a course status to "Published/Live."

#### 4.3 System Maintenance and Updates
1.  **Patch Management:**
    *   Critical security patches for the LMS core software or plugins must be applied within 72 hours of release.
    *   Non-critical updates are applied during the monthly Maintenance Window (typically the third Sunday of the month, 02:00 UTC).
2.  **Plugin Management:**
    *   Installation of new LMS plugins or extensions requires prior approval from the CISO to evaluate security risks and data exfiltration potential.
    *   Unused plugins must be uninstalled, not just deactivated.

#### 4.4 Data Privacy and Youth Protection
Given the Organization's commitment to removing barriers, the LMS may be accessed by minors.

1.  **Data Minimization:** The LMS must not collect more PII than is strictly necessary for account creation (Name, Email).
2.  **Direct Messaging:**
    *   To comply with *Youth Protection Policies*, direct private messaging between Learner accounts and Instructor accounts must be disabled or strictly logged and monitored.
    *   "Two-Deep" leadership rules apply to all virtual interactions.
3.  **Anonymization:**
    *   Learner data used for reporting or analytics must be anonymized before being shared with the Board or external stakeholders.

#### 4.5 Backup and Disaster Recovery
1.  **Frequency:**
    *   **Database:** Incremental backups every 6 hours; Full backups daily.
    *   **Files/Content:** Daily backups.
2.  **Retention:** Backups are retained for 30 days in an immutable, off-site cloud storage bucket.
3.  **Restoration Testing:** The LMS Administrator must perform a restoration test from backup files once per quarter to verify data integrity.

#### 4.6 Zero-Cost Configuration
1.  **Payment Gateways:**
    *   In accordance with Bylaws Article I, Section 1.3, payment gateways within the LMS must be disabled or configured to process transactions at $0.00.
    *   Any feature requiring a "paywall" is strictly prohibited unless authorized by the Board for specific fundraising events (e.g., a paid workshop distinct from core resources).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **VP of Education & Training** | Owner of the LMS. Approves all course content for publication. Ensures curriculum aligns with mission. |
| **LMS Administrator** | Performs technical maintenance, user provisioning, and patch management. Executes backups. |
| **CISO** | Approves plugins/extensions. Audits access logs. Oversees incident response regarding LMS data. |
| **Instructors** | Manage day-to-day course interactions (grading, forums). Report technical issues to the Administrator. |
| **Executive Director** | Final escalation point for disputes regarding user bans or content removal. |

### 6. Compliance and Enforcement
Failure to comply with this procedure may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action depending on the severity of the violation. Unauthorized modification of LMS records or grades is considered a severe ethical violation.

### 7. References
*   **Bylaws of Study GRC Inc.** (Specifically Art. I §1.3, Art. V §5.2, Art. IX §9.3)
*   **IS-POL-001:** Master Information Security Policy
*   **IS-POL-005:** Access Control Policy
*   **HR-POL-020:** Child and Youth Safeguarding Policy
*   **OPS-STD-004:** Digital Accessibility Standards (WCAG 2.2)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Compliance Architect | Initial Release |