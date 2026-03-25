### Database Access Control Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-021 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Bi-Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this policy is to establish the standards and controls for granting, monitoring, and revoking access to Study GRC Inc.'s database infrastructure. As a remote-first organization managing sensitive member data and youth participant information, strict access control is vital to prevent unauthorized disclosure, modification, or destruction of data.

This policy aligns with **Article IX, Section 9.2** of the Bylaws (Confidentiality & NDA) and ensures compliance with the Texas Data Privacy and Security Act (TDPSA), GDPR, and NIST 800-53 Access Control (AC) standards.

### 2. Scope
This policy applies to all Study GRC Inc. employees, contractors, volunteers, and third-party vendors ("Users") who require access to the Organization's database systems.

**In Scope:**
*   All relational (SQL) and non-relational (NoSQL) databases hosted on-premises or in the cloud (e.g., AWS RDS, Azure SQL, MongoDB Atlas).
*   Production, Development, Staging, and Testing database environments.
*   Database backups and snapshots.

**Exclusions:**
*   End-user access to data via the application front-end (GUI), which is governed by the *Application Access Policy*.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Database Administrator (DBA)** | Personnel responsible for the installation, configuration, upgrade, administration, monitoring, and maintenance of databases. |
| **Least Privilege** | The principle that users are granted the minimum level of access necessary to perform their job functions. |
| **PII** | Personally Identifiable Information. Any representation of information that permits the identity of an individual to whom the information applies to be reasonably inferred. |
| **Production Environment** | The live environment where active data is processed and stored for business operations. |
| **RBAC** | Role-Based Access Control. A method of restricting network access based on the roles of individual users within the enterprise. |
| **Sanitization/Masking** | The process of removing or obscuring sensitive data (PII) from a dataset to render it safe for non-production use. |

### 4. Policy Statements

#### 4.1 Principle of Least Privilege
4.1.1 Access to databases must be granted solely on a "need-to-know" and "need-to-do" basis.
4.1.2 The default access level for all users and service accounts is **None/Deny**.
4.1.3 Administrative access (e.g., `root`, `sa`, `admin`) is restricted to authorized DBAs and must be documented.

#### 4.2 Access Provisioning and Authorization
4.2.1 All requests for database access must be submitted via the Organization’s ticketing system.
4.2.2 Requests must be approved by the **Data Owner** (Operational Officer responsible for the data) and the **CISO** or their designee.
4.2.3 Access requests must specify:
*   The specific database(s) required.
*   The specific level of access (Read-Only, Read-Write, DDL Admin).
*   The business justification.
*   The duration of access (if temporary).

#### 4.3 Authentication Standards
4.3.1 **Named Accounts:** All human users must access databases using unique, named user accounts. The use of shared generic accounts (e.g., `dev_team`, `admin`) is strictly prohibited.
4.3.2 **Multi-Factor Authentication (MFA):** Direct access to database management consoles and cloud provider portals (e.g., AWS Console) hosting databases must require MFA.
4.3.3 **Service Accounts:** Applications connecting to databases must use dedicated service accounts. Credentials for service accounts must be:
*   Complex (minimum 25 characters).
*   Rotated at least every 90 days or immediately upon compromise.
*   Stored in a secure Secrets Manager (e.g., AWS Secrets Manager, HashiCorp Vault), never in plain text code.

#### 4.4 Role-Based Access Control (RBAC)
4.4.1 Database access must be assigned via defined roles/groups, not directly to individual users.
4.4.2 Standard roles include, but are not limited to:
*   **Read-Only:** `SELECT` permissions only.
*   **Read-Write:** `SELECT`, `INSERT`, `UPDATE`, `DELETE` permissions (DML).
*   **Schema Admin:** Permission to alter table structures (DDL). Restricted to Senior Developers/DBAs.
*   **Security Admin:** Permission to grant/revoke access. Restricted to CISO/Lead DBA.

#### 4.5 Network Access Control
4.5.1 Databases must not be directly accessible from the public internet.
4.5.2 Access must be restricted to:
*   Whitelisted application server IP addresses.
*   Authorized VPNs or Zero Trust Network Access (ZTNA) gateways for administrative access.
*   Bastion Hosts/Jump Boxes protected by MFA.

#### 4.6 Production vs. Non-Production Separation
4.6.1 Production databases must be logically and physically isolated from Development and Testing environments.
4.6.2 Developers are prohibited from having direct Write/Modify access to Production databases.
4.6.3 **Data Masking:** Production data containing PII or sensitive member information must be sanitized, masked, or synthesized before being copied to Development or Testing environments.

#### 4.7 Auditing and Logging
4.7.1 The following database events must be logged:
*   All successful and failed login attempts.
*   Changes to privileges or roles (Grant/Revoke).
*   Schema modifications (Drop/Alter Table).
*   Access to sensitive tables (e.g., `users`, `payments`).
4.7.2 Logs must be retained for a minimum of one (1) year in accordance with the *Document Retention and Destruction Policy*.

#### 4.8 Access Review and Recertification
4.8.1 The CISO shall conduct a **quarterly** review of all database access privileges.
4.8.2 Any access rights no longer needed or belonging to terminated personnel must be revoked immediately.
4.8.3 In accordance with **Bylaws Article IX, Section 9.3**, upon termination of service, all access to Organization Work Product and databases is immediately revoked.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Overall owner of this policy; conducts quarterly access reviews; approves high-privilege access requests. |
| **Data Owners** | Operational Officers (e.g., VP of Education, CFO) who authorize access to data domains under their purview. |
| **Database Administrators (DBAs)** | Implement technical controls (RBAC, firewalls); manage user accounts; ensure logging is active. |
| **Users (Devs/Volunteers)** | Protect their credentials; report suspected unauthorized access; adhere to the *Acceptable Use Policy*. |

### 6. Compliance and Enforcement
Failure to comply with this policy may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action.

**Unauthorized Access:** Any attempt to access, copy, or modify database information without explicit authorization is a violation of **Bylaws Article IX** and may constitute a criminal offense under the **Texas Computer Crimes Act (Penal Code Ch. 33)** and the **Computer Fraud and Abuse Act (CFAA)**.

### 7. References
*   **Bylaws of Study GRC Inc.** (Article IX: Policies & Data Protection)
*   **IS-POL-001:** Master Information Security Policy
*   **IS-POL-009:** Access Control Policy
*   **IS-POL-028:** Data Classification Standard
*   **NIST SP 800-53 Rev. 5:** AC-2 (Account Management), AC-3 (Access Enforcement), AC-6 (Least Privilege)
*   **Texas Data Privacy and Security Act (TDPSA)**

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Legal Officer | Initial Draft based on Bylaws and NIST Standards |