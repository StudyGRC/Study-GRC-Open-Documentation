### Generative AI Risk Assessment Template

| Document Control | |
| :--- | :--- |
| **Document ID** | DP-FRM-040 |
| **Document Type** | Form / Assessment |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-04-25 (Bi-Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) / AI Governance Board |
| **Document Owner** | Chief AI Officer (CAIO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this **Generative AI Risk Assessment Template** is to standardize the evaluation of Generative Artificial Intelligence (GenAI) tools and use cases prior to their adoption or deployment within Study GRC Inc. This assessment is mandatory to identify, categorize, and mitigate specific risks associated with GenAI, with a strict focus on **algorithmic bias**, **hallucinations (accuracy errors)**, **data privacy**, and **intellectual property** concerns. This form ensures compliance with the *Artificial Intelligence (AI) Acceptable Use Policy* and aligns with the NIST AI Risk Management Framework (AI RMF).

### 2. Scope
This assessment applies to all **Employees, Volunteers, Contractors, and Board Members** ("Requesters") seeking to:
1.  Procure or subscribe to a new GenAI tool (e.g., ChatGPT Enterprise, Midjourney, GitHub Copilot).
2.  Integrate GenAI APIs into Study GRC Inc. products or community platforms.
3.  Utilize free/open-source GenAI models for official Organization business.

**Exclusions:** This form is not required for incidental personal use of AI on personal devices that does not involve Organization data, provided such use adheres to the *Acceptable Use Policy*.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Generative AI (GenAI)** | AI systems capable of generating new content (text, images, code) in response to prompts (e.g., LLMs). |
| **Hallucination** | A phenomenon where an AI model generates incorrect, nonsensical, or unverifiable information while presenting it as fact. |
| **Algorithmic Bias** | Systematic and repeatable errors in a computer system that create unfair outcomes, such as privileging one arbitrary group of users over others. |
| **Human-in-the-Loop (HITL)** | A capability or process requiring human interaction to verify or approve AI output before it is finalized or published. |
| **Training Data** | The dataset used to teach the AI model. Risks arise if this data contains PII, copyrighted material, or biased information. |

### 4. Risk Assessment Questionnaire

*Instructions: The Requester must complete Sections A through E. The CISO/CAIO will complete Section F.*

#### Section A: General Information
| Field | Response |
| :--- | :--- |
| **Requester Name** | [Name] |
| **Department/Committee** | [e.g., Education & Training] |
| **Name of AI Tool/Model** | [e.g., ChatGPT-4, Claude 2] |
| **Vendor/Developer** | [e.g., OpenAI, Anthropic] |
| **Proposed Use Case** | [Describe exactly how this tool will be used. E.g., "Drafting curriculum summaries," "Chatbot for member support."] |

#### Section B: Data Privacy & Security
*Reference: Master Data Privacy Policy*

1.  **Data Input Classification:** What is the highest classification of data that will be input into this tool?
    *   [ ] Public (Website content, open-source resources)
    *   [ ] Internal (Meeting minutes, drafts)
    *   [ ] Confidential (Member PII, financial data, vulnerability reports)
    *   [ ] Restricted (Youth data, sensitive legal matters)

2.  **Training Data Usage:** Does the vendor use our input data to train their public models?
    *   [ ] Yes
    *   [ ] No (Enterprise/Zero-Retention agreement required)
    *   [ ] Unknown

3.  **Youth Interaction:** Will this tool interact directly with minors (under 18) or process data regarding minors?
    *   [ ] Yes (Requires *Child and Youth Safeguarding Policy* review)
    *   [ ] No

#### Section C: Accuracy & Hallucination Risk
*Reference: AI Output Verification Standard*

4.  **Impact of Errors:** If the AI generates false information (hallucinates), what is the worst-case impact?
    *   [ ] Low (Internal draft, easily corrected)
    *   [ ] Medium (Member confusion, reputational annoyance)
    *   [ ] High (Legal liability, incorrect security advice, financial loss)

5.  **Human Oversight Protocol:** Describe the mandatory Human-in-the-Loop (HITL) process. Who reviews the output before it is used?
    *   *Response:* [Describe the review process]

6.  **Fact-Checking:** For educational content, how will citations and technical facts be verified against authoritative sources?
    *   *Response:* [Describe verification method]

#### Section D: Bias & Ethical Impact
*Reference: Code of Ethics and Conduct*

7.  **Decision Making:** Will this tool assist in making decisions about individuals (e.g., scholarship applications, member discipline, hiring)?
    *   [ ] Yes
    *   [ ] No

8.  **Bias Mitigation:** If the tool generates content depicting people (text or images), how will you ensure diversity and prevent stereotype reinforcement?
    *   *Response:* [Describe prompting strategy or review guidelines]

9.  **Accessibility:** Does the tool's output comply with WCAG 2.2 AA standards (e.g., alt text for generated images)?
    *   [ ] Yes
    *   [ ] No
    *   [ ] N/A (Text only)

#### Section E: Intellectual Property (IP)
*Reference: Bylaws Article IX, Section 9.3*

10. **Ownership:** Per the vendor's Terms of Service, who owns the output generated by the tool?
    *   [ ] Study GRC Inc.
    *   [ ] The Vendor
    *   [ ] Public Domain / No Copyright

11. **Open Source Alignment:** Does using this tool restrict our ability to release the resulting work as Open Source/Creative Commons?
    *   [ ] Yes (Risk of "viral" restrictive licenses)
    *   [ ] No

---

#### Section F: Risk Scoring & Approval (To be completed by CISO/CAIO)

**Risk Calculator:**

| Risk Category | Assessed Level (Low/Med/High) | Mitigation Required? |
| :--- | :--- | :--- |
| **Data Leakage** | [Select] | [ ] Yes |
| **Hallucination** | [Select] | [ ] Yes |
| **Bias/Ethics** | [Select] | [ ] Yes |
| **Regulatory (GDPR/COPPA)**| [Select] | [ ] Yes |

**Final Determination:**
*   [ ] **APPROVED:** Risk is acceptable; standard controls apply.
*   [ ] **APPROVED WITH CONDITIONS:** Specific controls (listed below) must be implemented.
*   [ ] **REJECTED:** Risk outweighs benefit.

**Required Controls / Conditions of Approval:**
1.  [e.g., "User must enable 'Chat History & Training' opt-out."]
2.  [e.g., "Output must be reviewed by a Subject Matter Expert prior to publication."]
3.  [e.g., "No PII permitted in prompts."]

| Approver Name | Title | Signature | Date |
| :--- | :--- | :--- | :--- |
| [Name] | [Title] | __________________ | [Date] |

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Requester** | Completes Sections A-E truthfully; identifies the specific use case and data types involved. |
| **Department Head** | Validates the business need and ensures the Requester has the expertise to perform Human Oversight. |
| **Chief AI Officer (CAIO)** | Reviews the assessment for Bias and Hallucination risks; defines the Human-in-the-Loop requirements. |
| **CISO** | Reviews the assessment for Data Privacy and Security risks; validates vendor terms regarding data retention. |
| **Legal Counsel** | Consulted if the tool involves high-risk IP issues or processing of sensitive categories of data (e.g., Youth data). |

### 6. Compliance and Enforcement
Failure to complete this assessment prior to deploying a GenAI tool, or falsifying information within this assessment, constitutes a violation of the *Master Information Security Policy*. Violations may result in disciplinary action, up to and including termination of employment or volunteer assignment, and immediate revocation of API/tool access.

### 7. References
*   **Study GRC Inc. Bylaws (Article IX - IP & Data Protection)**
*   **NIST AI Risk Management Framework (AI RMF 1.0)**
*   **IS-POL-036 Artificial Intelligence (AI) Acceptable Use Policy**
*   **DP-POL-001 Master Data Privacy Policy**
*   **YP-POL-001 Child and Youth Safeguarding Policy**

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name] | Initial release of risk assessment template. |