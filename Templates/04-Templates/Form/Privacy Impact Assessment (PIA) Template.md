### Privacy Impact Assessment (PIA) Template

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-FRM-019 |
| **Document Type** | Form / Template |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Privacy Officer / CISO |
| **Classification** | Internal Use Only |

### 1. Purpose
The purpose of this Privacy Impact Assessment (PIA) is to identify, evaluate, and mitigate privacy risks associated with the processing of Personally Identifiable Information (PII) within Study GRC Inc. This document ensures "Privacy by Design" principles are integrated into all projects, systems, and vendor relationships, complying with the **NIST Privacy Framework** (Identify-P, Govern-P, Control-P), **GDPR Article 35**, and the **Texas Data Privacy and Security Act (TDPSA)**.

This assessment supports the Organization's commitment to transparency and data protection as outlined in **Article IX (Policies & Data Protection)** of the Bylaws.

### 2. Scope
This assessment is **mandatory** for:
*   **New Projects:** Any new system, software, or program that collects, stores, or processes PII.
*   **Vendor Procurement:** Before signing contracts with third-party service providers (SaaS, Cloud) that handle Study GRC data.
*   **Significant Changes:** Major updates to existing systems that alter data collection practices (e.g., adding biometric authentication or collecting data from minors).

**Exclusions:** Projects that strictly utilize publicly available, non-PII data (e.g., open-source threat intelligence feeds) do not require a full PIA but must file a "No PII Determination" memo.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **PII (Personally Identifiable Information)** | Any information that can be used to distinguish or trace an individual’s identity (e.g., name, email, IP address, biometric data) or is linked to a specific individual. |
| **Processing** | Any operation performed on data, including collection, recording, storage, adaptation, retrieval, consultation, use, disclosure, or destruction. |
| **Data Subject** | The individual to whom the PII relates (e.g., Members, Donors, Students, Volunteers). |
| **Sensitive Data** | Data revealing racial/ethnic origin, political opinions, religious beliefs, trade union membership, genetic/biometric data, health data, or data concerning a natural person's sex life or sexual orientation. |
| **NIST Privacy Framework** | A voluntary tool developed by NIST to help organizations identify and manage privacy risk to build innovative products and services while protecting individuals’ privacy. |

---

### 4. Assessment Questionnaire

*Instructions: The Project Owner or System Administrator must complete Sections 4.1 through 4.6. Do not leave fields blank. If a question does not apply, mark "N/A" and explain why.*

#### 4.1 Project Information & Metadata
| Field | Input |
| :--- | :--- |
| **Project / System Name** | [Enter Name] |
| **Project Owner** | [Name, Title] |
| **Department** | [e.g., Education, IT, Fundraising] |
| **Vendor Name (if applicable)** | [Enter Vendor or "Internal Build"] |
| **Estimated Launch Date** | [YYYY-MM-DD] |
| **Description of Project** | [Briefly describe what the system does and its business value] |

#### 4.2 Data Inventory (NIST ID.IM-P)
*Identify the types of data to be processed.*

**A. Data Subjects:** (Check all that apply)
- [ ] **Voting Members** (Supporting/Honorary)
- [ ] **Community Participants** (Non-voting)
- [ ] **Minors/Students (Under 18)** *[Critical for K-12 Compliance]*
- [ ] **Children (Under 13)** *[Requires COPPA Compliance]*
- [ ] **Employees/Contractors**
- [ ] **Donors**

**B. Data Elements:** (Check all that apply)
- [ ] **Contact Info:** Name, Email, Phone, Physical Address.
- [ ] **Authentication:** Passwords, Security Questions.
- [ ] **Financial:** Credit Card (PCI), Bank Account, Donation History.
- [ ] **Demographic:** Age, Gender, Race/Ethnicity.
- [ ] **Technical:** IP Address, Device ID, Cookies, Geolocation.
- [ ] **Biometric:** Facial recognition, Fingerprint (See Bylaws Art. IX).
- [ ] **Government ID:** SSN, Driver’s License, Passport.
- [ ] **User Content:** Forum posts, homework submissions, chat logs.

#### 4.3 Purpose and Necessity (NIST ID.RA-P)
*Justify the collection based on Data Minimization principles.*

**1. What is the specific business purpose for collecting this data?**
> [Response]

**2. Is this data collection required by law, contract, or strictly for operational necessity?**
> [Response]

**3. Data Minimization: Could the project function if the data was anonymized or if fewer data points were collected?**
> [Response]

#### 4.4 Data Flow and Storage (NIST PR.DS-P)
*Map the lifecycle of the data.*

**1. Collection Method:** How is data ingested? (e.g., Web form, API, manual entry, third-party import).
> [Response]

**2. Storage Location:** Where will data reside? (e.g., AWS US-East, Google Drive, Vendor Server). **Specify geographic region.**
> [Response]

**3. Cross-Border Transfer:** Will data leave the United States? (e.g., Support teams in EU/Asia).
> [Response]

**4. Retention Period:** How long will the data be kept? (Refer to *Records Retention Schedule*).
> [Response]

#### 4.5 Access and Security (NIST PR.AC-P)
*Define controls to protect the data.*

**1. Access Control:** Who has access? (e.g., "Only HR Managers," "All Volunteers").
> [Response]

**2. Encryption:**
*   Is data encrypted at rest? [ ] Yes [ ] No
*   Is data encrypted in transit (TLS/SSL)? [ ] Yes [ ] No

**3. Vendor Security:** If a third party is involved, have they signed a Data Processing Agreement (DPA) and NDA per **Bylaws Section 9.2**?
> [Response]

#### 4.6 Vulnerable Populations & Ethics (NIST ID.RA-P)
*Address specific risks related to the Organization's mission.*

**1. Youth Data:** Does this project involve users under age 13? If yes, describe the **Verifiable Parental Consent** mechanism (COPPA).
> [Response]

**2. Automated Decision Making:** Does the system make automated decisions that impact a user's eligibility or standing (e.g., auto-banning based on behavior)?
> [Response]

---

### 5. Risk Assessment & Scoring (To be completed by Privacy Officer/CISO)

*The Reviewer evaluates the responses above to assign a risk level.*

| Risk Category | Assessment | Score (1-5) |
| :--- | :--- | :--- |
| **Volume of Data** | (1=Low, 5=High Volume) | [ ] |
| **Sensitivity** | (1=Public Data, 5=Biometric/Financial/Youth) | [ ] |
| **Third-Party Risk** | (1=Internal Only, 5=Unknown Vendor) | [ ] |
| **Compliance Risk** | (1=No Regs, 5=GDPR/COPPA/HIPAA) | [ ] |
| **Total Score** | **(Max 20)** | **[ ]** |

**Risk Determination:**
*   **Low (0-8):** Proceed with standard controls.
*   **Medium (9-14):** Proceed with additional mitigation (listed below).
*   **High (15-20):** **STOP.** Requires Executive Director and Legal Counsel approval.

**Identified Risks:**
> [List specific privacy risks identified during review]

**Required Mitigations:**
> [List specific controls required before launch, e.g., "Enable MFA," "Update Privacy Policy"]

---

### 6. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Project Owner** | Completes the PIA questionnaire accurately and implements required mitigations. |
| **CISO / Privacy Officer** | Reviews the PIA, assigns risk scores, and prescribes security controls. |
| **Executive Director** | Final approval authority for "High Risk" projects. |
| **Legal Counsel** | Consulted on projects involving cross-border transfers, minors (COPPA), or biometric data. |

### 7. Compliance and Enforcement

**Approval Signature:**

_________________________________________________
**Chief Information Security Officer (CISO)**
Date: [YYYY-MM-DD]

**Executive Director Approval (Required for High Risk):**

_________________________________________________
**Executive Director**
Date: [YYYY-MM-DD]

Failure to complete a PIA prior to launching a data-processing project is a violation of the **Master Information Security Policy**. Employees or volunteers found bypassing this requirement may be subject to disciplinary action, up to and including termination of role, as outlined in the **Bylaws Article III (Removal of Directors)** or **Article V (Operational Leadership)**.

### 8. References
*   **Study GRC Inc. Bylaws:** Article IX (Policies & Data Protection).
*   **NIST Privacy Framework:** Version 1.0 (Identify, Govern, Control).
*   **GDPR:** Article 35 (Data Protection Impact Assessment).
*   **COPPA:** Children's Online Privacy Protection Act.
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-STD-005:** Data Classification Standard.

### 9. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | CISO | Initial Release aligned with NIST Privacy Framework. |