### Secure Configuration Management Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-024 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Bi-Annual) |
| **Approving Authority** | Executive Director (CEO) |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this policy is to establish the requirements for the development, documentation, and maintenance of secure baseline configurations for all information systems utilized by Study GRC Inc. By standardizing system settings and eliminating unnecessary functions, ports, and services, the Organization reduces its attack surface, mitigates the risk of unauthorized changes, and ensures compliance with **NIST SP 800-53 (CM-2)**.

### 2. Scope
This policy applies to all Information Technology (IT) assets owned, leased, or managed by Study GRC Inc., including but not limited to:
*   **Endpoints:** Laptops, desktops, and mobile devices issued to staff or volunteers.
*   **Infrastructure:** Servers (physical and virtual), network devices (firewalls, routers, switches), and cloud infrastructure (IaaS/PaaS) configurations.
*   **Software:** Operating systems, applications, and middleware.

**Exclusions:** Personal devices used under the *Bring Your Own Device (BYOD) Policy* are excluded from direct configuration management, provided they meet the minimum security posture requirements defined in the *Remote Access Policy*.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Baseline Configuration** | A documented set of specifications for an information system, or a configuration item within a system, that has been formally reviewed and agreed on at a given point in time, and which can be changed only through change control procedures. |
| **Hardening** | The process of securing a system by reducing its surface of vulnerability, which is larger when a system performs more functions; in principle, a single-function system is more secure than a multipurpose one. |
| **Configuration Drift** | The phenomenon where running servers or systems in an infrastructure become increasingly different from the original baseline configuration due to manual ad-hoc changes and updates. |
| **Gold Image** | A pre-configured template for a virtual machine or physical device that contains a pre-installed operating system and software stack approved by IT. |
| **Least Functionality** | The principle of configuring systems to provide only essential capabilities and specifically prohibiting or restricting the use of non-essential functions, ports, protocols, and services. |

### 4. Policy Statements

#### 4.1. Baseline Configuration Standards
The Chief Information Security Officer (CISO) must establish and maintain documented baseline configurations for all authorized hardware and software.
*   **4.1.1 Industry Standards:** Baselines must align with industry-accepted hardening standards, specifically the **Center for Internet Security (CIS) Benchmarks** (Level 1 minimum) or vendor-specific security guides (e.g., AWS Foundations Benchmark).
*   **4.1.2 Review Cycle:** Baselines must be reviewed and updated at least annually, or upon significant security events (e.g., new vulnerability discovery) or major software upgrades.
*   **4.1.3 Intellectual Property:** In accordance with **Bylaws Article IX**, all custom configuration scripts, Infrastructure-as-Code (IaC) templates, and Gold Images developed by staff or volunteers remain the exclusive property of Study GRC Inc.

#### 4.2. Principle of Least Functionality
Systems must be configured to the "deny-all" standard by default.
*   **4.2.1 Service Disabling:** All unnecessary services, applications, scripts, drivers, network protocols, and ports must be disabled or removed.
*   **4.2.2 Port Restrictions:** Only ports required for specific business functions may be opened.
*   **4.2.3 Software Restriction:** Only software listed on the *Authorized Software Inventory* may be installed. The execution of unauthorized binaries must be restricted via technical controls (e.g., AppLocker, WDAC) where feasible.

#### 4.3. Cloud and Remote-First Configuration
Given the Organization's remote-first nature, configuration management must extend to cloud environments and remote endpoints.
*   **4.3.1 Infrastructure as Code (IaC):** Cloud infrastructure (e.g., AWS, Azure) should be deployed using IaC (e.g., Terraform, CloudFormation) to ensure consistency and prevent manual configuration errors.
*   **4.3.2 MDM Enrollment:** All Organization-owned endpoints must be enrolled in a Mobile Device Management (MDM) solution (e.g., Intune, Jamf) prior to distribution to ensure the secure baseline is applied before the user accesses data.
*   **4.3.3 Default Passwords:** Vendor-supplied default passwords and usernames must be changed immediately upon system installation or deployment.

#### 4.4. Configuration Change Control
Changes to baseline configurations must follow the *Change Control and Management Procedure*.
*   **4.4.1 Authorization:** No changes to the baseline (e.g., opening a new firewall port, installing a new global plugin) may occur without approval from the Change Advisory Board (CAB) or the CISO.
*   **4.4.2 Testing:** Changes to baselines must be tested in a non-production environment to verify security impact and operational stability before deployment.

#### 4.5. Monitoring and Drift Management
The Organization must employ automated mechanisms to monitor for configuration drift.
*   **4.5.1 Automated Scanning:** Systems must be scanned regularly (at least weekly) to verify compliance with the established baseline.
*   **4.5.2 Remediation:** Detected deviations (drift) must be remediated within timelines defined in the *Vulnerability Remediation SLA*. Unauthorized changes must be reverted immediately.

#### 4.6. Exceptions
Deviations from the standard baseline for specific business needs (e.g., a developer requiring local admin rights or specific open ports) require a formal *Security Exception Request*.
*   **4.6.1 Risk Acceptance:** Exceptions must be documented, risk-assessed, and approved by the CISO.
*   **4.6.2 Compensating Controls:** Approved exceptions must include compensating security controls (e.g., network segmentation, enhanced monitoring).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Owns this policy; approves all baseline standards; authorizes exceptions; monitors compliance. |
| **IT Systems Administrators** | Develop technical baselines (Gold Images/Scripts); implement configuration changes; ensure new deployments match the baseline. |
| **Change Advisory Board (CAB)** | Reviews and approves proposed changes to global baseline configurations to ensure stability and security. |
| **Employees & Volunteers** | Adhere to configuration standards; prohibited from altering security settings, disabling agents, or installing unauthorized software. |
| **Internal Audit** | Periodically validates that systems match the documented baselines. |

### 6. Compliance and Enforcement
Failure to comply with this policy may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action depending on the severity of the violation.

*   **Technical Enforcement:** Devices found to be non-compliant with the secure baseline may be quarantined from the network or remotely wiped/re-imaged to restore the secure state.
*   **Legal:** Unauthorized alteration of system configurations that results in a data breach may trigger liability under the *Computer Fraud and Abuse Act* and relevant Texas state laws.

### 7. References
*   **NIST SP 800-53 Rev. 5:** Control CM-2 (Baseline Configuration) & CM-6 (Configuration Settings).
*   **CIS Benchmarks:** Center for Internet Security Configuration Guidelines.
*   **IS-PRC-042:** Change Control and Management Procedure.
*   **IS-POL-007:** Acceptable Use Policy (AUP).
*   **Study GRC Inc. Bylaws:** Article IX (Intellectual Property).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name] | Initial Release aligned with NIST CM-2 requirements. |