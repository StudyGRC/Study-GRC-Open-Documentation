### Patch Management Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-038 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Patch Management Policy is to establish a systematic process for the identification, acquisition, installation, and verification of security patches and updates for all Information Technology (IT) assets within Study GRC Inc. (the "Organization").

Unpatched systems represent one of the most significant vectors for cyberattacks. As an organization dedicated to Governance, Risk, and Compliance (GRC) knowledge and open-source resources, maintaining the integrity and availability of our infrastructure is critical to our reputation and mission. This policy mandates a proactive approach to vulnerability management to mitigate risks associated with known software defects and security vulnerabilities.

### 2. Scope
This policy applies to all information systems, software, and computing devices owned, managed, or utilized by Study GRC Inc. to process, store, or transmit Organizational data.

**In Scope:**
*   **Cloud Infrastructure:** Servers, containers, and virtual machines hosted in cloud environments (e.g., AWS, Azure).
*   **Network Equipment:** Firewalls, routers, switches, and VPN concentrators.
*   **Endpoints:** Laptops, desktops, and mobile devices issued by the Organization.
*   **Applications:** Server-side applications, databases, middleware, and client-side software.
*   **BYOD (Bring Your Own Device):** Personal devices used by volunteers or contractors to access Organizational resources must adhere to the minimum patching standards defined herein.

**Exclusions:**
*   Systems completely air-gapped from all networks (if any).
*   Third-party SaaS platforms where patching is the sole responsibility of the vendor (though monitoring vendor compliance remains in scope).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Patch** | A piece of software designed to update a computer program or its supporting data to fix or improve it, including fixing security vulnerabilities. |
| **Vulnerability** | A weakness in an information system, system security procedures, internal controls, or implementation that could be exploited or triggered by a threat source. |
| **CVSS (Common Vulnerability Scoring System)** | An industry standard for assessing the severity of computer system security vulnerabilities. |
| **Zero-Day** | A vulnerability that is discovered by attackers before the vendor has become aware of it or before a patch is available. |
| **Endpoint** | Any device that is physically an end point on a network, such as a laptop, mobile phone, or desktop computer. |
| **Compensating Control** | A data security measure that is designed to satisfy the requirement for some other security measure that is deemed too difficult or impractical to implement. |

### 4. Policy Statements

#### 4.1 General Mandate
All IT assets and software within the scope of this policy must be kept up-to-date with the latest vendor-supplied security patches. The Organization adopts a "security-first" posture; functionality concerns must be weighed heavily against security risks, but security integrity takes precedence in critical scenarios.

#### 4.2 Vulnerability Monitoring and Identification
The Chief Information Security Officer (CISO), as defined in **Bylaws Article V Section 5.2**, is responsible for establishing mechanisms to monitor for new vulnerabilities. This includes:
*   Subscribing to vendor security alerts (e.g., Microsoft, Linux distributions, Adobe).
*   Monitoring US-CERT/CISA alerts and the National Vulnerability Database (NVD).
*   Conducting regular vulnerability scans as defined in the *Vulnerability Scanning Policy (IS-POL-041)*.

#### 4.3 Patch Prioritization and Service Level Agreements (SLAs)
Patches must be applied based on the severity of the vulnerability they address. The Organization utilizes the CVSS v3.1 (or later) scoring system to determine severity.

| Severity Level | CVSS Score | Remediation SLA (Internet Facing) | Remediation SLA (Internal Only) |
| :--- | :--- | :--- | :--- |
| **Critical** | 9.0 - 10.0 | Within 48 Hours | Within 5 Days |
| **High** | 7.0 - 8.9 | Within 7 Days | Within 14 Days |
| **Medium** | 4.0 - 6.9 | Within 30 Days | Within 30 Days |
| **Low** | 0.0 - 3.9 | Next Maintenance Window | Next Maintenance Window |

*Note: In the event of an active exploitation (Zero-Day) or a directive from CISA (Binding Operational Directive), the CISO may declare an "Emergency Patch Cycle" requiring immediate remediation regardless of the standard SLA.*

#### 4.4 Testing and Change Management
To ensure the stability of the Organization's open-source resources and community platforms:
1.  **Testing:** Where technically feasible, patches for Critical and High vulnerabilities should be tested in a non-production (staging) environment prior to deployment.
2.  **Backup:** A verifiable backup or snapshot must be taken before applying patches to critical infrastructure, in accordance with the *Backup Policy (IS-POL-058)*.
3.  **Approval:** Patch deployment is a standard change; however, emergency patches requiring system downtime outside of maintenance windows require approval from the Executive Director or CISO.

#### 4.5 Endpoint and Volunteer Device Management
Given the Organization's remote-first nature:
*   **Managed Devices:** Organization-owned devices must have automated update agents installed (e.g., MDM profiles) that force the installation of critical OS and browser updates within the SLA windows.
*   **Volunteer/BYOD:** Volunteers accessing sensitive data or internal systems must attest that their operating system and browser are configured to install updates automatically. Access to Organizational systems may be revoked for devices found to be running unsupported (End-of-Life) operating systems.

#### 4.6 Patch Deferral and Risk Acceptance
If a patch cannot be applied due to technical incompatibility or mission-critical business requirements:
1.  A **Risk Acceptance Form** must be submitted to the CISO.
2.  **Compensating Controls** (e.g., network segmentation, WAF rules, disabling the specific vulnerable service) must be implemented immediately.
3.  The deferral must be reviewed monthly. Permanent deferral requires written approval from the Executive Director.

#### 4.7 Verification and Auditing
The CISO shall verify patch compliance through:
*   Automated reporting from patch management tools.
*   Monthly vulnerability scanning.
*   Random spot checks of volunteer devices (via screen share or evidence submission) if accessing Restricted Data.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Overall owner of the Patch Management Policy. Monitors vulnerability sources, declares emergency patch cycles, and approves patch deferrals. |
| **IT Systems Administrators** | Responsible for testing and deploying patches to infrastructure, servers, and managed endpoints. Responsible for verifying successful installation. |
| **Executive Director (CEO)** | Provides final authority on risk acceptance for critical vulnerabilities that cannot be patched. Ensures resources are available for patch management tools. |
| **Employees & Volunteers** | Responsible for rebooting their devices when prompted to finalize updates and ensuring their personal devices (BYOD) are not running End-of-Life software. |
| **Board of Directors** | Reviews high-level compliance reports annually as part of the *Annual Financial & Risk Report* (Bylaws Art. VIII). |

### 6. Compliance and Enforcement
Compliance with this policy is mandatory.
*   **System Isolation:** Devices or servers found to be non-compliant with Critical patch levels may be immediately disconnected from the Organization’s network until remediated.
*   **Disciplinary Action:** Failure to adhere to this policy may result in disciplinary action, up to and including termination of employment or revocation of volunteer status, in accordance with the *Employee Handbook* and *Volunteer Code of Conduct*.

### 7. References
*   **Bylaws of Study GRC Inc.** (Article V - Operational Leadership; Article IX - Data Protection)
*   **NIST CSF 2.0:** PR.PS-02 (Software is maintained and updated).
*   **IS-POL-041:** Vulnerability Scanning Policy.
*   **IS-POL-058:** Backup Policy and Procedures.
*   **IS-POL-045:** Incident Response Plan.
*   **IS-STD-028:** Data Classification Standard.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name/Title] | Initial Policy Draft and Adoption |