### Ransomware Defense/Recovery Strategy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-060 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this policy is to establish a comprehensive strategy to prevent, detect, respond to, and recover from ransomware attacks targeting Study GRC Inc. Given the Organization’s remote-first structure and reliance on digital platforms for educational delivery, ransomware poses an existential threat to operations and reputation.

This strategy aligns with **FBI guidance** discouraging ransom payments and emphasizes resilience through immutable backups and rapid recovery capabilities. It fulfills the Board’s fiduciary duty under **Bylaws Article III** to manage the affairs of the Organization prudently and protects assets required for federal grant compliance (2 CFR 200).

### 2. Scope
This policy applies to:
*   **Personnel:** All employees, Board members, contractors, and volunteers.
*   **Assets:** All Organization-owned devices, Bring Your Own Device (BYOD) endpoints used for Organization business, cloud environments (e.g., Google Workspace, AWS, Azure), and on-premise servers (if any).
*   **Data:** All proprietary, member, and financial data held by the Organization.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Ransomware** | Malicious software that encrypts data and demands payment for the decryption key. |
| **Double Extortion** | A tactic where attackers exfiltrate (steal) sensitive data prior to encryption, threatening to release it publicly if the ransom is not paid. |
| **Immutable Backup** | A backup file that cannot be altered, deleted, or overwritten, even by an administrator, for a set period. |
| **Air-Gapped** | A security measure where a computer or network is physically or logically isolated from unsecured networks (like the public internet). |
| **OFAC** | Office of Foreign Assets Control. A US Treasury agency that enforces economic and trade sanctions. Paying ransom to sanctioned entities is a violation of federal law. |
| **RTO (Recovery Time Objective)** | The targeted duration of time and a service level within which a business process must be restored after a disaster. |

### 4. Policy Statements

#### 4.1 Defense and Prevention (The Shield)
To minimize the attack surface in a remote-first environment, the Organization mandates the following controls:

1.  **Multi-Factor Authentication (MFA):** MFA is mandatory for all remote access, email, and cloud service accounts. No exceptions.
2.  **Endpoint Detection and Response (EDR):** All devices accessing Organization data must have the approved EDR agent installed and active.
3.  **RDP/VPN Restrictions:** Remote Desktop Protocol (RDP) must never be exposed directly to the internet. Access to internal resources must be mediated through a VPN or Zero Trust Network Access (ZTNA) solution requiring MFA.
4.  **Least Privilege:** Users shall operate with standard user privileges. Local Administrator rights are restricted to IT personnel and granted only via a Just-In-Time (JIT) access protocol.
5.  **Phishing Resilience:** The Organization will conduct continuous phishing simulation training. Repeated failures by personnel will trigger mandatory remedial training.

#### 4.2 Data Protection and Backups (The Safety Net)
Recovery without payment is the primary strategic objective.
1.  **3-2-1 Backup Rule:** The Organization shall maintain three copies of data, on two different media types, with one copy off-site (cloud).
2.  **Immutability:** Critical backups (financials, member databases, grant records) must be stored in an **immutable** state (WORM - Write Once, Read Many) to prevent encryption by ransomware spreading through the network.
3.  **Backup Isolation:** Backup management consoles must be segmented from the general corporate network and require separate, non-domain credentials for access.
4.  **Restoration Testing:** The CISO must validate backup integrity through a full restoration test at least **quarterly**.

#### 4.3 Response and Containment
Upon detection of a potential ransomware infection:
1.  **Disconnect, Do Not Power Off:** Affected users must immediately disconnect the device from the network (Wi-Fi/Ethernet) but **must not** power off the device, to preserve RAM for forensic analysis.
2.  **Isolate Operations:** The Incident Response Team (IRT) is authorized to sever connections to shared drives, cloud repositories, and email servers immediately to prevent lateral movement.
3.  **Out-of-Band Communication:** The IRT will move communication to a pre-designated out-of-band channel (e.g., Signal, personal cell phones) assuming corporate email is compromised.

#### 4.4 Ransom Payment Position
**Study GRC Inc. adopts a position of NON-PAYMENT.**

1.  **FBI Alignment:** In accordance with FBI guidance, the Organization generally will not pay ransoms. Payment encourages criminal activity and does not guarantee data recovery.
2.  **Sanctions Compliance (OFAC):** The Organization will not facilitate payments to individuals or entities on the Specially Designated Nationals and Blocked Persons List (SDN List). Doing so is a violation of US law.
3.  **Board Authority:** The authority to authorize a ransom payment rests **solely** with the Board of Directors.
    *   **Exception Criteria:** Payment may only be considered in extreme scenarios where there is an imminent threat to life or safety, or where the permanent loss of data would result in the immediate dissolution of the Organization.
    *   **Legal Review:** No payment may be authorized without a written opinion from Legal Counsel confirming that the payee is not a sanctioned entity.

#### 4.5 Reporting and Notification
1.  **Law Enforcement:** All confirmed ransomware incidents must be reported to the **FBI Internet Crime Complaint Center (IC3)** and the local FBI Field Office immediately.
2.  **CISA:** Incidents will be reported to the Cybersecurity and Infrastructure Security Agency (CISA) via the central reporting portal.
3.  **Grantors:** If the incident impacts federal grant funds or data, the CISO and CFO must notify the relevant Federal Awarding Agency within the timeframe specified in the grant terms (typically 24-72 hours).
4.  **Data Breach:** If data exfiltration (Double Extortion) is suspected, the Organization will trigger the *Data Breach Notification Procedure* to comply with Texas Business & Commerce Code § 521.053.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Board of Directors** | Sole authority to approve/deny ransom negotiations or payments. Reviews post-incident reports. |
| **Executive Director (CEO)** | Communicates with the Board and external stakeholders (media/partners). Activates the Crisis Communication Plan. |
| **CISO** | Operational commander of the incident. Manages containment, eradication, and recovery. Liaises with FBI/CISA. |
| **Legal Counsel** | Advises on OFAC compliance, liability, and regulatory notification obligations. |
| **CFO** | Assesses financial impact. If payment is authorized (rare), manages the cryptocurrency transaction mechanics. |
| **All Staff/Volunteers** | Responsible for immediately reporting suspicious behavior and disconnecting infected devices. |

### 6. Compliance and Enforcement
Failure to adhere to the preventative measures in this policy (e.g., disabling MFA, bypassing EDR) constitutes a serious violation of the Organization's security standards.

*   **Disciplinary Action:** Violations may result in disciplinary action, up to and including termination of employment or volunteer assignment.
*   **Unauthorized Payment:** Any employee or officer who negotiates or pays a ransom without explicit Board authorization may be personally liable for financial losses and subject to immediate termination and legal prosecution.

### 7. References
*   **FBI CISO Academy Guide:** Ransomware Prevention and Response.
*   **OFAC Advisory:** Potential Sanctions Risks for Facilitating Ransomware Payments (Sept 2021).
*   **NIST SP 800-61 Rev. 2:** Computer Security Incident Handling Guide.
*   **Study GRC Bylaws:** Article III (Board Powers).
*   **Internal Policy:** IS-POL-045 (Incident Response Plan).
*   **Internal Policy:** IS-POL-058 (Backup Policy and Procedures).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Legal Officer | Initial Draft based on FBI and OFAC guidance. |