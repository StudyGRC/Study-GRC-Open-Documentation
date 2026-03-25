### Secure Data Disposal Certificate

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-FRM-015 |
| **Document Type** | Form / Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2025-10-27 (Bi-Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | IT Operations Manager |
| **Classification** | Internal |

### 1. Purpose
The purpose of this document is to provide a formal, auditable record of data sanitization and media destruction. This certificate serves as the definitive proof that Study GRC Inc. (the "Organization") has met its obligation to render sensitive data irretrievable in compliance with **NIST SP 800-88 Rev. 1 (Guidelines for Media Sanitization)** and **Bylaws Article IX (Policies & Data Protection)**. This record is essential for legal defense ("defensible disposal") and regulatory compliance regarding Member and Youth data.

### 2. Scope
This form applies to all **Media** owned, leased, or managed by Study GRC Inc. that has reached the end of its lifecycle or is being transferred out of the Organization's control.

*   **Applies to:** All employees, volunteers, contractors, and third-party vendors handling Organization data.
*   **Media Types:** Includes but is not limited to Hard Disk Drives (HDD), Solid State Drives (SSD), Mobile Devices, Flash Memory, Paper Records, and Virtual/Cloud Storage Volumes.
*   **Exclusions:** Transient data deletion (e.g., emptying the Recycle Bin) during normal daily operations, unless the data is classified as "Restricted" or "Confidential."

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Sanitization** | A process to render access to "Target Data" on the media infeasible for a given level of effort. |
| **Clear** | A method using software or hardware to sanitize media to prevent information retrieval by data, disk, or file recovery utilities (e.g., Overwrite). |
| **Purge** | A method that renders Target Data infeasible to recover using state-of-the-art laboratory techniques (e.g., Secure Erase, Degaussing). |
| **Destroy** | The result of actions that render Target Data recovery infeasible using state-of-the-art laboratory techniques and results in the subsequent inability to use the media for storage of data (e.g., Shredding, Incineration). |
| **Media** | The physical or virtual material on which data is stored. |

### 4. Instructions for Use

#### 4.1 Mandatory Completion
This Certificate must be completed for every asset containing **Confidential** or **Restricted** data (as defined in the *Data Classification Standard*) prior to disposal, resale, return to lessor, or donation.

#### 4.2 NIST Alignment
The individual performing the sanitization must select the appropriate method based on the sensitivity of the data and the type of media, in accordance with **NIST SP 800-88 Guidelines**:
*   **Clear:** Acceptable for Internal data remaining within the organization.
*   **Purge:** Required for Confidential data leaving the organization's control.
*   **Destroy:** Required for Restricted data (e.g., Youth PII, Financials) or failed media.

#### 4.3 Verification
For physical media containing Restricted data, a second individual (Witness) or a generated log file from the sanitization software must verify the process.

---

### 5. CERTIFICATE OF SANITIZATION (FORM)

**Instructions:** Complete all sections below. Attach automated logs if available.

#### SECTION A: ASSET IDENTIFICATION
| Field | Details |
| :--- | :--- |
| **Asset Tag / ID** | |
| **Manufacturer** | |
| **Model Number** | |
| **Serial Number** | |
| **Media Type** | ☐ HDD &nbsp; ☐ SSD &nbsp; ☐ Mobile Device &nbsp; ☐ USB/Flash &nbsp; ☐ Paper &nbsp; ☐ Cloud Volume |
| **Data Classification** | ☐ Public &nbsp; ☐ Internal &nbsp; ☐ Confidential &nbsp; ☐ Restricted (PII/Financial) |

#### SECTION B: SANITIZATION METHOD (NIST SP 800-88)
*Select the method used to sanitize the media.*

**☐ Method 1: CLEAR (Overwrite)**
*   **Tool Used:** (e.g., DBAN, Active@ KillDisk) _____________________________
*   **Passes:** ☐ 1-Pass &nbsp; ☐ 3-Pass (DoD) &nbsp; ☐ 7-Pass
*   **Verification:** ☐ Full Verification &nbsp; ☐ 10% Sampling

**☐ Method 2: PURGE (Cryptographic Erase / Block Erase)**
*   **Technique:** ☐ ATA Secure Erase &nbsp; ☐ Crypto-Shredding (Key Destruction) &nbsp; ☐ Degaussing
*   **Tool/Device Used:** _____________________________

**☐ Method 3: DESTROY (Physical Destruction)**
*   **Technique:** ☐ Shredding (Cross-cut) &nbsp; ☐ Incineration &nbsp; ☐ Pulverization &nbsp; ☐ Drilling (4+ holes)
*   **Particle Size (if shredding):** ☐ < 6mm (Paper/SSD) &nbsp; ☐ Standard Strip

#### SECTION C: CHAIN OF CUSTODY & CERTIFICATION
*I certify that the media identified above has been sanitized in accordance with Study GRC Inc. policies and NIST SP 800-88 standards. The data is irretrievable.*

| Role | Name | Title | Signature | Date |
| :--- | :--- | :--- | :--- | :--- |
| **Sanitized By** | | | | |
| **Verified By** | | | | |
| **Disposal Method** | ☐ E-Waste Recycler &nbsp; ☐ Trash (Shredded Paper) &nbsp; ☐ Re-deployed &nbsp; ☐ Returned to Lessor |

---

### 6. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Asset Owner** | Identifies media requiring disposal and initiates the sanitization request. |
| **IT Operations / CISO** | Performs or oversees the technical sanitization process and signs as "Sanitized By." |
| **Witness / Auditor** | Verifies the destruction of media containing "Restricted" data and signs as "Verified By." |
| **Records Manager** | Retains this signed Certificate in the central compliance repository for a minimum of 7 years per the *Records Retention Schedule*. |

### 7. Compliance and Enforcement
Failure to complete this certificate prior to the disposal of hardware or records may result in disciplinary action, up to and including termination of employment or volunteer assignment. Falsification of this document is a violation of the **Board Code of Ethics** and may result in legal action.

### 8. References
*   **NIST SP 800-88 Rev. 1:** Guidelines for Media Sanitization
*   **Study GRC Bylaws Article IX:** Data Protection & Intellectual Property
*   **IS-POL-001:** Master Information Security Policy
*   **IS-STD-004:** Data Classification Standard

### 9. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Compliance Architect | Initial Release aligned with NIST 800-88. |