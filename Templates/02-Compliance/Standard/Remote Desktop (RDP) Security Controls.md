### Remote Desktop (RDP) Security Controls

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-027 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Standard is to define the mandatory configuration and usage requirements for Remote Desktop Protocol (RDP) within Study GRC Inc. RDP is a primary attack vector for ransomware and unauthorized access. As a remote-first organization, securing remote administrative access is critical to maintaining the integrity of our systems and protecting the data entrusted to us by our community and donors.

This Standard supports the data protection mandates outlined in **Bylaws Article IX, Section 9.2 (Confidentiality)** and aligns with the Board’s fiduciary duty to mitigate operational risk.

### 2. Scope
This Standard applies to all:
1.  **Assets:** Servers, workstations, virtual machines (VMs), and cloud instances (AWS, Azure, GCP) owned, leased, or managed by Study GRC Inc.
2.  **Personnel:** Employees, contractors, volunteers, and third-party vendors requiring remote administrative access.

**Exclusions:**
*   Third-party SaaS applications where the underlying Operating System (OS) is not managed by Study GRC Inc.
*   Consumer-grade remote support tools (e.g., TeamViewer, Zoom Remote Control) are governed separately under the *Remote Access Policy*.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **RDP (Remote Desktop Protocol)** | A proprietary protocol developed by Microsoft (Port 3389) that provides a user with a graphical interface to connect to another computer over a network connection. |
| **NLA (Network Level Authentication)** | A security feature that requires the connecting user to authenticate themselves to the network before a session is established with the server. |
| **Bastion Host / Jump Box** | A special-purpose computer on a network specifically designed and configured to withstand attacks, used as the single point of entry to the internal network. |
| **Tunneling** | The process of encapsulating RDP traffic within a secure protocol (such as SSH or VPN) to protect it from interception or direct exposure. |

### 4. Standards

#### 4.1 Network Exposure and Connectivity
To prevent ransomware scanning and brute-force attacks, the following network controls are mandatory:

*   **4.1.1 Direct Internet Exposure Prohibited:** RDP (TCP/UDP Port 3389) **must never** be directly exposed to the public internet (0.0.0.0/0).
*   **4.1.2 VPN or Gateway Requirement:** Access to RDP listeners must be restricted to connections originating from:
    *   The Organization’s corporate VPN (Virtual Private Network); or
    *   A Zero Trust Network Access (ZTNA) gateway; or
    *   An SSH Tunnel.
*   **4.1.3 Cloud Security Groups:** For cloud environments (AWS/Azure), Security Groups/Firewalls must explicitly deny inbound traffic on Port 3389 from "Any" source. Allow-listing is restricted to the specific internal IP range of the VPN concentrator or Bastion Host.

#### 4.2 Authentication and Access Control
*   **4.2.1 Multi-Factor Authentication (MFA):** MFA is **mandatory** for all remote administrative access. If the native RDP service cannot support MFA, the connection must be gated behind a VPN or Gateway that enforces MFA.
*   **4.2.2 Network Level Authentication (NLA):** NLA must be enabled on all Windows hosts accepting RDP connections.
*   **4.2.3 Least Privilege:**
    *   The default "Administrator" or "Root" account must **not** be used for remote login.
    *   Only users specifically added to the "Remote Desktop Users" group are permitted to connect.
    *   Domain Admin accounts should not be used for RDP into lower-trust workstations (to prevent Pass-the-Hash attacks).

#### 4.3 Session Configuration
To mitigate data exfiltration and session hijacking:

*   **4.3.1 Session Timeouts:**
    *   **Idle Session Limit:** Disconnect after 15 minutes of inactivity.
    *   **Disconnected Session Limit:** Terminate (log off) after 1 hour in a disconnected state.
*   **4.3.2 Device Redirection:**
    *   **Drive Redirection:** Must be **Disabled** (prevents malware jumping from client to host).
    *   **Clipboard Sharing:** Must be restricted based on role necessity.
    *   **Printer Redirection:** Must be **Disabled**.

#### 4.4 Patch Management and Vulnerability Mitigation
*   **4.4.1 Critical Patching:** All systems running RDP services must be patched within the timelines defined in the *Patch Management Policy*.
*   **4.4.2 BlueKeep/DejaBlue:** Legacy operating systems (e.g., Windows 7, Server 2008) that are vulnerable to wormable RDP exploits are **prohibited** from the network unless isolated in a strictly air-gapped environment with written CISO approval.

#### 4.5 Monitoring and Auditing
*   **4.5.1 Logging:** All RDP login attempts (Success and Failure) must be logged (e.g., Windows Event ID 4624 and 4625).
*   **4.5.2 Alerting:** The SIEM or Log Management system must trigger an alert upon:
    *   Detection of RDP traffic from non-VPN IP addresses.
    *   Multiple failed authentication attempts (Brute Force indicator).
    *   RDP connections occurring outside of standard business hours (unless pre-authorized).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Owns this Standard; authorizes any temporary exceptions; reviews logs for anomalies. |
| **System Administrators / DevOps** | Configure servers and firewalls to comply with this Standard; ensure NLA and MFA are active. |
| **Users / Volunteers** | Use approved VPN/Gateway methods for access; protect credentials; report suspicious session activity. |
| **Internal Audit** | Periodically verifies that no RDP ports are exposed to the public internet via vulnerability scanning. |

### 6. Compliance and Enforcement
**Zero Tolerance for Exposure:** Any asset found with RDP exposed directly to the internet is subject to immediate disconnection from the network without prior notice to the owner.

Failure to comply with this Standard may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action. This aligns with **Bylaws Article III, Section 3.6**, regarding removal for cause due to failure to adhere to organizational policies.

### 7. References
*   **Study GRC Bylaws:** Article IX (Policies & Data Protection)
*   **NIST SP 800-53 (Rev. 5):** AC-17 (Remote Access), IA-2 (Identification and Authentication)
*   **CISA Ransomware Guide:** Remote Access Best Practices
*   **CIS Benchmarks:** Windows Server (Remote Desktop Services Section)
*   **Related Document:** IS-POL-001 (Master Information Security Policy)
*   **Related Document:** IS-POL-008 (Remote Access Policy)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Compliance Architect | Initial Release - Aligned with Ransomware Prevention protocols. |