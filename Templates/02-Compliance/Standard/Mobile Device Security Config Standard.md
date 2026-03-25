### Mobile Device Security Config Standard

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-024 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Standard is to establish mandatory technical configuration requirements for all mobile devices (smartphones and tablets) that access, process, or store Study GRC Inc. data. This Standard aligns with **NIST SP 800-124 Rev. 2** (Guidelines for Managing the Security of Mobile Devices in the Enterprise) to mitigate risks associated with lost or stolen devices, malware, and unauthorized access in our remote-first environment.

This Standard supports **Bylaws Article IX (Policies & Data Protection)**, specifically Section 9.2, by ensuring technical controls are in place to maintain the confidentiality and integrity of the Organization's intellectual property and sensitive data.

### 2. Scope
This Standard applies to:
*   **Devices:** All mobile devices (iOS, Android, iPadOS) owned by Study GRC Inc., and all personally owned devices (BYOD) used by employees, contractors, or volunteers to access non-public organizational resources (e.g., email, Drive, CRM, Slack).
*   **Users:** All Directors, Officers, employees, contractors, and volunteers with access to Tier 2 (Internal) or Tier 3 (Confidential) data.

**Exclusions:**
*   Devices used solely by "Community Participants" (as defined in Bylaws Section 2.1) who do not hold an official role or access internal systems.
*   Devices used exclusively for Multi-Factor Authentication (MFA) generation without accessing organizational data directly.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **MDM** | Mobile Device Management. Software used to monitor, manage, and secure mobile devices. |
| **Containerization** | A method of isolating corporate applications and data from personal applications and data on a BYOD device. |
| **Jailbreaking/Rooting** | The process of removing software restrictions imposed by the device manufacturer, granting root access to the file system. |
| **Sideloading** | Installing applications from sources other than the official manufacturer app stores (e.g., Apple App Store, Google Play). |
| **Remote Wipe** | A security feature that allows an administrator to delete data from a mobile device remotely. |

### 4. Standards

All mobile devices within the scope must adhere to the following configuration standards. These settings will be enforced via the Organization’s MDM solution where technically feasible.

#### 4.1 General Configuration & Enrollment
4.1.1 **MDM Enrollment:** All devices accessing Study GRC Inc. email or file storage must be enrolled in the Organization’s MDM platform (e.g., Google Endpoint Management, Microsoft Intune, or Jamf).
4.1.2 **Asset Inventory:** All devices must be registered in the IT Asset Inventory with the user’s name, device model, and OS version.
4.1.3 **Least Privilege:** Devices must only be granted access to the specific data and applications required for the user's role.

#### 4.2 Operating System Integrity
4.2.1 **Supported OS Versions:** Devices must run a vendor-supported operating system.
*   **iOS/iPadOS:** Current version or the immediate predecessor (N-1).
*   **Android:** Versions receiving active security patches from Google or the OEM.
4.2.2 **Patching:** Security updates must be applied within 14 days of release. Automatic updates must be enabled.
4.2.3 **System Tampering:** Devices that are "Jailbroken" (iOS) or "Rooted" (Android) are **strictly prohibited**. The MDM solution must be configured to detect and immediately block access to any compromised device.

#### 4.3 Authentication and Access Control
4.3.1 **Passcode/PIN:** A device passcode is mandatory.
*   **Minimum Length:** 6 digits (numeric) or alphanumeric.
*   **Complexity:** Simple sequences (e.g., 123456, 111111) are prohibited.
4.3.2 **Biometrics:** Touch ID, Face ID, or Android Biometric Unlock are permitted as an alternative to entering the PIN, provided the underlying PIN meets the requirements in 4.3.1.
4.3.3 **Screen Lock Timeout:** Devices must automatically lock after a maximum of **15 minutes** of inactivity.
4.3.4 **Failed Attempts:** The device (or the corporate container) must wipe organizational data after **10 consecutive failed unlock attempts**.

#### 4.4 Data Protection and Encryption
4.4.1 **Encryption:** Full Disk Encryption (FDE) must be enabled for all data stored on the device.
4.4.2 **Containerization (BYOD):** For personally owned devices, a "Work Profile" or encrypted container must be used to separate Study GRC Inc. data from personal data.
4.4.3 **Data Leakage Prevention (DLP):**
*   **Copy/Paste:** Copying data from the Work Profile to the Personal Profile must be disabled.
*   **Screen Capture:** Taking screenshots within the Work Profile (Android) or managed apps (iOS) must be disabled where sensitive data is displayed.
*   **Cloud Backup:** Backup of organizational data to personal cloud accounts (e.g., personal iCloud or personal Google Drive) is prohibited.

#### 4.5 Network and Connectivity
4.5.1 **Wi-Fi Security:** Devices must not connect to unsecured (Open/WEP) public Wi-Fi networks to access organizational data unless a VPN is active.
4.5.2 **Bluetooth:** Bluetooth must be set to "Non-discoverable" when not pairing.
4.5.3 **USB Debugging:** USB Debugging (Android) must be disabled.

#### 4.6 Application Security
4.6.1 **Allowed Sources:** Applications must only be installed from official stores (Apple App Store, Google Play Store). Sideloading is prohibited.
4.6.2 **App Vetting:** The CISO maintains a list of "High Risk" applications. The MDM shall be configured to detect and alert/block if prohibited apps are installed within the Work Profile.
4.6.3 **Browser Security:** Anti-phishing and Safe Browsing features must be enabled on the default browser used for work.

#### 4.7 Physical Security & Loss Reporting
4.7.1 **Possession:** Users must maintain physical control of the device at all times in public spaces.
4.7.2 **Reporting:** Users must report a lost or stolen device to the IT Help Desk or CISO immediately, and no later than **2 hours** after discovery of the loss.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **CISO** | Defines security configuration baselines; reviews this Standard annually; approves exceptions. |
| **IT Administrator** | Configures the MDM policies to enforce this Standard; monitors compliance dashboards; executes remote wipes when authorized. |
| **Users (Employees/Volunteers)** | Keep devices updated; ensure physical security; report loss/theft immediately; consent to the installation of the MDM profile. |
| **HR / Volunteer Coordinator** | Ensures the "Mobile Device Security Config Standard" is acknowledged during onboarding. |

### 6. Compliance and Enforcement
**6.1 Monitoring:** Compliance with this standard is monitored continuously via the MDM solution. Devices found to be non-compliant (e.g., outdated OS, rooted) will be automatically quarantined and blocked from accessing Study GRC Inc. resources until remediated.

**6.2 Remote Wipe Authority:**
*   **Corporate Devices:** The Organization reserves the right to fully wipe corporate-owned devices at any time.
*   **BYOD Devices:** The Organization reserves the right to wipe the **Work Profile/Container** (removing only organizational data) upon termination of employment/service or report of device loss. Full device wipes on BYOD are avoided unless the device is fully compromised and the user consents.

**6.3 Disciplinary Action:** Failure to comply with this Standard, including attempting to bypass MDM controls or jailbreak a device used for work, may result in disciplinary action, up to and including termination of employment or volunteer assignment, in accordance with the *Progressive Discipline Policy*.

### 7. References
*   **NIST SP 800-124 Rev. 2:** Guidelines for Managing the Security of Mobile Devices in the Enterprise.
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-POL-008:** Bring Your Own Device (BYOD) Policy.
*   **HR-POL-003:** Remote Work and Telecommuting Policy.
*   **Bylaws of Study GRC Inc.:** Article IX (Intellectual Property & Data Protection).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name], CISO | Initial Release aligned with NIST SP 800-124. |