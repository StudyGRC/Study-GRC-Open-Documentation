### Vendor Privacy/Security Questionnaire

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-FRM-005 |
| **Document Type** | Form |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | CISO |
| **Classification** | Public (Blank) / Confidential (Completed) |

### 1. Purpose
The purpose of this **Vendor Privacy/Security Questionnaire (VSQ)** is to evaluate the information security and data privacy posture of third-party vendors, service providers, and partners prior to the execution of a contract or the sharing of Study GRC Inc. data.

As a Texas non-profit corporation dealing with youth data and federal grant funds, Study GRC Inc. must ensure that all downstream partners adhere to strict standards regarding:
1.  **Data Protection:** Compliance with GDPR, CCPA/CPRA, and the Texas Data Privacy and Security Act (TDPSA).
2.  **Youth Safety:** Strict adherence to COPPA and the Organization's *Child and Youth Safeguarding Policy*.
3.  **Federal Compliance:** Adherence to 2 CFR 200 provisions regarding protected personally identifiable information (PPII).

### 2. Scope
This questionnaire must be completed by any potential or existing vendor that will:
*   Process, store, or transmit Study GRC Inc. **Confidential** or **Restricted** data (including Member PII or Youth Data).
*   Have logical access to Study GRC Inc. systems, networks, or code repositories.
*   Provide critical infrastructure services (e.g., cloud hosting, authentication).

**Exclusions:** Vendors providing commodity goods (e.g., office supplies) with no access to digital systems or data are exempt from this form.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Confidential Information** | Data that is not public, including member lists, financial data, and strategic plans, as defined in Bylaws Article IX. |
| **Youth Data** | Any PII collected from or about individuals under the age of 18. |
| **Subprocessor** | Any third party engaged by the Vendor to process data on behalf of Study GRC Inc. |
| **COPPA** | Children's Online Privacy Protection Act (US Federal Law). |
| **MFA** | Multi-Factor Authentication. |
| **SOC 2** | Service Organization Control 2 (Audit report on controls relevant to security, availability, processing integrity, confidentiality, or privacy). |

### 4. Questionnaire Instructions
**To the Vendor:** Please answer all questions truthfully. Attach supporting documentation (e.g., SOC 2 Type II report, ISO 27001 certificate, Privacy Policy) where indicated. Failure to provide accurate information may result in disqualification from the procurement process or termination of existing contracts.

#### 4.1 General Information & Federal Compliance

| # | Question | Response |
| :--- | :--- | :--- |
| **1.1** | **Company Name:** | `[Enter Name]` |
| **1.2** | **Product/Service Name:** | `[Enter Product]` |
| **1.3** | **Data Residency:** Where will Study GRC data be stored? (List Countries) | `[Enter Locations]` |
| **1.4** | **Federal Debarment:** Is your organization currently suspended or debarred from receiving US Federal contracts (SAM.gov)? | [ ] Yes [ ] No |
| **1.5** | **Subcontractors:** Do you utilize third parties to process client data? If yes, provide a list. | [ ] Yes [ ] No |

#### 4.2 Information Security Governance & Certifications

| # | Question | Response |
| :--- | :--- | :--- |
| **2.1** | **Security Program:** Do you have a formal, written Information Security Program? | [ ] Yes [ ] No |
| **2.2** | **Leadership:** Is there a designated individual responsible for Information Security (e.g., CISO)? | [ ] Yes [ ] No |
| **2.3** | **Certifications:** Do you hold valid third-party attestations? (Check all that apply and attach copies) | [ ] SOC 2 Type II<br>[ ] ISO 27001<br>[ ] FedRAMP<br>[ ] None |
| **2.4** | **Policies:** Do you require employees to sign confidentiality agreements and undergo security awareness training annually? | [ ] Yes [ ] No |

#### 4.3 Access Control & Technical Security

| # | Question | Response |
| :--- | :--- | :--- |
| **3.1** | **Authentication:** Do you enforce Multi-Factor Authentication (MFA) for all administrative access to your environment? | [ ] Yes [ ] No |
| **3.2** | **Encryption (Transit):** Is all data encrypted in transit using TLS 1.2 or higher? | [ ] Yes [ ] No |
| **3.3** | **Encryption (Rest):** Is client data encrypted at rest (e.g., AES-256)? | [ ] Yes [ ] No |
| **3.4** | **Segregation:** Is client data logically separated from other customers' data? | [ ] Yes [ ] No |
| **3.5** | **Vulnerability Mgmt:** Do you perform regular vulnerability scans and penetration testing? | [ ] Yes [ ] No |
| **3.6** | **Remote Access:** Do you utilize a VPN or Zero Trust Network Access (ZTNA) solution for remote employee access? | [ ] Yes [ ] No |

#### 4.4 Privacy & Regulatory Compliance (GDPR / CCPA / TDPSA)

| # | Question | Response |
| :--- | :--- | :--- |
| **4.1** | **DPA:** Are you willing to sign a Data Processing Agreement (DPA) incorporating Standard Contractual Clauses (SCCs)? | [ ] Yes [ ] No |
| **4.2** | **Data Subject Rights:** Do you have a mechanism to respond to DSARs (Access, Deletion, Correction) within 30 days? | [ ] Yes [ ] No |
| **4.3** | **Data Sale:** Do you sell client data to third parties or use it for cross-context behavioral advertising? | [ ] Yes [ ] No |
| **4.4** | **Retention:** Do you support automated data deletion upon contract termination? | [ ] Yes [ ] No |

#### 4.5 Youth Protection (COPPA & Safety)
*Mandatory for any vendor interacting with the Study GRC Community Platform or Educational Resources.*

| # | Question | Response |
| :--- | :--- | :--- |
| **5.1** | **Target Audience:** Is your service directed at children under 13? | [ ] Yes [ ] No |
| **5.2** | **Age Gating:** Does your system have age-verification or age-gating mechanisms? | [ ] Yes [ ] No |
| **5.3** | **Parental Consent:** If you collect data from children <13, do you obtain Verifiable Parental Consent (VPC)? | [ ] Yes [ ] No |
| **5.4** | **Moderation:** If your service allows user interaction, do you employ moderation tools to prevent grooming or bullying? | [ ] Yes [ ] No |
| **5.5** | **Background Checks:** Do you perform criminal background checks on all employees with access to user data? | [ ] Yes [ ] No |

#### 4.6 Incident Response & Business Continuity

| # | Question | Response |
| :--- | :--- | :--- |
| **6.1** | **IR Plan:** Do you have a documented Incident Response Plan that is tested at least annually? | [ ] Yes [ ] No |
| **6.2** | **Notification:** Do you agree to notify Study GRC Inc. of a confirmed security breach affecting our data within **72 hours**? | [ ] Yes [ ] No |
| **6.3** | **Backups:** Are backups performed daily and tested for restoration integrity? | [ ] Yes [ ] No |
| **6.4** | **Disaster Recovery:** Do you have a Business Continuity/Disaster Recovery (BC/DR) plan? | [ ] Yes [ ] No |

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Vendor Representative** | Complete the questionnaire accurately, attach evidence, and sign the attestation. |
| **Requesting Department** | Initiate the VSQ process and ensure the vendor submits the form prior to contract negotiation. |
| **Chief Information Security Officer (CISO)** | Review submitted VSQ, assign a risk score, and approve or reject the vendor based on risk appetite. |
| **Legal Counsel** | Ensure the contract includes necessary clauses (DPA, BAA, etc.) based on the VSQ responses. |

### 6. Compliance and Enforcement
**Vendor Attestation:**
By submitting this form, the Vendor certifies that the information provided is true and correct. The Vendor acknowledges that any misrepresentation of their security posture may result in:
1.  Immediate disqualification from the bidding process.
2.  Termination of contract for cause (if discovered post-contract).
3.  Legal action for damages resulting from a breach caused by undisclosed security deficiencies.

**Internal Enforcement:**
Study GRC Inc. employees who bypass this Due Diligence process and share Confidential data with unvetted vendors are subject to disciplinary action, up to and including termination, in accordance with the *Master Information Security Policy*.

### 7. References
*   **Study GRC Bylaws Article IX:** Intellectual Property & Confidentiality.
*   **IS-POL-001:** Master Information Security Policy.
*   **GOV-POL-005:** Child and Youth Safeguarding Policy.
*   **2 CFR 200.318(h):** Federal Procurement Standards (Oversight).
*   **NIST SP 800-161:** Supply Chain Risk Management Practices.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | CISO | Initial Release |