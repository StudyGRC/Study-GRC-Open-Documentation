### Principle of Least Privilege Implementation

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-002 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Standard is to define the mandatory technical and procedural requirements for implementing the Principle of Least Privilege (PoLP) across Study GRC Inc.'s information systems. This Standard ensures that users and systems are granted only the minimum level of access necessary to perform their explicit job functions.

This document directly satisfies **NIST CSF 2.0 PR.AC-4**, mitigating the risk of lateral movement during a security breach, insider threats, and accidental data modification. It aligns with the Organization’s commitment to protecting member data and maintaining the integrity of our open-source resources.

### 2. Scope
This Standard applies to all logical access controls within the Organization’s technology environment.

*   **Applies to:**
    *   All personnel: Board Directors, Operational Officers, Employees, Volunteers, and Contractors.
    *   All systems: Cloud infrastructure (e.g., AWS, Azure), SaaS applications (e.g., Google Workspace, GitHub, Slack), and internal databases.
    *   Service accounts and non-human identities (API keys, bots).
*   **Exclusions:**
    *   Publicly accessible areas of the Organization’s website intended for general consumption (Transparency Page, Public Resources).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Principle of Least Privilege (PoLP)** | The information security concept that a user, program, or process should have only the bare minimum privileges necessary to perform its function. |
| **Role-Based Access Control (RBAC)** | A method of restricting network access based on the roles of individual users within an enterprise. |
| **Just-In-Time (JIT) Access** | The practice of granting privileged access only for the specific duration needed to complete a task, after which access is automatically revoked. |
| **Privileged Account** | An account with elevated permissions (e.g., Administrator, Root, Superuser) capable of altering system configurations or accessing sensitive data. |
| **Data Owner** | The Operational Officer or Department Head responsible for classifying data and authorizing access to it. |

### 4. Standard Requirements

#### 4.1 Default Deny Posture
All systems must be configured to a "Default Deny" state. No access rights shall be granted implicitly. Access must be explicitly authorized based on a documented business need.

#### 4.2 Role-Based Access Control (RBAC) Alignment
Access rights must be provisioned based on the individual's role within the Organization, not their identity.

*   **4.2.1 Governance vs. Operations Separation:**
    *   **Board of Directors:** Pursuant to **Bylaws Article III**, Directors manage the affairs of the Organization but do not inherently require administrative access to operational IT systems (e.g., production databases, member directories). Board access is restricted to governance platforms (e.g., Board portal, financial reports) unless the Director holds a dual Operational Officer role as defined in **Bylaws Article V**.
    *   **Committee Members:** Access for committee members is strictly limited to the scope defined in their Committee Charter (**Bylaws Article VI**).
*   **4.2.2 Operational Roles:**
    *   Operational Officers (e.g., VP of Education, DKG) shall have access only to the specific datasets and tools required for their department.
    *   **Example:** The Director of Kindness and Generosity (DKG) requires access to community moderation tools but must not have write-access to the Financial Ledger.

#### 4.3 Privileged Account Management
*   **4.3.1 Separation of Accounts:** Users with administrative responsibilities must have two distinct accounts:
    1.  A standard user account for daily activities (email, browsing, document editing).
    2.  A separate administrative account used *only* when performing privileged tasks.
*   **4.3.2 MFA Mandate:** All privileged accounts must be protected by phishing-resistant Multi-Factor Authentication (MFA).
*   **4.3.3 No Shared Roots:** The use of shared administrative accounts (e.g., "root," "admin@studygrc") is prohibited. All administrative actions must be attributable to a specific individual.

#### 4.4 Temporal and Contextual Restrictions
*   **4.4.1 Just-In-Time (JIT) Access:** Where technically feasible, permanent standing access to critical infrastructure (Production Environments) is prohibited. Access should be granted on a JIT basis via a ticketed request and revoked immediately upon task completion.
*   **4.4.2 Account Expiration:**
    *   **Volunteers:** Access for volunteers must be set to expire automatically at the end of their agreed term or after 90 days of inactivity.
    *   **Contractors:** Access must be coterminous with the contract end date.

#### 4.5 Access Reviews and Recertification
*   **4.5.1 Quarterly Review:** The CISO and relevant Data Owners must perform a review of all privileged access rights on a quarterly basis.
*   **4.5.2 Trigger-Based Review:** Access rights must be reviewed and adjusted within 24 hours of any "Fundamental Action" (**Bylaws Article X**) or significant role change (e.g., a Director resigning per **Bylaws Section 3.7**).

#### 4.6 Development and Production Separation
To protect the integrity of the Organization's intellectual property (**Bylaws Article IX**):
*   Developers and volunteers contributing code must not have write-access to the Production environment.
*   Code deployment must occur via an automated CI/CD pipeline using a service account with minimum necessary permissions, not via individual user accounts.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Owner of this Standard. Responsible for configuring RBAC profiles, conducting access reviews, and auditing compliance. |
| **Executive Director (CEO)** | Responsible for approving high-level role definitions and authorizing access for direct reports. |
| **Data Owners (Dept Heads)** | Responsible for defining the access requirements for their specific domains (e.g., Treasurer defines access to Finance systems). |
| **Human Resources / Volunteer Coordinator** | Responsible for notifying IT immediately upon the hiring, role change, or termination of any personnel to ensure access is adjusted. |
| **All Users** | Responsible for using standard accounts for daily work and reporting any instances of perceived over-privilege (having access they do not need). |

### 6. Compliance and Enforcement
Failure to comply with this Standard may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action depending on the severity of the violation.

Unauthorized escalation of privileges or the use of administrative credentials for non-administrative tasks is a direct violation of the **Acceptable Use Policy**.

### 7. References
*   **NIST CSF 2.0 PR.AC-4:** Access permissions and authorizations are managed, incorporating the principles of least privilege and separation of duties.
*   **Study GRC Inc. Bylaws:** Article III (Board), Article V (Operational Leadership), Article VI (Committees).
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-POL-003:** Access Control Policy.
*   **IS-PRC-005:** User Account Provisioning Procedure.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name], CISO | Initial Release |