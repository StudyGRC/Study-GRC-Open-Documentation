### Account Review and Re-Certification

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-013 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-04-25 (Bi-Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Director of IT Operations |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to mandate and standardize the periodic review of user access rights to Study GRC Inc. information systems and data. This procedure ensures adherence to the **Principle of Least Privilege (PoLP)**, mitigates the risk of unauthorized access by dormant or terminated accounts, and satisfies internal control requirements mandated by **2 CFR 200.303** and **NIST CSF 2.0 (PR.AC-1)**. This process verifies that only authorized individuals maintain access appropriate to their current role.

### 2. Scope
This procedure applies to all information systems, applications, databases, and network infrastructure owned, leased, or operated by Study GRC Inc.

*   **Applies to:** All user accounts (employees, volunteers, contractors, Board members, and third-party vendors) and service accounts.
*   **Exclusions:** Public-facing accounts with no internal privileges (e.g., community forum participants with "read-only" or standard "posting" access, provided they have no administrative capabilities).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **User Access Review (UAR)** | The periodic process of validating that a user's access rights are commensurate with their current job responsibilities. |
| **Privileged Account** | An account with elevated permissions (e.g., Administrator, Root, Superuser) capable of altering system configurations or accessing sensitive data. |
| **System Owner** | The individual responsible for the management and operation of a specific IT asset or application (e.g., the VP of Education is the System Owner for the LMS). |
| **Principle of Least Privilege (PoLP)** | The information security concept that a user should be granted the minimum level of access necessary to perform their job functions. |
| **Dormant Account** | An account that has not been logged into for a period exceeding 90 days. |

### 4. Procedures

#### 4.1 Review Frequency and Schedule
To maintain security without overburdening operational staff, reviews are categorized by risk level:

1.  **Privileged Accounts (High Risk):** Must be reviewed **Quarterly** (January, April, July, October).
2.  **Standard User Accounts (Medium Risk):** Must be reviewed **Semi-Annually** (January, July).
3.  **Service/System Accounts:** Must be reviewed **Annually** (January).

#### 4.2 Phase 1: Preparation (Initiation)
**Responsible Role:** IT Security Team

1.  **Generate User Lists:** On the first business day of the review month, the IT Security Team must extract a current list of all active accounts from each in-scope system (e.g., Google Workspace, GitHub, LMS, Accounting Software).
2.  **Generate Employment/Volunteer Roster:** Obtain the current "Source of Truth" roster from HR (for employees) and the Volunteer Coordinator (for volunteers).
3.  **Distribute Lists:** Send the system-specific user lists to the designated **System Owners** via the ticketing system or secure email.

#### 4.3 Phase 2: The Review Process
**Responsible Role:** System Owners

Upon receipt of the user list, the System Owner must verify the following for *every* account:

1.  **Identity Verification:** Does this account belong to a currently active employee, volunteer, or contractor?
    *   *Action:* Cross-reference with the HR/Volunteer Roster.
2.  **Role Verification:** Is the level of access (permissions/groups) appropriate for the user's *current* role?
    *   *Check:* Has the user changed departments? Have they moved from a Board role to an Advisory role?
3.  **Usage Verification:** Is the account active?
    *   *Check:* Identify accounts with "Last Login" > 90 days.
4.  **Determination:** Mark each account as:
    *   **Retain:** Access is correct.
    *   **Modify:** Access is too broad and needs reduction.
    *   **Revoke:** User is terminated, role has changed significantly, or account is dormant.

#### 4.4 Phase 3: Remediation
**Responsible Role:** IT Operations / System Administrators

1.  **Execute Changes:** Within five (5) business days of the System Owner's determination, IT Operations must:
    *   Disable accounts marked "Revoke."
    *   Adjust permissions for accounts marked "Modify."
2.  **Confirm Completion:** Update the review ticket confirming that all requested changes have been technically implemented.

#### 4.5 Phase 4: Certification and Sign-Off
**Responsible Role:** System Owners & CISO

1.  **Formal Sign-Off:** The System Owner must sign (electronically via ticketing system or DocuSign) the reviewed list, certifying: *"I have reviewed the access rights for [System Name] and certify that all users listed are authorized and hold appropriate privileges."*
2.  **Audit Trail Storage:** The finalized review, including the original list, the marked changes, and the remediation confirmation, must be stored in the **Governance, Risk, and Compliance (GRC) Repository** for a minimum of three (3) years.

#### 4.6 Handling Discrepancies and Exceptions
1.  **Immediate Revocation:** If a terminated employee or volunteer is found to still have active access during a review, access must be revoked **immediately** (within 1 hour of discovery), and an Incident Report must be filed per the *Incident Response Plan*.
2.  **Extension Requests:** If a System Owner cannot complete the review by the deadline due to extenuating circumstances, they must submit a formal risk acceptance request to the CISO.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **CISO** | Accountable for the overall success of the UAR process; monitors compliance; reports systemic risks to the Board. |
| **IT Security Team** | Facilitates the process; generates user lists; ensures "Source of Truth" data is available. |
| **System Owner** | Responsible for the accuracy of access within their specific domain (e.g., VP of Education reviews LMS access). |
| **HR / Volunteer Coordinator** | Provides accurate, up-to-date rosters of active personnel to facilitate comparison. |
| **Internal Audit** | Periodically validates that reviews are occurring according to this schedule and that remediation was effective. |

### 6. Compliance and Enforcement
Failure to comply with this procedure puts Study GRC Inc. at significant risk of data breach, intellectual property theft, and non-compliance with federal grant requirements.

*   **System Owners** who fail to complete reviews by the deadline may have their administrative privileges suspended until the review is submitted.
*   **Employees/Volunteers** found to be hoarding access rights or bypassing access controls may face disciplinary action, up to and including termination of employment or volunteer assignment, in accordance with the *Sanctions Policy*.

### 7. References
*   **Study GRC Bylaws Article IX, Section 9.2:** Confidentiality & NDA.
*   **Study GRC Bylaws Article V, Section 5.2:** CISO Responsibilities.
*   **NIST CSF 2.0 (PR.AC-1):** Identities and credentials are managed.
*   **NIST CSF 2.0 (PR.AC-4):** Access permissions and authorizations are managed.
*   **2 CFR 200.303:** Internal Controls for Federal Award Recipients.
*   **IS-POL-001:** Master Information Security Policy.
*   **HR-PRC-005:** Offboarding/Account Deprovisioning Checklist.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Legal Officer | Initial Draft and Release |