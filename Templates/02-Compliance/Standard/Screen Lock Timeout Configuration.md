### Screen Lock Timeout Configuration

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-015 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Standard is to minimize the risk of unauthorized access to Study GRC Inc. ("the Organization") information systems and data. By enforcing automated session locks, the Organization mitigates the risk of "insider threats" or opportunistic access when a user leaves their workstation unattended.

This Standard explicitly satisfies **NIST SP 800-53 Control AC-11 (Session Lock)** and supports the data protection mandates outlined in **Article IX (Policies & Data Protection)** of the Organization's Bylaws.

### 2. Scope
This Standard applies to all computing devices that process, store, or transmit Organization data.
*   **Applies to:**
    *   Organization-owned workstations (laptops, desktops).
    *   Personal devices used for Organization business under the **Bring Your Own Device (BYOD) Policy**.
    *   Mobile devices (smartphones, tablets) accessing Organization email or systems.
    *   All employees, contractors, Board Directors, and volunteers with access to non-public data.
*   **Exclusions:**
    *   Public-facing kiosk displays (must be configured to prevent interactive login).
    *   Servers (governed by separate console timeout configurations).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Session Lock** | A temporary suspension of user activity that hides the screen contents and requires re-authentication to resume. |
| **Idle Time** | The period of time a device remains inactive (no keyboard, mouse, or touch input) before a lock is triggered. |
| **Privileged Account** | An account with elevated permissions (e.g., System Administrator, CISO, Finance Director) capable of altering system configurations or accessing sensitive financial/youth data. |
| **MDM** | Mobile Device Management; software used to enforce policies on devices remotely. |
| **NIST AC-11** | The National Institute of Standards and Technology control requirement for "Session Lock." |

### 4. Standards

#### 4.1 General Session Lock Requirement
In accordance with **NIST AC-11**, all devices accessing Organization resources must be configured to initiate a session lock after a defined period of inactivity. The session lock must:
1.  Clear or obscure the display so that no information is visible.
2.  Retain the system state (applications remain open in the background).
3.  Require re-authentication (password, PIN, biometric, or smart card) to unlock.

#### 4.2 Maximum Idle Timeouts
The following maximum idle times are mandatory. Users may configure shorter times but may not exceed these limits:

| Device / User Role | Maximum Idle Time |
| :--- | :--- |
| **Standard Workstations** (Volunteers/General Staff) | **15 Minutes** |
| **Privileged Access Workstations** (Admins, HR, Finance) | **10 Minutes** |
| **Mobile Devices** (iOS/Android) | **5 Minutes** |
| **High-Risk Environments** (Public spaces, conferences) | **5 Minutes** (Recommended) |

#### 4.3 Screen Obscuration
The screen lock mechanism must display a blank screen, a static image, or a screensaver pattern.
*   **Prohibited:** Screensavers that display sensitive system information (e.g., IP address, username, OS version) or dynamic content that could reveal Organization data.
*   **Prohibited:** "Ticker" style screensavers displaying email subjects or instant messages.

#### 4.4 Manual Session Lock
Users are required to manually lock their sessions whenever they physically leave their immediate workspace, regardless of the duration of absence.
*   **Windows:** `Windows Key + L`
*   **macOS:** `Cmd + Ctrl + Q` or `Apple Menu > Lock Screen`

#### 4.5 Configuration Enforcement
*   **Organization-Owned Devices:** Settings must be enforced via Group Policy Object (GPO) or Mobile Device Management (MDM) profiles where technically feasible. Users must be restricted from increasing the timeout limit beyond the maximums defined in Section 4.2.
*   **BYOD:** Users utilizing personal devices must manually configure their operating system to meet or exceed these standards as a condition of access, pursuant to the **BYOD Policy**.

#### 4.6 Disable Lock Prohibitions
The use of hardware "mouse jigglers" or software tools (e.g., "Caffeine," "Move Mouse") designed to simulate activity and bypass screen lock policies is strictly prohibited on any device while connected to the Organization's network or VPN.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Define timeout thresholds; oversee MDM configuration; approve exceptions for specific use cases (e.g., presentations). |
| **IT System Administrators** | Implement technical controls (GPO/MDM) to enforce timeouts; audit configurations annually. |
| **Employees & Volunteers** | Manually lock devices when stepping away; ensure personal devices (BYOD) comply with this standard. |
| **Management** | Ensure staff are aware of this standard and do not attempt to circumvent controls. |

### 6. Compliance and Enforcement
Failure to comply with this Standard constitutes a violation of the Organization's security protocols.
*   **Technical Enforcement:** Devices found to be non-compliant may be quarantined or blocked from accessing Organization resources until remediated.
*   **Disciplinary Action:** Personnel found intentionally bypassing these controls (e.g., using mouse jigglers) may face disciplinary action, up to and including termination of employment or volunteer assignment, in accordance with the **Employee Handbook** and **Bylaws Article III (Removal of Directors/Officers)**.

### 7. References
*   **NIST SP 800-53 Rev. 5:** Control AC-11 (Session Lock).
*   **Study GRC Inc. Bylaws:** Article IX (Policies & Data Protection) & Article III (Governance).
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-POL-008:** Bring Your Own Device (BYOD) Policy.
*   **IS-STD-012:** Password Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name], CISO | Initial Release aligned with NIST AC-11. |