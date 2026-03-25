### Backup Policy and Procedures

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-015 |
| **Document Type** | Policy & Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this policy is to establish the requirements for the backup and recovery of Study GRC Inc. (the "Organization") data. This policy ensures the Organization can recover from data loss events—including ransomware attacks, hardware failures, accidental deletions, and natural disasters—thereby maintaining business continuity and complying with **Article VIII, Section 8.1** of the Bylaws regarding the maintenance of "correct and complete books and records."

### 2. Scope
This policy applies to all Organization data, information systems, and software applications used to conduct official business.
*   **In Scope:**
    *   Cloud Productivity Suites (e.g., Google Workspace, Microsoft 365).
    *   Financial Systems (e.g., QuickBooks Online, Stripe data).
    *   Website and Content Management Systems.
    *   Code Repositories (e.g., GitHub, GitLab).
    *   Donor Management Systems (CRM).
*   **Exclusions:**
    *   Transient data of no business value (e.g., temporary cache files).
    *   Personal data stored on personal devices (BYOD) that is not synchronized to Organization-managed cloud storage.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **RPO (Recovery Point Objective)** | The maximum acceptable amount of data loss measured in time (e.g., "we can lose up to 4 hours of data"). |
| **RTO (Recovery Time Objective)** | The maximum acceptable time allowed to restore the system after a disaster (e.g., "system must be back up within 8 hours"). |
| **3-2-1 Rule** | A backup strategy requiring three copies of data, on two different media types, with one copy kept off-site (or in a separate cloud region/provider). |
| **Immutable Backup** | A backup file that cannot be altered, deleted, or overwritten, even by an administrator, for a set period. This is a primary defense against ransomware. |
| **SaaS Backup** | Third-party backup solutions designed to protect data stored in cloud services (SaaS), independent of the vendor's native retention policies. |

### 4. Policy Statements

#### 4.1 Backup Strategy (The 3-2-1 Rule)
To ensure data survivability, the Organization must adhere to the **3-2-1 Rule** wherever technically feasible:
*   **Three (3) copies of data:** The production data plus two backup copies.
*   **Two (2) different media/platforms:** e.g., Production on Google Workspace, Backup on AWS S3.
*   **One (1) off-site/segregated copy:** For a cloud-native organization, this requires a **Cloud-to-Cloud (C2C)** backup solution that is logically separated from the primary production environment.

#### 4.2 SaaS Data Protection
Reliance on the "Recycle Bin" or "Trash" features of SaaS providers (e.g., Google, Microsoft, Slack) is **strictly prohibited** as a primary backup strategy. The CISO must implement independent, third-party backup solutions for all critical SaaS platforms to protect against account takeovers, malicious insider deletion, and vendor outages.

#### 4.3 Frequency and Retention (RPO)
Backup frequency must align with the criticality of the data:

| Data Classification | Backup Frequency | Retention Period | Target RPO |
| :--- | :--- | :--- | :--- |
| **Critical** (Financials, Donor Data, IP) | Daily (minimum) | 7 Years | 24 Hours |
| **Confidential** (Internal Comms, HR) | Daily | 3 Years | 24 Hours |
| **Public** (Website Content) | Weekly | 1 Year | 1 Week |

#### 4.4 Encryption and Security
*   **Encryption:** All backups must be encrypted **at rest** and **in transit** using industry-standard algorithms (e.g., AES-256).
*   **Access Control:** Access to backup repositories must be restricted to the CISO and designated IT administrators.
*   **MFA:** Multi-Factor Authentication (MFA) is **mandatory** for accessing any backup management console.

#### 4.5 Immutability (Ransomware Defense)
Where feasible, backup targets must utilize **Object Lock** or **Immutability** features. This ensures that even if a threat actor gains administrative credentials, they cannot delete or encrypt the backup history before the retention period expires.

#### 4.6 Testing and Validation
Backups are considered failed until proven successful.
*   **Automated Verification:** Backup jobs must generate daily success/failure logs sent to the IT team.
*   **Restoration Testing:** The CISO must perform a **quarterly** restoration test of a random sample of critical data to verify data integrity and RTO capabilities.

### 5. Procedures

#### 5.1 Cloud-to-Cloud Backup Configuration
1.  **Vendor Selection:** Select a backup vendor (e.g., Spanning, Backupify, Veeam) that supports OAuth connectivity to the Organization’s primary SaaS platforms.
2.  **Scope Definition:** Configure the backup tool to ingest:
    *   All User Mailboxes.
    *   Shared Drives / SharePoint Sites.
    *   Calendars and Contacts.
3.  **Schedule:** Set automated backup frequency to run at least once every 24 hours (automatic incremental).
4.  **Alerting:** Configure email alerts for "Job Failed" or "Token Expired" events to be sent immediately to `security@[organization].org`.

#### 5.2 Website and Database Backup
1.  **CMS Backup:** Configure the web hosting provider or a plugin (e.g., UpdraftPlus) to export the database and `wp-content` folder weekly.
2.  **Off-Site Storage:** Automatically push these exports to a dedicated, encrypted S3 bucket or separate cloud storage provider (not the web host's local storage).
3.  **Code Repositories:** Enable automated mirroring or third-party backup for all GitHub/GitLab repositories containing proprietary code or configurations.

#### 5.3 Restoration Testing Procedure (Quarterly)
1.  **Select Target:** Choose a specific file, email folder, or database table from a date at least 30 days prior.
2.  **Execute Restore:** Initiate a "Restore to New Folder" or "Non-Destructive Restore" operation.
3.  **Verify:** Open the restored file to ensure it is not corrupted and contains the expected data.
4.  **Document:** Log the test results in the **Backup Testing Register (IS-REG-004)**, noting the time taken (to validate RTO) and any errors encountered.

#### 5.4 Emergency Restoration (Incident Response)
In the event of data loss or ransomware:
1.  **Isolate:** Immediately disconnect affected systems from the network to prevent spread.
2.  **Assess:** Determine the timestamp of infection/deletion to identify the "Last Known Good" backup.
3.  **Authorize:** The CISO or Executive Director must authorize a mass restoration.
4.  **Restore:** Initiate restoration from the immutable backup copy.
    *   *Priority:* Restore critical identity and communication systems first, followed by financial and operational data.
5.  **Validate:** Confirm data integrity before reconnecting systems to the production network.

### 6. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Overall owner of the backup strategy. Responsible for selecting vendors, auditing compliance, and conducting quarterly restoration tests. |
| **IT Administrators** | Responsible for daily monitoring of backup logs, troubleshooting failures, and configuring backup schedules. |
| **Executive Director** | Responsible for authorizing budget for backup storage and tools; authorizes mass restoration during crisis events. |
| **Staff & Volunteers** | Responsible for saving all work to sanctioned cloud folders (e.g., Shared Drives). **Data saved locally on laptops is NOT backed up and is the user's responsibility.** |

### 7. Compliance and Enforcement
Failure to comply with this policy—specifically the intentional disabling of backup agents or storage of critical data in unapproved, unbacked-up locations—may result in disciplinary action, up to and including termination of employment or volunteer assignment.

### 8. References
*   **Bylaws of Study GRC Inc.** (Article VIII - Records, Transparency & Finance)
*   **IS-POL-001:** Master Information Security Policy
*   **IS-STD-002:** Data Classification Standard
*   **IS-REG-004:** Backup Testing Register
*   **NIST SP 800-53 (Rev. 5):** Control CP-9 (System Backup)

### 9. Revision History
| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | CISO | Initial Draft aligned with Bylaws and Remote-First context. |