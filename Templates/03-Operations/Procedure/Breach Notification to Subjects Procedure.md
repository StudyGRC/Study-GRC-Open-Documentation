### Breach Notification to Subjects Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | PRIV-PRC-027 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Executive Director (CEO) |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a standardized, legally compliant process for notifying data subjects (members, learners, volunteers, and employees) in the event of a confirmed data breach involving their Personally Identifiable Information (PII). This procedure ensures Study GRC Inc. complies with Texas Business & Commerce Code § 521.053, GDPR Article 34, and COPPA requirements while maintaining transparency and trust with the community.

### 2. Scope
This procedure applies to all data breaches involving **Sensitive Personal Information (SPI)** or **Personal Data** held by Study GRC Inc., regardless of whether the data is stored on internal servers, cloud environments, or third-party vendor systems.

*   **In Scope:** All incidents confirmed by the Incident Response Team (IRT) to have resulted in unauthorized acquisition of unencrypted sensitive data.
*   **Exclusions:** Security incidents where no data was exfiltrated or where data was fully encrypted with no compromised keys (safe harbor).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Breach of System Security** | Unauthorized acquisition of computerized data that compromises the security, confidentiality, or integrity of sensitive personal information maintained by the Organization. |
| **Sensitive Personal Information (SPI)** | As defined by TX Bus. & Com. Code § 521.002: An individual's name in combination with SSN, Driver’s License number, or financial account information; or medical/health insurance information. |
| **Data Subject** | The identified or identifiable natural person to whom the personal data relates (e.g., a member, student, or donor). |
| **Substitute Notice** | A method of notification used when the cost of providing direct notice is excessive or contact information is insufficient (e.g., website posting + media release). |
| **Unauthorized Acquisition** | Access to data by a person without authorization or exceeding authorization, including employee negligence or external cyberattack. |

### 4. Procedures

#### 4.1 Trigger and Assessment
**4.1.1** This procedure is triggered immediately upon the Incident Response Team (IRT) classifying an incident as a "Confirmed Data Breach" involving SPI.
**4.1.2** The CISO and Legal Counsel must conduct a **Risk of Harm Analysis** to determine:
*   The sensitivity of the data exposed.
*   The likelihood of identity theft, fraud, or physical harm to the subjects.
*   Applicable jurisdictional laws (e.g., Texas Law for TX residents, GDPR for EU residents).

#### 4.2 Timeline Determination
**4.2.1** Notification must be made **without unreasonable delay**.
**4.2.2** **Texas Standard:** Notification must occur no later than **60 days** after the determination that a breach occurred, unless law enforcement requests a delay.
**4.2.3** **GDPR Standard:** If high risk to rights and freedoms exists, notification must occur "without undue delay."
**4.2.4** **Internal SLA:** Study GRC Inc. aims to notify subjects within **30 days** of confirmation to uphold our value of transparency.

#### 4.3 Drafting the Notification
The Director of Kindness and Generosity (DKG), in coordination with Legal Counsel, must draft the notification. The notice **must** be written in plain English and include:

1.  **What Happened:** A brief description of the incident and the date of the breach.
2.  **What Information Was Involved:** Specific categories of data (e.g., "names and email addresses," not "your specific credit card number ending in 1234").
3.  **What We Are Doing:** Actions taken to contain the breach and prevent recurrence (e.g., "resetting passwords," "enhancing encryption").
4.  **What You Can Do:** Steps the subject should take to protect themselves (e.g., "change your password," "monitor credit reports").
5.  **Contact Information:** A toll-free number, email address, or website link for more information.
6.  **State-Specific Rights:** (For US residents) Information on obtaining police reports and placing security freezes on credit files.

#### 4.4 Review and Approval
**4.4.1** The draft notification must be reviewed by the CISO for technical accuracy.
**4.4.2** The draft must be reviewed by Legal Counsel to ensure compliance with TX Bus. & Com. Code § 521.053(d) and other relevant statutes.
**4.4.3** Final approval must be granted by the Executive Director (CEO).

#### 4.5 Delivery of Notification
Notification shall be provided via one of the following methods, in order of preference:

**4.5.1 Written Notice:** via email to the address on file (primary method for a digital-first organization).
*   *Requirement:* The email must be flagged as "High Importance" and clearly titled (e.g., "Notice of Data Security Incident").
*   *Verification:* The IT team must track bounce-backs.

**4.5.2 Postal Mail:** If no email address is available or if required by specific state law, notice will be sent via first-class mail.

**4.5.3 Substitute Notice:** If the cost of providing notice exceeds $250,000, or the number of affected persons exceeds 500,000, or contact info is insufficient, the Organization shall:
*   Post a conspicuous notice on the home page of the Study GRC website for a minimum of 30 days.
*   Notify major statewide media outlets (if applicable).

#### 4.6 Special Handling for Minors (K-12 Context)
**4.6.1** If the data subject is known to be a minor (under 18), notification **must** be addressed to the parent or legal guardian.
**4.6.2** Under COPPA, if a breach exposes persistent identifiers or geolocation data of children under 13, the Organization must contact parents immediately.

#### 4.7 Regulatory Coordination
**4.7.1** If the breach affects more than **250 residents of Texas**, the CISO must notify the Texas Attorney General via the mandated electronic form *before* or *concurrently* with notifying the subjects.
**4.7.2** If the breach involves Federal Grant data, the CISO must notify the awarding agency Grants Officer as per 2 CFR 200 terms.

#### 4.8 Post-Notification Support
**4.8.1** The Organization shall establish a dedicated email alias (e.g., `privacy-response@studygrc.org`) to handle inquiries.
**4.8.2** A FAQ document must be prepared for the support team/volunteers handling inquiries to ensure consistent messaging.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **CISO** | Determines technical scope of breach; validates technical accuracy of notice; manages AG notification. |
| **Legal Counsel** | Reviews notice for regulatory compliance; advises on "Risk of Harm" analysis. |
| **Director of Kindness (DKG)** | Drafts the communication; manages the tone to ensure empathy; handles community inquiries. |
| **Executive Director (CEO)** | Provides final authorization to release the notification. |
| **IT Dept** | Executes the mass email send; generates logs of successful delivery. |

### 6. Compliance and Enforcement
Failure to follow this procedure may result in severe regulatory fines (up to $100 per record per day in Texas; up to 4% of global revenue under GDPR) and significant reputational damage. Employees found to be obstructing the notification process or concealing a breach will be subject to disciplinary action, up to and including termination and legal prosecution.

### 7. References
*   **Texas Business & Commerce Code § 521.053** (Notification Required Following Breach of Security)
*   **GDPR Article 34** (Communication of a personal data breach to the data subject)
*   **COPPA** (Children's Online Privacy Protection Act)
*   **PRIV-POL-001:** Master Data Privacy Policy
*   **IS-PLN-001:** Incident Response Plan (IRP)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Legal Officer | Initial Release |