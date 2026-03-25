### User Account Provisioning Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-011 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | IT Operations Manager |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a standardized, secure, and auditable process for granting access to Study GRC Inc. information systems. This procedure ensures that access is granted based on the Principle of Least Privilege, minimizing the risk of unauthorized access to sensitive data, including intellectual property and youth participant information.

This document explicitly satisfies the requirements of **NIST SP 800-53 Control AC-2 (Account Management)**.

### 2. Scope
This procedure applies to the creation and modification of user accounts for all Study GRC Inc. information systems, applications, and network resources.

*   **Applies to:** All Employees, Board Directors, Operational Officers, Volunteers, Contractors, and Third-Party Vendors requiring internal system access.
*   **Systems Covered:** Google Workspace, Slack, GitHub, AWS/Azure, CRM, Financial Systems, and any other corporate-managed IT assets.
*   **Exclusions:** Public-facing "Community Participant" accounts (as defined in Bylaws Article II, Section 2.1) that do not possess internal administrative privileges or access to confidential organizational data.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Provisioning** | The process of creating a user account and assigning appropriate access rights and privileges. |
| **Principle of Least Privilege (PoLP)** | The information security concept that a user should be granted the minimum levels of access—or permissions—needed to perform their job functions. |
| **Privileged Account** | An account with elevated permissions (e.g., Administrator, Root, Superuser) capable of altering system configurations or accessing all data. |
| **System Owner** | The individual responsible for the management and security of a specific IT system (e.g., the CFO is the System Owner for the accounting software). |
| **RBAC** | Role-Based Access Control; assigning permissions based on the user's role within the organization rather than individual identity. |

### 4. Procedures

#### 4.1 Pre-Provisioning Requirements
Before any technical provisioning occurs, the following administrative checks must be completed:

1.  **Identity Verification:** The identity of the user must be verified by Human Resources or the Volunteer Coordinator.
2.  **Background Check Clearance:** For roles involving access to youth data or financial systems, a background check must be adjudicated as "Clear" per the *Background Check Policy*.
3.  **Legal Documentation:**
    *   **Employees/Contractors:** Must have a signed Employment/Contractor Agreement.
    *   **Volunteers/Board:** Must have a signed Non-Disclosure Agreement (NDA) and IP Assignment Agreement pursuant to **Bylaws Article IX, Sections 9.2 and 9.3**.

#### 4.2 Access Request Initiation
Access requests must be formally documented. Verbal requests or "hallway conversations" are strictly prohibited.

1.  The **Hiring Manager** (or Board Secretary for new Directors) must submit a **New User Request Ticket** via the IT Service Desk portal.
2.  The request must include:
    *   Full Legal Name.
    *   Role/Title.
    *   Start Date.
    *   Department.
    *   Required Systems (e.g., "Standard Office Suite" vs. "Developer Access").
    *   Justification for any Privileged Access.

#### 4.3 Approval Workflow
Access is granted based on the "Need-to-Know" and "Need-to-Do" principles.

1.  **Standard Access:** Requests for standard operational tools (Email, Slack, Document Read-Access) require approval from the user's Direct Manager.
2.  **Privileged/Admin Access:** Requests for administrative rights (e.g., Global Admin, Database Write Access) require dual approval:
    *   Direct Manager; **AND**
    *   Chief Information Security Officer (CISO) or System Owner.
3.  **Financial Systems:** Access to bank accounts or bookkeeping software requires explicit written approval from the **Treasurer** or **CFO**, pursuant to internal financial controls.

#### 4.4 Technical Provisioning Steps (IT Operations)
Upon receipt of an approved request, IT Operations personnel shall:

1.  **Create Unique Identity:** Generate a unique User ID (e.g., `firstname.lastname@studygrc.org`). Generic or shared accounts (e.g., `intern@studygrc.org`) are prohibited unless explicitly authorized by the CISO with a documented owner.
2.  **Assign Group Membership:** Add the user to the appropriate RBAC groups (e.g., `Group-Volunteers-Education`, `Group-Board-Directors`).
    *   *Note:* Permissions must be assigned to Groups, not directly to Users, whenever possible.
3.  **Configure Security Controls:**
    *   Enforce Multi-Factor Authentication (MFA) enrollment immediately upon first login.
    *   Set a temporary, high-complexity password (minimum 14 characters).
    *   Configure "User Must Change Password at Next Logon."
4.  **License Allocation:** Assign necessary software licenses.

#### 4.5 Credential Transmission
To ensure security during the handover:

1.  The initial temporary password must **never** be sent via the same channel as the username.
    *   *Acceptable:* Username via email; Password via SMS/Signal/One-Time-Link.
    *   *Prohibited:* Username and Password in the same email body.
2.  The user must be provided with the *Acceptable Use Policy (AUP)* and *Information Security Policy* alongside their credentials.

#### 4.6 Post-Provisioning Verification
Within 24 hours of account activation:

1.  The IT Operations team must verify that the user has successfully logged in and changed their password.
2.  The ticket is updated with the specific access rights granted and closed.
3.  The provisioning log is retained for audit purposes in accordance with the *Document Retention Policy*.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Hiring Manager / Requestor** | Initiates the request; defines required access levels; ensures pre-requisite legal documents (NDA) are signed. |
| **Human Resources** | Verifies identity and background check clearance status. |
| **IT Operations** | Executes technical account creation; enforces MFA; transmits credentials securely. |
| **CISO** | Approves all requests for Privileged/Administrative access; audits the provisioning process. |
| **System Owner** | Defines access roles (RBAC) for their specific systems (e.g., CFO defines roles for QuickBooks). |

### 6. Compliance and Enforcement
Failure to comply with this procedure may result in disciplinary action, up to and including termination of employment or volunteer assignment.

*   **Unauthorized Provisioning:** IT staff creating accounts without proper approval are subject to immediate disciplinary review.
*   **Bylaws Reference:** Violation of data access protocols may constitute a breach of **Bylaws Article IX (Policies & Data Protection)**, potentially leading to removal for cause under **Article III, Section 3.6**.

### 7. References
*   **NIST SP 800-53 Rev 5:** Control AC-2 (Account Management)
*   **Study GRC Inc. Bylaws:** Article IX (Data Protection)
*   **IS-POL-001:** Master Information Security Policy
*   **IS-POL-003:** Access Control Policy
*   **HR-POL-005:** Background Check Policy

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name/Title] | Initial release aligned with NIST AC-2 and Bylaws. |