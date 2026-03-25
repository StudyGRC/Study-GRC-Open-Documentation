### Vendor Security Questionnaire (VSQ)

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-FRM-005 |
| **Document Type** | Form / Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | IT Security Manager |
| **Classification** | Public (Blank) / Confidential (Completed) |

### 1. Purpose
The purpose of this Vendor Security Questionnaire (VSQ) is to assess the information security, data privacy, and compliance posture of third-party vendors prior to engagement. This document ensures Study GRC Inc. fulfills its due diligence obligations under **2 CFR § 200.318(h)** (oversight of contractors), **Texas Business and Commerce Code (TBCC) Chapter 521**, and **Bylaws Article IX** (Policies & Data Protection). It serves to identify risks associated with outsourcing services and ensures vendors meet the Organization's minimum security standards.

### 2. Scope
This questionnaire applies to all potential and existing Third-Party Vendors, Service Providers, and Contractors who:
1.  Process, store, or transmit Study GRC Inc. Confidential Information or Personally Identifiable Information (PII).
2.  Have logical access to Study GRC Inc. systems, networks, or code repositories.
3.  Provide critical infrastructure or software-as-a-service (SaaS) solutions.

**Exclusions:** Vendors providing commodity goods (e.g., office supplies) with no access to digital systems or data are exempt from this questionnaire unless otherwise directed by the CISO.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Confidential Information** | Any non-public data, including PII, donor lists, financial records, and unpublished intellectual property as defined in Bylaws Article IX. |
| **PII** | Personally Identifiable Information. Data that can identify a specific individual (e.g., name, email, IP address), specifically including data regarding minors. |
| **Subprocessor** | Any third party engaged by the Vendor to process data on behalf of Study GRC Inc. |
| **COPPA** | Children's Online Privacy Protection Act. Federal law regulating the collection of data from children under 13. |
| **2 CFR 200** | Uniform Administrative Requirements, Cost Principles, and Audit Requirements for Federal Awards (Uniform Guidance). |

### 4. Questionnaire Requirements

**Instructions to Vendor:**
Please complete the following sections truthfully and provide supporting documentation where requested. Failure to provide accurate information may result in disqualification from the procurement process or termination of existing contracts.

#### 4.1 General Information

| Question ID | Question | Vendor Response |
| :--- | :--- | :--- |
| **GEN-01** | Company Legal Name & Headquarters Location: | |
| **GEN-02** | Name and Title of person completing this form: | |
| **GEN-03** | Describe the specific service/product to be provided: | |
| **GEN-04** | Will you use Subprocessors to deliver this service? If yes, list them. | |

#### 4.2 Compliance & Certifications

| Question ID | Question | Vendor Response |
| :--- | :--- | :--- |
| **CMP-01** | Do you hold a current SOC 2 Type II report? (If yes, attach executive summary). | [ ] Yes [ ] No |
| **CMP-02** | Are you ISO 27001 certified? | [ ] Yes [ ] No |
| **CMP-03** | If handling credit card data, are you PCI-DSS compliant? | [ ] Yes [ ] No [ ] N/A |
| **CMP-04** | Have you undergone a third-party penetration test in the last 12 months? | [ ] Yes [ ] No |

#### 4.3 Data Privacy & Legal (GDPR / TDPSA / COPPA)

| Question ID | Question | Vendor Response |
| :--- | :--- | :--- |
| **PRV-01** | Do you comply with the Texas Data Privacy and Security Act (TDPSA)? | [ ] Yes [ ] No |
| **PRV-02** | **Critical:** Does your service collect data from individuals under the age of 13? If yes, describe your COPPA compliance mechanism (Verifiable Parental Consent). | |
| **PRV-03** | Do you sell user data to third parties? (Note: Study GRC strictly prohibits the sale of our community data). | [ ] Yes [ ] No |
| **PRV-04** | Can you support Data Subject Access Requests (DSAR) and Deletion requests within 30 days? | [ ] Yes [ ] No |
| **PRV-05** | Where will Study GRC data be geographically stored (Data Residency)? | |

#### 4.4 Information Security Controls

| Question ID | Question | Vendor Response |
| :--- | :--- | :--- |
| **SEC-01** | Is Multi-Factor Authentication (MFA) enforced for all employees with access to customer data? | [ ] Yes [ ] No |
| **SEC-02** | Is data encrypted at rest (e.g., AES-256) and in transit (e.g., TLS 1.2+)? | [ ] Yes [ ] No |
| **SEC-03** | Do you perform background checks on all employees with access to customer data? | [ ] Yes [ ] No |
| **SEC-04** | Do you have a formal Vulnerability Management program (patching timelines)? | [ ] Yes [ ] No |
| **SEC-05** | Do you support Single Sign-On (SSO) integration (SAML/OIDC)? | [ ] Yes [ ] No |

#### 4.5 Incident Response & Business Continuity

| Question ID | Question | Vendor Response |
| :--- | :--- | :--- |
| **IR-01** | Do you have a documented Incident Response Plan (IRP)? | [ ] Yes [ ] No |
| **IR-02** | Do you agree to notify Study GRC Inc. of a confirmed data breach affecting our data within 72 hours (or sooner if required by law)? | [ ] Yes [ ] No |
| **IR-03** | Do you maintain a Business Continuity Plan (BCP) and Disaster Recovery (DR) plan? | [ ] Yes [ ] No |
| **IR-04** | How frequently are data backups tested? | |

#### 4.6 Software Development Life Cycle (SDLC)
*Applicable only for Software/SaaS Vendors*

| Question ID | Question | Vendor Response |
| :--- | :--- | :--- |
| **DEV-01** | Do you follow OWASP Top 10 guidelines in your development process? | [ ] Yes [ ] No |
| **DEV-02** | Do you scan your code for vulnerabilities (SAST/DAST) prior to release? | [ ] Yes [ ] No |
| **DEV-03** | **IP Rights:** Do you claim ownership of any content or data generated by Study GRC users on your platform? (Reference Bylaws Art. IX §9.3). | [ ] Yes [ ] No |

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Vendor Representative** | Complete the questionnaire accurately, attach evidence, and sign the attestation. |
| **Internal Sponsor (Study GRC)** | Initiate the vendor assessment request and ensure the vendor understands the scope of work. |
| **CISO / Security Team** | Review submitted answers, assign a risk score, and approve or reject the vendor based on risk appetite. |
| **Legal / Procurement** | Ensure the Master Services Agreement (MSA) includes clauses enforcing the security controls claimed in this document. |

### 6. Compliance and Enforcement
Submission of this questionnaire constitutes a formal representation of the Vendor's security posture.
*   **Misrepresentation:** Providing false or misleading information is grounds for immediate contract termination for cause and potential legal action for damages.
*   **Audit Rights:** Study GRC Inc. reserves the right to audit the Vendor (or request third-party audit reports) to verify the responses provided herein, pursuant to the "Right to Audit" clause in the governing contract.

### 7. References
*   **Study GRC Bylaws Article IX:** Policies & Data Protection.
*   **NIST Cybersecurity Framework (CSF) 2.0:** Supply Chain Risk Management (GV.SC).
*   **2 CFR § 200.318:** General Procurement Standards.
*   **Texas Business & Commerce Code § 521.053:** Notification Required Following Breach of Security of Computerized Data.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | CISO | Initial Release aligned with Governance Framework. |