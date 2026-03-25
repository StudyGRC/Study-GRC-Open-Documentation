### System Hardening Standards (OS-Specific)

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-065 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Director of IT Operations |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Standard is to establish the minimum security configuration requirements ("hardening") for all operating systems (OS) and computing assets used by Study GRC Inc. Unsecured default configurations are a primary vector for cyberattacks. By reducing the attack surface through rigorous hardening, Study GRC Inc. protects its intellectual property, member data, and youth participant information in compliance with **Bylaws Article IX (Policies & Data Protection)** and **Article VII (Indemnification)** regarding the good faith performance of duties.

This Standard explicitly adopts the **Center for Internet Security (CIS) Benchmarks** as the authoritative baseline for system configuration.

### 2. Scope
This Standard applies to:
*   **Organization-Owned Assets:** All servers (cloud and on-premise), workstations, laptops, and mobile devices owned or leased by Study GRC Inc.
*   **Cloud Instances:** Virtual Machines (EC2, Azure VMs, Droplets) and containerized environments running an OS.
*   **BYOD (Bring Your Own Device):** Personal devices used by volunteers or employees to access Tier 2 (Internal) or Tier 3 (Confidential) data must meet the "Minimum Viable Hardening" requirements defined in Section 4.6.

**Exclusions:**
*   Third-party SaaS platforms (governed by *IS-POL-088 Cloud Services Security Policy*), though the endpoints accessing them are included here.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Hardening** | The process of securing a system by reducing its surface of vulnerability, typically by removing unnecessary software, disabling unnecessary services, and configuring strict security parameters. |
| **CIS Benchmarks** | Globally recognized best practices for securing IT systems and data, published by the Center for Internet Security. |
| **Golden Image** | A pre-configured template for a virtual machine or workstation that includes the OS and all required hardening settings, used to deploy new systems consistently. |
| **Level 1 Profile (CIS)** | The baseline security configuration recommendation that provides standard security without inhibiting system utility. |
| **Level 2 Profile (CIS)** | A stricter security profile intended for environments where security is paramount (e.g., servers hosting PII or financial data). |
| **Least Privilege** | The principle that a user or process should only have access to the specific data, resources, and applications needed to complete a required task. |

### 4. Standards

#### 4.1 General Hardening Principles
All systems, regardless of OS, must adhere to the following core principles:
1.  **Default Deny:** All inbound network traffic is blocked unless explicitly allowed.
2.  **Removal of Unnecessary Software:** Only software required for the specific business function may be installed. "Bloatware" and trial software must be removed.
3.  **Disable Unused Services:** Services and daemons not required for operation (e.g., FTP, Telnet, Print Spooler on web servers) must be disabled.
4.  **Patching:** The OS must be on a supported version with the latest security patches applied within timelines defined in the *IS-POL-040 Patch Management Policy*.

#### 4.2 Adoption of CIS Benchmarks
Study GRC Inc. adopts the **CIS Benchmarks** as the technical standard for hardening.
*   **Workstations (Laptops/Desktops):** Must meet **CIS Level 1** requirements.
*   **Servers (Production/Data Hosting):** Must meet **CIS Level 2** requirements.
*   **Dev/Test Environments:** Must meet **CIS Level 1** requirements.

#### 4.3 Windows Hardening Standards (Server & Workstation)
In addition to the CIS Benchmarks, the following specific controls are mandatory for all Windows assets:

*   **4.3.1 Account Policies:**
    *   **Password History:** Remember at least 24 passwords.
    *   **Lockout Threshold:** Account locks after 5 failed attempts.
    *   **Administrator Account:** The built-in Administrator account must be renamed and disabled.
    *   **Guest Account:** Must be disabled.

*   **4.3.2 Local Policies & User Rights:**
    *   **Debug Programs:** Restricted to Administrators only.
    *   **Access this computer from the network:** Strictly limited to authenticated users; "Everyone" permissions must be removed.

*   **4.3.3 Network & Firewall:**
    *   **Windows Defender Firewall:** Must be enabled on all profiles (Domain, Private, Public).
    *   **RDP (Remote Desktop):** Must be disabled on workstations. On servers, it must be restricted to specific management IP addresses or VPN tunnels.

*   **4.3.4 Encryption:**
    *   **BitLocker:** Full Disk Encryption (FDE) must be enabled on all laptops and portable drives. Keys must be backed up to the corporate Active Directory or MDM solution.

#### 4.4 Linux Hardening Standards (Ubuntu/RedHat/Amazon Linux)
For all Linux-based servers and cloud instances:

*   **4.4.1 SSH Configuration (`/etc/ssh/sshd_config`):**
    *   **Root Login:** `PermitRootLogin no` (Must be set to 'no').
    *   **Protocol:** Protocol 2 only.
    *   **Authentication:** `PasswordAuthentication no` (Must use SSH Keys).
    *   **Empty Passwords:** `PermitEmptyPasswords no`.

*   **4.4.2 Filesystem & Storage:**
    *   **Partitioning:** Separate partitions must be created for `/tmp`, `/var`, and `/home` to prevent resource exhaustion.
    *   **Mount Options:** `/tmp` and `/dev/shm` must be mounted with `nodev`, `nosuid`, and `noexec`.

*   **4.4.3 Network:**
    *   **Firewall:** `UFW` (Ubuntu) or `firewalld` (RHEL/CentOS) must be enabled.
    *   **IP Forwarding:** Must be disabled (`net.ipv4.ip_forward = 0`) unless the server is acting as a router/gateway.

#### 4.5 macOS Hardening Standards
For Apple hardware used by staff:

*   **4.5.1 System Preferences:**
    *   **FileVault 2:** Full disk encryption must be enabled.
    *   **Gatekeeper:** Must be set to "App Store and identified developers" or stricter.
    *   **Firewall:** Built-in firewall must be enabled; "Stealth Mode" enabled.

*   **4.5.2 User Accounts:**
    *   **Guest User:** Must be disabled.
    *   **Automatic Login:** Must be disabled.

#### 4.6 BYOD Minimum Viable Hardening
While Study GRC Inc. cannot enforce full CIS benchmarks on personal devices, volunteers and staff accessing organizational data on personal devices must certify the following:
1.  **OS Version:** The device is running a vendor-supported OS version (no Windows 7, no macOS High Sierra or older).
2.  **Encryption:** The device storage is encrypted (BitLocker/FileVault).
3.  **Authentication:** The device requires a password/PIN/Biometric to unlock.
4.  **Antivirus:** An active, updated antivirus solution is running.

#### 4.7 Configuration Management & Validation
*   **4.7.1 Golden Images:** The IT Operations team shall maintain "Golden Images" or Infrastructure-as-Code (IaC) scripts (e.g., Ansible, Terraform) that apply these standards automatically upon provisioning.
*   **4.7.2 Vulnerability Scanning:** Systems will be scanned monthly using authenticated scans to verify compliance with CIS Benchmarks.
*   **4.7.3 Drift Detection:** Any unauthorized changes to configuration files on production servers must trigger an alert to the Security Operations team.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Defines the hardening standards; approves exceptions; oversees compliance reporting. |
| **Director of IT Operations** | Ensures all "Golden Images" and deployment scripts comply with this Standard; manages the MDM solution. |
| **System Administrators / DevOps** | Applies hardening configurations; performs regular patching; remediates drift. |
| **Employees & Volunteers** | Ensures their assigned devices (and BYOD assets) meet the physical and logical security requirements; prohibits disabling security controls. |

### 6. Compliance and Enforcement
**Audit:** Compliance with this Standard will be verified through automated configuration scanning and annual internal audits.

**Enforcement:**
Failure to comply with this Standard puts the Organization and its community at risk.
*   **Technical Enforcement:** Non-compliant devices may be technically blocked from accessing the Study GRC Inc. network or cloud resources (Conditional Access).
*   **Disciplinary Action:** Personnel found to be intentionally bypassing hardening controls (e.g., disabling firewalls, rooting/jailbreaking devices) are subject to disciplinary action, up to and including termination of employment or volunteer assignment, per the *Employee Handbook* and *Volunteer Code of Conduct*.

### 7. References
*   **Center for Internet Security (CIS) Benchmarks:** [https://www.cisecurity.org/cis-benchmarks/](https://www.cisecurity.org/cis-benchmarks/)
*   **NIST SP 800-123:** Guide to General Server Security.
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-POL-040:** Patch Management Policy.
*   **IS-POL-022:** Bring Your Own Device (BYOD) Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Director of IT Operations | Initial release establishing CIS Benchmarks as the organizational standard. |