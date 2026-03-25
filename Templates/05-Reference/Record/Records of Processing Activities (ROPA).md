### Records of Processing Activities (ROPA)

| Document Control | |
| :--- | :--- |
| **Document ID** | PRIV-REG-033 |
| **Document Type** | Register / Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-04-27 (Bi-Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) / Data Protection Officer (DPO) |
| **Classification** | Internal / Confidential |

### 1. Purpose
The purpose of this **Records of Processing Activities (ROPA)** is to maintain a comprehensive inventory of all personal data processing activities conducted by Study GRC Inc. ("the Organization"). This document serves as the central compliance record required by **Article 30 of the General Data Protection Regulation (GDPR)** and aligns with the transparency requirements of the **Texas Data Privacy and Security Act (TDPSA)**.

This register demonstrates the Organization’s accountability regarding data protection and supports the enforcement of **Bylaws Article IX (Policies & Data Protection)**, ensuring that all personal data—particularly that of minors and voting members—is processed lawfully, fairly, and transparently.

### 2. Scope
This register applies to **all** personal data processed by the Organization, regardless of the data subject's citizenship or location.

*   **In Scope:**
    *   Data of Voting Members (Supporting/Honorary) and Community Participants.
    *   Data of Donors and Financial Contributors.
    *   Data of Employees, Contractors, and Volunteers.
    *   **Data of Minors** (K-12 program participants).
*   **Exclusions:**
    *   Anonymized or aggregated data where re-identification is impossible.
    *   Corporate data not linked to a natural person.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Controller** | The entity that determines the purposes and means of the processing of personal data (Study GRC Inc.). |
| **Processor** | A natural or legal person, public authority, agency, or other body which processes personal data on behalf of the controller (e.g., AWS, Stripe, Slack). |
| **Data Subject** | The identified or identifiable living individual to whom personal data relates. |
| **Processing** | Any operation performed on personal data, such as collection, recording, organization, structuring, storage, adaptation, retrieval, use, disclosure, or destruction. |
| **Special Category Data** | Data revealing racial or ethnic origin, political opinions, religious beliefs, trade union membership, genetic data, biometric data, or data concerning health or sexual orientation. |

### 4. Master Register of Processing Activities

The Organization acts primarily as a **Data Controller**. The following subsections detail the specific processing activities mandated for tracking by GDPR Article 30(1).

#### 4.1 Governance & Membership Management
*   **Purpose of Processing:** To manage the legal membership structure, facilitate voting, and maintain corporate records as required by Texas Business Organizations Code (TBOC).
*   **Data Subjects:** Voting Members (Supporting/Honorary), Board Directors.
*   **Categories of Data:** Name, Email Address, Physical Address (for legal notice), Payment History, Voting Record.
*   **Legal Basis:** Legal Obligation (TBOC); Contractual Necessity (Bylaws).
*   **Recipients:** Internal Governance Committee; Third-party voting platforms (Processors).
*   **Transfers:** Data stored in US-based cloud infrastructure.
*   **Retention:** Permanent for Minutes/Resolutions; 7 years for financial contribution records.

#### 4.2 Community & Education Operations
*   **Purpose of Processing:** To deliver educational content, manage the online community, and track certification/course progress.
*   **Data Subjects:** Community Participants (Non-Voting), Learners.
*   **Categories of Data:** Name, Email, Username, IP Address, Course Progress, Quiz Scores, Forum Posts.
*   **Legal Basis:** Legitimate Interest (Community building); Consent (Account creation).
*   **Recipients:** Learning Management System (LMS) providers; Community Platform providers.
*   **Transfers:** US-based hosting.
*   **Retention:** Duration of account activity + 2 years inactive.

#### 4.3 Youth Programs (K-12 Focus)
*   **Purpose of Processing:** To provide GRC education to minors and ensure safety/safeguarding.
*   **Data Subjects:** Minors (Under 18), Parents/Guardians.
*   **Categories of Data:** Name, Age/Grade, Parent Contact Info, Emergency Medical Info (Special Category), Video/Voice (during virtual sessions).
*   **Legal Basis:** Consent (Parental Consent required per COPPA/GDPR); Vital Interests (Medical emergencies).
*   **Recipients:** Youth Program Coordinators; Background Check Providers (for volunteers interacting with youth).
*   **Transfers:** Strictly limited; no cross-border transfer of minor data without explicit parental consent.
*   **Retention:** Until age of majority or request for deletion; Medical waivers retained per statute of limitations (min. 2 years post-event).

#### 4.4 Human Resources & Volunteering
*   **Purpose of Processing:** Recruitment, payroll, benefits administration, and volunteer management.
*   **Data Subjects:** Employees, Contractors, Volunteers.
*   **Categories of Data:** SSN/Tax ID, Bank Details, Background Check Results (Criminal History), Performance Reviews.
*   **Legal Basis:** Contract; Legal Obligation (Tax/Employment Law).
*   **Recipients:** IRS; Payroll Processors; Background Check Vendors.
*   **Retention:** Employment duration + 7 years (Tax/Personnel files).

#### 4.5 Donor Relations & Fundraising
*   **Purpose of Processing:** Processing donations, issuing tax receipts, and donor stewardship.
*   **Data Subjects:** Donors (Individual and Corporate).
*   **Categories of Data:** Name, Billing Address, Credit Card Token (PCI-DSS compliant), Donation History.
*   **Legal Basis:** Legal Obligation (IRS reporting); Legitimate Interest.
*   **Recipients:** Payment Gateways (Stripe/PayPal); Accounting Software.
*   **Retention:** 7 years (IRS requirement).

#### 4.6 IT Security & Logs
*   **Purpose of Processing:** Network security, fraud prevention, and incident response.
*   **Data Subjects:** All users of Organization systems.
*   **Categories of Data:** IP Addresses, Device IDs, Login Timestamps, Traffic Logs.
*   **Legal Basis:** Legitimate Interest (Security); Legal Obligation (Data breach preservation).
*   **Recipients:** SIEM providers; Law Enforcement (upon valid subpoena).
*   **Retention:** Rolling 12 months (unless held for investigation).

### 5. Technical and Organizational Security Measures
Pursuant to GDPR Article 32, the Organization implements the following measures to protect the data listed in Section 4:

1.  **Encryption:** All data at rest is encrypted (AES-256); data in transit is encrypted via TLS 1.2+.
2.  **Access Control:** Role-Based Access Control (RBAC) is enforced; Multi-Factor Authentication (MFA) is mandatory for all administrative accounts.
3.  **Minimization:** Data collection is limited to what is strictly necessary for the specific purpose.
4.  **Vendor Management:** All third-party processors must sign a Data Processing Agreement (DPA).
5.  **Youth Protection:** Enhanced access controls apply to data belonging to minors; "Two-Deep" leadership rule applies to accessing youth records.

### 6. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Board of Directors** | Ultimate accountability for compliance with Bylaws Art. IX and GDPR. |
| **CISO / DPO** | Responsible for maintaining this ROPA, conducting Privacy Impact Assessments (PIAs), and ensuring accuracy. |
| **Department Heads** | Responsible for notifying the CISO/DPO of any *new* data collection activities or changes in vendors *before* implementation. |
| **All Staff/Volunteers** | Responsible for adhering to data minimization principles and reporting processing changes. |

### 7. Compliance and Enforcement
Failure to maintain an accurate ROPA or processing data outside the scope defined in this register constitutes a violation of Organization policy and potentially international law.

*   **Internal:** Violations may result in disciplinary action, up to and including termination of employment or removal from the Board/Volunteer position.
*   **External:** Failure to comply with GDPR Art. 30 can result in regulatory fines up to €10 million or 2% of global turnover.

### 8. References
*   **GDPR Article 30:** Records of processing activities.
*   **Bylaws Article IX:** Policies & Data Protection.
*   **Bylaws Article II:** Membership Classes.
*   **Document ID PRIV-POL-001:** Master Data Privacy Policy.
*   **Document ID GOV-STD-005:** Records Retention Schedule.

### 9. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Legal Officer | Initial release of ROPA aligned with Bylaws and GDPR Art. 30. |