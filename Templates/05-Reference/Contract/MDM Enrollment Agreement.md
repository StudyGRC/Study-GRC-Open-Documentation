### MDM Enrollment Agreement

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-AGR-001 |
| **Document Type** | Contract / Agreement |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | IT Operations Manager |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Mobile Device Management (MDM) Enrollment Agreement (the "Agreement") is to define the terms under which Study GRC Inc. (the "Organization") grants access to corporate resources via mobile and remote devices. This Agreement balances the Organization’s need to secure Confidential Information and Intellectual Property, as defined in **Article IX of the Bylaws**, with the User's right to privacy. It establishes the technical controls, rights, and responsibilities associated with enrolling a device in the Organization’s MDM solution.

### 2. Scope
This Agreement applies to all employees, contractors, volunteers, and Board members (collectively "Users") who wish to access Organization data (including but not limited to email, Slack, Google Workspace, and donor databases) using:
1.  **Organization-Owned Devices:** Devices purchased and issued by Study GRC Inc.
2.  **Personally-Owned Devices (BYOD):** Personal devices used for organizational business.

**Exclusions:** Devices that do not access non-public organizational data (e.g., a personal phone used solely for public website browsing) are exempt from MDM enrollment.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **MDM (Mobile Device Management)** | Software that allows IT administrators to secure, manage, and monitor mobile devices accessing organizational data. |
| **BYOD (Bring Your Own Device)** | A policy allowing Users to use personally owned devices for work-related activities. |
| **Enterprise Wipe** | A remote command that removes *only* Organization-managed applications, data, and profiles from a device, leaving personal data intact. |
| **Full Device Wipe** | A remote command that resets the device to factory settings, erasing *all* data (personal and organizational). |
| **Jailbreaking/Rooting** | The process of removing software restrictions imposed by the device manufacturer, which compromises security. |
| **Confidential Information** | As defined in the Non-Disclosure Agreement (NDA) and Bylaws Article IX, including donor lists, student data, and proprietary curriculum. |

### 4. Agreement Terms

#### 4.1. Condition of Access
Enrollment in the Organization’s MDM solution is a mandatory condition for accessing internal networks and data on mobile devices. Users who decline enrollment may not use the device for organizational business and will be restricted to web-only access via non-mobile endpoints where applicable.

#### 4.2. Organization Rights and Technical Controls
By enrolling a device, the User grants the Organization the authority to enforce the following security configurations:
*   **Passcode Enforcement:** Requiring a minimum complexity passcode (e.g., 6 digits) and auto-lock timeout.
*   **Encryption:** Enforcing full-disk encryption to protect data at rest.
*   **Application Management:** Installing, updating, or removing Organization-managed applications (e.g., Google Drive, Slack, Authenticator).
*   **OS Updates:** Requiring the device to run a supported, patched version of the Operating System.
*   **Compliance Checks:** Detecting if the device has been Jailbroken/Rooted or if security protections are disabled.

#### 4.3. Privacy and Data Limitations (What We Cannot See)
To protect User privacy, the Organization explicitly configures the MDM solution to **prevent** administrative access to the following personal data on BYOD devices:
*   Personal text messages (SMS/MMS) and personal emails.
*   Personal photos and video galleries.
*   Browser history.
*   Call history.
*   Personal contacts.
*   GPS Location (except when "Lost Mode" is explicitly triggered by the User or for Organization-Owned devices reported stolen).

#### 4.4. Remote Wipe Authority
*   **BYOD Devices:** The Organization reserves the right to perform an **Enterprise Wipe** (removing only work data) upon termination of employment/service, report of a security breach, or if the device is non-compliant. The Organization will make reasonable efforts to avoid a Full Device Wipe on BYOD hardware unless explicitly requested by the User (e.g., in theft scenarios) or if technical limitations prevent a selective wipe.
*   **Organization-Owned Devices:** The Organization reserves the right to perform a **Full Device Wipe** at any time for security or asset management purposes.

#### 4.5. User Obligations
The User agrees to:
1.  **Report Loss/Theft:** Immediately report a lost or stolen device to the IT/Security team to initiate protective measures (e.g., locking or wiping).
2.  **Maintain Integrity:** Not attempt to remove the MDM profile while retaining access to corporate data, nor attempt to jailbreak/root the device.
3.  **Backups:** Maintain personal backups of their own data (photos, contacts). The Organization is not responsible for the loss of personal data resulting from a device wipe (Enterprise or Full) necessitated by security protocols.

#### 4.6. Intellectual Property
Pursuant to **Bylaws Article IX, Section 9.3**, all Work Product created, stored, or transmitted via the enrolled device regarding the Organization's business remains the sole property of Study GRC Inc. The MDM solution is a tool to secure this Intellectual Property.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **User** | Enrolls device, maintains compliance with security policies, and backs up personal data. |
| **IT Operations** | Configures MDM profiles, ensures privacy settings are active, and executes wipe commands only when authorized. |
| **CISO** | Authorizes wipe commands, audits MDM logs for privacy compliance, and updates this Agreement based on regulatory changes. |
| **HR / Volunteer Coordinator** | Notifies IT of User departures to trigger the offboarding/Enterprise Wipe process. |

### 6. Compliance and Enforcement
Failure to comply with this Agreement (e.g., removing the MDM profile to bypass security while accessing data) constitutes a violation of the **Acceptable Use Policy** and **Information Security Policy**.

*   **Consequences:** Violations may result in immediate revocation of access to Organization systems, disciplinary action up to and including termination of employment or volunteer assignment, and legal action if Intellectual Property is compromised.
*   **Liability:** The Organization is held harmless for any personal data loss incurred during necessary security operations (e.g., remote wiping a compromised device) as permitted by law.

### 7. References
*   **Study GRC Inc. Bylaws (Article IX - IP & Data)**
*   **IS-POL-001:** Master Information Security Policy
*   **IS-POL-008:** Bring Your Own Device (BYOD) Policy
*   **IS-POL-004:** Acceptable Use Policy
*   **NIST SP 800-124 Rev. 2:** Guidelines for Managing the Security of Mobile Devices in the Enterprise

### 8. Acknowledgment and Signature

By signing below, I acknowledge that I have read and understood the MDM Enrollment Agreement. I consent to the installation of the MDM agent on my device and agree to the terms regarding security controls and remote data deletion.

**Device Type:** ☐ Personal (BYOD)  ☐ Organization-Owned

**User Name (Print):** __________________________________________________

**User Signature:** __________________________________________________

**Date:** __________________________

**Device Serial Number / ID:** ________________________________________