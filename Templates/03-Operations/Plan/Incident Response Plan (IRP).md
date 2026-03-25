### Incident Response Plan (IRP)

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PLN-044 |
| **Document Type** | Plan |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Incident Response Plan (IRP) is to establish a comprehensive framework for managing cybersecurity incidents at Study GRC Inc. This plan ensures the Organization can detect, respond to, and recover from security incidents in a manner that minimizes impact on operations, protects the privacy of our community (specifically youth participants and donors), and ensures compliance with Texas state law, Federal grant requirements (2 CFR 200), and CISA guidelines.

This plan operationalizes the security mandate established in **Article V, Section 5.2** of the Bylaws, empowering the Chief Information Security Officer (CISO) to manage the Organization's technology and data privacy defense.

### 2. Scope
This plan applies to:
*   **Assets:** All information systems, networks, data, and accounts owned, leased, or operated by Study GRC Inc., including cloud-based infrastructure (SaaS/IaaS).
*   **Personnel:** All employees, Board Directors, Operational Officers, volunteers, and contractors.
*   **Environment:** Given the Organization's "Remote-First" nature, this scope extends to personal devices (BYOD) used to access organizational data, subject to the BYOD Policy.

**Exclusions:** Minor operational glitches (e.g., a single printer failure) that do not pose a threat to the confidentiality, integrity, or availability of data are considered "Service Requests" and are outside the scope of this IRP.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Event** | Any observable occurrence in a system or network (e.g., a user connecting to a file share, a server receiving a request). |
| **Incident** | An event that actually or potentially jeopardizes the confidentiality, integrity, or availability of an information system or the information the system processes, stores, or transmits. |
| **Breach** | An incident that results in the confirmed unauthorized access, acquisition, or disclosure of sensitive data (PII, donor data, youth records). |
| **IRT** | Incident Response Team: The designated group responsible for executing this plan. |
| **CISA** | Cybersecurity and Infrastructure Security Agency (U.S. Federal Government). |
| **PII** | Personally Identifiable Information. |

### 4. Plan Structure (The CISA Lifecycle)

Study GRC Inc. adopts the CISA and NIST SP 800-61 Rev. 2 incident response lifecycle.

#### 4.1 Phase 1: Preparation
To ensure readiness, the Organization must:
1.  **Tooling:** Maintain centralized logging, endpoint detection (EDR), and secure communication channels (out-of-band signal/phone) distinct from primary organizational email.
2.  **Training:** Conduct annual tabletop exercises for the IRT and Board leadership.
3.  **Roster:** Maintain an up-to-date contact list for the IRT, legal counsel, and cyber liability insurance carriers.

#### 4.2 Phase 2: Detection and Analysis
*   **Reporting:** All personnel must report suspected incidents immediately via the designated secure channel or to `security@studygrc.org`.
*   **Triage:** The CISO or designee will validate the alert to discard false positives.
*   **Classification:** Valid incidents are classified by severity:

| Severity | Description | Example | Response SLA |
| :--- | :--- | :--- | :--- |
| **Low** | Minimal impact; no sensitive data loss. | Phishing email caught by filter; single malware infection on isolated laptop. | 24 Hours |
| **Medium** | Localized impact; potential policy violation. | Lost unencrypted USB drive; suspected account compromise. | 4 Hours |
| **High** | Significant operational impact or sensitive data risk. | Ransomware on non-critical server; active intrusion attempt. | 1 Hour |
| **Critical** | Existential threat; confirmed data breach; youth safety risk. | Domain controller compromise; exfiltration of donor/youth database; public-facing defacement. | Immediate |

#### 4.3 Phase 3: Containment
The IRT must limit the magnitude of the incident.
1.  **Short-Term Containment:** Isolate affected systems immediately (e.g., disconnect from VPN, revoke session tokens, lock user accounts).
2.  **System Backup:** Preserve the state of the system for forensics before any reboot or wipe occurs.
3.  **Long-Term Containment:** Apply patches, update firewall rules, or change administrative credentials to prevent re-entry.

#### 4.4 Phase 4: Eradication
After containment, the IRT must remove the root cause.
1.  **Sanitization:** Re-image affected devices from known good media.
2.  **Remediation:** Remove malicious artifacts (malware, scripts) and close vulnerabilities.
3.  **Validation:** Verify that the threat is eliminated through scanning and monitoring.

#### 4.5 Phase 5: Recovery
Restore systems to normal operation.
1.  **Restoration:** Restore data from clean backups in accordance with the *Backup and Recovery Policy*.
2.  **Monitoring:** Implement heightened monitoring on restored systems for 48 hours to detect persistence.
3.  **Certification:** The CISO declares the incident "Closed" from a technical perspective.

#### 4.6 Phase 6: Post-Incident Activity
1.  **Lessons Learned:** Within 14 days of closure, the IRT must hold a retrospective meeting.
2.  **Report:** A "Post-Incident Report" (PIR) must be generated, detailing what happened, root cause, and recommendations for policy/infrastructure changes.
3.  **Board Reporting:** A summary of High/Critical incidents must be presented to the Board of Directors.

### 5. Communication and Notification Procedures

#### 5.1 Internal Notification
*   **Operational Officers:** The CISO must notify the Executive Director (CEO) immediately upon confirming a High or Critical incident.
*   **Board of Directors:** The CEO must notify the Board President within 24 hours of a Critical incident, pursuant to the transparency goals in **Bylaws Article VIII**.

#### 5.2 External Notification (Legal & Regulatory)
*   **Law Enforcement:** Notification to the FBI or local authorities is determined by the CEO in consultation with Legal Counsel.
*   **CISA Reporting:** As a Federal Grantee, the Organization may be required to report cyber incidents to CISA via `report@cisa.gov` or the CISA Incident Reporting System within established timeframes (typically 72 hours for covered entities).
*   **State Breach Notification:** If PII is compromised, the Organization must comply with **Texas Business & Commerce Code § 521.053**. Notification to affected individuals must occur without unreasonable delay (and no later than 60 days).
*   **Donors/Members:** Communication to the membership base regarding breaches is the sole responsibility of the CEO and Board President.

### 6. Roles and Responsibilities

| Role | Responsibilities |
| :--- | :--- |
| **Incident Response Team (IRT)** | Technical execution of the IRP (Containment, Eradication, Recovery). |
| **CISO (IRT Lead)** | Declares the incident severity; commands the tactical response; approves containment strategies. |
| **Executive Director (CEO)** | Strategic decision-making; approves external communications; authorizes emergency spending. |
| **Legal Counsel** | Advises on regulatory reporting obligations, liability, and evidence preservation. |
| **Board of Directors** | Provides oversight; approves major recovery expenditures; manages reputational risk (per Bylaws Art. III). |
| **All Employees/Volunteers** | Report suspicious activity immediately; comply with IRT instructions during an active incident. |

### 7. Compliance and Enforcement
Failure to follow the reporting procedures outlined in this plan, or intentional interference with an incident investigation, may result in disciplinary action, up to and including termination of employment or volunteer assignment (Bylaws Art. III & V), and potential legal action.

**Regulatory References:**
*   **CISA:** *Federal Government Cybersecurity Incident & Vulnerability Response Playbooks*.
*   **NIST:** *SP 800-61 Rev. 2 (Computer Security Incident Handling Guide)*.
*   **Texas Law:** *Texas Business & Commerce Code Chapter 521*.
*   **Federal Grants:** *2 CFR § 200.303 (Internal Controls)*.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | CISO | Initial Draft based on CISA Playbooks and Bylaws Art. V. |