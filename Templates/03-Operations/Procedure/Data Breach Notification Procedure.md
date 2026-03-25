### Data Breach Notification Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-025 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Public |

### 1. Purpose
The purpose of this procedure is to establish the mandatory steps Study GRC Inc. (the "Organization") must take in the event of a confirmed breach of system security. This procedure ensures compliance with **Texas Business & Commerce Code § 521.053**, minimizes harm to affected individuals, and maintains the Organization's commitment to transparency as outlined in **Article IX** of the Bylaws.

### 2. Scope
This procedure applies to:
*   All computerized data owned, licensed, or maintained by the Organization.
*   All employees, volunteers, contractors, and third-party vendors who process data on behalf of the Organization.
*   Incidents involving the unauthorized acquisition of Sensitive Personal Information (SPI).

**Exclusions:** This procedure does not apply to the inadvertent disclosure of internal, non-sensitive operational documents that do not contain SPI (e.g., a draft meeting agenda), though such incidents must still be logged via the *Incident Response Plan*.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Breach of System Security** | The unauthorized acquisition of computerized data that compromises the security, confidentiality, or integrity of sensitive personal information maintained by the Organization. Good faith acquisition by an employee or agent for Organization purposes is not a breach unless the information is used or disclosed unauthorizedly. |
| **Sensitive Personal Information (SPI)** | An individual's first name or first initial and last name in combination with any one or more of the following items, if the name and the items are not encrypted: (1) Social Security number; (2) Driver's license number or government ID number; (3) Account number or credit/debit card number in combination with any required security code, access code, or password that would permit access to an individual's financial account; or (4) Information that identifies an individual and relates to the physical or mental health or condition of the individual, the provision of health care to the individual, or payment for the provision of health care to the individual. |
| **Unauthorized Person** | Any person who does not have the legal right or authorization to access the specific data in question. |
| **Notification Trigger** | The point at which the Organization determines that SPI was, or is reasonably believed to have been, acquired by an unauthorized person. |

### 4. Procedures

#### 4.1 Phase I: Verification and Risk Assessment
Upon the activation of the *Incident Response Plan (IS-PLN-001)*, the Incident Response Team (IRT) must determine if a reportable breach has occurred.

1.  **Confirm Data Type:** The CISO must verify if the compromised data constitutes "Sensitive Personal Information" (SPI) under Texas law or "Personal Data" under applicable privacy regulations (e.g., GDPR, COPPA).
2.  **Determine Acquisition:** The CISO must determine if the data was actually "acquired" or if it is "reasonably believed" to have been acquired. Access alone may constitute acquisition depending on the duration and nature of the incident.
3.  **Encryption Safe Harbor Check:** If the data was encrypted, and the encryption key was **not** compromised, notification is generally not required under Texas law. The CISO must validate the integrity of the encryption keys.
4.  **Harm Analysis:** The IRT must assess the risk of harm to the affected individuals (e.g., risk of identity theft, fraud, or physical harm).

#### 4.2 Phase II: Law Enforcement Coordination
1.  **Consultation:** If the breach involves criminal activity (e.g., ransomware, hacking), the Executive Director and Legal Counsel must determine whether to contact law enforcement (FBI, local police).
2.  **Notification Delay:** Notification to individuals may be delayed **only** if a law enforcement agency determines that the notification will impede a criminal investigation.
3.  **Documentation:** If a delay is requested by law enforcement, the Organization must obtain this request in writing or document the verbal request contemporaneously in the Incident Log.

#### 4.3 Phase III: Notification Determination and Timeline
1.  **Timeline:** Pursuant to **Tex. Bus. & Com. Code § 521.053(b)**, notification must be made **"as quickly as possible"** following the discovery of the breach.
    *   **Internal Goal:** The Organization aims to issue notifications within **30 days** of discovery, barring law enforcement delays.
    *   **Third-Party Data:** If the Organization maintains data for another entity (e.g., a partner non-profit), the Organization must notify that entity **immediately** following discovery.
2.  **Board Notification:** The Executive Director must brief the Board of Directors regarding the breach and the intended notification strategy **prior** to public release, in accordance with **Bylaws Article III**.

#### 4.4 Phase IV: Drafting the Notification
The notification to affected individuals must be written in plain English and include:
1.  **What Happened:** A brief description of the incident and the date of the breach (if known).
2.  **What Information Was Involved:** Specific categories of data (e.g., "Your name and credit card number").
3.  **What We Are Doing:** Actions taken to secure the data and prevent recurrence.
4.  **What You Can Do:** Steps the individual can take to protect themselves (e.g., credit monitoring, changing passwords).
5.  **Contact Information:** A dedicated email address or phone number for inquiries (e.g., `privacy@studygrc.org`).

*Note: If the breach involves minors (under 18), the notification must be directed to the parent or legal guardian.*

#### 4.5 Phase V: Delivery of Notification
Notification must be provided via one of the following methods:
1.  **Written Notice:** Sent via postal mail to the last known address.
2.  **Electronic Notice:** Sent via email, provided the individual has agreed to receive electronic communications and the notice is consistent with 15 U.S.C. Section 7001 (E-Sign Act).
3.  **Substitute Notice:** Permitted **only** if:
    *   The cost of providing notice exceeds $250,000;
    *   The number of affected persons exceeds 500,000; or
    *   The Organization does not have sufficient contact information.
    *   *Substitute Notice Steps:* (1) Email notice to all available addresses; (2) Conspicuous posting on the Organization's website home page; and (3) Notification to major statewide media.

#### 4.6 Phase VI: Regulatory Reporting (Texas Attorney General)
1.  **Threshold:** If the breach involves **more than 250 residents of Texas**, the Organization must notify the Texas Attorney General.
2.  **Submission:** The CISO or Legal Counsel must submit the notification via the Texas Attorney General’s electronic breach reporting form.
3.  **Deadline:** This report must be submitted no later than **60 days** after the date the determination is made that the breach occurred.
4.  **Content:** The report must detail the nature of the breach, the number of affected residents, and measures taken regarding the breach.

#### 4.7 Phase VII: Credit Reporting Agencies
If the breach involves more than **10,000 persons**, the Organization must notify all consumer reporting agencies (Equifax, Experian, TransUnion) without unreasonable delay. This notification must include the timing, distribution, and content of the notices sent to individuals.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Executive Director (CEO)** | Final approval authority for all external communications and regulatory filings. Responsible for notifying the Board of Directors. |
| **Chief Information Security Officer (CISO)** | Leads the forensic investigation, determines the scope of the breach, and manages the technical remediation. Prepares the technical details for the notification. |
| **Legal Counsel** | Reviews notification drafts for legal compliance with Texas law and other applicable jurisdictions. Advises on law enforcement interaction. |
| **Director of Kindness (DKG)** | Manages the "Member Support" aspect, ensuring inquiries from affected members are handled with empathy and accuracy. |
| **Board of Directors** | Provides oversight and ensures the Organization has sufficient resources to manage the breach response. |

### 6. Compliance and Enforcement
Failure to comply with this procedure may result in:
*   **Internal:** Disciplinary action up to and including termination of employment or volunteer assignment.
*   **External:** Civil penalties under **Tex. Bus. & Com. Code § 521.151**, which allows for penalties of up to **$100 per record per day** of delayed notification, not to exceed $250,000 per breach, plus reasonable attorney's fees and injunctive relief.

### 7. References
*   **Texas Business & Commerce Code § 521.053** (Notification Required Following Breach of Security of Computerized Data)
*   **Texas Business & Commerce Code § 521.151** (Civil Penalty; Injunction)
*   **Bylaws of Study GRC Inc.** (Article IX - Policies & Data Protection)
*   **IS-PLN-001** Incident Response Plan
*   **IS-POL-001** Master Information Security Policy

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Legal Officer | Initial Draft based on Texas Bus. & Com. Code § 521.053 |