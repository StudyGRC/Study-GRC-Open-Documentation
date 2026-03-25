### Vendor Security Risk Assessment (VSRA)

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-FRM-005 |
| **Document Type** | Form / Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-01 |
| **Next Review Date** | 2024-10-01 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | IT Security Manager |
| **Classification** | Confidential (When Filled) |

### 1. Purpose
The purpose of this Vendor Security Risk Assessment (VSRA) is to evaluate the information security, privacy, and compliance posture of third-party vendors, service providers, and partners before Study GRC Inc. (the "Organization") enters into a contractual relationship.

This assessment ensures compliance with:
*   **Bylaws Article IX (Policies & Data Protection):** Specifically Section 9.2 regarding confidentiality and data protection.
*   **2 CFR 200.318 (General Procurement Standards):** Requiring oversight to ensure contractors perform in accordance with the terms, conditions, and specifications of their contracts.
*   **NIST Cybersecurity Framework (CSF) 2.0:** Supply Chain Risk Management (GV.SC).

### 2. Scope
This assessment applies to all potential and existing vendors, contractors, and SaaS providers who:
1.  Process, store, or transmit Organization Data (including Member PII, Youth Data, or Financial Records).
2.  Have logical access to the Organization’s IT systems or networks.
3.  Develop software or intellectual property for the Organization.

**Exclusions:** Vendors providing commodity goods (e.g., office supplies) with no access to digital systems or data are exempt from this full assessment but may require a simplified review.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Confidential Information** | As defined in Bylaws Article IX, Section 9.2, includes proprietary data, member lists, and sensitive financial information. |
| **COPPA** | Children's Online Privacy Protection Act; federal law regulating the collection of data from children under 13. |
| **PII** | Personally Identifiable Information (e.g., names, emails, addresses). |
| **SaaS** | Software as a Service; cloud-based applications. |
| **Subprocessor** | Any third party hired by the Vendor who will also have access to Study GRC Inc. data. |
| **Youth Data** | Any data related to participants in K-12 programs, requiring enhanced safeguarding. |

### 4. Assessment Questionnaire
*Instructions to Vendor: Please complete all sections below. Attach supporting documentation (SOC 2 reports, ISO certificates, policies) where indicated.*

#### 4.1 General Information
| Field | Response |
| :--- | :--- |
| **Vendor Name** | |
| **Product/Service Name** | |
| **Primary Security Contact** | |
| **Contact Email** | |
| **Headquarters Location** | |

#### 4.2 Compliance & Certifications
*Does the organization hold valid, third-party audited certifications?*

1.  **SOC 2 Type II:** [ ] Yes [ ] No (If Yes, attach most recent report).
2.  **ISO 27001:** [ ] Yes [ ] No (If Yes, attach certificate).
3.  **FedRAMP Authorized:** [ ] Yes [ ] No.
4.  **Debarment Status:** Is the vendor or its principals listed on the U.S. Government’s System for Award Management (SAM.gov) exclusion list? [ ] Yes [ ] No.

#### 4.3 Data Privacy & Youth Protection
*Pursuant to Study GRC Inc. Bylaws Article I, Section 1.3 (Educational Purposes) and Article IX.*

1.  **Data Residency:** Where will Study GRC Inc. data be stored? (Country/Region): __________________
2.  **Data Ownership:** Do you claim ownership of data uploaded by the customer? [ ] Yes [ ] No
3.  **Data Mining:** Do you use customer data for your own analytics, AI training, or marketing purposes? [ ] Yes [ ] No
4.  **COPPA Compliance:** If your service interacts with children under 13, do you have a mechanism for Verifiable Parental Consent? [ ] Yes [ ] No [ ] N/A
5.  **Data Subject Rights:** Do you have a process to support GDPR/TDPSA requests (Right to be Forgotten, Right to Access) within 30 days? [ ] Yes [ ] No

#### 4.4 Information Security Controls
*Based on NIST CSF 2.0 Standards.*

1.  **Encryption at Rest:** Is customer data encrypted at rest? [ ] Yes [ ] No (Algorithm: __________)
2.  **Encryption in Transit:** Is data encrypted in transit (TLS 1.2+)? [ ] Yes [ ] No
3.  **Access Control:** Do you support Single Sign-On (SSO) or enforce Multi-Factor Authentication (MFA) for administrative access? [ ] Yes [ ] No
4.  **Vulnerability Management:** Do you perform regular penetration testing or vulnerability scanning? [ ] Yes [ ] No (Frequency: __________)
5.  **Background Checks:** Do all employees with access to customer data undergo criminal background checks? [ ] Yes [ ] No

#### 4.5 Business Continuity & Incident Response
1.  **Incident Notification:** Do you agree to notify Study GRC Inc. within 72 hours of a confirmed data breach affecting our data? [ ] Yes [ ] No
2.  **Backups:** How frequently is data backed up? __________________
3.  **Disaster Recovery:** Do you have a documented Disaster Recovery Plan (DRP) tested annually? [ ] Yes [ ] No

#### 4.6 Intellectual Property & Development
*Applicable only if Vendor is developing custom code/content.*

1.  **Work Made for Hire:** Do you acknowledge that, pursuant to Bylaws Article IX, Section 9.3, all work product created for Study GRC Inc. is the exclusive property of the Organization? [ ] Yes [ ] No
2.  **Open Source:** Do you scan code for open-source licensing conflicts? [ ] Yes [ ] No

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Internal Sponsor** | Initiates the VSRA process; ensures the Vendor completes the form prior to contract signature. |
| **Vendor** | Provides accurate, truthful, and complete responses; supplies evidence (e.g., SOC 2 report). |
| **CISO / IT Security** | Reviews the completed VSRA; assigns a Risk Score (Low/Med/High); approves or rejects the vendor. |
| **Legal Counsel** | Incorporates necessary security addendums (DPA, SCCs) into the final contract based on VSRA findings. |

### 6. Compliance and Enforcement
**Internal:** Failure by Study GRC Inc. staff to execute a VSRA prior to sharing sensitive data with a vendor is a violation of the *Master Information Security Policy* and may result in disciplinary action.

**External:** Misrepresentation of security controls by a Vendor in this document constitutes a material breach of contract and may result in immediate termination of the agreement and legal action for damages.

### 7. References
*   **Study GRC Inc. Bylaws:** Article IX (Policies & Data Protection).
*   **2 CFR 200.318(h):** Procurement Standards - Oversight.
*   **NIST SP 800-161:** Supply Chain Risk Management Practices.
*   **IS-POL-001:** Master Information Security Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-01 | CISO | Initial Release |