### Encryption Policy (At Rest/Transit)

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-032 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this policy is to establish mandatory requirements for the use of cryptographic controls to protect the confidentiality, integrity, and availability of Study GRC Inc. (the "Organization") data. As a remote-first non-profit organization handling sensitive information—including youth participant data and federal grant information—reliance on encryption is the primary defense against data breaches resulting from device theft, unauthorized access, or interception.

This policy explicitly satisfies **NIST CSF 2.0 PR.DS-1** (Data-at-rest is protected) and **NIST CSF 2.0 PR.DS-2** (Data-in-transit is protected).

### 2. Scope
This policy applies to:
*   **Personnel:** All employees, Board Directors, contractors, volunteers, and interns.
*   **Assets:** All Organization-owned devices (laptops, mobile devices, servers), Bring Your Own Device (BYOD) assets used for Organization business, and cloud infrastructure (SaaS, PaaS, IaaS).
*   **Data:** All data classified as "Confidential," "Restricted," or "Internal" per the *Data Classification Standard*, including but not limited to Personally Identifiable Information (PII), youth data, and donor financial records.

**Exclusions:** Publicly available data (e.g., website marketing content) does not require encryption for confidentiality purposes, though integrity controls (TLS) remain mandatory.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Data at Rest** | Data that is not currently moving from device to device or network to network (e.g., data stored on hard drives, flash drives, cloud storage buckets, or databases). |
| **Data in Transit** | Data actively moving through a network, such as the internet or a private network (e.g., email, web traffic, API calls). |
| **Full Disk Encryption (FDE)** | Encryption that protects the entire hard drive volume, requiring authentication before the operating system boots or unlocks. |
| **End-to-End Encryption (E2EE)** | A method of secure communication that prevents third parties (including the service provider) from accessing data while it's transferred from one end system or device to another. |
| **Cryptographic Key** | A string of characters used within an encryption algorithm for altering data so that it appears random. Like a physical key, it locks (encrypts) and unlocks (decrypts) data. |
| **TLS (Transport Layer Security)** | A cryptographic protocol designed to provide communications security over a computer network. |

### 4. Policy Statements

#### 4.1 General Principles
4.1.1 **Encryption by Default:** All non-public data must be encrypted both at rest and in transit. When a system offers an option to encrypt, it must be enabled.
4.1.2 **Approved Algorithms:** The Organization shall only use industry-standard, non-deprecated cryptographic algorithms and key lengths (e.g., AES-256, RSA-2048 or higher, SHA-256). The use of proprietary or "home-grown" encryption algorithms is strictly prohibited.
4.1.3 **Regulatory Compliance:** Encryption implementation must align with the safe harbor provisions of the Texas Business & Commerce Code § 521.053 and federal grant requirements under 2 CFR 200.303(e).

#### 4.2 Protection of Data at Rest (NIST PR.DS-1)
4.2.1 **End-User Devices:** All laptops and desktops (Windows, macOS, Linux) used for Organization business must have Full Disk Encryption (FDE) enabled (e.g., BitLocker, FileVault, LUKS).
4.2.2 **Mobile Devices:** Mobile devices (phones, tablets) accessing Organization data (email, Slack, Drive) must be encrypted. Devices that do not support encryption or cannot be encrypted are prohibited from accessing Organization resources.
4.2.3 **Removable Media:** The use of USB drives or external hard drives is discouraged. If strictly necessary, any removable media containing Confidential or Restricted data must be hardware-encrypted or software-encrypted using AES-256.
4.2.4 **Cloud Storage & Databases:**
*   Cloud storage buckets (e.g., AWS S3, Google Cloud Storage) must have server-side encryption enabled by default.
*   Databases containing PII or youth data must utilize Transparent Data Encryption (TDE) or column-level encryption for sensitive fields.
4.2.5 **Backups:** All backups, whether local or cloud-based, must be encrypted.

#### 4.3 Protection of Data in Transit (NIST PR.DS-2)
4.3.1 **Web Traffic:** All web-based applications and websites owned or managed by the Organization must enforce HTTPS using TLS 1.2 or higher. SSL v3.0, TLS 1.0, and TLS 1.1 are prohibited.
4.3.2 **Remote Access:** Access to internal resources or administrative panels from public networks (e.g., coffee shops, airports) requires the use of an approved VPN or Zero Trust Network Access (ZTNA) solution.
4.3.3 **Email:** Transmission of sensitive PII (e.g., SSNs, financial data, youth medical info) via standard email body text is prohibited. Such data must be sent via an encrypted attachment, a secure file transfer link, or an E2EE messaging platform.
4.3.4 **File Transfer:** FTP and Telnet are strictly prohibited. SFTP, SCP, or HTTPS-based file transfers must be used.

#### 4.4 Key Management
4.4.1 **Separation of Duties:** Where technically feasible, the management of cryptographic keys should be separated from the management of the data those keys protect.
4.4.2 **Key Rotation:** Cryptographic keys must be rotated annually or immediately upon suspicion of compromise.
4.4.3 **Hardcoding Prohibited:** Encryption keys and secrets must never be hardcoded into software source code or scripts. They must be stored in a dedicated secrets management system (e.g., Vault, AWS Secrets Manager, GitHub Secrets).

#### 4.5 Youth Data Specifics
4.5.1 **Strict Encryption:** Any database or file system storing data regarding minors (under 18) must utilize encryption at rest without exception, to ensure compliance with the Organization's *Child and Youth Safeguarding Policy*.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Defines encryption standards; approves cryptographic algorithms; oversees key management strategy. |
| **IT / Systems Administrators** | Configure and enforce FDE on endpoints; manage TLS certificates; ensure cloud storage encryption is active. |
| **Developers / Engineering** | Implement encryption in code and databases; ensure keys are not hardcoded; utilize approved libraries. |
| **Employees & Volunteers** | Ensure their devices are encrypted; refrain from disabling security controls; report lost devices immediately. |
| **Board of Directors** | Reviews and approves this policy annually to ensure alignment with Bylaws Article IX (Intellectual Property & Data). |

### 6. Compliance and Enforcement
**Audit:** The CISO will conduct periodic audits (automated and manual) to verify encryption status on endpoints and cloud assets.

**Enforcement:** Failure to comply with this policy—specifically the disabling of encryption on devices or the transmission of unencrypted sensitive data—may result in disciplinary action, up to and including termination of employment or volunteer assignment.

**Legal Note:** Under Texas law, the loss of a device containing *unencrypted* PII triggers mandatory breach notification requirements. Loss of an *encrypted* device generally provides a "Safe Harbor" from notification, provided the encryption key was not also compromised.

### 7. References
*   **NIST CSF 2.0:** PR.DS-1 (Data-at-rest), PR.DS-2 (Data-in-transit)
*   **NIST SP 800-175B:** Guideline for Using Cryptographic Standards
*   **Study GRC Bylaws:** Article V (Operational Leadership), Article IX (Policies & Data Protection)
*   **Texas Business & Commerce Code:** § 521.053 (Notification Required Following Breach of Security of Computerized Data)
*   **Internal Policy:** IS-POL-028 (Data Classification Standard)
*   **Internal Policy:** IS-POL-001 (Master Information Security Policy)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | CISO | Initial Policy Release |