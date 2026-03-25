### Firewall Configuration and Management Standard

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-036 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-04-25 (Bi-Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Lead Cloud Architect |
| **Classification** | Internal |

### 1. Purpose
The purpose of this standard is to establish mandatory technical requirements for the configuration, management, and maintenance of network boundary protection mechanisms (firewalls) within Study GRC Inc. This standard mitigates the risks of unauthorized access, lateral movement of threats, and data exfiltration by enforcing a "Default Deny" posture across all network perimeters and host-based systems.

### 2. Scope
This standard applies to all network traffic control devices and software managed by Study GRC Inc., including but not limited to:
*   **Cloud Network Security Groups** (e.g., AWS Security Groups, Azure NSGs).
*   **Web Application Firewalls (WAF)** protecting public-facing resources.
*   **Host-Based Firewalls** installed on Organization-issued endpoints (laptops/servers).
*   **VPN Concentrators** and gateways.

**Exclusions:** This standard does not apply to the personal home network routers of remote volunteers or employees, though secure configuration of such devices is strongly encouraged via the *Remote Work Technology Requirements (HR-STD-009)*.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Default Deny** | A security stance where all traffic is blocked unless explicitly allowed by a specific rule. |
| **Ingress** | Network traffic entering the Organization's network or a specific host from an external source. |
| **Egress** | Network traffic leaving the Organization's network or a specific host to an external destination. |
| **Security Group** | A virtual firewall that controls inbound and outbound traffic for cloud resources (e.g., EC2 instances, RDS databases). |
| **Bastion Host / Jump Box** | A special-purpose computer on a network specifically designed and configured to withstand attacks, used as the single point of entry for administration. |
| **WAF** | Web Application Firewall; protects web applications by filtering and monitoring HTTP traffic between a web application and the Internet. |

### 4. Standard Statements

#### 4.1 General Configuration Principles
4.1.1 **Default Deny Policy:** All firewall configurations must adhere to an implicit "deny-all" strategy. Rules must explicitly permit only necessary traffic; all other traffic must be dropped.
4.1.2 **Rule Documentation:** Every firewall rule must include a comment or tag description identifying:
*   The purpose of the rule.
*   The Change Request ID (if applicable).
*   The date created.
*   The owner of the service requiring the access.
4.1.3 **No "Any/Any" Rules:** Rules allowing traffic from `0.0.0.0/0` (Any) to `Any` port are strictly prohibited, with the sole exception of public-facing web services (HTTP/HTTPS) on ports 80/443.

#### 4.2 Ingress (Inbound) Traffic Controls
4.2.1 **Management Ports:** Remote management ports (e.g., SSH port 22, RDP port 3389) must never be exposed directly to the public internet (`0.0.0.0/0`).
4.2.2 **Remote Access:** Administrative access to cloud infrastructure must be routed through a secure VPN, a Zero Trust Network Access (ZTNA) solution, or a hardened Bastion Host/Jump Box restricted to specific trusted IP addresses.
4.2.3 **Protocol Specificity:** Inbound rules must be restricted to the specific protocol (TCP/UDP) and port required. Port ranges (e.g., 1000-2000) are prohibited unless required by the specific application architecture and approved by the CISO.

#### 4.3 Egress (Outbound) Traffic Controls
4.3.1 **Data Exfiltration Prevention:** Outbound traffic must be restricted. Servers should only be allowed to initiate connections to necessary repositories (e.g., OS updates, code repositories, specific API endpoints).
4.3.2 **Direct Internet Access:** Database servers and internal backend services must not have direct routes to the internet. They must utilize NAT Gateways or Proxy servers with strict filtering if external access is required.

#### 4.4 Cloud Infrastructure (IaaS/PaaS)
4.4.1 **Security Groups:** Cloud Security Groups must be applied at the instance/resource level. Relying solely on Network Access Control Lists (NACLs) is insufficient.
4.4.2 **Database Protection:** Database instances (e.g., RDS, SQL) must utilize Security Groups that only accept traffic from the specific Security Groups of the application tier (App Servers), not from IP subnets generally.

#### 4.5 Web Application Firewalls (WAF)
4.5.1 **Public Facing Assets:** All public-facing web applications (e.g., the Study GRC learning platform) must be protected by a WAF.
4.5.2 **Blocking Mode:** WAFs must be configured in "Block" or "Prevention" mode for high-confidence rule sets (e.g., OWASP Top 10 protection), rather than "Detection" only mode, unless during a temporary tuning period (max 7 days).

#### 4.6 Host-Based Firewalls (Endpoints)
4.6.1 **Always-On:** Host-based firewalls (e.g., Windows Defender Firewall, macOS Firewall, `iptables`/`ufw`) must be enabled on all Organization-owned devices.
4.6.2 **Profile Configuration:**
*   **Public Networks:** Block all incoming connections.
*   **Private/Work Networks:** Allow only essential file sharing or management services required for operations.

#### 4.7 Review and Auditing
4.7.1 **Bi-Annual Review:** The IT Security Team must review all active firewall rules and Security Groups every six (6) months.
4.7.2 **Stale Rule Removal:** Rules associated with decommissioned services or termed projects must be removed within 48 hours of service termination.
4.7.3 **Logging:** Firewall logs (accept and deny events) must be ingested into the Organization's SIEM or centralized logging bucket for retention in accordance with the *Log Management and Retention Policy (IS-POL-021)*.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Approves this standard and authorizes any temporary exceptions based on risk assessment. |
| **Lead Cloud Architect** | Ensures cloud infrastructure (AWS/Azure) Security Groups are architected in compliance with this standard. |
| **System Administrators / DevOps** | Implements firewall rules, maintains documentation tags, and removes stale rules during decommissioning. |
| **All Employees/Volunteers** | Prohibited from disabling host-based firewalls on Organization-issued equipment. |

### 6. Compliance and Enforcement
Failure to comply with this standard may result in disciplinary action, up to and including termination of employment or volunteer assignment.
*   **Technical Enforcement:** Non-compliant firewall rules detected by automated scanning tools (e.g., CSPM) may be automatically reverted or quarantined without prior notice to preserve organizational security.
*   **Legal:** Negligence in boundary protection that leads to a data breach may expose the individual to liability under the *Indemnification Policy (Bylaws Article VII)* if actions were not taken in good faith.

### 7. References
*   **Study GRC Bylaws Article IX:** Data Protection & Intellectual Property.
*   **NIST CSF 2.0:** PR.AC-5 (Network integrity is protected).
*   **NIST SP 800-53 Rev 5:** SC-7 (Boundary Protection).
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-POL-021:** Log Management and Retention Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Compliance Architect | Initial release aligned with Cloud-First strategy. |