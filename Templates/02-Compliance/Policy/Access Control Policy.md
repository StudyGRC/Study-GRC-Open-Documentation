### Access Control Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-009 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Access Control Policy is to establish the technical and procedural standards for granting, modifying, and revoking access to Study GRC Inc. (the "Organization") information systems and data. This policy is designed to protect the confidentiality, integrity, and availability of organizational assets by ensuring that access is restricted to authorized users based on the principle of least privilege.

This policy aligns with **NIST Cybersecurity Framework (CSF) 2.0 Function: Protect (PR.AC)** and **CISA Cybersecurity Performance Goals (CPG)** regarding account security and access management.

### 2. Scope
This policy applies to all "Users" (including employees, Board Directors, volunteers, contractors, and temporary staff) and all Information Systems owned, leased, or operated by the Organization. This includes, but is not limited to:
*   Cloud-based infrastructure (e.g., AWS, Azure).
*   SaaS applications (e.g., Google Workspace, GitHub, Slack, Donor Management Systems).
*   Remote access mechanisms (VPN, SSO).
*   Physical records and computing devices.

**Exclusions:** Public-facing content on the Organization’s website intended for general consumption is exempt from authentication requirements.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Access Control** | The process of granting or denying specific requests to: 1) obtain and use information and related information processing services; and 2) enter specific physical facilities. |
| **Least Privilege** | The security principle that users should be granted the minimum level of access (privilege) necessary to perform their job functions and no more. |
| **MFA (Multi-Factor Authentication)** | An authentication method that requires the user to provide two or more verification factors to gain access to a resource (e.g., a password + a hardware token or mobile app code). |
| **Privileged Account** | An account with elevated permissions (e.g., Administrator, Root, Superuser) capable of altering system configurations, access rights, or security settings. |
| **RBAC (Role-Based Access Control)** | A method of restricting network access based on the roles of individual users within the Organization. |
| **User** | Any individual or system process authorized to access an information system. |

### 4. Policy Statements

#### 4.1 General Principles
4.1.1 **Principle of Least Privilege:** Access to data and systems must be granted solely based on the user's job responsibilities. Default access levels must be set to "Deny All" unless explicitly allowed.
4.1.2 **Need-to-Know:** Access to specific information (particularly Sensitive Personal Data or Youth Data) is restricted to individuals whose specific duties require such access.
4.1.3 **Separation of Duties:** Where operationally feasible, critical functions must be divided among different individuals to ensure that no single person has total control over a critical process (e.g., the person who approves a payment cannot be the same person who initiates it).

#### 4.2 User Registration and De-registration
4.2.1 **Unique Identification:** Every User must be issued a unique User ID. The use of shared, generic, or group accounts (e.g., "intern@studygrc.org" shared by three people) is strictly prohibited (CISA CPG 2.3).
4.2.2 **Provisioning:** Access is granted only upon receipt of a documented request approved by the User’s direct supervisor and the System Owner.
4.2.3 **De-provisioning (Termination):** Upon termination of employment, contract, or volunteer service:
*   Access to all systems must be revoked within **24 hours** of the effective termination date/time (CISA CPG 2.4).
*   In cases of involuntary termination (Hostile Exit), access must be revoked immediately prior to notification of the individual.

#### 4.3 Authentication Management
4.3.1 **Multi-Factor Authentication (MFA):** MFA is **mandatory** for all remote access, cloud-based email, administrative access, and any system housing Sensitive Personal Data. SMS-based MFA should be avoided in favor of App-based authenticators or hardware keys where supported (CISA CPG 2.1).
4.3.2 **Password Complexity:** Passwords must adhere to the Organization's *Password Policy*, requiring a minimum length of 12 characters. Complexity requirements must not enforce arbitrary rotation unless a compromise is suspected (NIST SP 800-63B).
4.3.3 **Default Passwords:** All vendor-supplied default passwords must be changed immediately upon system installation or deployment (CISA CPG 2.2).

#### 4.4 Privileged Access Management (PAM)
4.4.1 **Administrative Accounts:** Users with administrative privileges must have two separate accounts: one for standard daily work (email, web browsing) and a separate "Admin" account for system administration tasks.
4.4.2 **Review of Privileges:** The use of Privileged Accounts must be logged and monitored.
4.4.3 **Emergency Access:** "Break-glass" accounts for emergency system access must be kept in a secure, vaulted location (e.g., enterprise password manager) and their usage must trigger an immediate alert to the CISO.

#### 4.5 Access Review and Re-certification
4.5.1 **Periodic Review:** The CISO or designee must conduct a review of user access rights at least **semi-annually** (every 6 months).
4.5.2 **Privileged Access Review:** Accounts with administrative privileges must be reviewed **quarterly**.
4.5.3 **Dormant Accounts:** User accounts that have been inactive for **90 days** must be automatically disabled.

#### 4.6 Remote and Third-Party Access
4.6.1 **Remote Access:** All remote access to internal resources not exposed via public SaaS must be tunneled through an approved VPN or Zero Trust Network Access (ZTNA) solution.
4.6.2 **Vendor Access:** Third-party vendors requiring access to the Organization's systems must:
*   Sign a Non-Disclosure Agreement (NDA) per Bylaws Article IX, Section 9.2.
*   Be granted access only for the specific time window required to perform maintenance or support.
*   Be monitored during their session.

#### 4.7 Data Protection for Minors (Youth Safeguarding)
4.7.1 **Youth Data Segregation:** In accordance with the Organization's *Child and Youth Safeguarding Policy*, access to databases containing Personally Identifiable Information (PII) of minors is restricted to a pre-approved list of "Youth-Vetted" staff and volunteers.
4.7.2 **Audit Trails:** All access to Youth Data must generate an immutable audit log.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Defined in Bylaws Art. V §5.2. Responsible for the overall implementation of this policy, conducting access reviews, and investigating violations. |
| **System Owners** | Responsible for defining access requirements for their specific systems and approving access requests. |
| **Managers / Supervisors** | Responsible for requesting access for their staff and notifying IT/HR immediately upon a staff member's termination or role change. |
| **Users (Staff/Volunteers)** | Responsible for keeping their credentials confidential, not sharing passwords, and reporting any suspected unauthorized access. |
| **HR Department** | Responsible for notifying the CISO/IT team of all new hires, terminations, and role changes prior to the effective date. |

### 6. Compliance and Enforcement
Failure to comply with this policy may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action depending on the severity of the violation.

Unauthorized access to computer systems is a violation of federal law (Computer Fraud and Abuse Act) and Texas State Law (Texas Penal Code Chapter 33). The Organization reserves the right to report such violations to law enforcement.

### 7. References
*   **NIST Cybersecurity Framework 2.0:** PR.AC (Identity Management, Authentication, and Access Control)
*   **CISA Cybersecurity Performance Goals (CPG):** 2.1 (MFA), 2.2 (Default Passwords), 2.3 (Unique Credentials), 2.4 (Revocation).
*   **Study GRC Bylaws:** Article V (Operational Leadership), Article IX (Confidentiality).
*   **Study GRC Policy:** IS-POL-001 (Master Information Security Policy).
*   **Study GRC Policy:** HR-POL-020 (Child and Youth Safeguarding Policy).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | CISO | Initial Policy Release |