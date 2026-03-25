### AI System Impact Assessment

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-ASM-005 |
| **Document Type** | Assessment / Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-04-27 (Bi-Annual) |
| **Approving Authority** | Executive Director (CEO) |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this AI System Impact Assessment (AIA) is to systematically evaluate the risks, benefits, and ethical implications of any Artificial Intelligence (AI) system prior to its procurement, development, or deployment within Study GRC Inc.

This standard mandates a "Safety-First" approach, ensuring that algorithmic tools do not compromise the Organization’s tax-exempt mission, the safety of our K-12 community participants, or our commitment to open-source transparency. It aligns with the NIST AI Risk Management Framework (AI RMF) to identify "Safety-Impacting" and "Rights-Impacting" capabilities.

### 2. Scope
This assessment applies to all employees, contractors, and volunteers ("Users") seeking to introduce AI technologies into the Organization’s ecosystem.

**In Scope:**
*   Generative AI tools (e.g., LLMs, image generators).
*   Automated decision-making systems used for HR, membership vetting, or content moderation.
*   AI components embedded within third-party software (SaaS) used for critical operations.
*   Custom-developed AI models or fine-tuned open-source models.

**Exclusions:**
*   Standard office automation tools with incidental AI features (e.g., basic spell-check, spam filters) that do not process Sensitive Personal Data or make autonomous decisions.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **AI System** | A machine-based system that can, for a given set of human-defined objectives, make predictions, recommendations, or decisions influencing real or virtual environments. |
| **Safety-Impacting AI** | An AI system whose output produces legal, material, binding, or significant effects on an individual's physical or psychological safety, particularly regarding minors (e.g., automated content moderation in youth channels). |
| **Rights-Impacting AI** | An AI system whose output affects civil rights, civil liberties, privacy, equal opportunities, or access to critical services (e.g., resume screening algorithms). |
| **Human-in-the-Loop (HITL)** | A mandatory control where a qualified human must review and approve AI outputs before they are finalized or acted upon. |
| **Hallucination** | A phenomenon where an AI model generates incorrect, nonsensical, or unverifiable information presented as fact. |

### 4. Assessment Procedures

All proposed AI systems must undergo the following assessment phases **before** deployment.

#### 4.1 Phase I: Threshold Screening
The Project Owner must answer the following threshold questions. If the answer to **any** question is "Yes," a full Phase II Assessment is required.

1.  Will the system interact directly with Community Participants, specifically minors (under 18)?
2.  Will the system process "Sensitive Personal Data" as defined in the *Master Data Privacy Policy*?
3.  Will the system generate code or educational content that will be released as Open Source under the Organization's name?
4.  Does the system make decisions regarding employment, volunteer eligibility, or membership expulsion?

#### 4.2 Phase II: Impact Analysis Categories
The CISO and the requesting department must evaluate the system across four critical domains:

**4.2.1 Safety and Psychological Impact (Youth Protection)**
*   **Risk:** Does the system have the potential to expose minors to harmful content, radicalization, or grooming?
*   **Requirement:** Any AI acting as a moderator or tutor for youth must have strict content guardrails and fail-safe mechanisms.
*   **Assessment:** Test for "jailbreak" vulnerability where the AI could be coerced into violating safety guidelines.

**4.2.2 Rights and Bias Impact**
*   **Risk:** Does the training data or algorithm exhibit bias against protected classes (race, gender, disability, etc.)?
*   **Requirement:** For HR or Membership tools, the vendor must provide a bias audit or the Organization must conduct testing using synthetic data.
*   **Assessment:** Evaluate if the system adheres to the *Equal Employment Opportunity (EEO) Policy*.

**4.2.3 Intellectual Property and Open Source Alignment**
*   **Risk:** Does the AI claim ownership of the output, or does the vendor use our data to train their public models?
*   **Requirement:** Pursuant to **Bylaws Article IX (Intellectual Property)**, Study GRC Inc. must retain ownership of work product to ensure it remains open source.
*   **Assessment:** Review Terms of Service to ensure "Input Confidentiality" (our data is not used for training) and "Output Ownership" (we own what we create).

**4.2.4 Accuracy and Hallucination**
*   **Risk:** Will the AI generate educational material that is factually incorrect, damaging the Organization's reputation as a GRC authority?
*   **Requirement:** All AI-generated educational content requires subject matter expert (SME) review.
*   **Assessment:** Determine the documented error rate of the model.

#### 4.3 Phase III: Risk Scoring and Approval
Based on Phase II, the system is assigned a Risk Level:

| Risk Level | Criteria | Approval Required | Mandatory Controls |
| :--- | :--- | :--- | :--- |
| **Prohibited** | Biometric identification, real-time surveillance of staff, non-consensual deepfakes. | **N/A (Banned)** | N/A |
| **High** | Interactions with minors; HR/Hiring decisions; Code generation for production security tools. | **Executive Director + CISO** | Full HITL; Monthly Audits; DPIA Required. |
| **Medium** | Content drafting (marketing); Data analysis of non-sensitive data. | **Department Head** | SME Review of Output; Annual Review. |
| **Low** | Internal scheduling; Meeting summarization (non-confidential). | **Manager** | User Awareness Training. |

#### 4.4 Phase IV: Mitigation and Deployment
For all approved High and Medium risk systems, the following mitigations must be implemented:
1.  **Transparency:** Users/Members must be notified they are interacting with an AI (e.g., "This response was generated by AI").
2.  **Opt-Out:** Users must have the ability to request human review or opt-out of AI processing where feasible.
3.  **Data Minimization:** Only the minimum necessary data may be fed into the system.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Project Owner** | Initiates the assessment; provides technical specifications and intended use cases. |
| **Chief Information Security Officer (CISO)** | Conducts the technical security review; validates data privacy controls; assigns Risk Level. |
| **Director of Kindness & Generosity (DKG)** | Reviews the assessment for community culture impact, specifically regarding inclusivity and tone. |
| **Executive Director (CEO)** | Provides final authorization for High-Risk systems; ensures alignment with Strategic Plan. |
| **Board of Directors** | Receives notification of any High-Risk system approvals; reviews the *AI System Impact Assessment* standard annually. |

### 6. Compliance and Enforcement
**6.1 Audit Trail**
All completed Impact Assessments must be retained for a minimum of five (5) years in accordance with the *Document Retention and Destruction Policy*.

**6.2 Violations**
Deployment of an AI system without a completed and approved Impact Assessment is a violation of this standard.
*   **Consequences:** Immediate suspension of the AI tool, revocation of API keys, and disciplinary action against the responsible employee or volunteer, up to and including termination.
*   **Legal Liability:** Failure to assess safety-impacting AI that results in harm to a minor may result in personal liability and legal action against the Organization.

### 7. References
*   **Bylaws of Study GRC Inc.** (Article IX: Intellectual Property; Article III: Governance)
*   **NIST AI Risk Management Framework (AI RMF 1.0)**
*   **IS-POL-001:** Master Information Security Policy
*   **IS-POL-036:** Artificial Intelligence (AI) Acceptable Use Policy
*   **HR-POL-024:** Child and Youth Safeguarding Policy
*   **GDPR Article 35:** Data Protection Impact Assessment (DPIA)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name], CISO | Initial Release aligned with NIST AI RMF. |