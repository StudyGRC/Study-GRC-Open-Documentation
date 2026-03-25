### Passkey and Passwordless Standard

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-020 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this standard is to define the technical requirements and acceptable use of FIDO2/WebAuthn cryptographic credentials ("Passkeys") within Study GRC Inc. This standard aims to eliminate the use of shared secrets (passwords) wherever technically feasible to mitigate risks associated with phishing, credential stuffing, and weak password hygiene.

This standard supports the Organization’s commitment to data protection as outlined in **Article IX, Section 9.2** of the Bylaws and aligns with the National Institute of Standards and Technology (NIST) Digital Identity Guidelines (SP 800-63B).

### 2. Scope
This standard applies to:
*   **Personnel:** All employees, Board Directors, Operational Officers, and volunteers with access to Study GRC Inc. systems.
*   **Systems:** All Organization-managed Identity Providers (IdP), Single Sign-On (SSO) solutions, workstations, and critical applications that support FIDO2/WebAuthn protocols.
*   **Devices:** All Organization-issued hardware and approved Bring Your Own Device (BYOD) endpoints used for authentication.

**Exclusions:** Legacy systems that do not support FIDO2/WebAuthn protocols are excluded from this standard but remain subject to the *Password Policy (IS-STD-018)* and *Multi-Factor Authentication Mandate (IS-POL-015)*.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **FIDO2** | An open authentication standard hosted by the FIDO Alliance, consisting of the W3C Web Authentication (WebAuthn) specification and the Client to Authenticator Protocol (CTAP). |
| **Passkey** | A FIDO2 credential that is discoverable (resident) on an authenticator. It replaces the need for a username and password. |
| **Platform Authenticator** | An authenticator embedded in a computing device (e.g., Windows Hello, Apple TouchID/FaceID, Android Biometrics). |
| **Roaming Authenticator** | A portable hardware authenticator that connects across different devices (e.g., YubiKey, Titan Security Key). |
| **Synced Passkey** | A passkey that is synchronized across a user's devices via a cloud provider (e.g., iCloud Keychain, Google Password Manager). |
| **Device-Bound Passkey** | A passkey that cannot be exported from the specific hardware authenticator on which it was created. |
| **User Verification (UV)** | A method to verify that the person authenticating is the correct user, typically via biometrics (fingerprint/face) or a local PIN. |

### 4. Standards

#### 4.1 Approved Authenticator Types
Study GRC Inc. authorizes the use of the following FIDO2-compliant authenticators. Selection is based on the user's role and risk profile.

1.  **Platform Authenticators (Tier 1 - General Use):**
    *   **Windows:** Windows Hello for Business (TPM 2.0 required).
    *   **macOS/iOS:** TouchID or FaceID (Secure Enclave required).
    *   **Android:** Biometric authentication (Titan M chip or equivalent TEE required).
2.  **Roaming Hardware Authenticators (Tier 2 - High Security):**
    *   **YubiKey:** Series 5 or Bio Series (FIDO2/WebAuthn supported).
    *   **Google Titan:** Security Key (FIDO2 supported).
    *   **Requirement:** Roaming keys must be FIPS 140-2 or FIPS 140-3 validated for users with access to Federal Grant financial data (2 CFR 200 compliance).

#### 4.2 Technical Configuration Requirements
All Relying Parties (applications/IdPs) managed by Study GRC Inc. must be configured to enforce the following parameters during Passkey registration and authentication:

*   **User Verification (UV):** Must be set to `preferred` or `required`.
    *   *Note:* If the authenticator does not support biometrics, a local PIN is mandatory.
*   **User Presence (UP):** Must always be `true`. The user must physically interact with the device (touch or button press) to authorize the login.
*   **Attestation:**
    *   **Enterprise/Managed Devices:** Attestation should be set to `Direct` or `Enterprise` to verify the authenticator model and compliance.
    *   **BYOD/Personal Devices:** Attestation may be set to `None` or `Indirect` to preserve user privacy while maintaining cryptographic security.
*   **Discoverable Credentials:** Must be enabled to allow for passwordless flows (username-less login).

#### 4.3 Role-Based Implementation
To balance security and cost, the following hierarchy applies:

*   **High-Privilege Users (Admins, C-Suite, Finance, HR):**
    *   **Primary:** Must use a **Device-Bound Passkey** (Roaming Hardware Key) or a managed Platform Authenticator on a corporate device.
    *   **Synced Passkeys:** Prohibited for root/admin access to critical infrastructure.
*   **Standard Users (Volunteers, General Staff):**
    *   **Primary:** May use **Synced Passkeys** (e.g., iCloud Keychain, 1Password) or Platform Authenticators.
    *   **Objective:** Reduce friction to encourage adoption of phishing-resistant authentication.

#### 4.4 Registration and Lifecycle Management
*   **Initial Registration:** A Passkey may only be registered after the user has authenticated via a high-assurance method (e.g., initial onboarding video verification with HR, or an existing MFA-protected session).
*   **Naming Convention:** Users must label Passkeys clearly in the IdP (e.g., "MacBook Pro - TouchID", "YubiKey 5C - Backup").
*   **Lost/Stolen Devices:**
    *   Users must report lost devices containing Passkeys immediately to the CISO or IT Support.
    *   The specific Passkey associated with the lost device must be revoked from the IdP immediately.
*   **Offboarding:** Upon termination of employment or volunteer service, all registered Passkeys associated with the user's corporate identity must be revoked/deleted from the IdP.

#### 4.5 Fallback Mechanisms
In the event a Passkey is unavailable or a device is lost:
*   **Preferred Fallback:** A secondary registered Passkey (e.g., a backup YubiKey).
*   **Acceptable Fallback:** High-entropy password **PLUS** a Time-based One-Time Password (TOTP).
*   **Prohibited Fallback:** SMS or Email-based One-Time Passwords (OTP) are strictly prohibited as a fallback for Passkey-enabled accounts due to susceptibility to interception.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Defines the standard; approves new authenticator models; audits compliance logs. |
| **IT Systems Administrator** | Configures Identity Providers (IdP) to support FIDO2; enforces User Verification policies; manages credential revocation. |
| **Operational Officers** | Ensure their departmental staff have appropriate hardware/software to support this standard. |
| **Users (Staff/Volunteers)** | Protect their authenticators; set strong PINs for keys; report lost authenticators immediately. |

### 6. Compliance and Enforcement
Failure to comply with this standard—including the sharing of physical authenticators or bypassing User Verification requirements—may result in disciplinary action, up to and including termination of employment or volunteer assignment.

For Board Directors, violation of this standard constitutes a breach of the **Board of Directors Code of Ethics and Conduct** and may be grounds for removal for cause under **Bylaws Article III, Section 3.6**.

### 7. References
*   **Internal:**
    *   Master Information Security Policy (IS-POL-001)
    *   Access Control Policy (IS-POL-005)
    *   Multi-Factor Authentication Mandate (IS-POL-015)
*   **External:**
    *   FIDO Alliance: *FIDO2: Web Authentication (WebAuthn)*
    *   NIST SP 800-63B: *Digital Identity Guidelines - Authentication and Lifecycle Management* (Authenticator Assurance Level 3 alignment)
    *   2 CFR 200.303: *Internal Controls*

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Compliance Architect | Initial Draft aligned with FIDO2 and Bylaws. |