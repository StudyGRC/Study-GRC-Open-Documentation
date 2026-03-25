### Incident Classification/Severity Matrix

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-046 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Executive Director / CISO |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Standard is to establish a uniform framework for categorizing and prioritizing security, operational, and compliance incidents affecting Study GRC Inc. By defining severity levels based on impact and urgency, this document ensures that resources are allocated effectively to mitigate risks to the Organization’s data, reputation, youth participants, and federal grant compliance status. This Standard directly supports the **Incident Response Plan (IRP)** and satisfies the prioritization requirements of **NIST CSF 2.0 (RS.AN-2)** and **ISO 27001**.

### 2. Scope
This Standard applies to all incidents reported to or detected by Study GRC Inc., including but not limited to:
*   Information Security events (Confidentiality, Integrity, Availability).
*   Data Privacy breaches (GDPR, TDPSA, COPPA).
*   Youth Protection and Safeguarding issues.
*   Physical security and safety incidents.
*   Operational failures affecting critical infrastructure.

**Exclusions:** Routine IT service requests (e.g., password resets, software installation) that do not indicate a security compromise or policy violation are excluded from this matrix.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Incident** | An occurrence that actually or potentially jeopardizes the confidentiality, integrity, or availability of an information system or the information the system processes, stores, or transmits. |
| **Triage** | The process of inspecting a potential incident to determine its nature, severity, and priority. |
| **SLA (Service Level Agreement)** | The maximum allowable time to acknowledge, respond to, and resolve an incident based on its severity. |
| **PII / CUI** | Personally Identifiable Information / Controlled Unclassified Information (relevant to Federal Grants under 2 CFR 200). |
| **Youth Safety Incident** | Any event involving suspected abuse, grooming, or endangerment of a minor participant. |

### 4. Standards

#### 4.1 Severity Levels Defined
All incidents must be classified into one of four severity levels (SEV-1 to SEV-4). Classification is determined by the **highest** impact category triggered (e.g., if an incident is "Low" for Financial impact but "Critical" for Youth Safety, the incident is **SEV-1 Critical**).

#### 4.2 Classification Matrix

| Severity Level | Description | Impact Criteria (Must match at least one) |
| :--- | :--- | :--- |
| **SEV-1 (CRITICAL)** | **Emergency.** Immediate threat to safety, critical data, or existence of the Organization. Requires immediate executive mobilization. | • **Data:** Confirmed exfiltration of Sensitive PII, CUI, or Donor Financial Data (>10 records).<br>• **Ops:** Critical systems (LMS, Website, Voting System) down > 4 hours.<br>• **Youth:** Allegation of abuse/grooming; Law enforcement involvement required.<br>• **Legal:** Violation triggering mandatory breach notification (TDPSA, GDPR) or loss of 501(c)(3) status.<br>• **Financial:** Loss > $10,000 or fraud involving Federal Funds. |
| **SEV-2 (HIGH)** | **Urgent.** Significant threat or compromise. Operations are degraded but not halted. Immediate technical response required. | • **Data:** Unauthorized access to internal systems; suspected (but unconfirmed) data loss.<br>• **Ops:** Critical systems down < 4 hours; Non-critical systems down > 24 hours.<br>• **Youth:** Violation of "Two-Deep Leadership" policy without harm; Code of Conduct breach by Staff/Volunteer.<br>• **Security:** Ransomware detected but contained; Active malware propagation.<br>• **Reputation:** Negative press coverage or viral social media backlash. |
| **SEV-3 (MEDIUM)** | **Warning.** Localized issue or policy violation. No data loss confirmed. Handled during business hours (with urgency). | • **Data:** Lost encrypted device; accidental internal exposure of non-sensitive data.<br>• **Ops:** Intermittent performance issues; Single user outage.<br>• **Security:** Failed phishing campaign; localized malware infection (single endpoint).<br>• **Compliance:** Minor policy violation (e.g., late filing, missed training). |
| **SEV-4 (LOW)** | **Informational.** Routine anomaly or minor deviation. No operational impact. | • **Data:** Spam email; blocked firewall attempts.<br>• **Ops:** Minor bug in open-source resource; typo on website.<br>• **Security:** Vulnerability scan results (Low/Info severity).<br>• **Physical:** Minor facility maintenance issue not affecting safety. |

#### 4.3 Response Service Level Agreements (SLAs)
The Incident Response Team (IRT) must adhere to the following timelines based on the determined severity.

| Severity | Triage & Classification | Initial Response (Containment Start) | Update Frequency (To Stakeholders) | Target Resolution |
| :--- | :--- | :--- | :--- | :--- |
| **SEV-1** | Immediate (< 15 mins) | < 30 Minutes | Every 1 Hour | < 24 Hours (or Continuous Effort) |
| **SEV-2** | < 30 Minutes | < 2 Hours | Every 4 Hours | < 48 Hours |
| **SEV-3** | < 4 Hours | < 1 Business Day | Daily | < 5 Business Days |
| **SEV-4** | < 1 Business Day | < 3 Business Days | Weekly | Next Maintenance Cycle |

#### 4.4 Escalation and Notification Requirements
Pursuant to **Bylaws Article III (Board Governance)** and **Article V (Operational Leadership)**, specific incidents trigger mandatory notifications:

*   **SEV-1 (Critical):**
    *   **Must Notify:** Executive Director, CISO, Legal Counsel, and Board of Directors (President).
    *   **External:** Law Enforcement (if criminal), Regulatory Bodies (if breach), Cyber Insurance Carrier.
    *   **Note:** If the incident involves a "Fundamental Action" trigger (e.g., dissolution risk), the full Voting Membership may eventually require notification per **Bylaws Article X**.

*   **SEV-2 (High):**
    *   **Must Notify:** Executive Director, CISO, Relevant Department Head (e.g., VP of Education).
    *   **External:** Managed Service Providers (if applicable).

*   **SEV-3 (Medium):**
    *   **Must Notify:** CISO, Incident Commander.

*   **SEV-4 (Low):**
    *   **Must Notify:** IT/Security Staff (Logged in ticketing system).

#### 4.5 Re-Classification
Incidents are dynamic. The Incident Commander has the authority to upgrade or downgrade the severity level as new information becomes available.
*   **Upgrade:** If a SEV-3 malware event is found to have exfiltrated data, it must be immediately upgraded to SEV-1.
*   **Downgrade:** If a SEV-1 system outage is identified as a scheduled maintenance error with no malicious intent, it may be downgraded to SEV-3.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **First Responder** | Detects the event and performs initial Triage to propose a preliminary severity level. |
| **Incident Commander** | Validates and formally sets the Severity Level. Authorizes Escalation to SEV-1 or SEV-2. Manages the response according to the SLA. |
| **CISO** | Final authority on Classification disputes. Responsible for reporting SEV-1/SEV-2 incidents to the Executive Director and Board. |
| **Executive Director** | Responsible for authorizing external communications and legal engagement for SEV-1 incidents. |
| **Board of Directors** | Provides oversight for SEV-1 incidents involving significant financial, legal, or reputational risk. |

### 6. Compliance and Enforcement
Failure to correctly classify or escalate incidents in accordance with this Standard, particularly those involving Youth Protection or Data Privacy, constitutes a violation of the Organization's **Professional Ethics** and **Bylaws Article III**.

*   **Internal:** Violations may result in disciplinary action, up to and including termination of employment or removal from the Board/Volunteer role.
*   **External:** Failure to adhere to response timelines for SEV-1 incidents may result in regulatory fines (TDPSA, GDPR) or loss of Federal Grant eligibility (2 CFR 200).

### 7. References
*   **IS-POL-001:** Master Information Security Policy
*   **IS-PLN-002:** Incident Response Plan (IRP)
*   **GOV-POL-009:** Whistleblower Protection Policy
*   **HR-POL-020:** Child and Youth Safeguarding Policy
*   **External:** NIST SP 800-61 Rev. 2 (Computer Security Incident Handling Guide)
*   **External:** Texas Business Organizations Code (TBOC) § 22.221 (General Standards for Directors)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name], CISO | Initial Release aligned with NIST CSF and Bylaws. |