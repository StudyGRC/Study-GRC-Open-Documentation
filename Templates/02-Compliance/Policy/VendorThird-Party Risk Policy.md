### Vendor/Third-Party Risk Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-060 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Bi-Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this policy is to establish a framework for identifying, assessing, mitigating, and monitoring risks associated with third-party vendors, service providers, and partners. As a federal grantee and an organization entrusted with member data and youth protection, Study GRC Inc. must ensure that external parties do not compromise our security posture, financial integrity, or regulatory compliance. This policy aligns with NIST Cybersecurity Framework (Supply Chain Risk Management) and 2 CFR 200 (Uniform Guidance) procurement standards.

### 2. Scope
This policy applies to all relationships between Study GRC Inc. and external third parties, including but not limited to:
*   Technology vendors (SaaS, IaaS, PaaS).
*   Professional services consultants and contractors.
*   Marketing and operational partners.
*   Subrecipients of federal grant funds.

**Exclusions:**
*   One-time transactional purchases of commodity goods (e.g., office supplies) below the Micro-Purchase Threshold ($10,000) that do not involve access to Study GRC systems, data, or facilities.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Third-Party / Vendor** | Any external entity or individual that provides goods, services, or data processing capabilities to the Organization under a contract or agreement. |
| **Critical Vendor** | A vendor whose failure or breach would result in significant disruption to operations, financial loss, or reputational damage (e.g., Cloud Service Providers, Payment Processors). |
| **Subrecipient** | A non-federal entity that receives a subaward from Study GRC Inc. to carry out part of a federal program. Distinct from a contractor (See 2 CFR 200.330). |
| **Confidential Information** | Non-public information including PII, donor records, strategic plans, and proprietary educational content. |
| **SAM.gov** | The System for Award Management; the official U.S. government system used to verify if a vendor is suspended or debarred from receiving federal funds. |

### 4. Policy Statements

#### 4.1 Vendor Classification and Tiering
To prioritize risk management efforts, all vendors must be classified upon intake based on the nature of their access and criticality to operations.

*   **Tier 1 (Critical):** Vendors with access to Sensitive PII, financial systems, or youth data; or vendors whose unavailability would halt operations (e.g., AWS, Payroll Provider).
*   **Tier 2 (High):** Vendors with access to internal non-public data or limited system integration (e.g., CRM, Email Marketing).
*   **Tier 3 (Low):** Vendors with no access to systems or data, providing commodity services (e.g., Landscaping, Catering).

#### 4.2 Due Diligence and Selection
Prior to executing any contract, the "Contract Owner" must perform due diligence commensurate with the Vendor Tier.

*   **4.2.1 Security Assessment:** Tier 1 and Tier 2 vendors must undergo a security review by the CISO or designee. This includes reviewing SOC 2 Type II reports, ISO 27001 certifications, or completing a Vendor Security Questionnaire (VSRA).
*   **4.2.2 Federal Compliance (Debarment Check):** For all procurements utilizing federal funds, the Finance Department must verify that the vendor is not listed as "Suspended" or "Debarred" on SAM.gov. This search must be documented.
*   **4.2.3 Conflict of Interest:** In accordance with **Bylaws Article IX**, the individual selecting the vendor must disclose any personal, professional, or financial interest in the vendor.
*   **4.2.4 Financial Viability:** For contracts exceeding the Simplified Acquisition Threshold, the CFO must review the vendor's financial health to ensure continuity of service.

#### 4.3 Contracting Requirements
All vendor engagements must be governed by a written contract or Terms of Service that protects the Organization’s interests.

*   **4.3.1 Confidentiality:** All vendors must execute a Non-Disclosure Agreement (NDA) or have confidentiality clauses embedded in the Master Services Agreement (MSA), per **Bylaws Article IX, Section 9.2**.
*   **4.3.2 Data Protection:** Vendors processing personal data must sign a Data Processing Agreement (DPA) compliant with GDPR, TDPSA, and relevant privacy laws.
*   **4.3.3 Right to Audit:** Contracts for Tier 1 vendors must include a "Right to Audit" clause allowing Study GRC Inc. to review the vendor's security and compliance controls.
*   **4.3.4 Youth Protection:** Any vendor with direct contact with minors or access to data regarding minors must undergo background checks equivalent to those required for internal staff, compliant with the *Child and Youth Safeguarding Policy*.
*   **4.3.5 Intellectual Property:** Contracts must explicitly state that Work Product created for Study GRC Inc. is "work made for hire" and owned by the Organization, per **Bylaws Article IX, Section 9.3**.

#### 4.4 Federal Grant Specifics (Subrecipient vs. Contractor)
When passing through federal funds, the Organization must make a case-by-case determination whether the party is a "Subrecipient" or a "Contractor" in accordance with **2 CFR 200.331**.
*   **Subrecipients** are subject to federal audit requirements and must adhere to the terms and conditions of the federal award.
*   **Contractors** provide goods and services within normal business operations and are subject to procurement standards.

#### 4.5 Access Control and Least Privilege
*   **4.5.1 Provisioning:** Vendor access to Study GRC systems is granted only on a "need-to-know" basis.
*   **4.5.2 Authentication:** Vendors accessing internal systems must utilize Multi-Factor Authentication (MFA).
*   **4.5.3 Segregation:** Where possible, vendor accounts must be segregated from internal staff accounts and monitored for anomalous activity.

#### 4.6 Ongoing Monitoring
Risk management is not a one-time event.
*   **Annual Review:** Tier 1 vendors must be reviewed annually for security posture changes (e.g., new SOC 2 report) and performance.
*   **Incident Reporting:** Vendors must be contractually obligated to report security breaches affecting Study GRC data within a specific timeframe (e.g., 24-72 hours), aligning with the *Data Breach Notification Procedure*.

#### 4.7 Offboarding and Termination
Upon contract termination:
*   Access to all systems must be revoked immediately (within 24 hours).
*   The vendor must return or certify the destruction of all Study GRC data (Sanitization) in accordance with NIST SP 800-88.
*   Final payments shall be withheld until all assets and data are accounted for.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Board of Directors** | Approves this policy; reviews and approves contracts involving Fundamental Actions or significant financial thresholds. |
| **Executive Director (CEO)** | Ensures operational compliance; executes contracts within delegated authority; resolves disputes regarding vendor risk acceptance. |
| **Chief Information Security Officer (CISO)** | Conducts security assessments; maintains the Vendor Risk Register; approves/denies vendors based on cyber risk. |
| **Chief Financial Officer (CFO)** | Conducts financial viability checks; performs SAM.gov debarment checks; maintains contract repository. |
| **Contract Owner** | The internal employee responsible for the business relationship, performance monitoring, and initiating the offboarding process. |

### 6. Compliance and Enforcement
Failure to comply with this policy may result in disciplinary action, up to and including termination of employment or volunteer assignment. For vendors, violation of these requirements constitutes a material breach of contract, subject to immediate termination and legal pursuit of damages.

### 7. References
*   **Study GRC Inc. Bylaws:** Article IX (Conflict of Interest, IP, Confidentiality).
*   **2 CFR 200.318 - 200.327:** Federal Procurement Standards.
*   **2 CFR 200.331:** Subrecipient and Contractor Determinations.
*   **NIST CSF 2.0:** Governance (GV.SC) - Supply Chain Risk Management.
*   **NIST SP 800-161:** Supply Chain Risk Management Practices for Systems and Organizations.
*   **Texas Business Organizations Code:** Chapter 22.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Legal Officer | Initial Draft |