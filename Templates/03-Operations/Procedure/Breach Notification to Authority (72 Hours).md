### Breach Notification to Authority (72 Hours)

| Document Control | |
| :--- | :--- |
| **Document ID** | DP-PRC-026 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a strict, repeatable protocol for notifying relevant Supervisory Authorities (SAs) of a personal data breach within 72 hours of Study GRC Inc. becoming aware of the incident. This procedure ensures compliance with **Article 33 of the General Data Protection Regulation (GDPR)** and aligns with the Organization's commitment to transparency as outlined in **Article VIII** of the Bylaws.

### 2. Scope
This procedure applies to all suspected or confirmed breaches of Personal Data processed by Study GRC Inc., specifically where the data subjects are residents of the European Union (EU) or European Economic Area (EEA).

**Exclusions:**
*   Security incidents that do not involve Personal Data (e.g., server hardware failure with no data loss).
*   Breaches that are "unlikely to result in a risk to the rights and freedoms of natural persons" (as determined by the Risk Assessment in Section 4.2).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Personal Data Breach** | A breach of security leading to the accidental or unlawful destruction, loss, alteration, unauthorized disclosure of, or access to, personal data transmitted, stored, or otherwise processed. |
| **Supervisory Authority (SA)** | An independent public authority established by an EU Member State pursuant to Article 51 of the GDPR (e.g., the ICO in the UK, the DPC in Ireland). |
| **Awareness** | The moment Study GRC Inc. has a reasonable degree of certainty that a security incident has occurred that compromises personal data. This starts the 72-hour clock. |
| **Rights and Freedoms** | The fundamental rights of individuals, including privacy, freedom from discrimination, and protection against identity theft or fraud. |

### 4. Procedures

#### 4.1. Detection and Clock Initiation
1.  **Immediate Reporting:** Any employee, volunteer, or contractor who suspects a breach must report it immediately via the designated Incident Response channel (e.g., `security@studygrc.org`) per the *Incident Response Plan*.
2.  **Establishing Awareness:** The Chief Information Security Officer (CISO) or their designee must validate the alert.
    *   **The 72-hour clock begins** the moment the CISO determines with reasonable certainty that personal data has been compromised.
    *   *Note:* The clock does not wait for a full forensic investigation to be completed.

#### 4.2. Triage and Risk Assessment (Hours 0–24)
1.  **Incident Classification:** The Incident Response Team (IRT) must classify the breach based on the *Data Classification Standard*.
2.  **Risk Assessment:** The Data Protection Officer (DPO) or Legal Counsel must assess the likelihood of risk to individuals' rights and freedoms.
    *   **High Risk:** Notification is **MANDATORY**. (e.g., Theft of unencrypted database containing names and passwords).
    *   **Low Risk:** Notification is **NOT REQUIRED**, but the incident must be logged internally. (e.g., An encrypted laptop is lost, and the key remains secure).
3.  **Documentation:** If the decision is made *not* to notify, the justification must be documented in the *Breach Register* to satisfy GDPR accountability requirements.

#### 4.3. Drafting the Notification (Hours 24–48)
If the assessment in Section 4.2 indicates a risk to rights and freedoms, the DPO/CISO must draft the notification. Per GDPR Art. 33(3), the notification must include:
1.  **Nature of the Breach:** Describe what happened (e.g., ransomware, accidental publication), the categories of data (e.g., email addresses, financial data), and the approximate number of data subjects concerned.
2.  **Contact Point:** Name and contact details of the DPO or other contact point for more information.
3.  **Consequences:** Describe the likely consequences of the personal data breach (e.g., identity theft, loss of confidentiality).
4.  **Measures Taken:** Describe the measures taken or proposed to be taken by Study GRC Inc. to address the breach, including measures to mitigate its possible adverse effects.

#### 4.4. Review and Approval (Hours 48–60)
1.  **Executive Review:** The Executive Director (CEO) must review the draft notification.
2.  **Legal Review:** External Legal Counsel (if engaged) should review the wording to ensure it does not admit liability beyond factual occurrences.
3.  **Board Notification:** The President of the Board must be briefed on the impending external report, consistent with the Board's oversight role defined in **Bylaws Article III**.

#### 4.5. Submission to Supervisory Authority (Hours 60–72)
1.  **Identify the Lead SA:** Determine the appropriate Supervisory Authority based on the location of the affected data subjects or the nature of the processing.
2.  **Secure Submission:** The DPO/CISO shall submit the notification via the SA’s official secure portal (e.g., ICO Report a Breach portal).
3.  **Confirmation:** Save the submission receipt and reference number in the *Breach Register*.

#### 4.6. Phased Reporting (If Applicable)
If it is not possible to provide all information at the same time:
1.  **Initial Report:** Submit the initial notification within 72 hours with the information available.
2.  **Flagging:** Clearly state in the initial report that this is a "Preliminary Notification" and further details will follow.
3.  **Follow-up:** Provide the remaining information in phases without undue further delay.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **All Staff/Volunteers** | Immediately report suspected incidents to the Security Team. |
| **CISO** | Validates the breach, establishes "Awareness," and leads the technical investigation. |
| **Data Protection Officer (DPO)** | Conducts the Risk Assessment (Rights & Freedoms), drafts the notification, and serves as the liaison with the Supervisory Authority. |
| **Executive Director (CEO)** | Provides final operational approval for the release of the notification. |
| **Board of Directors** | Receives briefing on high-risk breaches; provides governance oversight. |

### 6. Compliance and Enforcement
Failure to comply with this procedure may result in:
*   **Regulatory Fines:** Under GDPR, failure to notify can result in fines up to 10,000,000 EUR or 2% of total worldwide annual turnover.
*   **Disciplinary Action:** Employees or volunteers who knowingly conceal a breach or delay reporting may face termination of employment or volunteer assignment, in accordance with the *Code of Ethics and Conduct*.

### 7. References
*   **GDPR Article 33:** Notification of a personal data breach to the supervisory authority.
*   **Study GRC Inc. Bylaws:** Article VIII (Transparency) and Article V (Operational Leadership).
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-PLN-001:** Incident Response Plan.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Legal Officer | Initial Draft based on GDPR Art. 33 requirements. |