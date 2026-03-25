### Incident Detection and Reporting Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-047 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Incident Response Team Lead |
| **Classification** | Public |

### 1. Purpose
The purpose of this procedure is to establish a standardized method for the timely detection, identification, and reporting of Information Security events and incidents within Study GRC Inc. Rapid detection and reporting are critical to minimizing the impact of security breaches, preserving evidence for forensic analysis, and complying with regulatory notification timelines, including Texas Business & Commerce Code § 521.053 and GDPR Article 33. This procedure operationalizes the "Awareness" function of our cybersecurity framework.

### 2. Scope
This procedure applies to:
*   **Personnel:** All employees, Board Directors, Operational Officers, and volunteers.
*   **Third Parties:** Contractors, vendors, and partners with access to Organization systems or data.
*   **Assets:** All information systems, networks, data (including member and youth data), and devices (including BYOD used for Organization business) owned or operated by Study GRC Inc.

**Exclusions:** Routine IT troubleshooting (e.g., printer jams) that does not involve a compromise of data confidentiality, integrity, or availability.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Security Event** | An observable occurrence in a system or network (e.g., a user connecting to a file share, a server receiving a request). |
| **Security Incident** | A violation or imminent threat of violation of computer security policies, acceptable use policies, or standard security practices (e.g., phishing, ransomware, lost laptop). |
| **Reporter** | Any individual who identifies and submits a report regarding a potential security event or incident. |
| **Triage** | The process of categorizing, prioritizing, and assigning an event to determine if it constitutes a genuine Incident. |
| **IRT** | Incident Response Team. |

### 4. Procedures

#### 4.1 Automated Detection
The Organization utilizes technical controls to automatically detect anomalies.
1.  **Log Monitoring:** The CISO and IT staff must configure systems (firewalls, servers, cloud platforms) to generate logs.
2.  **Alerting:** Automated alerts must be configured for high-risk indicators, including but not limited to:
    *   Multiple failed login attempts (Brute Force).
    *   Malware detection by Endpoint Detection and Response (EDR) agents.
    *   Unauthorized privilege escalation.
    *   Data exfiltration signatures.
3.  **Review:** Alerts must be routed to the `security-alerts` channel or ticketing system for daily review by the IRT.

#### 4.2 Human Detection and Reporting (See Something, Say Something)
All personnel are responsible for reporting suspicious activity immediately.

**4.2.1 Reporting Channels**
*   **Primary Method (Email):** Send details to `security@[organization-domain].org`.
*   **Urgent/Critical Method (Slack/Discord):** Post in the private `#security-incident` channel or Direct Message the CISO.
*   **Anonymous Method:** Use the Whistleblower Complaint Intake Form (referencing *Whistleblower Protection Policy*) if the incident involves internal misconduct.

**4.2.2 Reportable Scenarios**
Personnel **must** report the following immediately:
*   **Phishing:** Receipt of suspicious emails, especially those requesting credentials or wire transfers.
*   **Lost/Stolen Devices:** Loss of any laptop, phone, or tablet used to access Organization data (referencing *BYOD Policy*).
*   **Unauthorized Access:** Observing a user accessing data they should not have (e.g., a volunteer accessing donor financial records).
*   **Data Leakage:** Accidental posting of sensitive data (e.g., API keys, PII) to public repositories (GitHub) or public channels.
*   **Youth Safety:** Any digital interaction involving minors that violates the *Child and Youth Safeguarding Policy* (e.g., grooming behavior).

#### 4.3 Triage and Validation
Upon receipt of a report, the Incident Response Team (IRT) must perform the following within **4 hours**:

1.  **Acknowledge:** Confirm receipt of the report to the Reporter (unless anonymous).
2.  **Verify:** Investigate to determine if the event is a False Positive or a True Positive.
3.  **Classify:** Assign a severity level based on the *Incident Classification Matrix*:
    *   *Low:* Phishing attempt blocked; no data loss.
    *   *Medium:* Lost encrypted device; potential localized virus.
    *   *High:* Active ransomware; unencrypted data exfiltration; compromise of Administrator account.
    *   *Critical:* Breach of Youth Data; compromise of production environment; public reputational crisis.
4.  **Escalate:**
    *   **High/Critical** incidents require immediate notification to the CISO and Executive Director.
    *   Incidents involving Youth Protection must be cross-reported to the *Director of Kindness and Generosity (DKG)* immediately.

#### 4.4 Documentation
1.  **Incident Ticket:** A ticket must be created in the IT Service Management tool for every validated incident.
2.  **Chain of Custody:** If the incident involves potential legal action or forensic analysis, the IRT must document the seizure and storage of digital evidence in the *Incident Documentation Form*.

#### 4.5 External Reporting (Safe Harbor)
1.  **Vulnerability Disclosure:** External security researchers may report vulnerabilities via `security@[organization-domain].org`.
2.  **Safe Harbor:** Study GRC Inc. will not pursue legal action against researchers who identify and report vulnerabilities in good faith, provided they adhere to the *Responsible Disclosure Guidelines* and do not exploit the vulnerability for data exfiltration.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **All Personnel** | Responsible for knowing how to identify common threats (phishing) and reporting them immediately via designated channels. |
| **Incident Response Team (IRT)** | Responsible for monitoring alert queues, triaging incoming reports, and validating incidents. |
| **Chief Information Security Officer (CISO)** | Responsible for the overall detection strategy, ensuring tools are functional, and acting as the escalation point for High/Critical incidents. (Per Bylaws Art. V § 5.2). |
| **Director of Kindness & Generosity (DKG)** | Responsible for receiving escalated reports regarding Community Guidelines violations or Youth Protection issues originating from IT incidents. |

### 6. Compliance and Enforcement
**Failure to Report:** Failure by an employee or volunteer to report a known security incident (e.g., losing a device and hiding it) constitutes a violation of the *Code of Ethics* and *Master Information Security Policy*.

**Consequences:** Violations may result in disciplinary action, up to and including termination of employment or volunteer assignment. In cases involving deliberate concealment of data breaches, individuals may face personal civil or criminal liability under Texas Business & Commerce Code § 521.

**Non-Retaliation:** Pursuant to the *Whistleblower Protection Policy*, no individual shall face retaliation for reporting a security concern in good faith.

### 7. References
*   **IS-POL-001:** Master Information Security Policy
*   **IS-PLN-001:** Incident Response Plan (IRP)
*   **GOV-POL-005:** Whistleblower Protection Policy
*   **HR-POL-020:** Child and Youth Safeguarding Policy
*   **External:** Texas Business & Commerce Code § 521.053 (Notification Required Following Breach of Security)
*   **External:** NIST CSF 2.0 (DE.AE: Adverse Events are analyzed)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Legal Officer | Initial Draft aligned with Bylaws and NIST CSF. |