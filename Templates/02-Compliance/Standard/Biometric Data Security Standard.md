### Biometric Data Security Standard

| Document Control | |
| :--- | :--- |
| **Document ID** | DP-STD-053 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-26 |
| **Next Review Date** | 2024-10-26 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Standard is to define the mandatory technical and administrative controls required to protect Biometric Data collected, stored, or processed by Study GRC Inc. This document ensures compliance with **GDPR Article 32 (Security of Processing)** regarding the processing of special category data, and the **Texas Capture or Use of Biometric Identifier Act (CUBI)** (Texas Business & Commerce Code § 503.001). It establishes a "reasonable standard of care" to prevent unauthorized access, disclosure, or theft of biometric identifiers.

### 2. Scope
This Standard applies to all Study GRC Inc. information systems, databases, applications, and third-party vendors that process Biometric Data.
*   **Applies to:** All employees, contractors, and volunteers who design, manage, or access systems containing biometric data.
*   **Includes:** Data used for authentication (e.g., fingerprint scanners), identity verification (e.g., facial recognition for remote proctoring), or attendance tracking.
*   **Exclusions:** General photographs or video recordings that are *not* processed using specific technical means to allow the unique identification or authentication of a natural person (as defined by GDPR Recital 51).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Biometric Identifier** | As defined by Texas CUBI: A retina or iris scan, fingerprint, voiceprint, or record of hand or face geometry. |
| **Biometric Data** | As defined by GDPR Art. 4(14): Personal data resulting from specific technical processing relating to the physical, physiological, or behavioral characteristics of a natural person, which allow or confirm the unique identification of that natural person. |
| **Biometric Template** | A digital representation of distinct characteristics extracted from a biometric sample (e.g., a mathematical map of facial nodes), rather than the raw image itself. |
| **Salt** | Random data that is used as an additional input to a one-way function that hashes data, a password, or passphrase. |
| **Pseudonymization** | The processing of personal data in such a manner that the personal data can no longer be attributed to a specific data subject without the use of additional information. |

### 4. Standards

#### 4.1. Data Minimization and Raw Data Prohibition
4.1.1 **Prohibition on Raw Storage:** Study GRC Inc. systems **must not** store raw biometric images (e.g., actual fingerprint images or high-resolution face scans) unless strictly required by law or for a specific, temporary diagnostic purpose approved by the CISO.
4.1.2 **Template Storage:** Systems must only store **Biometric Templates** (mathematical representations/hashes) derived from the raw data.
4.1.3 **Irreversibility:** The algorithm used to generate the Biometric Template must be designed such that the raw biometric image cannot be reconstructed from the template.

#### 4.2. Encryption and Hashing Requirements
4.2.1 **Encryption at Rest:** All Biometric Data and Templates must be encrypted at rest using **AES-256** or higher standards.
4.2.2 **Encryption in Transit:** All transmission of Biometric Data across public or private networks must be encrypted using **TLS 1.3** or higher.
4.2.3 **Hashing:** Biometric Templates must be hashed using a strong cryptographic algorithm (e.g., SHA-256 or stronger).
4.2.4 **Salting:** To prevent rainbow table attacks, all hashed Biometric Templates must be **salted** with a unique, random value for each user.

#### 4.3. Access Control and Isolation
4.3.1 **Data Separation (Pseudonymization):** Biometric Data must be stored in a database or table logically separated from other Personally Identifiable Information (PII) such as names, emails, or addresses. A unique, opaque identifier (e.g., a UUID) must link the two datasets.
4.3.2 **Least Privilege:** Access to the database containing Biometric Data is restricted to the absolute minimum number of administrators required for maintenance (Max: 3 individuals).
4.3.3 **MFA Requirement:** Administrative access to servers or databases hosting Biometric Data **must** require Phishing-Resistant Multi-Factor Authentication (MFA).
4.3.4 **API Security:** API endpoints accessing Biometric Data must not expose the Biometric Template in the response body. Responses should be limited to boolean verification (Match/No Match) or authentication tokens.

#### 4.4. Retention and Destruction
4.4.1 **Automated Purging:** Systems must be configured to automatically delete Biometric Data upon the earliest of:
    *   The termination of the relationship with the individual (e.g., account closure, end of employment).
    *   One (1) year after the last interaction with the individual (per Texas CUBI requirements for "reasonable time").
    *   Withdrawal of consent by the Data Subject.
4.4.2 **Sanitization Standard:** Deletion must adhere to **NIST SP 800-88 Guidelines for Media Sanitization** (Clear or Purge methods) to ensure data is irretrievable. Simple file deletion commands are insufficient; data must be overwritten.

#### 4.5. Third-Party Vendor Requirements
4.5.1 **Vendor Assessment:** Any third-party vendor (e.g., remote proctoring services, identity verification providers) processing Biometric Data on behalf of Study GRC Inc. must undergo a **Vendor Security Risk Assessment (VSRA)** prior to contract execution.
4.5.2 **Contractual Guarantees:** Vendors must contractually agree to:
    *   Not sell, lease, or trade Biometric Data.
    *   Maintain security controls equal to or exceeding this Standard.
    *   Notify Study GRC Inc. of any breach involving Biometric Data within 24 hours.

#### 4.6. Incident Response
4.6.1 **Severity Classification:** Any unauthorized access, theft, or disclosure of Biometric Data is automatically classified as a **High Severity Incident** in the Incident Response Plan.
4.6.2 **Notification:** In the event of a breach, the Data Protection Officer (DPO) must be notified immediately to facilitate mandatory reporting to regulatory bodies (e.g., Texas Attorney General, EU Data Protection Authorities) within statutory timeframes (often 72 hours).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Owns this Standard; approves cryptographic algorithms; conducts annual audits of biometric storage systems. |
| **Data Protection Officer (DPO)** | Ensures alignment with GDPR and Texas CUBI; reviews Data Protection Impact Assessments (DPIAs) for biometric projects. |
| **System Architects / Developers** | Implement encryption, hashing, and separation controls defined in Section 4. |
| **IT Operations** | Manages access controls and ensures automated deletion scripts are functioning. |
| **Third-Party Vendors** | Adhere to these standards via contractual obligation and Data Processing Agreements (DPAs). |

### 6. Compliance and Enforcement
Failure to comply with this Standard may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action.
*   **Legal Risks:** Non-compliance may expose Study GRC Inc. to substantial fines under GDPR (up to 4% of global turnover) and civil penalties under Texas CUBI (up to $25,000 per violation).
*   **Verification:** Compliance with this standard is verified via annual penetration testing and internal audits.

### 7. References
*   **DP-POL-050:** Master Data Privacy Policy
*   **DP-POL-052:** Biometric Data Capture/Retention Policy
*   **Regulation:** GDPR Article 32 (Security of Processing)
*   **Regulation:** Texas Business & Commerce Code § 503.001 (Capture or Use of Biometric Identifier)
*   **Standard:** NIST SP 800-63B (Digital Identity Guidelines)
*   **Standard:** NIST SP 800-88 (Guidelines for Media Sanitization)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-26 | Chief Legal Officer | Initial Release aligned with GDPR and Texas CUBI. |