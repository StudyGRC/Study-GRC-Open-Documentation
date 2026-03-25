### IT Procurement Security Checklist

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-CHK-015 |
| **Document Type** | Checklist / Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Director of IT Operations |
| **Classification** | Internal |

### 1. Purpose
The purpose of this document is to establish a mandatory security review process for all Information Technology (IT) procurement activities at Study GRC Inc. This checklist ensures that all software, hardware, and cloud services (SaaS/PaaS/IaaS) acquired by the Organization meet our minimum security, privacy, and compliance standards prior to purchase or implementation.

This document supports the **Master Information Security Policy** and the **Procurement Policy (Federal Standards)** by mitigating supply chain risks, preventing "Shadow IT," and ensuring compliance with 2 CFR 200 and Texas Business Organizations Code.

### 2. Scope
This checklist applies to **all** employees, contractors, and board members initiating a request for new technology.

**In Scope:**
*   **SaaS Applications:** (e.g., Project management tools, CRM, marketing platforms).
*   **Infrastructure:** Cloud hosting, servers, networking equipment.
*   **Development Tools:** Code repositories, libraries, APIs.
*   **Hardware:** Laptops, mobile devices, biometric scanners.
*   **Free/Open Source Software:** "Zero-cost" tools must still undergo this review to ensure security integrity.

**Exclusions:**
*   Standard office supplies (non-digital).
*   Renewal of existing contracts (unless significant changes to scope or architecture have occurred).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **SaaS** | Software as a Service; cloud-based applications accessed via the internet. |
| **Pll** | Personally Identifiable Information; data that can identify an individual (e.g., names, emails). |
| **MFA** | Multi-Factor Authentication; a security system that requires more than one method of authentication. |
| **SSO** | Single Sign-On; an authentication scheme that allows a user to log in with a single ID to any of several related, yet independent, software systems. |
| **SOC 2 Type II** | A rigorous audit report that evaluates an organization's information systems relevant to security, availability, processing integrity, confidentiality, and privacy. |
| **Section 889** | Part of the NDAA 2019 prohibiting federal grantees from procuring telecommunications equipment from specific Chinese entities (e.g., Huawei, ZTE). |

### 4. Checklist Items

The Requestor must complete **Part A**. The Security Team (CISO or designee) must complete **Part B**.

#### 4.1 Part A: Requestor Preliminary Information
*To be completed by the individual requesting the tool.*

*   [ ] **Business Justification:** Clear statement of need and why existing approved tools cannot fulfill this function.
*   [ ] **Data Classification:** What type of data will this tool process?
    *   [ ] Public
    *   [ ] Internal
    *   [ ] Confidential (PII, Financials)
    *   [ ] Restricted (Youth Data, Biometrics, Credentials)
*   [ ] **User Base:** Who will access this? (e.g., All Staff, HR only, Board only).
*   [ ] **Cost/Funding Source:** Is this funded by a Federal Grant? (If yes, Section 889 checks are mandatory).

#### 4.2 Part B: Security & Compliance Review
*To be completed by the IT/Security Team. "Critical" items are mandatory for approval.*

**I. Authentication & Access Control**
*   [ ] **(Critical)** Does the solution support **Multi-Factor Authentication (MFA)**?
*   [ ] **(Preferred)** Does the solution support **Single Sign-On (SSO)** via SAML/OIDC (e.g., Google Workspace integration)?
*   [ ] **(Critical)** Does the solution support Role-Based Access Control (RBAC) to enforce Least Privilege?
*   [ ] **(Critical)** Is there a process for immediate account deprovisioning upon termination?

**II. Data Protection & Privacy**
*   [ ] **(Critical)** Is data encrypted **at rest** (AES-256 or equivalent)?
*   [ ] **(Critical)** Is data encrypted **in transit** (TLS 1.2+)?
*   [ ] **(Critical)** Does the vendor have a published Privacy Policy compliant with GDPR/CCPA/TDPSA?
*   [ ] **(Critical - Youth)** If the tool involves minors (under 18), is it **COPPA compliant**? (Check for parental consent mechanisms and data minimization).
*   [ ] **(Critical)** Does the vendor agree to sign a **Data Processing Agreement (DPA)**?
*   [ ] **(Preferred)** Is data hosted within the United States (Data Residency)?

**III. Vendor Risk & Compliance**
*   [ ] **(Preferred)** Does the vendor possess a valid **SOC 2 Type II** or **ISO 27001** certification?
*   [ ] **(Critical)** **Section 889 Check:** Confirm vendor is not on the prohibited telecommunications list (Huawei, ZTE, Hytera, Hikvision, Dahua).
*   [ ] **(Critical)** **Sanctions Check:** Confirm vendor is not on the OFAC SDNs list or SAM.gov exclusion list.
*   [ ] **(Preferred)** Has the vendor provided a recent Penetration Test summary?

**IV. Legal & Contractual**
*   [ ] **(Critical)** Does the contract include an **Indemnification** clause protecting Study GRC Inc. from third-party IP claims?
*   [ ] **(Critical)** Does the contract clearly state that Study GRC Inc. retains **ownership** of all data uploaded/created?
*   [ ] **(Critical)** Is there a defined **Service Level Agreement (SLA)** for uptime and support?
*   [ ] **(Critical)** Does the contract allow for a "Right to Audit" or provide annual security questionnaires?

**V. Software Integrity (For Dev/Code Tools)**
*   [ ] **(Critical)** Does the vendor provide a **Software Bill of Materials (SBOM)** or disclose open-source dependencies?
*   [ ] **(Critical)** Are there known CVEs (Common Vulnerabilities and Exposures) associated with this product version?

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Requestor** | Identifies the need, gathers initial vendor documentation (Privacy Policy, SOC 2), and submits the request via the ticketing system. |
| **IT/Security Analyst** | Conducts the technical review using this checklist, verifies certifications, and performs Section 889 checks. |
| **Legal Counsel** | Reviews the Terms of Service (ToS), Master Service Agreement (MSA), and Data Processing Agreement (DPA). |
| **CISO** | Provides final approval or rejection based on the aggregate risk profile. |
| **CFO** | Verifies budget availability and grant allowability after security clearance. |

### 6. Compliance and Enforcement
**Strict Prohibition on Shadow IT:** No employee or volunteer may enter into a contract, click "I Agree" on a Terms of Service, or input Organization data into a new system without completing this checklist and receiving written approval.

Failure to comply with this standard may result in disciplinary action, up to and including termination of employment or volunteer assignment. Unauthorized procurements will not be reimbursed.

### 7. References
*   **IS-POL-001:** Master Information Security Policy
*   **FIN-POL-022:** Procurement Policy (Federal Standards)
*   **IS-STD-028:** Data Classification Standard
*   **NIST CSF 2.0:** Supply Chain Risk Management (GV.SC)
*   **2 CFR 200.318:** General Procurement Standards

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | CISO | Initial Draft aligned with NIST CSF and Federal Grant requirements. |