### Password Manager Recommendation

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-GUD-018 |
| **Document Type** | Guideline |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-26 |
| **Next Review Date** | 2025-10-26 (Bi-Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | IT Security Manager |
| **Classification** | Internal |

### 1. Purpose
The purpose of this guideline is to assist Study GRC Inc. ("the Organization") personnel in selecting and utilizing a Password Manager to secure credentials. While the *Password Policy (IS-STD-018)* mandates password complexity and prohibits reuse, the human brain is incapable of memorizing unique, complex passwords for every service.

This document bridges the gap between security requirements and **usability**, ensuring that staff and volunteers can maintain high security standards without impeding their workflow or resorting to insecure practices (e.g., writing passwords on sticky notes or spreadsheets).

### 2. Scope
This guideline applies to all **Directors, Officers, Operational Leadership, Volunteers, and Contractors** who access Organization systems or data.

*   **In Scope:** Selection, installation, and configuration of password management software for Organization-related accounts.
*   **Exclusions:** Management of API keys, service account secrets, or machine-to-machine credentials, which should be handled via the *Secrets Management Standard*.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Password Manager** | An encrypted software application used to store, generate, and manage passwords and other credentials. |
| **Master Password** | The single, strong passphrase used to decrypt the Password Manager vault. This is the only password the user must memorize. |
| **Zero-Knowledge Architecture** | A security model where the service provider (the Password Manager vendor) has no knowledge of, and no way to access, the data stored in the user's vault. |
| **Vault** | The encrypted database where credentials, notes, and identities are stored. |
| **2FA / MFA** | Two-Factor or Multi-Factor Authentication. A security process in which the user provides two different authentication factors to verify themselves. |

### 4. Guidelines

#### 4.1 The Necessity of Password Managers
To comply with the Organization's *Password Policy*, users must not reuse passwords across sites and must use high-entropy (random) strings. A Password Manager is the recommended tool to achieve this compliance. It reduces cognitive load by requiring the user to remember only one strong **Master Password**.

#### 4.2 Recommended Solutions
In alignment with the Organization's mission to support **open-source resources** (Bylaws Article I, Section 1.3), the Organization prioritizes tools that are transparent and auditable.

**Primary Recommendation:**
*   **Bitwarden:** An open-source, zero-knowledge password manager. It offers a robust free tier and affordable enterprise options. It is cross-platform (Windows, Mac, Linux, iOS, Android) and supports secure sharing of credentials between teams.

**Alternative Acceptable Solutions:**
*   **1Password:** A highly reputable, paid commercial solution known for excellent usability and security auditing.
*   **KeePassXC:** An offline, open-source password manager. Recommended only for advanced technical users who prefer local-only storage without cloud synchronization.

**Discouraged Solutions:**
*   **Browser-Based Managers (Chrome/Edge/Safari):** While convenient, these often lack the robust encryption and portability of dedicated managers. If a device is compromised, browser-stored passwords are easily extracted.
*   **LastPass:** Due to historical security incidents, this platform is currently not recommended for high-value Organization accounts.

#### 4.3 Configuration Best Practices
When setting up a Password Manager, users should adhere to the following configurations:

1.  **Strong Master Password:** The Master Password must be a passphrase consisting of at least 4 random words (e.g., `Correct-Horse-Battery-Staple`) or a complex string of 16+ characters.
2.  **Mandatory MFA:** Multi-Factor Authentication (MFA) **must** be enabled on the Password Manager account itself. A YubiKey or Authenticator App (TOTP) is preferred over SMS.
3.  **Timeout Settings:** Configure the vault to lock automatically after a specific period of inactivity (recommended: 15 minutes) or upon system sleep/lock.
4.  **Emergency Access:** If the platform supports it (e.g., Bitwarden/1Password), configure "Emergency Access" granting a trusted individual (or the CISO) access to the vault after a waiting period (e.g., 7 days) to ensure business continuity in the event of incapacitation.

#### 4.4 Usage Guidelines
*   **Generation:** Always use the built-in "Password Generator" to create credentials. Do not create passwords manually.
*   **URLs:** Launch websites directly from the Password Manager to prevent phishing (the manager will not autofill if the URL does not match exactly).
*   **Separation of Duties:** If using a personal Password Manager for work purposes, ensure Organization credentials are clearly labeled or stored in a separate "Organization" folder/collection.
*   **Shared Credentials:** Never share passwords via email, Slack, or Discord. Use the "Secure Send" or "Collection Sharing" features native to the Password Manager.

#### 4.5 Data Protection and IP
Pursuant to **Bylaws Article IX, Section 9.3**, the Organization retains ownership of all accounts created for Organization business. Upon termination of a volunteer or staff member's service, they must transfer any Organization credentials stored in personal vaults back to the Organization before deleting them.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **All Users** | Adopt a recommended Password Manager; secure the Master Password; enable MFA on the vault. |
| **CISO / IT Security** | Vet and approve Password Manager vendors; manage Enterprise licenses (if applicable); provide training on usage. |
| **Department Heads** | Ensure team members have access to shared credentials via secure vault sharing, rather than insecure spreadsheets. |

### 6. Compliance and Enforcement
While the use of a specific brand of Password Manager is a guideline, the **outcome**—secure, unique, complex passwords—is mandatory under the *Password Policy*.

Failure to secure credentials resulting in a breach, particularly if caused by password reuse or weak passwords that could have been prevented by using a Password Manager, may result in disciplinary action up to and including termination of volunteer assignment or employment.

### 7. References
*   **NIST SP 800-63B:** Digital Identity Guidelines (Authentication and Lifecycle Management).
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-STD-018:** Password Policy.
*   **Study GRC Inc. Bylaws:** Article IX (Intellectual Property & Data).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-26 | CISO | Initial Draft |