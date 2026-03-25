### Network Security Architecture Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-035 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Executive Director / Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this policy is to establish the architectural standards and security requirements for Study GRC Inc.’s network infrastructure. As a remote-first, cloud-native organization, the traditional network perimeter has dissolved. This policy mandates a **Defense-in-Depth** strategy, utilizing network segmentation and **Zero Trust** principles to minimize the attack surface, prevent lateral movement of threats, and protect sensitive assets—specifically Member Data and Youth Participant information—from unauthorized access.

### 2. Scope
This policy applies to all network resources owned, managed, or utilized by Study GRC Inc., including but not limited to:
*   **Cloud Infrastructure:** Virtual Private Clouds (VPCs), subnets, and container networking within Infrastructure-as-a-Service (IaaS) and Platform-as-a-Service (PaaS) environments (e.g., AWS, Azure, Google Cloud).
*   **Remote Access:** VPNs, SASE (Secure Access Service Edge), and SD-WAN solutions used by employees and volunteers.
*   **Physical Networks:** Any temporary or permanent physical network infrastructure deployed for Organization events (e.g., Annual Meetings, workshops).
*   **Endpoints:** The network interfaces of devices connecting to Organization resources.

**Exclusions:** Home networks of remote volunteers/employees are excluded from direct management, though they must meet minimum security standards defined in the *Remote Work and Telecommuting Policy (HR-POL-003)* to connect to corporate resources.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Network Segmentation** | The practice of splitting a network into smaller sub-networks (segments) to boost performance and security. It limits the blast radius of a cyberattack. |
| **Zero Trust Architecture (ZTA)** | A security model that assumes no user or device is trustworthy by default, regardless of their location relative to the network perimeter. Verification is required for every access request. |
| **VPC (Virtual Private Cloud)** | An isolated logical network within a public cloud provider that allows the Organization to define IP address ranges, subnets, route tables, and network gateways. |
| **Lateral Movement** | Techniques used by cyber attackers to move deeper into a network in search of sensitive data and other high-value assets after gaining initial access. |
| **Demilitarized Zone (DMZ)** | A physical or logical sub-network that contains and exposes an organization's external-facing services to an untrusted network (usually the Internet). |
| **Ingress/Egress** | Ingress refers to traffic entering the network; Egress refers to traffic exiting the network. |

### 4. Policy Statements

#### 4.1 Network Segmentation and Isolation
To prevent lateral movement and ensure compliance with data protection standards (including COPPA and GDPR), the Organization’s network must be segmented based on trust levels and data classification.

*   **4.1.1 Environment Separation:** Production, Staging/Test, and Development environments must be logically isolated. Traffic between these environments is prohibited by default and must be explicitly allowed only via secure, monitored gateways.
*   **4.1.2 Data Sensitivity Isolation:** Systems processing **Confidential** or **Restricted** data (specifically Youth Participant Data and Donor Financial Information) must reside in isolated subnets with strict Access Control Lists (ACLs).
*   **4.1.3 Management Plane Isolation:** Administrative interfaces (e.g., SSH, RDP, Cloud Console APIs) must not be directly exposed to the public internet. Access must be mediated through a bastion host, VPN, or secure identity-aware proxy.

#### 4.2 Zero Trust Principles
Given the Organization's remote-first nature, the network architecture must adhere to Zero Trust principles as defined in NIST SP 800-207.

*   **4.2.1 Identity as Perimeter:** Access to network resources must be granted based on the identity of the user and the security posture of the device, not solely on network location (IP address).
*   **4.2.2 Least Privilege Access:** Network flows must be restricted to the minimum necessary for a service or user to perform their function. "Any-to-Any" rules are strictly prohibited within internal zones.
*   **4.2.3 Continuous Verification:** Authentication and authorization must be continuously validated, not just at the initial login.

#### 4.3 Cloud Network Security
As the Organization relies on cloud infrastructure, the following controls are mandatory:

*   **4.3.1 Default Deny:** All Security Groups and Network ACLs must be configured to "Deny All" inbound and outbound traffic by default. Allow rules must be created only for specific, required ports and protocols.
*   **4.3.2 Public vs. Private Subnets:** Only resources that strictly require internet exposure (e.g., Load Balancers, NAT Gateways) may reside in Public Subnets. Application servers and databases must reside in Private Subnets with no direct route to the internet.
*   **4.3.3 Flow Logging:** VPC Flow Logs (or equivalent) must be enabled for all production networks and ingested into the SIEM for monitoring and anomaly detection.

#### 4.4 Remote Access Security
Pursuant to the *Remote Work and Telecommuting Policy*, secure connectivity is required for all administrative work.

*   **4.4.1 Encryption:** All remote access connections must utilize strong encryption (TLS 1.2+ or IPsec) to protect data in transit.
*   **4.4.2 Multi-Factor Authentication (MFA):** All remote network access (VPN, SASE, SSH) requires MFA.
*   **4.4.3 Split Tunneling:** Split tunneling on VPNs is permitted only if configured to route traffic destined for Organization resources through the secure tunnel, while allowing commodity internet traffic to bypass it, provided endpoint security controls are active.

#### 4.5 Wireless and Event Network Security
For physical events hosted by the Organization:

*   **4.5.1 Guest Isolation:** Guest Wi-Fi networks must be completely segmented from the Organization’s administrative network. Client isolation must be enabled to prevent guests from accessing each other’s devices.
*   **4.5.2 Encryption:** Wireless networks transmitting Organization data must use WPA3 or WPA2-Enterprise encryption.

#### 4.6 Traffic Filtering and Inspection
*   **4.6.1 Egress Filtering:** Outbound traffic must be filtered to prevent communication with known malicious command-and-control (C2) servers.
*   **4.6.2 Web Application Firewalls (WAF):** All public-facing web applications must be protected by a WAF configured to block OWASP Top 10 vulnerabilities.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Defined in Bylaws Art. V §5.2. Responsible for approving the network security architecture, defining segmentation strategy, and authorizing exceptions. |
| **Cloud Architects / DevOps Engineers** | Responsible for implementing network controls (VPCs, Security Groups) in accordance with this policy and maintaining "Infrastructure as Code" configurations. |
| **IT Operations** | Responsible for managing remote access solutions (VPN/SASE) and monitoring network logs. |
| **Employees & Volunteers** | Responsible for using approved remote access methods and refraining from bypassing network security controls (e.g., creating unauthorized bridges). |

### 6. Compliance and Enforcement
The CISO will conduct periodic architectural reviews and penetration tests to verify compliance with this policy.

Failure to comply with this policy may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action depending on the severity of the violation. Unauthorized circumvention of network segmentation controls (e.g., bridging networks) is considered a severe violation.

### 7. References
*   **Bylaws of Study GRC Inc.** (Article V - Operational Leadership)
*   **NIST Cybersecurity Framework (CSF) 2.0:** PR.AC-5 (Network Integrity), PR.DS-5 (Data Leakage Protection)
*   **NIST SP 800-207:** Zero Trust Architecture
*   **IS-POL-001:** Master Information Security Policy
*   **IS-STD-005:** Data Classification Standard
*   **HR-POL-003:** Remote Work and Telecommuting Policy

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name], CISO | Initial Policy Draft |