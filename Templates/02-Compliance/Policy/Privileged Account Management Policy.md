### Privileged Account Management Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-014 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director (CEO) |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this policy is to establish the controls and standards for the creation, usage, monitoring, and protection of Privileged Accounts within Study GRC Inc. (the "Organization"). Misuse or compromise of privileged accounts represents a critical risk to the Organization’s mission to provide open-source GRC resources. This policy explicitly satisfies **CISA Cybersecurity Performance Goal (CPG) 2.3** by ensuring privileged access is strictly controlled, monitored, and separated from standard user activities.

### 2. Scope
This policy applies to all employees, Board Directors, contractors, volunteers, and third-party vendors who possess administrative or elevated access rights to the Organization’s Information Systems.

**In Scope:**
*   Domain Administrator accounts (e.g., Google Workspace Super Admins).
*   Cloud Infrastructure root/IAM admin accounts (e.g., AWS, Azure).
*   Application Administrators (e.g., GitHub Organization Owners, Slack Admins).
*   Database Administrators (DBAs).
*   Financial System Administrators (e.g., QuickBooks Online Admins).
*   Social Media Account Administrators.

**Exclusions:**
*   Standard user accounts with no elevated privileges.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Privileged Account** | An account with elevated permissions that allow the user to configure systems, manage other accounts, access sensitive data, or bypass security controls (e.g., "root," "admin," "superuser"). |
| **Least Privilege** | The principle that a user or process should only be granted the minimum level of access (or privileges) necessary to perform their specific job function. |
| **Separation of Duties** | A security concept where critical tasks are divided among different people to prevent error or fraud. In this context, it also refers to separating administrative accounts from standard user accounts. |
| **Break-Glass Account** | A highly privileged emergency account used only when normal administrative access methods fail or during a catastrophic system failure. |
| **MFA** | Multi-Factor Authentication; requiring two or more verification methods to gain access. |

### 4. Policy Statements

#### 4.1 Principle of Least Privilege (PoLP)
In accordance with **Bylaws Article V, Section 5.2** regarding the CISO's duty to protect data, all access rights must be granted based on the Principle of Least Privilege.
*   Privileged access is granted only when explicitly required by a job role or volunteer assignment.
*   Privileges must be limited to the specific resources and timeframe necessary to perform the required task.
*   "Standing privileges" (permanent admin access) must be minimized in favor of Just-in-Time (JIT) access where technically feasible.

#### 4.2 Separation of Accounts (Prohibition of Dual-Use)
To comply with **CISA CPG 2.3**, the use of a single account for both administrative and standard daily activities is **strictly prohibited**.
*   **Standard Account:** Used for email, web browsing, document creation, and general communication.
*   **Privileged Account:** Used **only** for administrative tasks (e.g., system configuration, user management).
*   **Naming Convention:** Privileged accounts must be clearly distinguishable (e.g., `admin.jdoe@studygrc.org` vs. `jdoe@studygrc.org`).
*   **Restriction:** Privileged accounts must not be used to browse the internet or access external email, as these activities increase exposure to phishing and malware.

#### 4.3 Inventory and Review
The CISO shall maintain a definitive **Privileged Account Inventory** identifying all active privileged accounts, the assigned individual, and the justification for access.
*   **Quarterly Review:** A review of all privileged access rights must be conducted every 90 days.
*   **Dormancy:** Privileged accounts inactive for more than 30 days must be disabled immediately.
*   **Termination:** Upon the resignation or termination of an individual (referencing **Bylaws Article III, Section 3.7** for Directors or HR policies for staff), privileged access must be revoked **immediately** (within 1 hour of notification).

#### 4.4 Authentication and Security Controls
*   **Mandatory MFA:** Multi-Factor Authentication is **mandatory** for *all* privileged accounts without exception. Hardware security keys (e.g., YubiKey) are the preferred method for Root/Super Admin accounts.
*   **Password Complexity:** Passwords for privileged accounts must exceed standard complexity requirements (minimum 16 characters) or utilize passwordless authentication methods.
*   **Password Managers:** Credentials for shared privileged accounts (where unavoidable) must be stored in the Organization’s approved enterprise password manager, with access logging enabled.

#### 4.5 Emergency "Break-Glass" Accounts
To ensure business continuity during a "No Board" or catastrophic scenario (referencing **Bylaws Article III, Section 3.10**), specific emergency accounts must be created.
*   Credentials for break-glass accounts must be vaulted and split (e.g., password known by the CISO, MFA token held by the President).
*   Usage of a break-glass account must trigger an immediate high-priority alert to the Board of Directors and the Audit Committee.

#### 4.6 Vendor and Third-Party Access
*   Vendors requiring privileged access must sign a Non-Disclosure Agreement (NDA) per **Bylaws Article IX, Section 9.2**.
*   Vendor accounts must be temporary, monitored, and disabled immediately upon completion of the contracted work.

#### 4.7 Prohibited Conduct
*   Sharing personal privileged credentials with any other individual.
*   Hard-coding privileged credentials into software code or scripts (referencing **Bylaws Article IX, Section 9.3** regarding Intellectual Property/Code).
*   Using privileged accounts to access data outside the scope of authorized administrative duties (e.g., reading other employees' emails without legal authorization).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Owner of this policy. Maintains the Privileged Account Inventory. Conducts quarterly access reviews. |
| **System Owners** | Responsible for approving requests for privileged access to their specific systems based on valid business justification. |
| **Privileged Users (Admins)** | Adhere to the separation of accounts rule. Protect credentials. Use privileges only for authorized tasks. |
| **HR / Volunteer Coordinators** | Notify IT/Security immediately (prior to or at the moment of) any termination or role change involving a privileged user. |
| **Audit Committee** | Reviews reports on privileged access violations and validates the quarterly review process. |

### 6. Compliance and Enforcement
Failure to comply with this policy may result in disciplinary action, up to and including termination of employment, removal from volunteer service, or expulsion from membership.

Any user found to be abusing privileged access to view confidential data without authorization, or to bypass security controls, will be subject to immediate revocation of access and potential legal action.

### 7. References
*   **CISA Cybersecurity Performance Goal (CPG) 2.3:** Manage Privileged Access.
*   **NIST SP 800-53 (AC-6):** Least Privilege.
*   **Study GRC Inc. Bylaws:** Article III (Governance), Article V (Operational Leadership), Article IX (Data Protection).
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-POL-003:** Access Control Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Legal Officer | Initial Draft aligned with CISA CPG 2.3 and Bylaws. |