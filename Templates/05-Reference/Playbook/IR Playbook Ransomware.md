### IR Playbook: Ransomware

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PBK-002 |
| **Document Type** | Playbook / Standard Operating Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-04-27 (Bi-Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Incident Response Team Lead |
| **Classification** | **Internal / Confidential** |

### 1. Purpose
The purpose of this Playbook is to define the specific operational procedures for detecting, containing, eradicating, and recovering from a ransomware attack against Study GRC Inc. This document aligns with **CISA (Cybersecurity & Infrastructure Security Agency)** guidance and **NIST SP 800-61r2**. Its primary goals are to minimize operational downtime, protect the privacy of member and youth data, preserve forensic evidence for law enforcement, and strictly govern the decision-making process regarding ransom demands.

### 2. Scope
This playbook applies to all Study GRC Inc. information systems, networks, endpoints (including remote work devices connected to organizational resources), and cloud environments (SaaS/IaaS).

**Applies to:**
*   Incident Response Team (IRT)
*   Executive Leadership Team (ELT)
*   Board of Directors (regarding financial authorization)
*   All employees, contractors, and volunteers.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Ransomware** | A type of malicious software that encrypts a victim's data and demands payment for the decryption key. |
| **Double Extortion** | A tactic where attackers exfiltrate (steal) sensitive data prior to encryption, threatening to release it publicly if the ransom is not paid. |
| **OOB (Out-of-Band)** | Communication methods that do not rely on the organization's potentially compromised infrastructure (e.g., Signal, personal cell phones, external email). |
| **Air Gap** | A security measure that involves isolating a computer or network and preventing it from establishing an external connection. |
| **OFAC** | Office of Foreign Assets Control. Paying ransom to sanctioned entities is a violation of federal law. |

### 4. Procedures

#### 4.1 Phase 1: Detection and Analysis
* **4.1.1 Indicators of Compromise (IoCs):**
    *   Inability to access files or systems.
    *   Files renamed with unusual extensions (e.g., `.locked`, `.crypt`).
    *   "Ransom Note" text files or desktop backgrounds appearing.
    *   Unexpected high CPU/Disk usage or network traffic.
    *   Disabled antivirus or security logging services.
* **4.1.2 Verification:**
    *   The Service Desk or discovering user must immediately report the anomaly to the CISO via the **Emergency Hotline** or **OOB Communication Channel**.
    *   **DO NOT** communicate about the incident via internal email or Slack/Teams until the channel is verified secure.
* **4.1.3 Classification:**
    *   The CISO shall classify the incident severity. Confirmed ransomware is automatically classified as **Critical (Severity Level 1)**.

#### 4.2 Phase 2: Containment (Immediate Action)
* **4.2.1 Isolation (The "Stop the Bleed" Step):**
    *   **Disconnect:** Immediately disconnect infected devices from the network (Wi-Fi, Ethernet, VPN).
    *   **Power State:** **DO NOT** power off the device unless encryption is actively observed and cannot be stopped otherwise. Powering off destroys RAM evidence. If necessary, use **Hibernate**.
* **4.2.2 Network Segmentation:**
    *   IT Operations must isolate the affected VLANs or subnets to prevent lateral movement.
    *   Disable all VPN connections to the corporate network immediately.
* **4.2.3 Account Lockdown:**
    *   Reset passwords for all accounts associated with the infected systems.
    *   Force a global reset of all Domain Admin and Privileged User credentials.
    *   Disable the compromised user account in the Identity Provider (IdP).

#### 4.3 Phase 3: Investigation and Forensics
* **4.3.1 Evidence Preservation:**
    *   Create a forensic image of the affected system(s) *before* attempting any restoration.
    *   Preserve firewall logs, VPN logs, and cloud audit logs (Office 365/Google Workspace) to determine the entry point.
* **4.3.2 Determine Scope:**
    *   Identify "Patient Zero" (initial point of entry).
    *   Determine if data was exfiltrated (Double Extortion check). *Note: This triggers specific notification obligations under Texas Business & Commerce Code § 521.053.*
* **4.3.3 Threat Identification:**
    *   Identify the ransomware variant. Use resources like **ID Ransomware** or **No More Ransom Project** (on a secure, non-connected device).
    *   **DO NOT** input sensitive data into public decryption tools.

#### 4.4 Phase 4: Eradication
* **4.4.1 Root Cause Remediation:**
    *   Patch the vulnerability exploited (e.g., RDP exposure, unpatched software, phishing credential theft).
    *   Remove malicious artifacts, backdoors, and persistence mechanisms (Registry keys, Scheduled Tasks).
* **4.4.2 Sanitization:**
    *   Infected systems should generally be considered untrusted. The standard procedure is to **wipe and re-image** from a known clean "Gold Image."

#### 4.5 Phase 5: The Ransom Decision
* **4.5.1 Policy Position:**
    *   Study GRC Inc. generally **DOES NOT** pay ransoms. Paying does not guarantee data recovery and encourages further criminal activity.
* **4.5.2 Decision Authority:**
    *   Any deviation from the "No Pay" position requires a unanimous vote by the **Executive Director**, **CISO**, and **Legal Counsel**, with notification to the **Board of Directors**.
* **4.5.3 OFAC Check:**
    *   Before even considering payment, Legal Counsel must verify the attacker's wallet address against the **OFAC Sanctions List**. Payment to sanctioned entities is strictly prohibited.

#### 4.6 Phase 6: Recovery
* **4.6.1 Restoration Priority:**
    1.  Critical Infrastructure (Identity Management, Security Tools).
    2.  Business Critical Applications (Finance, Donor Management).
    3.  User Endpoints.
* **4.6.2 Backup Verification:**
    *   Verify that backups are clean and were not encrypted or infected prior to restoration. Scan backups with updated anti-malware signatures before restoring.
* **4.6.3 Staged Restoration:**
    *   Restore systems in isolated network segments.
    *   Monitor for signs of reinfection for at least 24 hours before reconnecting to the main network.

#### 4.7 Phase 7: Notification and Reporting
* **4.7.1 Regulatory Reporting:**
    *   **CISA:** Report the incident to CISA via `us-cert.cisa.gov` or local FBI field office (required for Federal Grant compliance/best practice).
    *   **Texas Attorney General:** If >250 Texas residents are affected by a data breach.
* **4.7.2 Stakeholder Communication:**
    *   The **Executive Director** handles all external communications.
    *   Draft notifications to donors/members if data exfiltration is confirmed, in consultation with Legal Counsel.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Incident Commander (CISO)** | Directs the technical response, authorizes containment measures, and serves as the primary liaison to the Executive Director. |
| **IT Operations** | Executes technical containment (isolation), forensic imaging, and system restoration from backups. |
| **Legal Counsel** | Advises on notification laws (Texas/GDPR), OFAC compliance, and engages external forensics (if needed) to maintain attorney-client privilege. |
| **Executive Director (CEO)** | Manages internal/external communications; authorizes resource allocation for recovery; updates the Board. |
| **Board of Directors** | Provides fiduciary oversight; informed of major financial impacts or risks to the organization's existence. |
| **Employees/Volunteers** | Immediately report suspicious activity; stop using infected devices; wait for instructions via OOB channels. |

### 6. Compliance and Enforcement
Failure to follow this playbook, particularly regarding the preservation of evidence or unauthorized communication with threat actors, may result in disciplinary action up to and including termination.

**Federal Sanctions Warning:** Facilitating a ransom payment to a sanctioned entity/individual without a license from OFAC may subject the Organization and individuals to substantial civil and criminal penalties.

### 7. References
*   **CISA Ransomware Guide (Sept 2020)**
*   **NIST SP 800-61r2 (Computer Security Incident Handling Guide)**
*   **IS-POL-001 Master Information Security Policy**
*   **IS-POL-005 Backup and Recovery Policy**
*   **Texas Business & Commerce Code § 521.053 (Notification Required Following Breach)**

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | CISO | Initial Draft based on CISA Guidance |