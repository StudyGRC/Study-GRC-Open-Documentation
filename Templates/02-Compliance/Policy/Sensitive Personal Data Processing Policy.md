### Sensitive Personal Data Processing Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | DP-POL-035 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Public |

### 1. Purpose
The purpose of this policy is to establish strict governance regarding the collection, processing, and storage of "Sensitive Data" within Study GRC Inc. As a Texas non-profit operating under the Texas Data Privacy and Security Act (TDPSA), the Organization is legally mandated to obtain specific, informed, and unambiguous consent before processing sensitive personal information. This policy mitigates legal liability, protects the civil liberties of our community members—specifically K-12 participants—and ensures compliance with Article IX of the Bylaws regarding Data Protection.

### 2. Scope
This policy applies to all "Sensitive Data" collected, processed, or stored by Study GRC Inc., regardless of the format (electronic or physical).

*   **Applies to:** All employees, Board Directors, volunteers, contractors, and third-party vendors acting on behalf of the Organization.
*   **Exclusions:** Data that is publicly available (as defined by TDPSA), de-identified data where re-identification is prevented via technical controls, and standard non-sensitive personal data (e.g., business email addresses) covered under the *Master Data Privacy Policy (DP-POL-001)*.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Sensitive Data** | Under TDPSA, personal data revealing racial or ethnic origin, religious beliefs, mental or physical health diagnosis, sexuality, citizenship or immigration status; genetic or biometric data processed for identification; precise geolocation data; and **personal data of a known child** (under 13). |
| **Consent** | A clear, affirmative act signifying a consumer’s freely given, specific, informed, and unambiguous agreement to process their personal data. It cannot be obtained via "Dark Patterns" or broad Terms of Service acceptance. |
| **Dark Pattern** | A user interface designed or manipulated with the substantial effect of subverting or impairing user autonomy, decision-making, or choice (e.g., pre-checked boxes). |
| **Data Protection Impact Assessment (DPIA)** | A documented process to identify and minimize the data protection risks of a project, mandatory under TDPSA for sensitive data processing. |
| **Known Child** | An individual known to be under the age of 13 (per COPPA/TDPSA) or under 18 for the purposes of Study GRC's internal youth protection standards. |

### 4. Policy Statements

#### 4.1 General Prohibition and Minimization
Study GRC Inc. adopts a "default deny" posture regarding Sensitive Data. No employee, volunteer, or system may collect Sensitive Data unless:
1.  There is a documented, critical business or educational necessity.
2.  A **Data Protection Impact Assessment (DPIA)** has been completed and approved by the CISO or Data Protection Officer (DPO).
3.  Explicit **Consent** has been obtained from the data subject (or parent/guardian) prior to collection.

#### 4.2 Mandatory Consent Requirements (TDPSA Compliance)
In accordance with TDPSA Sec. 541.101, the Organization must obtain consent *before* processing Sensitive Data.
*   **4.2.1 Clear and Affirmative Act:** Consent must be obtained via a standalone action (e.g., clicking a specific "I Consent" button or signing a specific form). Pre-checked boxes are strictly prohibited.
*   **4.2.2 No Bundling:** Consent for Sensitive Data processing cannot be bundled with the general Terms of Service or Privacy Policy. It must be a distinct request.
*   **4.2.3 Revocability:** Data subjects must be able to revoke consent as easily as they gave it. Upon revocation, processing must cease within 15 days.
*   **4.2.4 Dark Patterns:** The use of user interfaces that manipulate, deceive, or coerce a user into providing consent (Dark Patterns) is prohibited.

#### 4.3 Processing Data of a Known Child
Given the Organization's K-12 focus, the processing of youth data is classified as "Sensitive" by default.
*   **4.3.1 Parental Consent:** For any participant under the age of 13, Verifiable Parental Consent (VPC) is required prior to collection, in alignment with COPPA and TDPSA.
*   **4.3.2 Youth Protection:** For participants aged 13-17, the Organization shall treat data with the same security controls as Sensitive Data, requiring affirmative consent from the participant and/or guardian depending on the specific program risk profile.

#### 4.4 Biometric Data
In accordance with the Texas Capture or Use of Biometric Identifier (CUBI) Act and Bylaws Article IX:
*   The Organization shall not capture biometric identifiers (fingerprints, retina scans, face geometry) unless strictly necessary for security or accessibility.
*   Commercialization (selling/leasing) of biometric data is strictly prohibited.

#### 4.5 Security Controls for Sensitive Data
*   **4.5.1 Encryption:** All Sensitive Data must be encrypted at rest (AES-256 or higher) and in transit (TLS 1.2+).
*   **4.5.2 Access Control:** Access is restricted to the specific individuals who require it for the stated purpose (Principle of Least Privilege).
*   **4.5.3 BYOD Restriction:** Sensitive Data must never be downloaded to or stored on personal unmanaged devices. It may only be accessed via secure, Organization-managed environments or encrypted virtual desktop infrastructure (VDI).

#### 4.6 Data Protection Impact Assessments (DPIA)
Pursuant to TDPSA Sec. 541.105, the Organization must conduct and document a DPIA for any processing activity involving Sensitive Data. The DPIA must weigh the benefits of processing against the potential risks to the rights of the consumer.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Owns this policy; approves DPIAs; ensures technical controls (encryption/access) are effective. |
| **Data Protection Officer (DPO)** | Monitors compliance with TDPSA; reviews consent mechanisms for legal sufficiency; manages consent revocation requests. |
| **Program Directors (e.g., VP Education)** | Identifies business needs for Sensitive Data; ensures staff do not collect data outside of approved channels. |
| **All Staff & Volunteers** | Adhere to the "Default Deny" standard; report any unauthorized collection of Sensitive Data immediately. |
| **Board of Directors** | Reviews annual reports on data privacy compliance and high-risk processing activities per Bylaws Article III. |

### 6. Compliance and Enforcement
Failure to comply with this policy may result in disciplinary action, up to and including termination of employment or volunteer assignment.
*   **Legal Penalties:** Violations of TDPSA can result in civil penalties of up to $7,500 per violation enforced by the Texas Attorney General.
*   **Internal Action:** Any volunteer or employee found circumventing consent mechanisms or using Dark Patterns will be subject to immediate removal for cause.

### 7. References
*   **Texas Data Privacy and Security Act (TDPSA)** (Bus. & Com. Code Ch. 541)
*   **Children’s Online Privacy Protection Act (COPPA)**
*   **Texas CUBI Act** (Bus. & Com. Code Ch. 503)
*   **Study GRC Bylaws** (Article IX - Policies & Data Protection)
*   **DP-POL-001:** Master Data Privacy Policy
*   **DP-FRM-005:** Data Protection Impact Assessment (DPIA) Template

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Legal Officer | Initial Draft aligned with TDPSA requirements. |