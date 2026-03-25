### Secure Network Configuration Standard

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-038 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Director of Infrastructure / DevOps Lead |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Standard is to establish mandatory technical requirements for the configuration of all network devices and virtual network infrastructure managed by Study GRC Inc. ("the Organization").

In accordance with **Bylaws Article I, Section 1.3**, the Organization is dedicated to maintaining a "community-driven ecosystem." To protect this ecosystem and the integrity of our open-source resources, we must minimize the attack surface of our infrastructure. This Standard aligns with **NIST SP 800-123** (Guide to General Server Security) and **NIST SP 800-41** (Guidelines on Firewalls and Firewalls Policy) to mitigate risks associated with unauthorized access, data exfiltration, and lateral movement within our networks.

### 2. Scope
This Standard applies to all network infrastructure components owned, leased, or managed by the Organization, including but not limited to:
*   **Cloud Network Infrastructure:** Virtual Private Clouds (VPCs), Security Groups, Virtual Firewalls, and Load Balancers (e.g., AWS, Azure, GCP).
*   **Physical Network Devices:** Routers, switches, firewalls, and Wireless Access Points (WAPs) located in any physical office or facility operated by the Organization.
*   **Remote Access Gateways:** VPN concentrators and Zero Trust Network Access (ZTNA) nodes.

**Exclusions:**
*   Home network equipment (routers/modems) owned personally by volunteers or employees, unless that equipment is contractually managed by the Organization via a specific telework agreement.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Default Deny** | A security stance where all traffic is blocked by default, and only specific, authorized traffic is allowed. |
| **Ingress/Egress** | Ingress refers to traffic entering the network; Egress refers to traffic leaving the network. |
| **Management Interface** | A network interface used strictly for administrative access (e.g., SSH, RDP, Web Console). |
| **Security Group** | A virtual firewall that controls the traffic for one or more instances in a cloud environment. |
| **VPC** | Virtual Private Cloud; an isolated cloud network environment. |
| **Bastion Host** | A special-purpose computer on a network specifically designed and configured to withstand attacks, used as a jump server to access internal resources. |

### 4. Standards

#### 4.1 General Configuration Principles
4.1.1 **Default Deny Posture:** All firewalls, routers, and security groups must be configured to "Deny All" inbound and outbound traffic by default. Allow rules must be created only for specific, business-justified protocols and ports.
4.1.2 **Least Privilege:** Network access permissions must be granted only to the extent necessary for the resource to function.
4.1.3 **Configuration Management:** All network device configurations must be treated as code (Infrastructure as Code - IaC) where feasible. Changes must follow the **Change Control and Management Procedure (IS-PRC-072)**.

#### 4.2 Cloud Network Security (VPC/Virtual)
4.2.1 **Segmentation:**
*   Production environments must be logically isolated from Development and Staging environments via separate VPCs or Accounts.
*   VPCs must utilize public and private subnets. Database instances and application servers not requiring direct internet access must reside in private subnets.
4.2.2 **Security Groups & NACLs:**
*   **0.0.0.0/0 Restrictions:** Ingress rules allowing `0.0.0.0/0` (global internet) are strictly prohibited for administrative ports (e.g., SSH port 22, RDP port 3389, Telnet port 23).
*   **Web Traffic:** Ingress from `0.0.0.0/0` is permitted only for HTTP (80) and HTTPS (443) on public-facing Load Balancers or Web Servers. HTTP traffic must immediately redirect to HTTPS.
4.2.3 **Flow Logs:** VPC Flow Logs (or equivalent) must be enabled for all production networks and ingested into the Organization’s SIEM or log repository for analysis, in compliance with **Bylaws Article VIII (Records)**.

#### 4.3 Device Hardening (Physical & Virtual Appliances)
4.3.1 **Default Credentials:** All vendor-supplied default usernames and passwords must be changed immediately upon device provisioning.
4.3.2 **Insecure Protocols:**
*   Clear-text management protocols (Telnet, HTTP, FTP, SNMPv1/v2) are prohibited.
*   Management must be performed via encrypted protocols (SSHv2, HTTPS, SFTP, SNMPv3).
4.3.3 **Banner Grabbing:** Default banners disclosing device model, OS version, or internal IP information must be disabled or replaced with the Organization’s authorized legal warning banner.
4.3.4 **NTP Synchronization:** All network devices must synchronize time against the Organization’s authorized NTP sources to ensure log integrity.

#### 4.4 Remote Management & Access
4.4.1 **Management Plane Protection:** Administrative access to network devices must be restricted to specific trusted IP addresses (e.g., the Organization’s VPN egress IP) or via a secured Bastion Host/Jump Box.
4.4.2 **Session Timeouts:**
*   Console/Terminal sessions must disconnect after a maximum of 15 minutes of inactivity.
*   VPN sessions must require re-authentication after a maximum of 12 hours.
4.4.3 **Multi-Factor Authentication (MFA):** In accordance with **IS-POL-015**, MFA is mandatory for all remote administrative access to network infrastructure.

#### 4.5 Wireless Network Security (If Applicable)
4.5.1 **Encryption:** All wireless networks must use WPA3 Enterprise or WPA2 Enterprise (AES/CCMP) encryption at a minimum. WEP and WPA-TKIP are prohibited.
4.5.2 **Guest Isolation:** Guest wireless networks must be logically isolated (VLAN segregation) from the internal corporate network and must not allow peer-to-peer communication.

#### 4.6 Documentation and Backup
4.6.1 **Network Diagrams:** High-level and low-level network diagrams must be maintained and reviewed quarterly.
4.6.2 **Configuration Backups:** Automated backups of network device configurations must occur daily. Backups must be encrypted at rest.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **CISO** | Approves this Standard and authorizes exceptions based on risk assessment. |
| **Director of Infrastructure** | Ensures all cloud and physical network configurations comply with this Standard. |
| **DevOps Engineers** | Implement IaC scripts and Security Groups in compliance with this Standard. |
| **Internal Audit** | Conducts periodic vulnerability scans and configuration reviews to verify compliance. |

### 6. Compliance and Enforcement
Failure to comply with this Standard represents a risk to the Organization’s tax-exempt purpose and community trust.
*   **Technical Enforcement:** Non-compliant resources identified during automated scans may be automatically quarantined or terminated.
*   **Personnel:** Violations may result in disciplinary action, up to and including termination of employment or volunteer assignment.
*   **Governance:** In cases of gross negligence regarding network security by an Officer, provisions for removal under **Bylaws Article V, Section 5.3** may be invoked.

### 7. References
*   **NIST SP 800-123:** Guide to General Server Security.
*   **NIST SP 800-41 Rev 1:** Guidelines on Firewalls and Firewalls Policy.
*   **CIS Benchmarks:** Center for Internet Security Benchmarks for AWS/Azure/Cisco.
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-PRC-072:** Change Control and Management Procedure.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Compliance Architect | Initial Release aligned with NIST Hardening standards. |