### Password Policy (Complexity/Rotation)

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-018 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-26 |
| **Next Review Date** | 2024-10-26 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Standard is to establish the technical requirements for the creation, maintenance, and management of passwords (memorized secrets) within Study GRC Inc. This document is designed to mitigate the risks associated with unauthorized access resulting from weak authentication credentials, credential stuffing, and brute-force attacks.

This Standard aligns with **NIST Special Publication 800-63B (Digital Identity Guidelines)**, shifting focus from arbitrary complexity and rotation to length, complexity-by-entropy, and compromise detection. It supports the data protection mandates outlined in **Bylaws Article IX**.

### 2. Scope
This Standard applies to all Information Systems, applications, and networks owned, managed, or utilized by Study GRC Inc.

*   **Applies to:** All employees, Board Directors, volunteers, contractors, and third-party vendors (collectively "Users") accessing Organization resources.
*   **Applies to:** All user accounts, privileged accounts (admin), and service accounts.
*   **Exclusions:** Third-party platforms where Study GRC Inc. does not have administrative control over authentication settings (though Users are encouraged to apply these standards personally).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Memorized Secret** | A string of characters (password or passphrase) that a subscriber memorizes and uses to authenticate their identity. |
| **Entropy** | A measure of the randomness or unpredictability of a password. Higher entropy indicates a stronger password. |
| **Credential Stuffing** | A cyberattack where stolen account credentials (username/password pairs) are used to gain unauthorized access to user accounts through large-scale automated login requests. |
| **Salt** | A random string of data used to modify a password hash. Salting passwords prevents attackers from using pre-computed tables (Rainbow Tables) to crack passwords. |
| **MFA** | Multi-Factor Authentication; requiring more than one distinct authentication factor for successful access. |

### 4. Standards

#### 4.1 Password Length and Complexity (NIST 800-63B § 5.1.1.2)
To maximize entropy and resistance to brute-force attacks without imposing undue burden on Users:

*   **4.1.1 Minimum Length:** All user-generated passwords must be a minimum of **8 characters** in length.
*   **4.1.2 Recommended Length:** Users are strongly encouraged to use "passphrases" (a sequence of words) with a length of **12 characters or more**.
*   **4.1.3 Composition Rules:**
    *   The Organization **shall not** impose composition rules (e.g., requiring a mix of upper case, lower case, numbers, and special characters) *unless* a specific legacy system technically requires it.
    *   Users **must** be permitted to use all printable ASCII characters, including spaces, and Unicode characters (including emojis) where system support exists.
*   **4.1.4 Truncation:** Systems must not truncate passwords to a length shorter than 64 characters.

#### 4.2 Password Rotation and Expiration (NIST 800-63B § 5.1.1.2)
Arbitrary password rotation often leads to weaker passwords (e.g., `Summer2023!` becoming `Summer2023@`). Therefore:

*   **4.2.1 Periodic Rotation:** Study GRC Inc. **shall not** require Users to change passwords periodically (e.g., every 90 days).
*   **4.2.2 Forced Rotation:** Passwords must only be changed if there is evidence of compromise, such as:
    *   Notification of a data breach involving the User's credentials.
    *   Detection of a phishing event involving the User.
    *   System logs indicating unauthorized access attempts.

#### 4.3 Compromised Credential Checking (NIST 800-63B § 5.1.1.2)
*   **4.3.1 Blacklisting:** When a User creates or changes a password, the system must verify that the password does not appear on a list of known compromised values (e.g., via integration with services like *Have I Been Pwned* or similar APIs).
*   **4.3.2 Dictionary Attacks:** Passwords must be checked against a dictionary of commonly used, expected, or compromised passwords (e.g., "password", "admin", "StudyGRC", "123456").
*   **4.3.3 Rejection:** If a chosen password is found on a blacklist or dictionary, the system must reject it and require the User to select a different one.

#### 4.4 Password Managers
*   **4.4.1 Usage:** Given the remote-first nature of the Organization, Users are **authorized and highly encouraged** to use a reputable Password Manager to generate and store unique, high-entropy passwords for every account.
*   **4.4.2 Master Password:** The Master Password used to unlock a User's Password Manager must be exceptionally strong (minimum 12 characters) and must not be stored or written down.

#### 4.5 Storage and Transmission
*   **4.5.1 Encryption:** Passwords must never be transmitted over the network in clear text. All authentication sessions must utilize TLS 1.2 or higher.
*   **4.5.2 Hashing:** Passwords must never be stored in clear text. They must be salted and hashed using an approved cryptographic algorithm (e.g., Argon2, PBKDF2, bcrypt) per **IS-POL-033 (Encryption Policy)**.

#### 4.6 Multi-Factor Authentication (MFA) Interaction
*   **4.6.1 Mandate:** Per **IS-POL-015**, MFA is mandatory for all remote access and privileged accounts.
*   **4.6.2 Reliance:** The strength of the authentication process relies on the combination of the Memorized Secret (Password) and the Possession Factor (MFA token). A strong password does not negate the requirement for MFA.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Owns this Standard; reviews annually for alignment with NIST guidelines; monitors compliance via audit logs. |
| **IT Systems Administrators** | Configure Identity Providers (IdP) and system policies (e.g., Google Workspace, Active Directory) to technically enforce length and blacklist requirements. |
| **Users (Employees/Volunteers)** | Responsible for creating compliant passwords, keeping them confidential, and reporting any suspected compromise immediately. |
| **Developers** | Ensure internal applications support long passwords (64+ chars), Unicode, and secure hashing/salting of credentials. |

### 6. Compliance and Enforcement
Failure to comply with this Standard may result in the suspension of access privileges to Study GRC Inc. systems.

**Disciplinary Action:** Employees or volunteers found to be willfully bypassing password controls (e.g., sharing passwords, using scripts to bypass rotation triggers if applicable) may face disciplinary action, up to and including termination of employment or volunteer assignment, in accordance with the **Employee Handbook** and **Bylaws Article III (Removal of Directors/Officers)**.

### 7. References
*   **NIST Special Publication 800-63B:** Digital Identity Guidelines - Authentication and Lifecycle Management.
*   **Bylaws of Study GRC Inc.:** Article IX (Policies & Data Protection).
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-POL-015:** Multi-Factor Authentication (MFA) Mandate.
*   **IS-POL-033:** Encryption Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-26 | Chief Compliance Architect | Initial release aligned with NIST 800-63B. |