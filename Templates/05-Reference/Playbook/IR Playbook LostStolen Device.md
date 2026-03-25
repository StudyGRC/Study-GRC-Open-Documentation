### IR Playbook: Lost/Stolen Device

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PLB-003 |
| **Document Type** | Playbook / Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Incident Response Team Lead |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Playbook is to outline the specific, immediate actions required when a Study GRC Inc. computing device (laptop, smartphone, tablet, or external drive) is reported lost or stolen. This document aims to minimize the risk of unauthorized access to sensitive data—specifically youth participant data and intellectual property—and to ensure compliance with data breach notification laws, including **Texas Business & Commerce Code § 521.053** and **GDPR**.

### 2. Scope
This playbook applies to:
*   **Organization-Owned Devices:** All hardware assets purchased and issued by Study GRC Inc.
*   **BYOD (Bring Your Own Device):** Personal devices used by employees, contractors, or volunteers to access Study GRC Inc. resources (email, Slack, Drive, etc.), pursuant to the *Bring Your Own Device (BYOD) Policy*.
*   **Personnel:** All Board Directors, Officers, employees, volunteers, and contractors.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Remote Wipe** | A command sent via Mobile Device Management (MDM) software that erases data from a device. |
| **Encryption** | The process of encoding information (e.g., BitLocker, FileVault) so that only authorized parties can access it. |
| **MDM** | Mobile Device Management; software used to secure, monitor, and manage mobile devices. |
| **PII** | Personally Identifiable Information (e.g., names, addresses, SSNs). |
| **Sensitive Youth Data** | Any data regarding minors (under 18), including medical info, photos, or location data, protected under *COPPA* and the *Child and Youth Safeguarding Policy*. |

### 4. Procedures

#### 4.1 Phase 1: Identification and Reporting (The "Golden Hour")
**Time is critical.** The window to execute a remote wipe effectively is often limited to the battery life of the device.

1.  **User Reporting:**
    *   Any individual who discovers a device is missing must report it **immediately** (within 1 hour of discovery).
    *   **Reporting Channel:** Submit a ticket via the "Emergency Incident" portal OR contact the IT Help Desk via the emergency hotline.
    *   **Required Information:**
        *   Device Type (Laptop, Phone, Tablet).
        *   Asset Tag (if known).
        *   Last known location and time.
        *   Circumstances (e.g., "Left in Uber," "Stolen from car," "Misplaced at home").
        *   Whether the device was unlocked or logged in at the time of loss.

2.  **IT/Security Intake:**
    *   The Incident Response Team (IRT) creates an Incident Ticket (Severity: High).
    *   IRT verifies if the device is Organization-Owned or BYOD.

#### 4.2 Phase 2: Containment (Stop the Bleeding)
The IRT must execute the following steps immediately upon receipt of the report:

1.  **Execute Remote Lock/Wipe:**
    *   **Organization-Owned:** Log into the MDM console. Send a **Remote Wipe** command immediately. If a full wipe is not possible, send a **Device Lock** command with a custom message (e.g., "Property of Study GRC. Please contact [Email/Phone]").
    *   **BYOD:** Log into the MDM/MAM console. Execute an **Enterprise Wipe** (removing only Study GRC data/apps). If the device is not enrolled in MDM, proceed to Step 2 immediately.

2.  **Revoke Access Tokens (Kill Switch):**
    *   Reset the user’s Study GRC Single Sign-On (SSO) password immediately.
    *   Force a "Sign Out of All Sessions" via the Google Workspace and Slack admin consoles.
    *   Revoke any active VPN certificates associated with the device.
    *   Revoke MFA tokens associated with the device and require re-enrollment on a new device.

3.  **Physical Security (If applicable):**
    *   If the device contained physical access credentials (e.g., a saved door code or digital key), notify the Facilities Manager to change the code.

#### 4.3 Phase 3: Assessment and Classification
Once the device is secured (or confirmed unrecoverable), the IRT and Legal/Compliance must determine the exposure.

1.  **Encryption Verification:**
    *   Check MDM logs to verify if **Full Disk Encryption** (BitLocker/FileVault) was active and compliant at the time of the last check-in.
    *   *Note:* Under many regulations (including Texas law), loss of an encrypted device where the key was not compromised may not constitute a reportable breach.

2.  **Data Inventory Analysis:**
    *   Interview the user to determine what data was stored *locally* on the device (e.g., downloaded spreadsheets, cached emails).
    *   **Critical Check:** Did the device contain **Sensitive Youth Data** or unencrypted lists of donors/members?

3.  **Breach Determination:**
    *   **Low Risk:** Device was encrypted, strong password enabled, remote wipe confirmed successful, no local sensitive data. -> *Incident Closed.*
    *   **High Risk:** Device unencrypted, weak password, wipe failed, or confirmed local storage of PII/Youth Data. -> *Escalate to Data Breach Response Protocol.*

#### 4.4 Phase 4: Eradication and Recovery
1.  **Police Report:**
    *   If the device was stolen, the User (or Ops Team) must file a police report within 24 hours and provide a copy to Study GRC. This is required for insurance claims and potential asset write-offs.

2.  **Asset Deprovisioning:**
    *   Mark the device as "Lost/Stolen" in the Asset Inventory system.
    *   Initiate the *Remote Wipe* command to remain pending indefinitely (in case the device connects to the internet months later).

3.  **User Restoration:**
    *   Provision a replacement device for the user.
    *   Restore user data from the cloud backup (Google Drive/OneDrive).
    *   Conduct a brief re-training with the user on physical asset security.

#### 4.5 Phase 5: Post-Incident Activity
1.  **Documentation:**
    *   Update the Incident Ticket with all actions taken, timestamps, and the final classification.
    *   File the *Lost/Stolen Device Report* in the compliance repository.

2.  **Lessons Learned:**
    *   If the device was unencrypted or not in MDM, identify the process failure that allowed a non-compliant device to access organizational data.
    *   Update the *Master Information Security Policy* or *MDM Enrollment Procedure* if gaps are found.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **User** | Report loss immediately (within 1 hour). File police report if stolen. Cooperate with data inventory interview. |
| **Incident Response Team (IT)** | Execute remote wipe/lock. Reset passwords/tokens. Verify encryption status. |
| **CISO** | Oversee containment. Approve final risk classification. |
| **Legal / Compliance** | Determine if the loss constitutes a "Data Breach" under Texas § 521.053 or GDPR. Manage external notifications if required. |
| **HR / Ops** | Process asset write-off. Manage disciplinary action if negligence was involved. |

### 6. Compliance and Enforcement
**Failure to Report:** Failure to report a lost or stolen device immediately is a serious violation of the *Code of Ethics* and *Information Security Policy*. It prevents the organization from mitigating risks to youth participants and members.

**Negligence:** If the loss is determined to be a result of gross negligence (e.g., leaving a laptop visible in an unlocked car), the employee or volunteer may be subject to disciplinary action, up to and including termination and potential financial liability for the replacement cost of the asset, as permitted by law.

### 7. References
*   **IS-POL-001:** Master Information Security Policy
*   **IS-POL-005:** Bring Your Own Device (BYOD) Policy
*   **IS-PLB-001:** Incident Response Plan (Master)
*   **LEG-POL-002:** Data Breach Notification Procedure
*   **Regulation:** Texas Business & Commerce Code § 521.053 (Notification Required Following Breach of Security)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Legal Officer | Initial Draft |