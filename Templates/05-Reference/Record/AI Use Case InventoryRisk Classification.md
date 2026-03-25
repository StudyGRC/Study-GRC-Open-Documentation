### AI Use Case Inventory and Risk Classification Standard

|  | Document Control |
| --- | --- |
| **Document ID** | DP-STD-005 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | AI Governance Board |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Public (Transparency) |

### 1. Purpose
The purpose of this Standard is to establish a mandatory framework for identifying, cataloging, and classifying all Artificial Intelligence (AI) systems used by Study GRC Inc. This document satisfies the **MAP Function** of the NIST AI Risk Management Framework (AI RMF) by creating a comprehensive context of usage.

As a 501(c)(3) organization dedicated to GRC knowledge and open-source resources, Study GRC Inc. must ensure its use of AI aligns with our charitable purpose (Bylaws Article I, Section 1.3) and protects our community, particularly regarding K-12 youth interactions. This inventory serves as the primary mechanism to track AI assets, assess their risks, and ensure compliance with the EU AI Act, NIST AI RMF, and federal grant requirements (2 CFR 200).

### 2. Scope
This Standard applies to all "AI Systems" (defined below) utilized by Study GRC Inc., including:
- **Internally Developed Models:** AI tools built or fine-tuned by Study GRC volunteers or staff.
- **Third-Party Vendor Tools:** SaaS platforms with embedded AI features (e.g., Zoom AI Companion, Slack integrations, HR recruiting tools).
- **Generative AI:** Tools used for content creation, code generation, or image synthesis.
- **Grant-Funded Projects:** AI systems procured or developed using federal funds.

**Exclusions:**
- Standard software automation (e.g., spreadsheet formulas, basic "if-then" scripts) that does not utilize machine learning or probabilistic reasoning.

### 3. Definitions

| Term | Definition |
| --- | --- |
| **AI System** | A machine-based system that can, for a given set of human-defined objectives, make predictions, recommendations, or decisions influencing real or virtual environments. |
| **Generative AI (GenAI)** | AI models designed to generate new content (text, code, images, audio) in response to user prompts. |
| **System Owner** | The specific Operational Officer or Department Head responsible for the procurement, deployment, and oversight of a specific AI tool. |
| **Risk Classification** | The categorization of an AI system based on its potential impact on individual rights, safety, and organizational reputation. |
| **Shadow AI** | The use of AI tools or systems by employees or volunteers without formal approval, inventory registration, or security vetting. |

### 4. Standards and Procedures

#### 4.1. The Master AI Inventory (The Register)
The Organization shall maintain a centralized **Master AI Inventory**. This is a living database/register. For every AI system in use, the following data points **must** be recorded:

1. **System Name & Vendor:** (e.g., "ChatGPT Enterprise," "GitHub Copilot").
2. **System Owner:** (Name and Role).
3. **Use Case Description:** A clear, non-technical explanation of what the AI does (e.g., "Summarizing Board meeting minutes," "Generating Python code for open-source projects").
4. **Data Inputs:** What data is fed into the system? (e.g., Public web data, Member PII, Proprietary code).
5. **Deployment Status:** (Pilot, Production, Retired).
6. **Risk Classification:** (Assigned per Section 4.2).
7. **Human Oversight Method:** How is the output verified? (e.g., "Human-in-the-loop review of all code").

#### 4.2. Risk Classification Framework
All AI systems must be classified into one of the following four tiers. This classification dictates the level of governance and approval required.

**Tier 1: Unacceptable Risk (PROHIBITED)**
- **Definition:** Systems that pose a clear threat to safety, livelihoods, or rights.
- **Examples:**
- Social scoring of members or volunteers.
- Real-time remote biometric identification (facial recognition) in public spaces or events.
- AI systems that use subliminal techniques to manipulate behavior.
- **Youth Protection:** Any AI tool that collects behavioral data on minors (under 18) for the purpose of marketing or profiling.
- **Action:** Strictly prohibited. Cannot be procured or deployed.

**Tier 2: High Risk**
- **Definition:** Systems used in critical areas that could impact a person's life, career, or safety, or systems interacting directly with vulnerable populations (Youth).
- **Examples:**
- **HR/Recruiting:** AI used to filter resumes or rank job/volunteer applicants (Bias risk).
- **Education:** AI tutors or grading assistants used in K-12 programs.
- **Security:** AI-driven automated network defense that can autonomously ban users.
- **Action:** Requires **Board of Directors** approval, a full Data Protection Impact Assessment (DPIA), and rigorous ongoing monitoring.

**Tier 3: Moderate Risk (Limited)**
- **Definition:** Systems with specific transparency obligations, where the risk of harm is low but manipulation is possible.
- **Examples:**
- **Chatbots:** Customer service or community support bots (Must disclose they are AI).
- **Content Generation:** GenAI used to draft blog posts, emails, or marketing copy.
- **Code Generation:** AI coding assistants (e.g., Copilot).
- **Action:** Requires **Executive Director** approval. Output must be labeled as AI-generated. Mandatory human review of outputs.

**Tier 4: Low / Minimal Risk**
- **Definition:** Passive tools or standard business automation.
- **Examples:**
- Spam filters.
- Inventory management predictors.
- Grammar checkers / Autocorrect.
- **Action:** Requires **Department Head** approval. Logged in inventory but minimal ongoing compliance burden.

#### 4.3. Inventory Maintenance and Review
- **Trigger-Based Updates:** The Inventory must be updated *prior* to the procurement or deployment of any new AI tool (Pre-deployment registration).
- **Quarterly Audit:** The CISO and AI Governance Board shall review the inventory quarterly to ensure classifications remain accurate as tools evolve.
- **Decommissioning:** When a tool is retired, it must be marked as "Retired" in the inventory, and data destruction procedures (per *DP-STD-015*) must be executed.

#### 4.4. Transparency and Public Disclosure
In accordance with Bylaws Article VIII (Transparency), Study GRC Inc. shall publish a **Public AI Register** on its website. This public version will list:
- The names of High and Moderate risk AI systems in use.
- The purpose of the system.
- The logic involved (high-level).
- *Note: Vendor-specific security configurations or proprietary data inputs will be redacted from the public version.*

### 5. Roles and Responsibilities

| Role | Responsibility |
| --- | --- |
| **AI Governance Board** | Owns the Risk Classification Framework. Approves all Tier 2 (High Risk) systems. Reviews the inventory quarterly. |
| **System Owner** | Responsible for registering the tool in the inventory, accurately describing the use case, and ensuring human oversight of the tool's output. |
| **Chief Information Security Officer (CISO)** | Validates the security of the AI tool. Ensures no "Shadow AI" exists on the network. |
| **Data Protection Officer (DPO)** | Reviews Data Inputs for privacy compliance (GDPR/CCPA/COPPA). Conducts DPIAs for High-Risk systems. |
| **Executive Director** | Final approving authority for Tier 3 systems. Ensures budget alignment for AI procurement. |

### 6. Compliance and Enforcement
**Shadow AI Prohibition:** The use of AI tools that have not been registered in the Master AI Inventory and assigned a Risk Classification is strictly prohibited.

Failure to comply with this standard—specifically the deployment of High-Risk or Prohibited AI systems without authorization—may result in disciplinary action, up to and including termination of employment or removal from volunteer service. For Board members, violations may constitute "cause" for removal under Bylaws Article III, Section 3.6.

### 7. References
- **NIST AI Risk Management Framework (AI RMF 1.0):** Govern 1.2, Map 1.1, Map 1.5.
- **EU AI Act:** Classification of High-Risk AI Systems (Annex III).
- **Bylaws of Study GRC Inc.:** Article I (Purpose) and Article VIII (Transparency).
- **DP-POL-001:** Master Data Privacy Policy.
- **DP-POL-040:** Artificial Intelligence (AI) Acceptable Use Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| --- | --- | --- | --- |
| v1.0 | [Date] | Chief Compliance Architect | Initial Release aligned with NIST AI RMF. |
