### Publicly Available GenAI Restrictions

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-045 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-04-25 (Bi-Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Public |

### 1. Purpose
The purpose of this policy is to mitigate the risks of data leakage, intellectual property loss, and privacy violations associated with the use of publicly available Generative Artificial Intelligence (GenAI) tools. While Study GRC Inc. embraces innovation, we must ensure that our proprietary data, Member information, and sensitive operational details are not inadvertently exposed to third-party models for training purposes, thereby becoming public knowledge.

### 2. Scope
This policy applies to all "Authorized Users," defined as Directors, Officers, employees, volunteers, contractors, and committee members of Study GRC Inc.

**In Scope:**
*   All publicly available GenAI tools (e.g., ChatGPT (Free/Plus), Claude.ai, Google Gemini, Midjourney, GitHub Copilot for Individuals) where Study GRC Inc. does not hold an Enterprise License Agreement (ELA) with specific data privacy guarantees.
*   Any device (personal or organization-owned) used to perform work for Study GRC Inc.

**Out of Scope:**
*   Enterprise-grade AI instances hosted within Study GRC Inc.’s secure perimeter (e.g., Azure OpenAI Service) that have been explicitly vetted and approved by the CISO as "Private/No-Training" environments.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Public GenAI** | Artificial intelligence models accessible to the general public where the terms of service allow the provider to use input data to train or improve the model (e.g., the default setting of ChatGPT). |
| **Input Data** | Any text, code, image, or file uploaded or typed into a GenAI prompt by a user. |
| **Confidential Information** | As defined in Bylaws Article IX §9.2 and the Data Classification Standard, this includes PII, financial records, security vulnerabilities, and strategic non-public documents. |
| **Model Training** | The process by which an AI provider uses user inputs to teach the AI model, potentially allowing the AI to reproduce that information to other users outside the Organization. |
| **PII** | Personally Identifiable Information (e.g., names, emails, addresses), specifically including data regarding youth participants. |

### 4. Policy Statements

#### 4.1 General Prohibition on Sensitive Data Input
Authorized Users are strictly prohibited from inputting, pasting, or uploading **Confidential** or **Restricted** data into any Public GenAI tool. Public GenAI tools must be treated as "untrusted public environments," similar to posting data on a public social media forum.

#### 4.2 Prohibited Data Categories
To ensure compliance with Bylaws Article IX (Policies & Data Protection) and Article VII (Indemnification), the following specific data types must **never** be entered into a Public GenAI prompt:

1.  **Personal Data (PII):** Names, addresses, emails, or phone numbers of Members, donors, or volunteers.
2.  **Youth Data:** Any information regarding K-12 participants, regardless of anonymity. This is critical for COPPA compliance.
3.  **Security Credentials:** Passwords, API keys, encryption keys, or private certificates.
4.  **Financial Data:** Bank account numbers, credit card numbers, or unreleased financial reports (prior to public release per Bylaws Article VIII §8.2).
5.  **Legal & Strategic:** Draft contracts, attorney-client privileged communications, or unannounced strategic partnership details.
6.  **Proprietary Code:** Source code that has not yet been released as Open Source by the Organization.

#### 4.3 Acceptable Use of Public GenAI
Authorized Users may use Public GenAI tools for productivity, provided the input data is classified as **Public** or is generic in nature. Examples of acceptable use include:
*   Drafting generic emails (without specific names/details).
*   Summarizing publicly available articles or regulatory texts (e.g., "Summarize Texas BOC § 22.101").
*   Debugging generic code snippets that contain no business logic or credentials.
*   Brainstorming marketing copy for public events.

#### 4.4 Mandatory Settings Configuration
When using Public GenAI tools for Organization business, Authorized Users must:
1.  **Disable Training History:** Where the platform allows (e.g., ChatGPT "Chat History & Training" toggle), users must disable the feature that allows the provider to use data for model training.
2.  **Use Corporate Credentials:** If an account is required, users should use their Study GRC Inc. email address, not personal email addresses, to ensure the Organization retains administrative oversight where possible.

#### 4.5 Intellectual Property and Ownership
Pursuant to **Bylaws Article IX §9.3 (Intellectual Property)**:
*   Any content generated by AI for the Organization is considered "Work Product."
*   The User agrees that Study GRC Inc. owns all rights to the output generated for organizational purposes.
*   Users must not claim AI-generated output as their own original work without disclosure.
*   Users are responsible for ensuring AI-generated code or content does not infringe on third-party copyright before submission.

#### 4.6 Output Verification
AI models are prone to "hallucinations" (confident but false information). Users must verify all AI-generated facts, citations, and code against authoritative sources before using them in Study GRC Inc. materials. Unverified AI content must not be published to the community.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Authorized Users** | Responsible for sanitizing all inputs to ensure no Confidential data is shared with Public GenAI tools. Responsible for verifying the accuracy of AI outputs. |
| **Chief Information Security Officer (CISO)** | Responsible for maintaining a list of approved/blocked AI tools and monitoring network traffic for data exfiltration attempts via AI platforms. |
| **Executive Director** | Responsible for ensuring staff and volunteers are trained on the distinction between Public and Private data. |
| **Board of Directors** | Responsible for reviewing this policy annually to adapt to the rapidly changing AI landscape. |

### 6. Compliance and Enforcement
Failure to comply with this policy puts the Organization at significant legal and reputational risk.

*   **Violations:** Entering Confidential data (especially Youth Data or Credentials) into a Public GenAI tool is a violation of the Non-Disclosure Agreement (NDA) required by Bylaws Article IX §9.2.
*   **Consequences:** Violations may result in disciplinary action, up to and including termination of employment, removal from volunteer service, or removal from the Board of Directors for cause (Bylaws Article III §3.6). Legal action may be pursued for damages resulting from data breaches.

### 7. References
*   **Bylaws of Study GRC Inc.** (Specifically Article IX: Policies & Data Protection)
*   **IS-STD-005:** Data Classification Standard
*   **IS-POL-001:** Master Information Security Policy
*   **HR-POL-020:** Child and Youth Safeguarding Policy (COPPA Compliance)
*   **NIST AI Risk Management Framework (AI RMF 1.0)**

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Legal Officer | Initial Policy Release |