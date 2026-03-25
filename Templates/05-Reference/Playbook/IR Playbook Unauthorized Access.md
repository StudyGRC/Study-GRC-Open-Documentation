### IR Playbook: Unauthorized Access

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PLY-005 |
| **Document Type** | Playbook (Procedure) |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-04-27 (Bi-Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Incident Response Team Lead |
| **Classification** | **Confidential** |

### 1. Purpose
The purpose of this Playbook is to define the standardized, step-by-step response procedures for detecting, containing, analyzing, and remediating incidents involving **Unauthorized Access** to Study GRC Inc. systems, data, or networks.

This document ensures that the Organization minimizes operational disruption, prevents data exfiltration, and strictly adheres to **forensic preservation requirements** necessary for potential legal action, regulatory reporting (Texas Business & Commerce Code § 521.053), and root cause analysis.

### 2. Scope
This Playbook applies to all Information Systems owned, leased, or operated by Study GRC Inc., including but not limited to:
*   **Cloud Infrastructure:** AWS, Azure, or other IaaS/PaaS environments.
*   **SaaS Applications:** Google Workspace, GitHub, Slack, CRM, and Financial Systems.
*   **Endpoints:** Laptops, servers, and mobile devices used for Organization business.
*   **User Accounts:** Employee, volunteer, contractor, and service accounts.

**Exclusions:** This Playbook does not apply to authorized penetration testing activities, provided such activities remain within the scope of the engagement letter and Rules of Engagement (RoE).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Unauthorized Access** | Logical or physical access to a system, application, or data by a user, process, or bot that does not possess the required permission or authorization. |
| **IoC** | **Indicator of Compromise**. Artifacts observed on a network or in an operating system that with high confidence indicate a computer intrusion (e.g., unrecognized IP addresses, impossible travel logins, hash values of malware). |
| **Chain of Custody** | The chronological documentation or paper trail that records the sequence of custody, control, transfer, analysis, and disposition of physical or electronic evidence. |
| **Order of Volatility** | The order in which forensic evidence should be collected based on how easily the data can be lost (e.g., CPU cache > RAM > Swap File > Hard Drive > Logs). |
| **Isolation** | The process of restricting a compromised system's network access to prevent lateral movement while keeping the system powered on for forensic analysis. |

### 4. Procedures

#### 4.1 Phase 1: Identification and Triage
*The goal is to verify if an incident has occurred and determine its severity.*

1.  **Alert Validation:** The First Responder must validate the alert (e.g., SIEM alert, user report, AWS GuardDuty finding).
    *   Check for "Impossible Travel" (login from Texas followed by login from Russia within 1 hour).
    *   Check for privilege escalation attempts.
    *   Verify if the user was performing authorized maintenance.
2.  **Severity Classification:**
    *   **Low:** Failed login attempts; no successful access.
    *   **Medium:** Successful access to non-sensitive system; no data exfiltration suspected.
    *   **High:** Successful access to sensitive data (PII, Financial), Administrator/Root compromise, or lateral movement detected.
3.  **Declaration:** If validated, the Incident Commander declares an Incident and assigns a Ticket ID.

#### 4.2 Phase 2: Containment
*The goal is to stop the attacker's access and prevent lateral movement. **Do not power off systems** unless data destruction is imminent, as this destroys RAM evidence.*

1.  **Account Suspension:**
    *   Immediately suspend (do not delete) the compromised user account(s) in the Identity Provider (e.g., Google Workspace, Active Directory).
    *   Revoke active sessions and API keys.
    *   Reset passwords for the compromised account and any associated service accounts.
2.  **System Isolation (Network Quarantine):**
    *   **Cloud/Server:** Update Security Groups/Firewall rules to block all traffic *except* from the forensic workstation IP.
    *   **Endpoint:** Disconnect the device from the network (Wi-Fi/Ethernet). If remote, use EDR (Endpoint Detection and Response) tools to "Network Isolate" the host.
3.  **Backdoor Check:**
    *   Quickly scan for recently created accounts or modified scheduled tasks that could serve as persistence mechanisms.

#### 4.3 Phase 3: Forensic Preservation (Mandatory)
*This phase is critical for legal and regulatory compliance. Failure to preserve evidence may compromise the Organization's ability to prosecute or defend against liability.*

1.  **Order of Volatility Collection:** Collect evidence in this specific order:
    *   **Memory (RAM):** Capture a full memory dump before any reboot.
    *   **Network Connections:** Capture `netstat` or equivalent active connection logs.
    *   **Running Processes:** Capture list of running processes.
    *   **Disk Image:** Create a bit-for-bit forensic image (e.g., `.E01` format) of the compromised drive/volume.
2.  **Cloud Forensics:**
    *   Snapshot the compromised EBS volume/Virtual Machine.
    *   Export CloudTrail/Audit logs to a Write-Once-Read-Many (WORM) storage bucket (e.g., S3 Object Lock).
3.  **Chain of Custody Documentation:**
    *   Every transfer of data (e.g., "Hard Drive A handed to Analyst B") must be logged on the **Chain of Custody Form**.
    *   Hash values (MD5/SHA-256) of images must be recorded immediately upon creation to prove integrity.
4.  **Legal Hold:**
    *   Notify the Legal Department to issue a **Legal Hold** on all relevant logs, email inboxes, and Slack channels associated with the incident.

#### 4.4 Phase 4: Eradication
*The goal is to remove the root cause and any artifacts left by the attacker.*

1.  **Malware Removal:** Use anti-malware tools to remove identified malicious binaries.
2.  **Vulnerability Remediation:** Patch the vulnerability exploited to gain access (e.g., update unpatched software, fix misconfigured S3 bucket).
3.  **Persistence Removal:** Delete unauthorized accounts, cron jobs, SSH keys, or backdoors identified during analysis.
4.  **Credential Rotation:** Force a password reset for **all** users if the scope of compromise suggests a wider credential harvesting attack.

#### 4.5 Phase 5: Recovery
*The goal is to restore normal operations.*

1.  **System Restoration:**
    *   Re-image compromised endpoints from a known clean "Gold Image."
    *   Restore servers from clean backups created *prior* to the established time of compromise.
2.  **Validation:**
    *   Verify system functionality.
    *   Monitor the system closely (enhanced logging) for 24-48 hours to ensure the attacker does not return.
3.  **Re-enablement:**
    *   Restore network connectivity.
    *   Unlock user accounts after verifying identity via video call or secondary channel.

#### 4.6 Phase 6: Post-Incident Activity
1.  **Documentation:** Compile a Final Incident Report including timeline, root cause, and impact.
2.  **Lessons Learned:** Conduct a "Hot Wash" meeting within 72 hours to discuss what went well and what failed.
3.  **Playbook Update:** Update this Playbook based on gaps identified during the incident.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Incident Commander (IC)** | Overall authority for the incident. Makes the decision to isolate systems. Coordinates with Legal and C-Suite. |
| **First Responder / Analyst** | Performs triage, containment, and technical eradication. Responsible for creating forensic images. |
| **Legal / Compliance** | Determines regulatory notification requirements (e.g., GDPR, TX Law). Issues Legal Holds. Reviews external communications. |
| **IT Systems Admin** | Assists with account suspension, password resets, and restoring backups. |
| **CISO** | Provides strategic oversight. Approves the Final Incident Report. Briefs the Board of Directors if the incident is a "Fundamental Action" or poses existential risk. |

### 6. Compliance and Enforcement
Failure to follow the **Forensic Preservation** steps outlined in Section 4.3 may result in the inadmissibility of evidence in court and potential liability for spoliation of evidence.

Employees found to have facilitated Unauthorized Access (Insider Threat) will be subject to immediate disciplinary action, up to and including termination and referral to law enforcement, in accordance with the **Sanctions Policy** and **Bylaws Article IX (Intellectual Property & Ethics)**.

### 7. References
*   **IS-POL-001:** Master Information Security Policy
*   **IS-PRC-010:** Incident Documentation/Evidence Protocol
*   **IS-FRM-005:** Chain of Custody Form
*   **External:** Texas Business & Commerce Code § 521.053 (Notification of Breach)
*   **External:** NIST SP 800-61 Rev. 2 (Computer Security Incident Handling Guide)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Compliance Architect | Initial Draft created for Board Review. |