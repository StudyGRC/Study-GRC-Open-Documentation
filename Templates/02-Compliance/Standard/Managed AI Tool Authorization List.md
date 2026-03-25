### Managed AI Tool Authorization List

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-012 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-04-25 (Bi-Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | IT Security Manager |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Standard is to define the specific Artificial Intelligence (AI) and Machine Learning (ML) tools authorized for use within Study GRC Inc. ("the Organization"). This document maps specific tools to the Organization's **Data Classification Policy** to prevent the unauthorized disclosure of sensitive information, protect Intellectual Property (IP) rights as defined in **Bylaws Article IX**, and ensure compliance with privacy regulations (including GDPR, CCPA, and COPPA).

This Standard serves as the definitive "Allow List" for AI usage. Any tool not explicitly listed herein is considered **prohibited** for business use until vetted and approved.

### 2. Scope
This Standard applies to:
*   **Personnel:** All Directors, Officers, employees, contractors, and volunteers.
*   **Assets:** All Organization-owned devices and BYOD devices when used to process Organization data.
*   **Data:** All data types including text, code, images, video, and audio generated or processed by the Organization.

**Exclusions:**
*   Personal use of AI tools on personal devices that does not involve *any* Organization data, IP, or references to Study GRC Inc.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Generative AI (GenAI)** | Algorithms (such as ChatGPT, Claude, Midjourney) that can be used to create new content, including audio, code, images, text, simulations, and videos. |
| **Training Data** | Information input into an AI model that the vendor may use to improve their model. Data used for training is generally considered publicly exposed. |
| **Zero-Retention** | A configuration where the AI vendor does not store inputs or outputs for model training purposes. |
| **Public Data** | Information intended for public release (e.g., published blog posts, open-source code, marketing materials). |
| **Internal Data** | Information for internal operations but not sensitive (e.g., meeting agendas, draft policies, internal memos). |
| **Confidential Data** | Sensitive information requiring protection (e.g., donor lists, unpublished financial reports, strategic plans). |
| **Restricted Data** | Highly sensitive data (e.g., PII, passwords, youth participant data, private keys). |

### 4. Standards

#### 4.1 General Authorization Principles
1.  **Default Denial:** If a tool is not listed in Section 4.2, it is prohibited for use with Internal, Confidential, or Restricted data.
2.  **Data Mapping:** Users must strictly adhere to the "Max Data Classification" column. Placing Confidential data into a tool authorized only for Public data is a violation of this Standard.
3.  **Youth Data Prohibition:** Under no circumstances may PII, photos, or identifiers of minors (Youth Participants) be input into *any* Generative AI tool, regardless of the tool's security rating, without explicit written approval from the CISO and Legal Counsel.

#### 4.2 Authorized Tool Matrix

The following tools are authorized for use subject to the specified configurations and data limitations.

| Tool Name | Vendor | License Type | Max Data Classification | Required Configuration / Notes |
| :--- | :--- | :--- | :--- | :--- |
| **ChatGPT (Free/Plus)** | OpenAI | Personal/Free | **Public Only** | **MUST** disable "Chat History & Training" in settings. Do not paste proprietary code or internal memos. |
| **ChatGPT Team/Ent** | OpenAI | Corporate | **Confidential** | Authorized for business strategy and drafting. Vendor has zero-retention agreement in place. |
| **GitHub Copilot** | Microsoft | Business | **Internal** | Authorized for code generation. **MUST** enable "Block suggestions matching public code" filter. |
| **Claude 2/3** | Anthropic | Personal/Free | **Public Only** | Use only for summarizing public documents. No internal data allowed. |
| **Midjourney** | Midjourney | Standard | **Public Only** | Images generated are public by default. Do not upload photos of staff or members for manipulation. |
| **Canva (Magic Write)** | Canva | Teams | **Internal** | Authorized for marketing copy and design. |
| **Grammarly** | Grammarly | Business | **Internal** | Authorized for spelling/grammar checking of general business communications. |
| **Microsoft 365 Copilot** | Microsoft | Enterprise | **Confidential** | Authorized for summarizing emails, Teams meetings, and Word documents within the tenant. |

#### 4.3 Prohibited Tools (Blacklist)
While not exhaustive, the following tools are explicitly prohibited due to aggressive data harvesting terms or lack of security controls:
1.  **Otter.ai (Free Version):** Prohibited for recording Confidential/Executive Session meetings due to auto-join features and data retention.
2.  **Any "Wrapper" Tool:** Browser extensions or websites that claim to "access GPT-4 for free" without a clear vendor privacy policy.
3.  **Deepfake Generators:** Any tool designed specifically to impersonate real individuals (voice or video) without consent.

#### 4.4 Input Sanitization Requirements
Before inputting data into any authorized tool with a classification of **Public** or **Internal**:
1.  **Anonymization:** Remove real names, addresses, and phone numbers.
2.  **Genericization:** Replace specific entity names (e.g., "Study GRC Inc.") with generic terms (e.g., "The Non-Profit") if the prompt context allows.
3.  **Secret Stripping:** Ensure no API keys, passwords, or credentials are included in code snippets pasted into AI coding assistants.

#### 4.5 Output Ownership and IP
Pursuant to **Bylaws Article IX (Intellectual Property)**:
1.  **Work Made for Hire:** Any content generated by AI tools during the course of service to the Organization is considered the property of Study GRC Inc., to the extent permitted by law.
2.  **Disclosure:** Personnel must disclose if a deliverable (code, policy, article) was significantly generated (>50%) by AI.
3.  **Copyright Risk:** Users must not use AI to generate content that deliberately infringes on known third-party trademarks or copyrighted works.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **CISO** | Maintains this Standard; reviews new tool requests; conducts risk assessments on AI vendors. |
| **IT Department** | Implements technical blocks (CASB/Firewall) for prohibited tools; manages Enterprise licenses. |
| **Department Heads** | Ensure team members are using the correct license tier (e.g., ensuring staff use the Corporate account, not personal). |
| **Users (Staff/Vols)** | Verify the tool is on the Authorized List before use; sanitize data inputs; report "hallucinations" or security anomalies. |

### 6. Compliance and Enforcement
Failure to comply with this Standard—specifically the input of Confidential or Restricted data into unauthorized Public tools—constitutes a data breach.

**Consequences:**
*   **Volunteers/Staff:** Disciplinary action up to and including termination of employment or volunteer assignment.
*   **Legal:** Potential civil liability if the action results in the loss of Intellectual Property rights or regulatory fines (e.g., GDPR/COPPA violations).

### 7. References
*   **IS-POL-001:** Master Information Security Policy
*   **IS-STD-005:** Data Classification Standard
*   **GOV-POL-009:** Intellectual Property Policy
*   **Bylaws of Study GRC Inc.:** Article IX (Intellectual Property)
*   **NIST AI RMF:** NIST AI Risk Management Framework 1.0

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | CISO | Initial release of Authorized AI Tool List. |