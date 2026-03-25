### Log Management and Retention Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-015 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this policy is to establish the standards for the generation, transmission, storage, analysis, and disposal of information system logs within Study GRC Inc. ("the Organization"). Effective log management is critical for ensuring the confidentiality, integrity, and availability of the Organization's information assets.

This policy is designed to satisfy **NIST SP 800-53 Control AU-2 (Audit Events)** and ensures the Organization can detect unauthorized activity, investigate security incidents, and meet the record-keeping requirements of **2 CFR 200** (Federal Uniform Guidance) and **Article VIII (Records, Transparency & Finance)** of the Organization's Bylaws.

### 2. Scope
This policy applies to all information systems, networks, applications, and cloud services (SaaS, IaaS, PaaS) owned, leased, or operated by Study GRC Inc.

**Inclusions:**
*   Server and workstation operating systems.
*   Network infrastructure (firewalls, routers, VPNs).
*   Identity and Access Management (IAM) systems.
*   Cloud platforms (e.g., AWS, Azure, Google Workspace).
*   Critical applications processing PII, financial data, or youth participant data.

**Exclusions:**
*   Personal devices (BYOD) are excluded from *system-level* logging requirements, but their access to Organizational resources must be logged by the receiving application or gateway.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Audit Log** | A chronological record of system activities, including records of system access and operations performed by a given user or process. |
| **Event** | An observable occurrence in a system or network (e.g., a user logging in, a file being accessed). |
| **SIEM** | Security Information and Event Management; a solution that aggregates and analyzes log data from various sources. |
| **Immutable** | Data that cannot be changed or deleted once written. |
| **PII** | Personally Identifiable Information; data that can identify a specific individual. |
| **NTP** | Network Time Protocol; used to synchronize clocks between computer systems. |

### 4. Policy Statements

#### 4.1. General Logging Requirement (NIST AU-2)
All critical systems and applications must be configured to generate audit logs. The Organization must determine that the information system is capable of auditing the events defined in Section 4.2. Disabling logging mechanisms on production systems without written authorization from the CISO is strictly prohibited.

#### 4.2. Mandatory Loggable Events
At a minimum, the following events must be captured across all in-scope systems:
*   **User Access:** Successful and failed login attempts.
*   **Privilege Escalation:** Use of administrative privileges (e.g., `sudo`, "Run as Administrator").
*   **Account Management:** Creation, modification, or deletion of user accounts and groups.
*   **Data Access:** Access to sensitive data repositories, specifically those containing youth participant data or financial records.
*   **System Changes:** Installation of software, changes to OS configurations, or modification of security settings.
*   **Network Connections:** Inbound and outbound traffic through perimeter firewalls and VPN concentrators.

#### 4.3. Log Content Standards (NIST AU-3)
To ensure logs are actionable for forensic analysis, each log entry must contain, at a minimum:
1.  **Timestamp:** Precise date and time of the event (synchronized via NTP).
2.  **Source:** The IP address, device ID, or system name where the event originated.
3.  **User Identity:** The User ID or account name associated with the event.
4.  **Event Type:** A description of the action (e.g., "File Delete," "Login Failed").
5.  **Outcome:** Success or failure of the event.

#### 4.4. Log Protection and Integrity (NIST AU-9)
Audit information must be protected from unauthorized access, modification, and deletion.
*   **Centralization:** Logs must be forwarded in near real-time to a centralized, secure repository (e.g., SIEM or dedicated log server) separate from the system generating the logs.
*   **Access Control:** Access to audit logs is restricted to the CISO, IT Security staff, and authorized auditors.
*   **Immutability:** Where technically feasible, log archives must be stored in a Write-Once-Read-Many (WORM) format to prevent tampering.

#### 4.5. Time Synchronization (NIST AU-8)
All information systems must synchronize their internal clocks with the Organization’s designated authoritative time source (e.g., a stratum-1 NTP server). This ensures that log entries from different systems can be accurately correlated.

#### 4.6. Log Retention Schedule
Logs must be retained in accordance with the **Records Retention Schedule (GOV-STD-013)** and **2 CFR 200.334**:

| Log Type | Active Storage (Hot) | Archive Storage (Cold) | Total Retention |
| :--- | :--- | :--- | :--- |
| **Security/Audit Logs** | 90 Days | 1 Year | 1 Year + 90 Days |
| **Financial System Logs** | 1 Year | 2 Years | 3 Years |
| **Incident Investigation Logs** | Indefinite (until legal hold release) | N/A | Indefinite |

*   **Hot Storage:** Immediately searchable for analysis.
*   **Cold Storage:** Compressed and stored for compliance; accessible within 48 hours upon request.

#### 4.7. Log Review and Analysis (NIST AU-6)
*   **Automated Review:** The Organization shall employ automated mechanisms (SIEM) to alert security personnel of critical audit events (e.g., repeated failed logins, malware detection) in real-time.
*   **Manual Review:** The CISO or designee must perform a manual review of summary reports for anomalies at least weekly.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Owns this policy; defines log retention requirements; oversees the central logging infrastructure; authorizes exceptions. |
| **System Administrators** | Configure systems to generate required logs; ensure clocks are synchronized; ensure logs are successfully shipping to the central repository. |
| **All Users** | Prohibited from tampering with, deleting, or disabling logging agents on Organization-issued devices. |
| **Audit Committee** | Reviews compliance with this policy annually as part of the internal control framework defined in Bylaws Article VI. |

### 6. Compliance and Enforcement
Failure to comply with this policy may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action depending on the severity of the violation.

Intentional alteration or deletion of audit logs to conceal misconduct is considered a severe violation of the **Board of Directors Code of Ethics and Conduct** and may trigger immediate termination and referral to law enforcement.

### 7. References
*   **NIST SP 800-53 Rev. 5:** Controls AU-2, AU-3, AU-6, AU-8, AU-9.
*   **2 CFR 200.334:** Retention requirements for records (Federal Awards).
*   **Bylaws of Study GRC Inc.:** Article VIII (Records) and Article IX (Data Protection).
*   **IS-POL-001:** Master Information Security Policy.
*   **GOV-STD-013:** Records Retention Schedule.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | CISO | Initial Policy Draft aligned with NIST AU-2. |