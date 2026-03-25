### Data Handling Procedures (Classification)

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-028 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to define the specific operational requirements for handling information assets belonging to Study GRC Inc. based on the sensitivity levels defined in the *Data Classification Standard*. This procedure ensures that appropriate protection measures—including labeling, storage, transmission, and destruction—are applied to data throughout its lifecycle to prevent unauthorized disclosure, modification, or loss, in compliance with NIST CSF (ID.AM-2) and Texas Business Organizations Code (TBOC).

### 2. Scope
This procedure applies to all **Study GRC Inc.** employees, Board Directors, contractors, volunteers, and third-party vendors ("Users") who access, process, or store Organization data.

*   **In Scope:** All electronic data (databases, files, emails, code), physical records (paper documents), and verbal communications.
*   **Exclusions:** Publicly released open-source educational materials are exempt from access control restrictions but remain subject to integrity and availability protections.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Public (Level 1)** | Information intended for public release (e.g., website content, open-source curriculum). Disclosure causes no harm. |
| **Internal (Level 2)** | Information for internal operations (e.g., org charts, standard operating procedures, internal memos). Unauthorized disclosure causes minimal harm. |
| **Confidential (Level 3)** | Sensitive information requiring access restrictions (e.g., donor lists, non-public financial reports, vendor contracts). Disclosure could cause reputational or financial damage. |
| **Restricted (Level 4)** | Highly sensitive data regulated by law or critical to security (e.g., Youth/Minor PII, SSNs, passwords, private keys, whistleblowing reports). Disclosure causes severe legal or financial harm. |
| **Encryption** | The process of encoding information (AES-256 or equivalent) so that only authorized parties can access it. |
| **TLP (Traffic Light Protocol)** | A set of designations used to ensure that sensitive information is shared with the appropriate audience. |

### 4. Procedures

#### 4.1. Labeling and Marking
Users must visually identify data sensitivity to ensure recipients understand handling requirements.

**4.1.1. Electronic Documents (Word, PDF, Slides)**
*   **Public:** No marking required.
*   **Internal:** No marking required, but "Internal Use Only" is recommended for drafts.
*   **Confidential:** Must include "CONFIDENTIAL" in the header or footer of every page.
*   **Restricted:** Must include "RESTRICTED - [Reason]" (e.g., "RESTRICTED - YOUTH DATA") in the header of every page.

**4.1.2. Email and Communication**
*   **Confidential/Restricted:** Subject lines must begin with `[SECURE]` or `[CONFIDENTIAL]`.
*   **Code Repositories:** Private repositories containing non-public code must be tagged with the appropriate classification topic in GitHub/GitLab.

#### 4.2. Storage and Access
Data must be stored only in authorized locations commensurate with its classification.

| Classification | Authorized Storage Locations | Prohibited Storage |
| :--- | :--- | :--- |
| **Public** | Public Website, Public GitHub Repos, Social Media. | N/A |
| **Internal** | Google Workspace (Shared Drives), Slack (General Channels), Internal Wiki. | Personal devices without MDM. |
| **Confidential** | Secure Google Drive (Restricted Access), CRM, Accounting Software. | Local desktop/downloads folder (unless encrypted), Slack Public Channels, Removable Media (USB). |
| **Restricted** | Encrypted Databases, Password Managers (1Password/LastPass), Secure HR Systems. | **Strictly Prohibited:** Local drives, Unencrypted Cloud Storage, Slack/Discord, Email Inboxes (must be moved to secure storage immediately). |

**4.2.1. Remote Work Storage**
*   Pursuant to the *Remote Work Policy*, **Restricted** data must never be saved to the local hard drive of a personal device. It must be accessed via VDI (Virtual Desktop) or secure web portals only.
*   **Confidential** data saved to Organization-issued laptops must be protected by Full Disk Encryption (BitLocker/FileVault).

#### 4.3. Transmission and Transfer
Users must secure data while it is moving between systems or people.

**4.3.1. Email**
*   **Internal:** Standard email is permitted.
*   **Confidential:** May be sent via email *within* the organization domain. If sent externally, the file must be password-protected or sent via a secure link (e.g., Google Drive link with expiration).
*   **Restricted:** **Never** send Restricted data (e.g., SSNs, passwords) via email body or unencrypted attachment. Use a secure file transfer protocol (SFTP) or a secure credential sharing tool.

**4.3.2. Instant Messaging (Slack/Discord)**
*   **Restricted** data (including API keys, passwords, or youth PII) must **never** be pasted into chat channels, including Direct Messages (DMs).

**4.3.3. Verbal Communication**
*   Users must not discuss **Confidential** or **Restricted** information in public places (coffee shops, co-working spaces) where conversations can be overheard.
*   Headphones must be used for all meetings involving non-public data.

#### 4.4. Physical Handling (Hard Copies)
While Study GRC is remote-first, physical records (e.g., mailed checks, contracts) must be handled securely.

*   **Clean Desk:** **Confidential** and **Restricted** documents must not be left unattended on desks or visible during video calls.
*   **Storage:** Physical records containing **Restricted** data must be stored in a locked cabinet or safe when not in use.
*   **Printing:** Printing of **Restricted** data is prohibited unless legally required (e.g., wet ink signature for government filing).

#### 4.5. Destruction and Disposal
Data must be disposed of securely when no longer needed, in accordance with the *Records Retention Schedule*.

**4.5.1. Electronic Data**
*   **Public/Internal:** Standard deletion (Empty Trash/Recycle Bin).
*   **Confidential:** Standard deletion followed by emptying the Trash.
*   **Restricted:** Must be securely erased using a wipe utility (e.g., DoD 5220.22-M standard) or the storage media must be physically destroyed.

**4.5.2. Physical Media**
*   **Confidential/Restricted:** Must be shredded using a cross-cut shredder. Placing intact documents in a recycling bin is prohibited.

#### 4.6. Incident Reporting
*   Any observation of data being handled in violation of this procedure (e.g., Restricted data found in a public Slack channel) must be reported immediately to the CISO or via the *Whistleblower Complaint Intake Form*.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **All Users** | Apply correct labels, use authorized storage, and follow transmission rules for all data they handle. |
| **Data Owners** | Determine the initial classification of data sets and grant access rights based on the "Need-to-Know" principle. |
| **CISO** | Monitor compliance via DLP (Data Loss Prevention) tools; update authorized storage lists; conduct audits. |
| **IT Department** | Configure systems (Google Workspace, Slack) to enforce storage and encryption requirements automatically where possible. |

### 6. Compliance and Enforcement
Failure to comply with this procedure may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action.

*   **Intellectual Property:** Per **Bylaws Article IX, Section 9.3**, all Work Product created by volunteers/staff belongs to the Organization. Unauthorized retention of Organization data after separation is a violation of the Bylaws and this procedure.
*   **Youth Protection:** Mishandling of **Restricted** youth data may trigger mandatory reporting requirements under Texas Family Code Chapter 261.

### 7. References
*   **IS-STD-005:** Data Classification Standard
*   **IS-POL-001:** Master Information Security Policy
*   **HR-POL-003:** Remote Work and Telecommuting Policy
*   **Bylaws of Study GRC Inc.:** Article VIII (Records) & Article IX (IP)
*   **NIST CSF 2.0:** ID.AM-2 (Data Management)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Legal Officer | Initial Release |