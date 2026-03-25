### Vendor Contract Security Requirements

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-062 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Standard is to define the mandatory security, privacy, and legal clauses that must be included in all contracts, Master Service Agreements (MSAs), and Data Processing Agreements (DPAs) with third-party vendors. This ensures that Study GRC Inc. ("the Organization") mitigates supply chain risk, maintains compliance with regulatory obligations (including COPPA and TDPSA), and protects its intellectual property in accordance with Bylaws Article IX.

### 2. Scope
**Applies to:** All employees, contractors, and departments responsible for procuring software, hardware, or services where the vendor will:
1.  Process, store, or access the Organization’s Confidential Information or Personally Identifiable Information (PII).
2.  Have logical or physical access to the Organization’s systems, networks, or facilities.
3.  Interact directly with the Organization’s community members, including minors.

**Exclusions:** Procurement of off-the-shelf commodity hardware or supplies (e.g., office furniture, peripherals) where the vendor has no access to organizational data or networks.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Confidential Information** | Any non-public data, including PII, donor lists, financial records, proprietary curriculum, and security configurations. |
| **Subprocessor** | Any third party engaged by the Vendor to process data on behalf of the Organization. |
| **Security Incident** | The accidental or unlawful destruction, loss, alteration, unauthorized disclosure of, or access to, Confidential Information. |
| **TDPSA** | Texas Data Privacy and Security Act. |
| **COPPA** | Children's Online Privacy Protection Act (Federal). |

### 4. Standard Requirements

All contracts within the scope of this Standard must contain provisions addressing the following domains. If a Vendor refuses these terms, a Risk Acceptance Form must be signed by the Executive Director and CISO prior to contract execution.

#### 4.1 Information Security Controls
The contract must mandate that the Vendor maintains a comprehensive information security program.
*   **4.1.1 Framework Alignment:** Vendor must attest to alignment with a recognized framework (e.g., NIST CSF, ISO 27001, SOC 2 Type II).
*   **4.1.2 Encryption:** Vendor must warrant that all Confidential Information is encrypted at rest and in transit using industry-standard strong encryption (e.g., AES-256, TLS 1.2+).
*   **4.1.3 Access Control:** Vendor must utilize Multi-Factor Authentication (MFA) for all administrative access to systems hosting the Organization's data.

#### 4.2 Data Privacy and Regulatory Compliance
*   **4.2.1 Data Ownership:** The contract must explicitly state that Study GRC Inc. retains exclusive ownership of all data provided to the Vendor.
*   **4.2.2 Youth Protection (COPPA):** If the Vendor collects data from users under 13, they must warrant compliance with COPPA, including verifiable parental consent mechanisms, and agree not to use such data for behavioral advertising.
*   **4.2.3 TDPSA Compliance:** Vendor must act as a "Processor" under the Texas Data Privacy and Security Act and adhere to instructions regarding the processing of personal data.
*   **4.2.4 Data Location:** Vendor must disclose the geographic location of data storage. Storage outside the United States requires explicit prior written approval.

#### 4.3 Incident Notification and Management
*   **4.3.1 Notification Timeline:** Vendor must notify the Organization of any confirmed or suspected Security Incident without undue delay, and in no event later than **48 hours** after discovery.
*   **4.3.2 Cooperation:** Vendor must agree to provide all necessary cooperation and data to assist the Organization in its investigation and regulatory reporting obligations.

#### 4.4 Intellectual Property (Bylaws Art. IX)
*   **4.4.1 Work Made for Hire:** In accordance with Bylaws Article IX, Section 9.3, any custom code, content, or materials created by the Vendor for the Organization must be defined as "Work Made for Hire," with all rights assigned to Study GRC Inc.
*   **4.4.2 Open Source Compatibility:** Vendor must warrant that no deliverables contain copyleft open-source code that would legally compel the Organization to release its proprietary systems under a specific license, unless explicitly authorized.

#### 4.5 Audit and Assessment Rights
*   **4.5.1 Right to Audit:** The Organization (or its designated independent auditor) reserves the right to audit the Vendor’s security controls and compliance with the agreement annually or following a Security Incident.
*   **4.5.2 Documentation:** Vendor agrees to provide current SOC 2 Type II reports, ISO certificates, or equivalent third-party attestations upon request.

#### 4.6 Liability and Indemnification
*   **4.6.1 Indemnification:** Vendor must indemnify and hold harmless Study GRC Inc., its Directors, and Officers against all claims, liabilities, and expenses arising from the Vendor’s negligence, misconduct, or breach of data privacy obligations.
*   **4.6.2 Cyber Liability Insurance:** Vendor must maintain Cyber Liability Insurance with coverage of not less than $1,000,000 per occurrence.

#### 4.7 Termination and Data Destruction
*   **4.7.1 Return of Data:** Upon termination of the agreement, Vendor must return all Confidential Information in a usable, machine-readable format within 30 days.
*   **4.7.2 Secure Destruction:** Following the return of data, Vendor must securely destroy all remaining copies in accordance with NIST SP 800-88 guidelines and provide a Certificate of Destruction.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Contract Owner** | Ensures the Vendor is aware of these requirements during the RFP/negotiation phase. |
| **CISO** | Reviews Vendor security addendums and assesses compliance with this Standard; authorizes exceptions. |
| **Legal Counsel** | Drafts and approves final contract language; negotiates specific liability caps. |
| **Executive Director** | Final signatory authority; approves Risk Acceptance for deviations from this Standard. |

### 6. Compliance and Enforcement
Failure to include these mandatory requirements in applicable contracts without an approved exception may result in the revocation of procurement authority and disciplinary action, up to and including termination of employment. Contracts executed in violation of this Standard may be declared voidable by the Board of Directors.

### 7. References
*   **Bylaws of Study GRC Inc.** (Article IX - Intellectual Property)
*   **IS-POL-001:** Master Information Security Policy
*   **IS-POL-020:** Vendor/Third-Party Risk Policy
*   **External:** Texas Data Privacy and Security Act (TDPSA)
*   **External:** Children's Online Privacy Protection Act (COPPA)
*   **External:** NIST SP 800-88 (Guidelines for Media Sanitization)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Legal Officer | Initial Release |