### Remote Access Policy (VPN/Zero Trust)

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-025 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Bi-Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this policy is to establish the rules and standards for connecting to Study GRC Inc.'s internal network resources and sensitive data repositories from remote locations. As a remote-first organization, the perimeter is identity-based. This policy mandates the implementation of secure remote access technologies—specifically Virtual Private Networks (VPN) and Zero Trust Network Access (ZTNA)—to protect the confidentiality, integrity, and availability of organizational assets.

This policy is designed to satisfy **NIST SP 800-53 Control AC-17 (Remote Access)** and aligns with the data protection mandates outlined in **Article IX** of the Organization’s Bylaws.

### 2. Scope
This policy applies to all Study GRC Inc. personnel, including:
*   **Employees and Operational Officers**
*   **Board of Directors**
*   **Contractors and Consultants**
*   **Volunteers with privileged access**

**Scope of Systems:**
This policy applies to all methods used to remotely access non-public organizational resources, including but not limited to:
*   Cloud Infrastructure (AWS, Azure, GCP)
*   Internal Databases containing Member or Youth data
*   Administrative consoles for SaaS applications
*   Remote Desktop Protocol (RDP) and Secure Shell (SSH) sessions

**Exclusions:**
Access to public-facing resources (e.g., the public website, public community forums) does not require VPN/ZTNA authentication.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Remote Access** | Access to an organizational information system by a user (or a process acting on behalf of a user) communicating through an external network (e.g., the Internet). |
| **VPN (Virtual Private Network)** | A technology that creates a safe and encrypted connection over a less secure network, such as the internet. |
| **ZTNA (Zero Trust Network Access)** | An IT security solution that provides secure remote access to an organization's applications, data, and services based on clearly defined access control policies. It operates on the principle of "never trust, always verify." |
| **Split Tunneling** | A method of simultaneously allowing a remote user to access a public network (like the internet) and a local network (via VPN). |
| **MFA (Multi-Factor Authentication)** | An authentication method that requires the user to provide two or more verification factors to gain access to a resource. |
| **Privileged Access** | Access rights that allow a user to perform security-relevant functions (e.g., system administration, configuration changes). |

### 4. Policy Statements

#### 4.1 Authorization and Access Control (NIST AC-17(2))
4.1.1 **Approval Required:** Remote access to internal infrastructure is not granted by default. It must be explicitly authorized by the CISO or their designee based on a demonstrated business need or role requirement.
4.1.2 **Role-Based Access:** Access rights must be provisioned according to the Principle of Least Privilege. Users must only be granted access to the specific network segments or applications required for their role.
4.1.3 **Review:** Remote access privileges must be reviewed semi-annually. Access must be immediately revoked upon termination of employment or volunteer service, in accordance with the **Offboarding Checklist**.

#### 4.2 Acceptable Methods of Connection (NIST AC-17(1))
4.2.1 **Authorized Tools:** Users must only use Organization-approved VPN clients or ZTNA agents (e.g., OpenVPN, WireGuard, Cloudflare Access, AWS Client VPN) to access internal resources.
4.2.2 **Encryption:** All remote access sessions must utilize strong encryption (e.g., TLS 1.2+, AES-256) to protect data in transit.
4.2.3 **Authentication:** Multi-Factor Authentication (MFA) is **mandatory** for all remote access connections. No exceptions are permitted for privileged infrastructure access.

#### 4.3 Device Security Requirements (NIST AC-17(3))
4.3.1 **Managed Devices:** Ideally, remote access should only be initiated from Organization-managed devices.
4.3.2 **BYOD Compliance:** If a personal device (BYOD) is used to establish a VPN/ZTNA connection, it must comply with the **Bring Your Own Device (BYOD) Policy**, including:
*   Active, up-to-date antivirus/anti-malware software.
*   Operating system patches applied within 14 days of release.
*   Firewall enabled.
4.3.3 **Posturing:** Where technically feasible, the VPN/ZTNA solution must perform a "health check" (posture assessment) on the connecting device before granting access.

#### 4.4 Operational Restrictions
4.4.1 **Split Tunneling:** To prevent data exfiltration and bypass of security controls, "Split Tunneling" is **prohibited** for connections accessing High Availability or Confidential data environments, unless explicitly architected via a secure ZTNA solution that isolates application traffic.
4.4.2 **Timeouts:** Remote access sessions must enforce an idle timeout of no more than **30 minutes**. Re-authentication is required after the timeout.
4.4.3 **Simultaneous Connections:** Users are prohibited from establishing dual remote connections (e.g., bridging the Organization’s VPN with a third-party VPN) that could create an unauthorized bridge between networks.

#### 4.5 Privileged Remote Access (RDP/SSH)
4.5.1 **Direct Exposure Prohibited:** Remote Desktop Protocol (RDP), SSH, and Telnet ports must **never** be exposed directly to the public internet.
4.5.2 **Bastion Hosts/Gateways:** Administrative access to servers must be routed through an encrypted VPN tunnel, a Bastion Host, or a privileged access management (PAM) gateway.

#### 4.6 Monitoring and Logging (NIST AC-17(4))
4.6.1 **Session Logging:** The Organization reserves the right to log and monitor all remote access sessions to ensure compliance with this policy. Logs must capture:
*   User ID.
*   Source IP address.
*   Date and time of connection/disconnection.
*   Resources accessed.
4.6.2 **Privacy Notice:** Users have no reasonable expectation of privacy regarding traffic flowing through the Organization’s VPN or ZTNA infrastructure.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Defines the remote access architecture; selects approved VPN/ZTNA solutions; monitors compliance. |
| **IT/System Administrators** | Configures VPN concentrators and ZTNA policies; provisions user access; ensures logs are captured and retained. |
| **Users (Employees/Volunteers)** | Protects authentication credentials; ensures their remote device meets security standards; disconnects sessions when not in use. |
| **Board of Directors** | Reviews and approves this policy as part of the Organization's risk management framework. |

### 6. Compliance and Enforcement
Failure to comply with this policy may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action depending on the severity of the violation.

Any user found to be bypassing remote access controls (e.g., creating unauthorized backdoors, using unapproved proxies) will face immediate suspension of all system access pending an investigation.

### 7. References
*   **NIST SP 800-53 Rev. 5:** Control AC-17 (Remote Access), AC-3 (Access Enforcement), IA-2 (Identification and Authentication).
*   **Study GRC Inc. Bylaws:** Article IX (Policies & Data Protection).
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-POL-003:** Access Control Policy.
*   **IS-POL-022:** Bring Your Own Device (BYOD) Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name], CISO | Initial Draft aligned with NIST AC-17 and Bylaws. |