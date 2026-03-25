### User Account Deprovisioning Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-005 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-04-27 (Bi-Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a standardized, secure, and timely process for revoking system access and recovering assets when an individual’s relationship with Study GRC Inc. concludes or changes. This procedure mitigates risks associated with unauthorized access, data exfiltration, and intellectual property theft, ensuring compliance with **Bylaws Article IX (Intellectual Property)** and **Article VII (Indemnification)** regarding good faith performance.

### 2. Scope
This procedure applies to all Information Technology (IT) resources, systems, applications, and physical assets owned or managed by Study GRC Inc.

**Applies to:**
*   Employees and Contractors.
*   **Operational Officers** (as defined in Bylaws Article V).
*   **Board Directors** (upon resignation or removal per Bylaws Article III).
*   Volunteers and Interns with assigned organizational accounts (e.g., `@studygrc.org` email).

**Exclusions:**
*   Public-facing "Community Participant" accounts on open forums, unless a ban is issued under the *Code of Conduct*.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Deprovisioning** | The technical process of removing access rights and privileges from a user account. |
| **Involuntary Separation** | Termination of employment or service for cause, or removal of a Director/Officer by vote (Hostile/High Risk). |
| **Voluntary Separation** | Resignation, retirement, or end of contract term (Standard Risk). |
| **Privileged Account** | An account with elevated permissions (e.g., Administrator, Root, Superuser) capable of altering system configurations. |
| **MDM** | Mobile Device Management; software used to secure and manage remote devices. |

### 4. Procedures

#### 4.1 Notification of Separation
The deprovisioning process must be initiated via a formal notification ticket or secure communication to the IT/Security Department.

1.  **Standard Separation:** The Supervising Manager or HR representative must notify IT at least **72 hours** prior to the user's last day.
2.  **Involuntary/Hostile Separation:** The Supervising Manager must notify the CISO or Executive Director **immediately** upon the decision to terminate. Technical revocation must be coordinated to occur simultaneously with the termination meeting.
3.  **Board/Officer Removal:** Upon the affirmative vote for removal (Bylaws §3.6 or §5.3), the Board Secretary must immediately notify the CISO.

#### 4.2 Timing of Access Revocation
*   **Voluntary:** Access remains active until 5:00 PM (User's Local Time) on the final day of service, unless otherwise requested by management.
*   **Involuntary:** Access is revoked **immediately** upon notification from the authorized requestor.
*   **Immediate Revocation Protocol:** If a user poses an immediate threat to data or systems, the CISO is authorized to suspend access prior to formal termination paperwork, pending investigation.

#### 4.3 Technical Deprovisioning Steps
The IT Administrator or CISO must execute the following steps in order:

**4.3.1 Identity Provider (IdP) & SSO**
1.  Reset the user’s primary password.
2.  Force a sign-out of all active web sessions and tokens.
3.  Disable the user account in the primary directory (e.g., Google Workspace, Azure AD).
4.  Remove the user from all distribution lists and security groups.

**4.3.2 Multi-Factor Authentication (MFA)**
1.  Revoke all registered MFA tokens and trusted devices immediately to prevent offline access or bypass.

**4.3.3 Email and Communication**
1.  Convert the user mailbox to a "Shared Mailbox" or archive status to preserve data for legal retention.
2.  Assign "Read and Manage" permissions to the user’s manager or designated successor.
3.  Set an auto-reply message on the account: *"This email address is no longer active. Please contact [General/Manager Email] for assistance."*
4.  Remove the user from internal communication platforms (e.g., Slack, Discord private channels).

**4.3.4 Third-Party Applications & SaaS**
1.  Revoke access to critical third-party tools not behind SSO (e.g., GitHub, Banking Portals, Cloud Infrastructure).
2.  **GitHub Specific:** Ensure all code commits are pushed. If the user holds "Owner" status on any repository, transfer ownership to the Organization immediately, pursuant to **Bylaws Article IX §9.3 (Work Made for Hire)**.

**4.3.5 Remote Device Management (MDM)**
1.  Issue a "Device Lock" command to Organization-owned laptops/devices.
2.  If the device cannot be recovered or contains highly sensitive data during a hostile termination, issue a "Remote Wipe" command (Corporate Data Only) upon CISO approval.

#### 4.4 Asset Recovery (Remote-First Context)
1.  IT/Operations must send a prepaid shipping box/label to the user’s registered address within 24 hours of separation.
2.  The user must return all hardware (laptops, YubiKeys, monitors) within **10 business days**.
3.  IT must inspect returned hardware for physical damage and verify that the drive has not been tampered with before reimaging.

#### 4.5 Data Preservation and Legal Hold
1.  Do **not** delete the user account or mailbox data for a minimum of **90 days** (or longer if defined in the *Records Retention Schedule*).
2.  If the separation involves potential litigation (e.g., Whistleblower complaint, termination for cause), a **Legal Hold** must be placed on the account, preventing any deletion until authorized by Legal Counsel.

#### 4.6 Board Director Specifics
1.  Upon the resignation or removal of a Director, their access to the Board Portal and confidential Board folders must be revoked immediately.
2.  The Secretary must verify that the former Director has destroyed or returned any downloaded confidential materials, including Executive Session minutes.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Supervising Manager / HR** | Initiates the separation request; collects physical assets (if in-person); ensures knowledge transfer occurs before the last day. |
| **IT Administrator** | Executes technical revocation steps; monitors logs for post-termination access attempts. |
| **CISO** | Approves immediate/hostile revocation plans; authorizes remote wipes; oversees access to former employee data. |
| **Board Secretary** | Notifies IT regarding Board Member or Officer changes. |
| **Departing User** | Returns all organizational assets; ceases use of all IP; abides by NDA post-employment. |

### 6. Compliance and Enforcement
Failure to follow this procedure may result in data breaches, loss of intellectual property, or legal liability.
*   **Internal:** Staff found neglecting to deprovision users in a timely manner are subject to disciplinary action, up to and including termination.
*   **External:** Former users who attempt to access Study GRC Inc. systems after their separation date will be considered in violation of the **Computer Fraud and Abuse Act (CFAA)** and **Texas Penal Code § 33.02 (Breach of Computer Security)** and will be referred to law enforcement.

### 7. References
*   **Bylaws of Study GRC Inc.** (Article III - Board; Article IX - Intellectual Property)
*   **IS-POL-001:** Master Information Security Policy
*   **IS-STD-004:** Asset Management Standard
*   **HR-POL-015:** Termination and Separation Procedure
*   **NIST CSF 2.0:** PR.AC-4 (Access permissions are managed, incorporating the principles of least privilege and separation of duties).
*   **ISO 27001:2022:** Control A.5.16 (Identity management), A.8.10 (Information deletion).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | CISO | Initial Draft based on Bylaws and Remote-First requirements. |