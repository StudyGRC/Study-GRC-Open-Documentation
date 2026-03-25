### SaaS Security Assessment

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-ASM-001 |
| **Document Type** | Assessment / Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | IT Security Manager |
| **Classification** | Internal |

### 1. Purpose
The purpose of this SaaS Security Assessment is to establish a rigorous, standardized framework for evaluating the security, privacy, and compliance posture of third-party Software-as-a-Service (SaaS) providers prior to procurement or deployment.

As a remote-first organization handling sensitive data (including youth data) and operating under federal grant requirements (2 CFR 200), Study GRC Inc. must ensure that all external vendors meet our internal security standards. This document satisfies the "Due Diligence" requirements mandated by our **Vendor/Third-Party Risk Policy** and mitigates the risks of supply chain attacks, data breaches, and regulatory non-compliance.

### 2. Scope
This assessment applies to all SaaS applications, cloud platforms, and web-based tools proposed for use within Study GRC Inc., regardless of cost (including free or open-source tools).

**In Scope:**
*   New SaaS procurement requests.
*   Renewals of existing SaaS contracts.
*   "Shadow IT" discovered during audits.
*   Free tools requiring corporate email registration or data input.

**Exclusions:**
*   Client-side software that does not transmit data to a third party (rare).
*   Transient websites used for reference only (no login/data entry).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **SaaS (Software-as-a-Service)** | A software licensing and delivery model in which software is licensed on a subscription basis and is centrally hosted by a third-party provider. |
| **Confidential Information** | Data that is not public, including member PII, donor financial data, and proprietary curriculum content. |
| **SOC 2 Type II** | An audit report attesting to the operating effectiveness of a service organization's controls over a period of time (usually 6-12 months). |
| **SSO (Single Sign-On)** | An authentication scheme that allows a user to log in with a single ID and password to any of several related, yet independent, software systems. |
| **COPPA** | Children's Online Privacy Protection Act; federal law regulating the collection of personal information from children under 13. |
| **Shadow IT** | Information technology systems built, managed, or used without explicit organizational approval. |

### 4. Assessment Standards & Procedures

#### 4.1 Assessment Triage (Risk Tiering)
Before a full assessment is conducted, the Requestor must submit the tool for Triage. The CISO or designee will assign a Risk Tier based on the intended use.

*   **Tier 1 (Critical/High Risk):** Processes PII, financial data, youth data, or integrates with core systems (e.g., Google Workspace, HRIS). **Full Assessment Required.**
*   **Tier 2 (Medium Risk):** Internal operational data, no PII, no youth interaction. **Standard Assessment Required.**
*   **Tier 3 (Low Risk):** No sensitive data processing, no integration, public data only. **Abbreviated Review.**

#### 4.2 Mandatory Security Controls (Go/No-Go Criteria)
Any SaaS provider failing to meet the following "Must-Have" criteria will be automatically rejected unless a formal Risk Acceptance is signed by the Executive Director.

1.  **Encryption:** Data must be encrypted in transit (TLS 1.2+) and at rest (AES-256).
2.  **Authentication:**
    *   Must support Multi-Factor Authentication (MFA).
    *   Tier 1 apps must support SSO (SAML/OIDC) integration with the Organization’s Identity Provider.
3.  **Data Ownership:** Terms of Service must explicitly state that Study GRC Inc. retains ownership of all data uploaded (Pursuant to **Bylaws Article IX, Section 9.3**).
4.  **Youth Safety (If applicable):** If the tool interacts with minors, it must be COPPA compliant and allow for parental consent mechanisms.

#### 4.3 Detailed Assessment Domains
For Tier 1 and Tier 2 applications, the CISO will evaluate the vendor against the following domains:

**4.3.1 Compliance & Certifications**
*   Does the vendor possess a valid SOC 2 Type II or ISO 27001 certification?
*   If no certification exists, has the vendor completed a CAIQ (Consensus Assessments Initiative Questionnaire) or VSA (Vendor Security Assessment)?

**4.3.2 Privacy & Regulatory (GDPR/TDPSA/COPPA)**
*   Does the vendor have a publicly available Privacy Policy?
*   Does the vendor sell data to third parties? (Strictly Prohibited).
*   Does the vendor offer a Data Processing Agreement (DPA)?
*   **Data Locality:** Where is the data hosted? (Preference: US-based or GDPR-adequate jurisdictions).

**4.3.3 Business Continuity & Availability**
*   What is the vendor's SLA for uptime (e.g., 99.9%)?
*   Does the vendor perform regular backups?
*   Does the vendor have a documented Disaster Recovery Plan?

**4.3.4 Application Security**
*   Does the vendor perform regular penetration testing?
*   Does the vendor have a Vulnerability Disclosure Program?
*   Are role-based access controls (RBAC) available?

#### 4.4 Contractual & Legal Review
Pursuant to **Bylaws Article V**, Operational Officers must ensure contracts do not expose the organization to undue liability.
*   **Indemnification:** Vendor must indemnify Study GRC Inc. against data breaches caused by Vendor negligence.
*   **Termination:** We must be able to export our data in a usable format (CSV, JSON) upon contract termination.
*   **Right to Audit:** For Tier 1 vendors, we reserve the right to review third-party audit reports annually.

#### 4.5 Federal Procurement Compliance
As a federal grantee subject to **2 CFR 200**:
*   **Suspension/Debarment:** The vendor must be checked against SAM.gov to ensure they are not debarred from doing business with the federal government.
*   **Domestic Preference:** Preference should be given to U.S.-based hosting where appropriate (2 CFR 200.322).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Requestor** | Initiates the assessment request; provides business justification and cost data. |
| **CISO** | Conducts the technical security review; assigns Risk Tier; approves or rejects technical controls. |
| **Legal / Compliance** | Reviews Terms of Service, DPA, and privacy policies; validates COPPA compliance for youth tools. |
| **Treasurer / CFO** | Reviews financial viability of the vendor and approves budget pursuant to **Bylaws Article IV**. |
| **Executive Director** | Final approving authority for Tier 1 vendors or Risk Acceptance for exceptions. |

### 6. Compliance and Enforcement
**Prohibition on Shadow IT:** Employees and volunteers are strictly prohibited from creating accounts on SaaS platforms for organizational business without prior approval.

**Enforcement:**
*   **Technical:** Unapproved SaaS applications may be blocked at the network or browser level via CASB (Cloud Access Security Broker) policies.
*   **Administrative:** Failure to adhere to this assessment process may result in disciplinary action, up to and including termination of employment or volunteer assignment.
*   **Financial:** Expenses for unapproved SaaS tools will not be reimbursed.

### 7. References
*   **Study GRC Inc. Bylaws** (Articles IV, V, IX)
*   **IS-POL-001:** Master Information Security Policy
*   **IS-STD-005:** Data Classification Standard
*   **FIN-POL-022:** Procurement Policy (Federal Standards)
*   **NIST CSF 2.0:** Supply Chain Risk Management (GV.SC)
*   **2 CFR 200.318:** General Procurement Standards

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | CISO | Initial Release |