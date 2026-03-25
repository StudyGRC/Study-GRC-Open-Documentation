### Right to Data Portability Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | GOV-PRC-045 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Bi-Annual) |
| **Approving Authority** | Executive Director / Chief Information Security Officer (CISO) |
| **Document Owner** | Data Protection Officer (DPO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to operationalize the "Right to Data Portability" as mandated by **Article 20 of the General Data Protection Regulation (GDPR)** and aligned with the transparency goals defined in **Article IX (Policies & Data Protection)** of the Study GRC Inc. Bylaws. This procedure defines the steps for receiving, verifying, processing, and fulfilling requests from Data Subjects to receive their personal data in a structured, commonly used, and machine-readable format, or to transmit that data directly to another controller.

### 2. Scope
This procedure applies to all personal data processed by Study GRC Inc. ("the Organization") that meets the following criteria:
1.  The data was **provided by the Data Subject** to the Organization.
2.  The processing is based on **Consent** or the performance of a **Contract** (e.g., Membership Agreement).
3.  The processing is carried out by **automated means** (i.e., digital records, not paper files).

**Exclusions:**
*   Data inferred or derived by the Organization (e.g., user profiling scores, internal notes).
*   Data processed based on "Legitimate Interest" or "Legal Obligation."
*   Paper-based records.
*   Data where portability would adversely affect the rights and freedoms of others (e.g., data containing third-party private information).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Data Portability** | The right of a data subject to receive their personal data in a format that allows them to move, copy, or transfer it easily from one IT environment to another. |
| **Machine-Readable** | A file format structured so that software applications can easily identify, recognize, and extract specific data (e.g., CSV, JSON, XML). |
| **Provided Data** | Data actively and knowingly given by the data subject (e.g., account details) and observed data (e.g., activity logs, history). It excludes inferred/derived data. |
| **Controller** | The entity that determines the purposes and means of the processing of personal data (Study GRC Inc.). |

### 4. Procedures

#### 4.1 Request Intake
1.  Data Subjects must submit portability requests via the designated channel: `privacy@studygrc.org` or the "My Data" section of the Member Portal.
2.  The Privacy Team must log the request in the **Data Subject Access Request (DSAR) Register** immediately upon receipt.
3.  The 30-day compliance clock begins the day the request is received.

#### 4.2 Identity Verification
To prevent data theft, the identity of the requester must be verified before any data is compiled.
1.  **Portal Requests:** Verification is confirmed via active login session and Multi-Factor Authentication (MFA) if enabled.
2.  **Email Requests:** The Privacy Team must send a verification challenge to the email address on file.
    *   If the requester cannot verify ownership of the account, the request must be denied to protect data security.

#### 4.3 Request Assessment
The Data Protection Officer (DPO) or designee must review the request to ensure eligibility under GDPR Art. 20:
1.  Confirm the legal basis of processing is **Consent** or **Contract**.
2.  Confirm the data is processed automatically.
3.  Identify if the request is for **Direct Download** or **Direct Transmission** to another controller.

#### 4.4 Data Compilation and Extraction
The IT/System Administrator shall extract applicable data from relevant systems (CRM, LMS, Community Platform):
1.  **Profile Data:** Name, email, contact details.
2.  **Activity Data:** Course progress, exam scores, forum posts, volunteer hours logs.
3.  **Uploaded Content:** Files or documents uploaded by the user.
4.  **Exclusion Filter:** The Administrator must filter out internal administrative notes, derived analytics, or data belonging to other users.

#### 4.5 Format Conversion
1.  Extracted data must be converted into a structured, open standard format.
    *   **Preferred:** JSON (JavaScript Object Notation) or CSV (Comma Separated Values).
    *   **Prohibited:** Proprietary formats that require paid software to open (e.g., proprietary database backup files).
2.  The file structure must include a manifest or "Read Me" explaining the data fields if the headers are not self-explanatory.

#### 4.6 Security and Delivery (Direct Download)
1.  The data package must be encrypted (e.g., ZIP with AES-256 encryption).
2.  The password for the encrypted package must be transmitted separately from the download link (e.g., via SMS or a separate email thread), or the file must be hosted behind the secure Member Portal login.
3.  **Strict Prohibition:** Never send unencrypted bulk personal data via standard email attachments.

#### 4.7 Direct Transmission (Controller-to-Controller)
If the Data Subject requests transfer to another organization (e.g., another certification body):
1.  **Feasibility Check:** The CISO determines if a secure, automated connection (API) exists or if a secure file transfer protocol (SFTP) can be established with the receiving Controller.
2.  **Technical Barrier:** If no secure interface exists, the Organization is not obligated to build one. In this case, the Organization will provide the data to the Data Subject (Procedure 4.6) for them to upload to the new Controller manually.
3.  **Execution:** If technically feasible and secure, the data is transmitted directly.

#### 4.8 Completion and Record Keeping
1.  Notify the Data Subject that the request has been fulfilled.
2.  Update the **DSAR Register** with the completion date and outcome.
3.  Retain the request log for audit purposes for a period of 2 years; do *not* retain the generated export package longer than 7 days.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Data Subject** | Submits request and completes identity verification steps. |
| **Data Protection Officer (DPO)** | Validates request eligibility; oversees the 30-day timeline; communicates with the Data Subject. |
| **IT / System Administrator** | Executes technical extraction of data; ensures format is machine-readable; applies security controls to the export package. |
| **Chief Information Security Officer (CISO)** | Determines technical feasibility of direct controller-to-controller transfers; approves security of transfer methods. |

### 6. Compliance and Enforcement
Failure to comply with this procedure may result in violations of GDPR Article 20, leading to significant regulatory fines (up to 4% of global turnover or €20 million) and reputational damage.

Internal non-compliance:
*   **Employees/Volunteers:** Failure to assist in a timely data extraction or obstructing a valid request may result in disciplinary action, up to and including termination of employment or volunteer assignment.
*   **System Owners:** Failure to maintain systems that allow for data extraction may result in a mandatory remediation plan.

### 7. References
*   **Regulation (EU) 2016/679 (GDPR)** - Article 20 (Right to Data Portability)
*   **Study GRC Inc. Bylaws** - Article IX (Policies & Data Protection)
*   **GOV-POL-040** - Master Data Privacy Policy
*   **GOV-PRC-042** - Data Subject Access Request (DSAR) Procedure
*   **IS-STD-010** - Data Classification Standard

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Legal Officer | Initial Draft aligned with GDPR Art. 20 |