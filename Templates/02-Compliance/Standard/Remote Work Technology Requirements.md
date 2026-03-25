### Remote Work Technology Requirements

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-009 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Standard is to define the minimum technical security configurations and environmental requirements for all remote work locations and devices used to access **Study GRC Inc.** data and systems. As a remote-first organization handling sensitive community and youth data, strict adherence to these requirements is necessary to maintain the **Confidentiality, Integrity, and Availability** of organizational assets and to mitigate risks associated with unsecured networks and unmanaged devices.

### 2. Scope
This Standard applies to all **Personnel** (Employees, Board Directors, Officers, Volunteers, and Contractors) who access Study GRC Inc. resources from a remote location (e.g., home office, co-working space, coffee shop).

*   **Inclusions:** Company-issued devices and personal devices (BYOD) approved for business use.
*   **Exclusions:** Public users accessing the Organization’s public-facing website or open-source repositories without privileged credentials.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **BYOD** | **Bring Your Own Device**. The practice of allowing personnel to use their own computers, smartphones, or tablets for work purposes. |
| **Endpoint** | Any device (laptop, desktop, mobile phone) that connects to the Organization's network or cloud services. |
| **MFA** | **Multi-Factor Authentication**. A security system that requires more than one method of authentication from independent categories of credentials to verify the user's identity. |
| **VPN** | **Virtual Private Network**. An encrypted connection over the Internet from a device to a network. |
| **EOL** | **End of Life**. Software or hardware that is no longer supported or patched by the vendor. |

### 4. Requirements

All remote work environments and devices must strictly adhere to the following technical specifications. Failure to meet these standards prohibits the user from accessing Study GRC Inc. internal systems.

#### 4.1 Operating System and Patching
To prevent exploitation of known vulnerabilities:
*   **4.1.1 Supported OS:** Devices must run an Operating System currently supported by the vendor.
    *   **Windows:** Windows 10 or 11 (Pro or Enterprise recommended).
    *   **macOS:** Current version minus two (e.g., if current is macOS 14, minimum is macOS 12).
    *   **Linux:** Current LTS distribution (e.g., Ubuntu LTS).
    *   **Mobile:** iOS (latest - 2) or Android (latest - 2).
*   **4.1.2 Automatic Updates:** Automatic security updates/patching must be **enabled** and set to install within 7 days of release.
*   **4.1.3 EOL Prohibition:** The use of End-of-Life (EOL) operating systems (e.g., Windows 7, Windows 8.1) is strictly **prohibited**.

#### 4.2 Device Security Configuration
All endpoints accessing Organization data must utilize:
*   **4.2.1 Full Disk Encryption:** Encryption must be enabled for the entire drive.
    *   **Windows:** BitLocker.
    *   **macOS:** FileVault.
    *   **Linux:** LUKS or equivalent.
*   **4.2.2 Authentication:** Devices must be secured with a strong password (minimum 12 characters) or biometric authentication (FaceID, TouchID, Windows Hello).
*   **4.2.3 Screen Lock:** Devices must be configured to automatically lock the screen after a maximum of **15 minutes** of inactivity.
*   **4.2.4 Firewall:** Host-based firewalls (e.g., Windows Defender Firewall) must be **enabled**.
*   **4.2.5 Anti-Malware:** An active, up-to-date Anti-Virus or Endpoint Detection and Response (EDR) solution must be installed and running.

#### 4.3 Network Security
*   **4.3.1 Home Wi-Fi:**
    *   Must use **WPA2-AES** or **WPA3** encryption. WEP and WPA-TKIP are prohibited.
    *   Default router administrator passwords must be changed.
    *   Firmware on networking equipment must be kept up to date.
*   **4.3.2 Public Wi-Fi:** Accessing internal systems (Google Workspace, Slack, Financial Systems) over public Wi-Fi (e.g., airports, cafes) is **prohibited** unless a trusted **VPN** is active.
*   **4.3.3 IoT Isolation:** It is recommended that work devices be placed on a separate "Guest" VLAN or network segment from high-risk IoT devices (smart bulbs, fridges, etc.) within the home.

#### 4.4 Access Control and Identity
*   **4.4.1 MFA Mandate:** **Multi-Factor Authentication (MFA)** must be enabled on all accounts accessing Study GRC Inc. resources. SMS-based MFA is discouraged; Authenticator Apps (TOTP) or Hardware Keys (FIDO2/YubiKey) are required where supported.
*   **4.4.2 Account Separation:** If a device is shared with family members (e.g., a home PC), the Study GRC Inc. user must utilize a **separate user profile/account** on the OS that is password-protected and inaccessible to other household members.
    *   *Note:* Devices used to access sensitive **Youth/Minor data** must **not** be shared with other household members under any circumstances.

#### 4.5 Physical Security
*   **4.5.1 Theft Prevention:** Devices must not be left unattended in public spaces or visible in vehicles.
*   **4.5.2 Privacy Filters:** If working in public spaces where screens are visible to others ("shoulder surfing"), a privacy screen filter must be used.
*   **4.5.3 Voice Privacy:** Professional discussions involving confidential information must not take place in public areas or near smart listening devices (e.g., Alexa, Google Home) unless the microphone on the listening device is muted.

#### 4.6 Prohibited Software and Hardware
*   **4.6.1 Jailbreaking/Rooting:** Devices that have been "jailbroken" (iOS) or "rooted" (Android) are **prohibited** from accessing Organization data.
*   **4.6.2 Peer-to-Peer (P2P):** The use of P2P file-sharing software (e.g., BitTorrent) is prohibited on devices while they are connected to the Organization's VPN or logged into Organization accounts.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Personnel (Users)** | Ensure their remote environment and devices meet these requirements prior to accessing systems. Report lost or stolen devices immediately. |
| **CISO / IT Security** | Maintain this Standard. Provide guidance on configuration. Conduct periodic audits or automated health checks of devices accessing the network. |
| **Management** | Ensure their direct reports have the necessary resources (hardware/software) to meet these requirements. |
| **Board of Directors** | Review and approve budget allocations necessary to support secure remote work technologies. |

### 6. Compliance and Enforcement
**Automated Verification:** Study GRC Inc. reserves the right to use technical controls (e.g., Conditional Access Policies) to block access from devices that do not meet minimum OS or encryption requirements.

**Disciplinary Action:** Failure to comply with this Standard may result in the revocation of remote access privileges, disciplinary action up to and including termination of employment or volunteer assignment, and potential legal action depending on the severity of the violation.

### 7. References
*   **IS-POL-001:** Master Information Security Policy
*   **HR-POL-003:** Remote Work and Telecommuting Policy
*   **IS-POL-008:** Bring Your Own Device (BYOD) Policy
*   **External:** NIST Special Publication 800-46 Rev. 2 (Guide to Enterprise Telework, Remote Access, and Bring Your Own Device Security)
*   **External:** CISA Cyber Performance Goals (CPG) 2.1 (MFA) & 4.1 (Asset Inventory)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Legal Officer | Initial Release aligned with Governance Framework. |