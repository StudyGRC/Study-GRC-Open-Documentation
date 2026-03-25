### Breach Assessment/Documentation Form

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-FRM-005 |
| **Document Type** | Form / Record |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Incident Response Team Lead |
| **Classification** | **Confidential / Attorney-Client Privileged** (When utilized) |

### 1. Purpose
The purpose of this **Breach Assessment/Documentation Form** is to serve as the official record for the evaluation of security incidents affecting Study GRC Inc. This document guides the Incident Response Team (IRT) through the legal and regulatory analysis required to determine if a security "incident" rises to the level of a reportable "breach" under applicable laws (including Texas Business & Commerce Code § 521.053, GDPR Art. 33/34, and 2 CFR 200).

Completion of this form is mandatory for any incident involving the potential compromise of Sensitive Personal Information (SPI), Youth Data, or Confidential Intellectual Property. It serves as the primary evidence of due diligence and decision-making for the Organization’s "Breach Register."

### 2. Scope
This form applies to all information systems, networks, and data repositories owned, operated, or leased by Study GRC Inc. It must be utilized by the Incident Commander, CISO, or designated Privacy Officer upon the confirmation of a security incident.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Incident** | An occurrence that actually or potentially jeopardizes the confidentiality, integrity, or availability of an information system or the information the system processes, stores, or transmits. |
| **Breach (Texas)** | Unauthorized **acquisition** of computerized data that compromises the security, confidentiality, or integrity of sensitive personal information (TX Bus. & Com. Code § 521.053). |
| **Personal Data Breach (GDPR)** | A breach of security leading to the accidental or unlawful destruction, loss, alteration, unauthorized disclosure of, or access to, personal data transmitted, stored, or otherwise processed. |
| **SPI (Sensitive Personal Info)** | An individual’s first name/initial and last name in combination with: SSN, Driver’s License Number, or Financial Account Number (with credentials). |
| **Youth Data** | Any data pertaining to individuals under the age of 18, subject to enhanced protections under COPPA and the Organization's *Child and Youth Safeguarding Policy*. |

### 4. Breach Assessment Form

*Note: This section constitutes the template to be filled out during an incident.*

#### PART I: INCIDENT TRIAGE & TIMELINE

| Field | Entry |
| :--- | :--- |
| **Incident ID** | [e.g., INC-2024-001] |
| **Incident Commander** | [Name] |
| **Date/Time Incident Occurred** | [YYYY-MM-DD HH:MM] |
| **Date/Time Incident Discovered** | [YYYY-MM-DD HH:MM] |
| **Discovery Method** | [ ] SIEM Alert [ ] User Report [ ] 3rd Party Notification [ ] Audit |
| **72-Hour Notification Deadline** | [Calculated Date/Time for GDPR/Regulators] |

#### PART II: NATURE OF THE INCIDENT

**Description of Event:**
[Provide a detailed narrative of what occurred. Example: "Ransomware attack on Finance Server" or "Lost laptop containing donor list."]

**Attack Vector (Select all that apply):**
*   [ ] Phishing / Social Engineering
*   [ ] Malware / Ransomware
*   [ ] Unpatched Vulnerability / Exploit
*   [ ] Insider Threat (Malicious or Accidental)
*   [ ] Physical Theft / Loss of Device
*   [ ] Vendor / Supply Chain Compromise
*   [ ] Misconfiguration (e.g., Open S3 Bucket)

#### PART III: DATA IMPACT ANALYSIS

**Data Categories Involved:**
*   [ ] **Member Data:** Names, Emails, Addresses.
*   [ ] **SPI (Texas):** SSN, Driver's License, Govt ID.
*   [ ] **Financial:** Credit Card Numbers, Bank Accounts.
*   [ ] **Youth Data:** Information on minors (High Risk).
*   [ ] **Employee Data:** HR records, Health info, Payroll.
*   [ ] **Credentials:** Passwords, API Keys, Private Keys.
*   [ ] **Intellectual Property:** Unpublished curriculum, code signing keys.

**Volume of Records:**
*   Estimated number of individuals impacted: [Number]
*   Number of Texas residents impacted: [Number]
*   Number of EU/EEA residents impacted: [Number]

**Status of Data (Crucial for "Safe Harbor"):**
*   [ ] **Encrypted:** Was the data encrypted at rest/transit?
    *   *If Yes:* Was the encryption key also compromised? [ ] Yes [ ] No
*   [ ] **Redacted/Anonymized:** Was the data readable?
*   [ ] **Publicly Available:** Is this data already public?

#### PART IV: RISK OF HARM ASSESSMENT (Legal Test)

*Evaluate the likelihood that the incident will result in physical, material, or non-material damage to natural persons.*

**1. Unauthorized Acquisition vs. Access:**
*   Is there evidence that data was exfiltrated (downloaded/stolen)? [ ] Yes [ ] No [ ] Unknown
*   Or was it only accessed (viewed)? [ ] Yes [ ] No [ ] Unknown

**2. Risk Factors:**
*   Can the data be used for identity theft or fraud? [ ] High [ ] Medium [ ] Low
*   Is there a risk of physical harm (e.g., location data of at-risk youth)? [ ] Yes [ ] No
*   Is there a risk of reputational damage or humiliation to the data subjects? [ ] Yes [ ] No

**3. Assessment Conclusion:**
Based on the facts above, does this incident create a "Risk of Harm" (Texas) or "Risk to Rights and Freedoms" (GDPR)?
*   [ ] **NO RISK:** Data was encrypted/unusable, or no exfiltration occurred.
*   [ ] **LOW RISK:** Unlikely to result in harm.
*   [ ] **HIGH RISK:** Notification is likely required.

#### PART V: NOTIFICATION DETERMINATION

*Based on the assessment in Part IV, indicate required notifications.*

| Stakeholder | Required? | Deadline | Rationale / Citation |
| :--- | :--- | :--- | :--- |
| **Board of Directors** | [ ] Yes [ ] No | Immediate | Bylaws Art. III (Fiduciary Duty) |
| **Affected Individuals** | [ ] Yes [ ] No | Asap / 60 Days | TX Bus. & Com. § 521.053(b) |
| **Texas Attorney General** | [ ] Yes [ ] No | 60 Days | Required if >250 TX residents impacted. |
| **GDPR Supervisory Auth.** | [ ] Yes [ ] No | 72 Hours | GDPR Art. 33 |
| **Federal Grantor** | [ ] Yes [ ] No | Per Contract | 2 CFR 200 / Grant Agreement |
| **Cyber Insurance Carrier** | [ ] Yes [ ] No | Per Policy | Policy Notification Clause |
| **Law Enforcement** | [ ] Yes [ ] No | Discretionary | FBI / Local Police |

#### PART VI: REMEDIATION & CLOSURE

**Immediate Containment Actions Taken:**
[List actions: e.g., "Account disabled," "Firewall rule added," "Device remotely wiped."]

**Root Cause:**
[Briefly describe the underlying failure.]

**Corrective Actions (Long Term):**
[List CAPs: e.g., "Implement MFA," "Update Vendor Risk Policy."]

**Final Sign-Off:**

__________________________________
**Incident Commander Signature**
Date: [YYYY-MM-DD]

__________________________________
**Legal/Privacy Officer Signature**
Date: [YYYY-MM-DD]

---

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Incident Commander** | Responsible for the initial completion of Parts I, II, and III of this form during the active incident. |
| **Privacy Officer / Legal** | Responsible for completing Part IV (Risk Assessment) and Part V (Notification Determination) to ensure legal privilege and accuracy. |
| **CISO** | Reviews the final assessment and ensures technical remediation steps (Part VI) are technically sound. |
| **Executive Director** | Must be briefed on any assessment resulting in a "High Risk" determination or external notification requirement. |

### 6. Compliance and Enforcement
This form is a critical legal record. Falsification of information on this form, or failure to document a known incident, constitutes a violation of the *Code of Ethics* and the *Information Security Policy*. Such violations may result in disciplinary action, up to and including termination.

Information contained within completed forms may be protected by **Attorney-Client Privilege** or **Work Product Doctrine** if prepared in anticipation of litigation. Distribution should be limited strictly to the Incident Response Team and Legal Counsel.

### 7. References
*   **IS-POL-001:** Master Information Security Policy
*   **IS-PLN-001:** Incident Response Plan
*   **GOV-POL-005:** Whistleblower Protection Policy
*   **External:** Texas Business & Commerce Code § 521.053
*   **External:** GDPR Articles 33 & 34

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Legal Officer | Initial Release aligned with Breach Register requirements. |