### Explicit Consent Mechanism (Sensitive Data)

| Document Control | |
| :--- | :--- |
| **Document ID** | GOV-STD-035 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Board of Directors / Chief Information Security Officer (CISO) |
| **Document Owner** | Data Protection Officer (DPO) |
| **Classification** | Public |

### 1. Purpose
The purpose of this Standard is to define the mandatory technical and visual requirements for obtaining **Explicit Consent** prior to the collection, processing, or sharing of **Sensitive Personal Data**.

As a Texas Non-Profit operating globally with a focus on K-12 education and open-source resources, Study GRC Inc. adopts a "highest common denominator" approach to privacy. This Standard ensures compliance with the Texas Data Privacy and Security Act (TDPSA), the General Data Protection Regulation (GDPR) Article 9, and the Children's Online Privacy Protection Act (COPPA). It mitigates the risk of unauthorized data processing and establishes a verifiable audit trail of user consent.

### 2. Scope
This Standard applies to all Study GRC Inc. digital interfaces, paper forms, and third-party data collection tools (e.g., event registration platforms, learning management systems) where Sensitive Data is requested.

**Applies to:**
*   Web forms and mobile applications developed or managed by Study GRC.
*   Third-party vendors (Processors) collecting data on behalf of the Organization.
*   Program registration involving minors.

**Exclusions:**
*   Collection of "Non-Sensitive" data (e.g., business email address, job title) which is governed by the *General Privacy Policy* and standard opt-in procedures.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Sensitive Data** | Information revealing racial or ethnic origin, political opinions, religious beliefs, trade union membership, genetic data, biometric data (for ID purposes), health data, sex life/orientation, precise geolocation, and **any personal data of a known child under 13**. |
| **Explicit Consent** | A voluntary, specific, informed, and unambiguous indication of the data subject's wishes by which they, by a statement or by a clear affirmative action, signify agreement to the processing of personal data relating to them. |
| **Opt-In** | A mechanism where the default state is "off" or "reject," requiring the user to take a deliberate action to enable the feature or collection. |
| **Granularity** | The practice of requesting separate consents for separate types of data processing activities, rather than bundling them into a single "I agree" checkbox. |
| **Verifiable Parental Consent (VPC)** | A method reasonably calculated, in light of available technology, to ensure that the person providing consent for a child is the child's parent or legal guardian (per COPPA). |

### 4. Standards

#### 4.1 Interface and UX Design Requirements
To be considered "Explicit," the consent mechanism must adhere to the following design standards:

1.  **No Pre-Ticked Boxes:** Checkboxes requesting consent for sensitive data **must** be unchecked by default. Pre-ticked boxes, silence, or inactivity do not constitute consent.
2.  **Unbundled Presentation:** Consent for sensitive data processing must be separate from the acceptance of the *Terms of Service* or *General Privacy Policy*.
    *   *Correct:* [ ] I agree to the Terms of Service. [ ] I consent to the processing of my dietary requirements for event catering.
    *   *Incorrect:* [ ] I agree to the Terms, Privacy Policy, and the processing of my health data.
3.  **Granularity:** If multiple types of sensitive data are collected for different purposes, separate checkboxes must be provided.
    *   *Example:* Consent for **Biometric Data** (e.g., facial recognition for secure login) must be separate from consent for **Health Data** (e.g., accessibility accommodations).
4.  **Visual Prominence:** The consent request must be distinct from other text, using a font size and color that ensures readability. It cannot be buried in a scrollable text block without a forced stop.

#### 4.2 Language and Content Requirements
The text accompanying the consent mechanism must be written in "Plain English" (targeting a reading level appropriate for the audience, generally 8th grade) and must include:

1.  **Specific Data Points:** Clearly state exactly what sensitive data is being collected (e.g., "We are asking for your racial/ethnic origin...").
2.  **Specific Purpose:** Clearly state why the data is needed (e.g., "...for the purpose of monitoring diversity within our scholarship program.").
3.  **Withdrawal Right:** A statement informing the user that they can withdraw consent at any time (e.g., "You may revoke this consent at any time via your account settings.").
4.  **Third-Party Sharing:** If the data will be shared with external partners, this must be explicitly stated.

#### 4.3 Technical Implementation and Audit Trail
For every instance of Explicit Consent obtained, the system must generate an immutable audit log containing:

1.  **User Identifier:** User ID, Email, or Session ID.
2.  **Timestamp:** Date and time (UTC) the consent was given.
3.  **Consent Version:** A reference to the specific version of the consent language/form presented to the user at that time.
4.  **Method:** The specific action taken (e.g., "Checkbox_Click", "Digital_Signature").
5.  **IP Address:** The IP address from which the consent was registered (subject to data minimization policies).

#### 4.4 Special Requirement: Children (Under 13)
Pursuant to the *Child and Youth Safeguarding Policy* and COPPA:

1.  **Strict Prohibition:** Sensitive data regarding children under 13 must not be collected via standard web forms.
2.  **Verifiable Parental Consent (VPC):** If sensitive data is required for a specific program (e.g., allergies for a youth camp), it must be collected via a VPC flow that includes a "Plus" method (e.g., credit card verification, video conference, or signed digital form) before the data is processed.

#### 4.5 Withdrawal of Consent
The mechanism to withdraw consent must be as easy as the mechanism to give it.
1.  **User Interface:** Users must be able to toggle "Off" the consent in their Account Settings or Privacy Dashboard.
2.  **Effect:** Upon withdrawal, the system must immediately cease processing the sensitive data and trigger the *Data Retention and Destruction Policy* to remove the data, unless a legal obligation requires retention.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Product Owners / Developers** | Ensure all web forms and app interfaces implement the "No Pre-Tick" and "Granularity" standards defined in Section 4.1. |
| **Data Protection Officer (DPO)** | Review and approve the specific wording of all consent notices (Section 4.2) prior to deployment. |
| **Chief Information Security Officer (CISO)** | Verify that the audit trail (Section 4.3) is logging correctly and is protected from tampering. |
| **Director of Kindness (DKG)** | Ensure community managers do not solicit sensitive data via informal channels (e.g., Slack/Discord) where explicit consent cannot be logged. |

### 6. Compliance and Enforcement
Failure to comply with this Standard puts Study GRC Inc. at risk of significant legal penalties under GDPR (up to 4% of global revenue) and the Texas Data Privacy and Security Act.

**Enforcement:**
*   **Technical:** Non-compliant forms will be blocked from deployment by the Change Advisory Board (CAB).
*   **Personnel:** Employees or volunteers found bypassing consent mechanisms to collect sensitive data will face disciplinary action, up to and including termination and legal action.

### 7. References
*   **Bylaws of Study GRC Inc.** (Article IX: Policies & Data Protection)
*   **Texas Data Privacy and Security Act (TDPSA)**
*   **General Data Protection Regulation (GDPR)** - Articles 7 & 9
*   **Children's Online Privacy Protection Act (COPPA)**
*   **GOV-POL-030:** Master Data Privacy Policy
*   **IS-STD-028:** Data Classification Standard

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Compliance Architect | Initial Release aligned with TDPSA and GDPR requirements. |