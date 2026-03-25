### Cloud Storage and File Sharing Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IT-POL-009 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director / CISO |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this policy is to establish the standards and rules for the use of cloud storage and file-sharing services within Study GRC Inc. As a remote-first organization, cloud storage is essential for collaboration; however, uncontrolled use poses significant risks regarding data leakage, regulatory non-compliance (e.g., COPPA, TDPSA, GDPR), and loss of intellectual property. This policy ensures that data is stored, shared, and managed in accordance with the Organization's **Data Classification Standard** and **Bylaws Article IX (Intellectual Property)**.

### 2. Scope
This policy applies to all employees, Board Directors, officers, volunteers, contractors, and third-party partners (collectively "Users") who access, store, or share Study GRC Inc. data.

*   **In Scope:** All cloud-based storage platforms, file transfer services, and content collaboration platforms used for Organization business.
*   **Out of Scope:** Personal cloud storage accounts used strictly for personal data, provided no Organization data is uploaded to or processed within those personal accounts.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Sanctioned Cloud Service** | A cloud storage platform that has been formally vetted, approved, and provisioned by the IT/Security department (e.g., Organization-managed Google Workspace, GitHub). |
| **Unsanctioned Cloud Service** | Any cloud storage service not centrally managed by Study GRC Inc. (often referred to as "Shadow IT"), including personal Dropbox, personal Google Drive, or iCloud accounts. |
| **Data Classification** | The categorization of data based on its sensitivity and the impact to the Organization should that data be disclosed, altered, or destroyed. |
| **Public Link** | A file-sharing setting that allows anyone with the URL to access a file without authentication (e.g., "Anyone with the link can view"). |
| **PII** | Personally Identifiable Information. Any representation of information that permits the identity of an individual to whom the information applies to be reasonably inferred by either direct or indirect means. |

### 4. Policy Statements

#### 4.1 Sanctioned Platforms
Users must only use **Sanctioned Cloud Services** for the storage and sharing of Organization data.
*   **Primary Storage:** The Organization’s managed Google Workspace (Drive) is the designated repository for documents and administrative files.
*   **Code Repositories:** The Organization’s managed GitHub Enterprise account is the designated repository for source code and technical documentation.
*   **Prohibition:** The use of personal cloud accounts (e.g., personal Gmail Drive, Dropbox, OneDrive) for storing Study GRC Inc. data is strictly prohibited.

#### 4.2 Data Classification and Storage Requirements
All files stored in the cloud must be handled according to the **Data Classification Standard**. Users are responsible for knowing the classification of the data they handle.

*   **Public Data:** (e.g., Open-source educational materials, published blog posts).
    *   *Storage:* Public folders or Public GitHub repositories.
    *   *Sharing:* "Public Links" are permitted.
*   **Internal Data:** (e.g., Policies, meeting minutes, internal memos).
    *   *Storage:* Team Drives/Shared Drives restricted to staff/volunteers.
    *   *Sharing:* Must require authentication (Study GRC login). "Public Links" are prohibited.
*   **Confidential Data:** (e.g., Donor lists, non-public financials, vendor contracts).
    *   *Storage:* Restricted folders with specific access control lists (ACLs).
    *   *Sharing:* Restricted to specific email addresses. External sharing requires a Non-Disclosure Agreement (NDA) per **Bylaws Article IX, Section 9.2**.
*   **Restricted Data:** (e.g., Youth participant PII, background check results, passwords/keys).
    *   *Storage:* Encrypted volumes or highly restricted folders with logging enabled.
    *   *Sharing:* **Strictly Prohibited** via standard file sharing. Must use secure, encrypted transfer methods approved by the CISO.

#### 4.3 Access Control and Permissions
*   **Principle of Least Privilege:** Users must grant the minimum level of access necessary for a recipient to perform their task (e.g., "Viewer" rather than "Editor").
*   **Separation of Duties:** Per **Bylaws Article V**, Operational Officers must ensure that financial records stored in the cloud are accessible only to authorized finance personnel and the Treasurer, maintaining segregation from general volunteers.
*   **MFA Requirement:** Access to any Sanctioned Cloud Service containing Internal, Confidential, or Restricted data must be protected by Multi-Factor Authentication (MFA).

#### 4.4 External Sharing and Expiration
*   **Time-Bound Access:** When sharing Confidential data with external parties (e.g., auditors, partners), Users must set an expiration date for the access link (default: 30 days), after which access is automatically revoked.
*   **Youth Protection:** In compliance with the **Child and Youth Safeguarding Policy**, no User may create a private, 1-on-1 shared folder with a minor (Community Participant under 18) without the inclusion of a second adult leader (Two-Deep Leadership).

#### 4.5 Intellectual Property and Ownership
Pursuant to **Bylaws Article IX, Section 9.3**, all content, code, and materials created by Users and stored in Sanctioned Cloud Services are "works made for hire" and are the sole property of Study GRC Inc.
*   Users may not transfer ownership of files to personal accounts.
*   Upon termination of employment or volunteer service, access to cloud storage will be immediately revoked.

#### 4.6 Monitoring and Auditing
Study GRC Inc. reserves the right to monitor, access, review, and record all data stored in Sanctioned Cloud Services to ensure compliance with this policy, investigate security incidents, or respond to legal requests. Users have no reasonable expectation of privacy regarding business data stored in these environments.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **CISO** | Defines the Sanctioned Cloud Services; configures global security settings (e.g., disabling "Public Link" sharing for specific organizational units); conducts periodic audits of sharing permissions. |
| **Department Heads** | Ensure their teams classify data correctly before uploading; review access permissions for their department's Shared Drives quarterly. |
| **Users (Staff/Volunteers)** | Adhere to data classification rules; ensure no Organization data is stored on personal devices or unsanctioned clouds; report accidental data exposure immediately. |
| **IT Administrators** | Provision and deprovision access accounts; implement technical controls (MFA enforcement, DLP rules) to support this policy. |

### 6. Compliance and Enforcement
Failure to comply with this policy may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action.
*   **Data Leakage:** Unauthorized sharing of Restricted Data (specifically Youth PII) will result in immediate suspension pending investigation and may trigger mandatory reporting under Texas state law and federal regulations (COPPA).
*   **IP Theft:** Transferring proprietary data to personal accounts upon exit is a violation of the Bylaws and may result in civil litigation.

### 7. References
*   **Bylaws of Study GRC Inc.** (Specifically Article IX: Policies & Data Protection)
*   **IT-STD-005:** Data Classification Standard
*   **IT-POL-001:** Master Information Security Policy
*   **HR-POL-020:** Child and Youth Safeguarding Policy
*   **NIST CSF 2.0:** PR.DS-1 (Data Security), PR.AC-4 (Access Control)
*   **2 CFR 200.334:** Retention Requirements for Records

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Legal Officer | Initial Policy Release |