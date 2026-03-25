### Data Protection Impact Assessment (DPIA) Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-020 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director / CISO |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a systematic process for identifying, evaluating, and mitigating privacy risks associated with the processing of personal data *before* such processing begins. This procedure ensures Study GRC Inc. complies with Article 35 of the General Data Protection Regulation (GDPR), Section 541.105 of the Texas Data Privacy and Security Act (TDPSA), and COPPA regulations regarding youth data. It serves to operationalize the Organization's commitment to "Privacy by Design" as mandated in **Bylaws Article IX, Section 9.1**.

### 2. Scope
This procedure applies to all employees, volunteers, contractors, and third-party vendors of Study GRC Inc. It is mandatory for any new project, technology implementation, or significant change to existing systems that involves the processing of Personal Data.

**Specific Triggers:** A DPIA is strictly required prior to:
*   Processing data of children under age 16 (K-12 focus).
*   Implementing new technologies (e.g., AI, machine learning, biometric authentication).
*   Systematic and extensive evaluation of personal aspects (profiling).
*   Processing sensitive data on a large scale (e.g., racial/ethnic origin, health data, political opinions).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **DPIA** | Data Protection Impact Assessment; a process to identify and minimize the data protection risks of a project. |
| **High Risk Processing** | Processing that is likely to result in a high risk to the rights and freedoms of natural persons, often involving new technologies or vulnerable subjects (children). |
| **Data Subject** | The identified or identifiable living individual to whom personal data relates (e.g., members, students, donors). |
| **Project Lead** | The operational owner (e.g., VP of Education, DKG) proposing the new data processing activity. |
| **Residual Risk** | The level of risk remaining after risk treatment/mitigation measures have been implemented. |

### 4. Procedures

#### 4.1 Phase 1: Threshold Assessment (Screening)
Before initiating a full DPIA, the Project Lead must determine if one is legally required.

1.  **Initiation:** The Project Lead must complete the *DPIA Screening Checklist (IS-FRM-021)* during the planning phase of any new project.
2.  **Mandatory Triggers:** If the project involves any of the following, a full DPIA is **automatic**:
    *   Targeted advertising based on online behavior.
    *   Sale of personal data.
    *   Profiling that produces legal or similarly significant effects.
    *   Processing of Sensitive Data (including data of known minors).
3.  **Review:** The CISO reviews the Screening Checklist.
    *   **Outcome A:** No DPIA required. The CISO signs off; the project proceeds.
    *   **Outcome B:** DPIA required. The project moves to Phase 2.

#### 4.2 Phase 2: Preparation and Consultation
1.  **Team Assembly:** The Project Lead must assemble a working group, including technical staff and the CISO.
2.  **Stakeholder Consultation:**
    *   If the data involves Voting Members, the Project Lead must consider member expectations per **Bylaws Article II**.
    *   If the data involves minors, the *Director of Kindness and Generosity* must be consulted regarding safeguarding implications.
3.  **Vendor Assessment:** If a third-party processor is involved, the Project Lead must obtain their security certifications (SOC2, ISO 27001) and Data Processing Agreement (DPA).

#### 4.3 Phase 3: Assessment Execution
The Project Lead, guided by the CISO, must complete the *DPIA Template (IS-FRM-022)* covering the following four pillars:

**4.3.1 Description of Processing**
*   Describe the nature, scope, context, and purposes of the processing.
*   Map the data flow: Collection $\rightarrow$ Storage $\rightarrow$ Usage $\rightarrow$ Transfer $\rightarrow$ Destruction.
*   Explicitly state the Lawful Basis for processing (e.g., Consent, Contract, Legitimate Interest).

**4.3.2 Necessity and Proportionality**
*   Justify why the data is needed.
*   Confirm data minimization (is the volume of data appropriate for the goal?).
*   Confirm retention periods align with the *Records Retention Schedule (GOV-STD-005)*.

**4.3.3 Risk Identification**
*   Identify risks to the rights and freedoms of data subjects (e.g., identity theft, discrimination, loss of confidentiality, re-identification of pseudonymized data).
*   Assess risks specifically related to AI/Automated Decision Making if applicable.

**4.3.4 Risk Evaluation**
*   Score each risk based on **Likelihood** (1-5) and **Severity** (1-5).
*   Any risk score above the defined threshold in the *Risk Management Strategy (IS-POL-003)* requires mitigation.

#### 4.4 Phase 4: Risk Mitigation
For every identified risk, the working group must propose a mitigation strategy:
1.  **Technical Measures:** Encryption, pseudonymization, access controls, MFA.
2.  **Organizational Measures:** Staff training, policy updates, strict access governance.
3.  **Re-scoring:** Re-evaluate the risk score *after* applying mitigation to determine the **Residual Risk**.

#### 4.5 Phase 5: Review and Approval
1.  **CISO Review:** The CISO reviews the DPIA for completeness and technical accuracy.
2.  **DPO/Legal Review:** Legal Counsel (or DPO) provides a written opinion on compliance with TDPSA/GDPR/COPPA.
3.  **Executive Sign-Off:**
    *   If **Residual Risk is Low/Medium:** The CISO may approve.
    *   If **Residual Risk is High:** The Executive Director (CEO) must formally accept the risk or reject the project.
    *   **Doomsday Clause:** If the processing poses an existential threat to the organization or violates **Bylaws Article I (Purpose)**, the Board of Directors must be notified.

#### 4.6 Phase 6: Integration and Monitoring
1.  **Implementation:** Approved mitigation measures must be integrated into the project plan *before* Go-Live.
2.  **Documentation:** The final signed DPIA is stored in the *Central Compliance Repository*.
3.  **Re-Assessment:** The DPIA must be reviewed:
    *   Annually.
    *   Whenever the scope of processing changes (e.g., new data fields collected).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Project Lead** | Initiates the DPIA, describes processing, and implements mitigation measures. |
| **CISO** | Owns the DPIA process, provides technical guidance, and verifies mitigation effectiveness. |
| **Legal Counsel / DPO** | Reviews DPIA for regulatory compliance (TDPSA, GDPR, COPPA) and advises on liability. |
| **Executive Director** | Final decision-maker for accepting High Residual Risks. |
| **Board of Directors** | Informed of any processing activities that create systemic high risks to the organization. |

### 6. Compliance and Enforcement
Failure to conduct a DPIA for high-risk processing is a violation of this procedure and potentially state/federal law.
*   **Internal:** Employees bypassing this procedure may face disciplinary action up to and including termination.
*   **External:** Failure to comply with TDPSA or GDPR DPIA requirements can result in significant financial penalties against Study GRC Inc.
*   **Audit:** DPIA records must be maintained for at least 5 years and made available to the Texas Attorney General or Data Protection Authorities upon request.

### 7. References
*   **Bylaws of Study GRC Inc.** (Article IX - Policies & Data Protection)
*   **Texas Data Privacy and Security Act (TDPSA)** (Sec. 541.105)
*   **GDPR Article 35** (Data Protection Impact Assessment)
*   **COPPA** (Children's Online Privacy Protection Act)
*   **IS-POL-001:** Master Information Security Policy
*   **IS-FRM-021:** DPIA Screening Checklist
*   **IS-FRM-022:** DPIA Template

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Legal Officer | Initial Release aligned with TDPSA and GDPR requirements. |