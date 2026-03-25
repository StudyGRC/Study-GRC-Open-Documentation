### Biometric Data Destruction Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | DP-PRC-053 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to mandate the specific steps, timelines, and technical methods for the permanent destruction of Biometric Identifiers held or processed by Study GRC Inc. This procedure ensures compliance with the **Texas Capture or Use of Biometric Identifier Act (CUBI)** (Tex. Bus. & Com. Code § 503.001 et seq.) and aligns with the Organization’s commitment to data privacy as outlined in **Article IX** of the Bylaws.

### 2. Scope
This procedure applies to all Study GRC Inc. personnel, volunteers, and third-party vendors who collect, possess, or store Biometric Identifiers on behalf of the Organization.

*   **In Scope:** All electronic or physical records containing Biometric Identifiers used for authentication, security, or identity verification (e.g., fingerprint scanners for device access, facial recognition for exam proctoring).
*   **Out of Scope:** Standard photographs, video, or audio recordings that are **not** processed through biometric algorithms for the purpose of unique identification.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Biometric Identifier** | As defined by Texas CUBI: A retina or iris scan, fingerprint, voiceprint, or record of hand or face geometry. |
| **Termination of Purpose** | The point in time when the initial reason for collecting the biometric data is no longer valid (e.g., termination of employment, conclusion of a proctored exam, or discontinuance of a security system). |
| **Sanitization** | The process of rendering access to target data on media infeasible for a given level of effort (per NIST SP 800-88). |
| **Crypto-Shredding** | The practice of deleting the encryption keys that protect encrypted data, thereby rendering the data unreadable and unrecoverable. |

### 4. Procedures

#### 4.1 Determination of Destruction Trigger
Biometric Identifiers must be scheduled for destruction immediately upon the occurrence of any of the following "Trigger Events":
1.  **Termination of Relationship:** The individual’s employment, volunteer service, or contractual relationship with Study GRC Inc. ends.
2.  **Discontinuation of Technology:** The Organization ceases the use of the specific biometric system (e.g., switching from fingerprint to YubiKey authentication).
3.  **Expiration of Purpose:** The specific project or security requirement for which the data was collected has concluded.
4.  **Withdrawal of Consent:** The individual formally withdraws consent for biometric processing (subject to security policy requirements).

**Statutory Deadline:** In strict compliance with Texas CUBI § 503.001(c)(3), destruction must be completed **not later than the first anniversary** of the date the purpose for collecting the identifier expires. Study GRC Inc. sets an internal standard to complete this process within **30 days** of the Trigger Event.

#### 4.2 Notification Workflow
1.  **HR/Volunteer Management Notification:** Upon a Trigger Event (e.g., employee offboarding), the HR Department or Volunteer Coordinator must submit a *Data Purge Request* to the IT Security Team within 24 hours.
2.  **Asset Identification:** The CISO or designee must identify all repositories (local servers, cloud storage, third-party vendors) where the subject's biometric data resides.

#### 4.3 Technical Destruction Methods
Biometric data must be rendered unrecoverable. Simple file deletion ("moving to trash") is strictly prohibited.

**4.3.1 Electronic Records (Cloud & Server)**
*   **Overwrite:** Where possible, data must be overwritten using a standard 3-pass wipe procedure.
*   **Crypto-Shredding:** If the biometric database is encrypted (as required by Policy IS-POL-032), the specific decryption keys associated with that user's biometric template must be destroyed.
*   **Database Purge:** Execute SQL `DELETE` commands followed by a database compaction/optimization routine to remove artifacts from storage blocks.

**4.3.2 Physical Media (Backups & Devices)**
*   If biometric data exists on physical media (e.g., decommissioned hard drives, USBs) that cannot be sanitized via software, the media must be physically destroyed via:
    *   **Shredding:** Industrial shredding to < 2mm particle size.
    *   **Degaussing:** For magnetic media, using an NSA-evaluated degausser.

#### 4.4 Third-Party Vendor Enforcement
Since Study GRC Inc. operates as a remote-first entity, biometric data is often processed by third-party processors (e.g., Identity Verification providers).

1.  **Request for Deletion:** The CISO must issue a formal written request to the vendor requiring the deletion of the specific individual's biometric data.
2.  **Verification:** The vendor must provide a *Certificate of Destruction* or a formal confirmation email stating that the data has been purged from both active systems and backups.
3.  **Contractual Review:** If a vendor refuses or fails to confirm destruction within the statutory one-year limit, the CISO must escalate the matter to Legal Counsel immediately.

#### 4.5 Documentation and Audit Trail
To prove compliance without retaining the sensitive data itself, the following log must be maintained in the *Secure Data Disposal Register* (DP-REG-002):

1.  **Name of Individual:** (Do not store the biometric ID).
2.  **Type of Identifier:** (e.g., "Fingerprint Template").
3.  **Date of Trigger Event:** (e.g., Termination Date).
4.  **Date of Destruction:** (Actual execution date).
5.  **Method Used:** (e.g., "NIST Purge" or "Vendor Confirmation").
6.  **Performed By:** (Name of IT Administrator).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Owns this procedure; verifies technical execution of destruction; manages vendor compliance. |
| **Human Resources / Volunteer Coordinator** | Notifies IT immediately upon termination of employment or volunteer service to trigger the destruction clock. |
| **IT Administrators** | Execute the technical sanitization or crypto-shredding of data; update the Disposal Register. |
| **Legal Counsel** | Provides guidance if a vendor disputes a deletion request; reviews compliance with Texas CUBI annually. |

### 6. Compliance and Enforcement
Failure to strictly adhere to this procedure places Study GRC Inc. at significant legal risk under Texas law.

*   **Civil Penalty:** Texas CUBI allows for civil penalties of up to **$25,000 per violation**.
*   **Internal Discipline:** Employees found to be retaining biometric data past the retention period, or falsifying destruction logs, are subject to disciplinary action up to and including termination of employment and legal action.

### 7. References
*   **Texas Business & Commerce Code § 503.001** (Capture or Use of Biometric Identifier).
*   **NIST SP 800-88 Rev. 1**: Guidelines for Media Sanitization.
*   **Study GRC Inc. Bylaws**: Article IX (Policies & Data Protection).
*   **IS-POL-001**: Master Information Security Policy.
*   **DP-POL-050**: Biometric Data Capture/Retention Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Compliance Architect | Initial Release aligned with Texas CUBI Act. |