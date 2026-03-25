### Incident Response Team Charter

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-CHR-001 |
| **Document Type** | Charter |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Charter is to establish the **Incident Response Team (IRT)** for Study GRC Inc. (the "Organization"). This Charter defines the IRT’s authority, composition, and responsibilities in managing cybersecurity incidents, data breaches, and significant operational disruptions.

This document ensures the Organization maintains **Accountability** by establishing a clear chain of command and decision-making framework during crises, ensuring compliance with the Texas Business & Commerce Code § 521.053, NIST SP 800-61 Rev. 2, and the Organization’s Bylaws Article V regarding Operational Leadership.

### 2. Scope
This Charter applies to the designated members of the IRT and all personnel (employees, volunteers, contractors) during an active incident declaration.

*   **In Scope:** All Information Technology (IT) assets, data (including Member, Youth, and Donor data), cloud infrastructure, and physical premises owned or leased by the Organization.
*   **Exclusions:** Routine IT troubleshooting or service requests that do not constitute a security threat or policy violation.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Incident** | An occurrence that actually or potentially jeopardizes the confidentiality, integrity, or availability of an information system or the information the system processes, stores, or transmits. |
| **Breach** | An incident that results in the confirmed unauthorized acquisition of sensitive personal information (SPI), requiring legal notification under Texas law or other applicable regulations (e.g., GDPR, COPPA). |
| **Incident Commander (IC)** | The individual responsible for overall management of the incident response, usually the CISO or their designee. |
| **Triage** | The process of categorizing, prioritizing, and assigning events and incidents. |

### 4. Charter Statements

#### 4.1 Mandate and Authority
Pursuant to **Bylaws Article V (Operational Leadership)**, the Board of Directors delegates the following authority to the IRT:
1.  **Emergency Action:** The IRT is authorized to take immediate, unilateral action to contain a threat, including severing network connections, disabling user accounts, shutting down services, or isolating systems, even if such actions result in temporary business interruption.
2.  **Access:** The IRT is granted unrestricted access to all Organization systems, logs, and physical spaces necessary to investigate and remediate an incident.
3.  **Resource Allocation:** The Incident Commander is authorized to reallocate staff time and procure emergency services (e.g., forensics firms, outside counsel) up to the limit defined in the **Delegation of Authority (DoA) Matrix** for emergency procurement.

#### 4.2 Team Composition
The IRT operates on a tiered structure:

**A. Core Team (Permanent Members)**
*   **Incident Commander:** Chief Information Security Officer (CISO).
*   **Legal Lead:** General Counsel (or designated Outside Counsel).
*   **Technical Lead:** Senior IT/DevOps Lead.

**B. Extended Team (Activated as Needed)**
*   **Communications Lead:** Director of Kindness and Generosity (DKG) (Responsible for community/member messaging).
*   **Human Resources:** For insider threats or employee disciplinary actions.
*   **Executive Liaison:** Executive Director (CEO).

#### 4.3 Activation and Severity Levels
The IRT is activated when an event is classified as **Severity Level Medium (Sev-2)** or higher, based on the *Incident Classification Matrix*:
*   **Sev-3 (Low):** Routine malware, failed phishing. Handled by IT Ops; IRT notified via log.
*   **Sev-2 (Medium):** Targeted attack, potential data exposure, or loss of critical service. **IRT Activated.**
*   **Sev-1 (High):** Confirmed data breach (Member/Youth data), ransomware, or total system compromise. **IRT Activated; Board Notified.**

#### 4.4 Decision Making
*   **Operational Decisions:** The Incident Commander has final authority over technical containment and eradication strategies.
*   **Legal/Strategic Decisions:** Decisions regarding external notification (regulators, members, media) or paying ransom demands require consensus between the Incident Commander, Legal Counsel, and the Executive Director, with final ratification by the Board of Directors if the financial impact exceeds the CEO's authority.

#### 4.5 Confidentiality and Privilege
To protect the Organization during potential litigation:
*   All IRT communications regarding Sev-1 incidents must be marked "Privileged and Confidential – Prepared in Anticipation of Litigation."
*   The Legal Lead directs the investigation to maintain Attorney-Client Privilege where applicable.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Incident Commander (CISO)** | Directs all response activities; declares incident severity; authorizes containment measures; serves as the primary liaison to the Executive Director. |
| **Legal Counsel** | Advises on legal obligations (breach notification laws); manages engagement with law enforcement; oversees preservation of evidence (Legal Hold). |
| **Technical Lead** | Executes technical containment, eradication, and recovery; preserves forensic evidence; provides technical analysis to the IC. |
| **Communications Lead (DKG)** | Manages internal and external communications; drafts transparency statements for the community; monitors social media sentiment. |
| **Scribe** | Maintains a chronological log of all decisions, actions, and timestamps during the incident (The "Master Events Log"). |
| **Board of Directors** | Provides strategic oversight for Sev-1 incidents; approves extraordinary expenditures; bears ultimate fiduciary responsibility. |

### 6. Compliance and Enforcement
*   **Cooperation:** All employees and volunteers are required to cooperate fully with IRT investigations. Withholding information or obstructing an investigation is grounds for immediate termination and potential legal action.
*   **Non-Retaliation:** The Organization strictly prohibits retaliation against any individual who reports a security incident in good faith, in accordance with the **Whistleblower Protection Policy**.
*   **Accountability:** The IRT must produce a "Post-Incident Review" (PIR) report within 14 days of incident closure. Failure to implement agreed-upon corrective actions from the PIR may result in disciplinary action for the responsible process owners.

### 7. References
*   **Bylaws of Study GRC Inc.** (Article V - Operational Leadership)
*   **IS-POL-001:** Master Information Security Policy
*   **IS-PLN-001:** Incident Response Plan (IRP)
*   **NIST SP 800-61 Rev. 2:** Computer Security Incident Handling Guide
*   **Texas Business & Commerce Code § 521.053:** Notification Required Following Breach of Security of Computerized Data

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Legal Officer | Initial Charter creation and Board ratification. |