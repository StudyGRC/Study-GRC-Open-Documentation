### DPIA Necessity Screening Tool

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-TOL-021 |
| **Document Type** | Tool / Assessment |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Data Protection Officer (DPO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this **DPIA Necessity Screening Tool** is to determine whether a full Data Protection Impact Assessment (DPIA) is legally required under GDPR Article 35 and Study GRC Inc.'s internal privacy standards.

This tool acts as a preliminary filter (a "Pre-DPIA") to identify data processing activities that are "likely to result in a high risk" to the rights and freedoms of natural persons. It ensures that Study GRC Inc. allocates resources efficiently, conducting full assessments only where necessary, while maintaining strict compliance with global privacy laws and **Article IX (Policies & Data Protection)** of the Organization’s Bylaws.

### 2. Scope
This tool must be completed by the Project Lead or Product Owner **prior to** the commencement of any new project, software implementation, or significant change to existing processes that involves the collection, storage, or processing of Personal Data.

**Applies to:**
*   New software procurement or development.
*   New marketing or community outreach campaigns.
*   Changes to the collection of member or student data.
*   Implementation of new technologies (e.g., AI, Machine Learning, Biometrics).

**Exclusions:**
*   Minor administrative changes that do not alter data processing scope (e.g., changing the color scheme of a website).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **DPIA** | Data Protection Impact Assessment. A formal process to describe processing, assess necessity/proportionality, and manage risks to rights and freedoms. |
| **Personal Data** | Any information relating to an identified or identifiable natural person (e.g., name, email, IP address, photo). |
| **Special Category Data** | Data revealing racial/ethnic origin, political opinions, religious beliefs, trade union membership, genetic/biometric data, health data, or sexual orientation. |
| **Vulnerable Subjects** | Individuals who may be unable to consent or oppose processing, or where there is a power imbalance. For Study GRC, this explicitly includes **children/minors (K-12 students)**, employees, and elderly persons. |
| **Large Scale** | Processing involving a considerable amount of data, affecting a large number of subjects, over a long duration, or across a wide geographical extent. |

### 4. Screening Questionnaire

**Instructions:** The Project Lead must answer the following questions regarding the proposed project.

#### 4.1 Category A: Mandatory Triggers (Automatic Requirement)
*If you answer **YES** to any question in this section, a full DPIA is **MANDATORY**.*

| ID | Question | Yes | No |
| :--- | :--- | :--- | :--- |
| **A1** | Does the project involve **systematic and extensive evaluation** of personal aspects based on automated processing (including profiling) which produces legal effects or significantly affects the individual? (e.g., automated rejection of job applicants, credit scoring). | ☐ | ☐ |
| **A2** | Does the project involve processing on a **large scale of Special Category Data** (health, race, religion, biometrics) or data relating to criminal convictions? | ☐ | ☐ |
| **A3** | Does the project involve **systematic monitoring of a publicly accessible area** on a large scale? (e.g., CCTV, public video surveillance). | ☐ | ☐ |

#### 4.2 Category B: High-Risk Indicators (Cumulative Requirement)
*If you answer **YES** to **two (2) or more** questions in this section, a full DPIA is **MANDATORY**. If you answer Yes to only one, consult the DPO.*

| ID | Question | Yes | No |
| :--- | :--- | :--- | :--- |
| **B1** | **Evaluation or Scoring:** Will the project involve scoring, profiling, or predicting behavior? (e.g., analyzing student learning patterns to predict failure, employee performance monitoring). | ☐ | ☐ |
| **B2** | **Automated Decision Making:** Will decisions be made about individuals without human intervention? | ☐ | ☐ |
| **B3** | **Systematic Monitoring:** Will the project involve tracking or monitoring individuals? (e.g., remote proctoring software, employee keystroke logging, GPS tracking). | ☐ | ☐ |
| **B4** | **Sensitive Data:** Does the project involve sensitive data (even if not "large scale") or data of a highly personal nature? (e.g., financial data, private communications). | ☐ | ☐ |
| **B5** | **Data Processed on a Large Scale:** Does the project involve a large number of subjects (e.g., >5,000 members) or a large volume of data per subject? | ☐ | ☐ |
| **B6** | **Matching or Combining Datasets:** Will data from two or more different sources be matched or combined in a way that exceeds the reasonable expectations of the user? | ☐ | ☐ |
| **B7** | **Vulnerable Subjects:** Does the project involve processing data of **children (under 18)**, employees, or mentally ill persons? *(Note: Given Study GRC's K-12 focus, strictly evaluate this).* | ☐ | ☐ |
| **B8** | **Innovative Use:** Does the project involve applying new technological or organizational solutions? (e.g., Artificial Intelligence, Facial Recognition, Blockchain). | ☐ | ☐ |
| **B9** | **Cross-Border Transfer:** Will data be transferred outside the EU/EEA to countries without an adequacy decision (e.g., to the US without Data Privacy Framework certification)? | ☐ | ☐ |
| **B10** | **Preventing Rights:** Will the processing prevent data subjects from exercising a right or using a service or contract? (e.g., screening against a database before allowing entry). | ☐ | ☐ |

#### 4.3 Decision Logic & Determination

**To be completed by the Project Lead:**

**Total "Yes" in Category A:** ______
**Total "Yes" in Category B:** ______

**Determination:**
*   [ ] **DPIA REQUIRED:** (Any "Yes" in Cat A **OR** 2+ "Yes" in Cat B).
*   [ ] **DPO CONSULTATION REQUIRED:** (0 "Yes" in Cat A **AND** 1 "Yes" in Cat B).
*   [ ] **DPIA NOT REQUIRED:** (0 "Yes" in Cat A **AND** 0 "Yes" in Cat B).

**Project Lead Signature:** __________________________ **Date:** ____________

---

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Project Lead / Product Owner** | Responsible for completing this Screening Tool accurately during the planning phase of any project. |
| **Data Protection Officer (DPO)** | Responsible for reviewing completed Screening Tools, verifying the determination, and advising on "borderline" cases (1 "Yes" in Cat B). |
| **Chief Information Security Officer (CISO)** | Responsible for ensuring that the technical infrastructure supports the outcome of the screening (e.g., if DPIA is required, ensuring security controls are assessed). |
| **Board of Directors** | Responsible for high-level oversight of risk management as defined in **Bylaws Article III**. |

### 6. Compliance and Enforcement
Failure to utilize this tool prior to the processing of personal data constitutes a violation of the Organization’s **Master Data Privacy Policy**.

*   **Internal:** Employees or volunteers who bypass this screening may face disciplinary action, up to and including termination or removal from the Board/Volunteer role.
*   **External:** Failure to conduct a required DPIA is a violation of GDPR Article 35 and may subject Study GRC Inc. to fines of up to €10 million or 2% of global turnover.

### 7. References
*   **GDPR Article 35:** Data protection impact assessment.
*   **Study GRC Bylaws Article IX:** Policies & Data Protection.
*   **WP29 Guidelines (WP 248 rev.01):** Guidelines on Data Protection Impact Assessment (DPIA).
*   **IS-POL-020:** Master Data Privacy Policy.
*   **IS-PRC-022:** Data Protection Impact Assessment (DPIA) Procedure.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Legal Officer | Initial release aligned with GDPR Art. 35 requirements. |