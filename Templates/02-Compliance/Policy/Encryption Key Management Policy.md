### Encryption Key Management Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-033 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this policy is to establish the standards and procedures for the generation, storage, distribution, usage, rotation, and destruction of cryptographic keys within Study GRC Inc. ("the Organization").

As an organization dedicated to open-source GRC resources and youth education, maintaining the integrity and confidentiality of our data is paramount. Proper key management ensures that encrypted data remains secure even if other controls fail, and prevents unauthorized access to critical infrastructure. This policy satisfies the requirements of **NIST SP 800-53 (Control SC-12)** and aligns with **NIST SP 800-57**.

### 2. Scope
This policy applies to all employees, contractors, volunteers, and third-party vendors who manage, access, or utilize cryptographic keys on behalf of the Organization.

**In Scope:**
*   Symmetric and Asymmetric keys used for data encryption (at rest and in transit).
*   API keys, secrets, and tokens used for authentication.
*   X.509 Certificates (SSL/TLS).
*   Code signing keys (critical for our Open Source deliverables).
*   SSH keys used for infrastructure access.
*   Cloud Provider Key Management Services (e.g., AWS KMS, Azure Key Vault).

**Exclusions:**
*   User passwords (governed by *IS-STD-018 Password Policy*).
*   Personal cryptographic keys used by volunteers on non-Organization devices, provided they are not used to access Organization production environments.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Cryptographic Key** | A string of bits used by a cryptographic algorithm to transform plain text into cipher text or vice versa. |
| **Key Lifecycle** | The complete set of phases a key goes through, including generation, distribution, storage, use, rotation, revocation, and destruction. |
| **KMS** | Key Management Service. A system (cloud or on-premise) used to manage cryptographic keys. |
| **Hard-Coding** | The prohibited practice of embedding keys directly into source code or configuration files. |
| **Split Knowledge** | A security principle where a key is split into multiple parts, requiring multiple authorized individuals to combine their parts to reconstruct the key (e.g., for Root CA keys). |
| **Crypto-Shredding** | The practice of deleting data by deliberately destroying the encryption key used to encrypt that data. |

### 4. Policy Statements

#### 4.1. General Principles
4.1.1 **Ownership:** In accordance with **Bylaws Article IX (Intellectual Property)**, all cryptographic keys generated for Organization business are the sole property of Study GRC Inc.
4.1.2 **Least Privilege:** Access to keys must be restricted to the minimum number of personnel and services required to perform essential duties.
4.1.3 **Separation of Duties:** Individuals authorized to approve key generation must be different from those authorized to use the keys, where operationally feasible.

#### 4.2. Key Generation
4.2.1 **Approved Algorithms:** Keys must be generated using FIPS 140-2 (or higher) validated cryptographic modules or industry-standard strong algorithms (e.g., AES-256 for symmetric, RSA-2048+ or ECC for asymmetric).
4.2.2 **Randomness:** Keys must be generated using a cryptographically secure pseudo-random number generator (CSPRNG).
4.2.3 **Code Signing Keys:** Keys used to sign open-source releases must be generated on air-gapped or highly restricted hardware (e.g., YubiKey or HSM) to prevent compromise of the software supply chain.

#### 4.3. Key Storage
4.3.1 **Prohibition on Hard-Coding:** Cryptographic keys, secrets, and API tokens **must never** be hard-coded into source code, version control systems (e.g., GitHub, GitLab), or unencrypted configuration files.
4.3.2 **Vault Usage:** Keys must be stored in approved secure vaults (e.g., AWS KMS, HashiCorp Vault, Azure Key Vault, 1Password for Teams).
4.3.3 **Encryption at Rest:** Keys stored outside of a Hardware Security Module (HSM) must be encrypted using a Key Encryption Key (KEK).

#### 4.4. Key Distribution
4.4.1 **Secure Transmission:** Keys must never be transmitted via insecure channels such as email, Slack/Discord, or chat logs.
4.4.2 **Out-of-Band:** If manual distribution is required, it must occur via a secure, out-of-band mechanism or a secure secret sharing tool (e.g., 1Password "Share" feature) with expiration and one-time view settings enabled.

#### 4.5. Key Usage and Rotation
4.5.1 **Cryptographic Period:** Keys must be rotated automatically or manually based on the following schedule:
*   **Data Encryption Keys (DEK):** Rotated at least annually.
*   **Key Encryption Keys (KEK):** Rotated at least every 2 years.
*   **SSL/TLS Certificates:** Rotated annually (or shorter, e.g., 90 days via Let's Encrypt).
*   **SSH Keys:** Rotated at least annually or upon staff departure.
4.5.2 **Compromise:** Any key suspected of being compromised must be rotated immediately.

#### 4.6. Key Revocation and Destruction
4.6.1 **Revocation:** Keys must be revoked immediately upon:
*   Termination of the employee or volunteer holding the key.
*   Suspected or confirmed compromise.
*   End of the key's operational life.
4.6.2 **Destruction:** Withdrawn or revoked keys must be destroyed using methods that ensure they cannot be recovered (e.g., crypto-shredding or physical destruction of the token).
4.6.3 **Archive:** Keys used for data encryption must be archived securely before destruction if the data they protect is retained, to ensure data remains retrievable for the retention period defined in the *Records Retention Schedule*.

#### 4.7. Audit and Logging
4.7.1 **Logging:** All key management operations (generation, access, rotation, destruction) must be logged.
4.7.2 **Monitoring:** The CISO or designee must configure alerts for anomalous key usage (e.g., usage of a root key, failed access attempts).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Defines cryptographic standards; approves Key Management systems; oversees incident response regarding key compromise. |
| **DevOps / IT Engineering** | Implements automated key rotation; manages cloud KMS configurations; ensures no keys are committed to version control. |
| **Developers** | Adhere to the prohibition on hard-coding keys; utilize approved vaults for application secrets. |
| **Audit Committee** | Reviews this policy annually; ensures key management practices align with external compliance requirements (e.g., IRS, Donors). |

### 6. Compliance and Enforcement
Failure to comply with this policy puts the Organization and its community at significant risk.

*   **Code Repositories:** Any commit found containing a hard-coded key or secret will be rejected or immediately reverted. The repository history must be scrubbed, and the exposed key must be revoked and rotated immediately.
*   **Disciplinary Action:** Violations of this policy may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action, in accordance with the *Employee Handbook* and *Volunteer Handbook*.

### 7. References
*   **NIST SP 800-53 Rev 5:** Security and Privacy Controls (Control SC-12: Cryptographic Key Establishment and Management).
*   **NIST SP 800-57:** Recommendation for Key Management.
*   **Study GRC Bylaws:** Article V (Operational Leadership), Article IX (Intellectual Property).
*   **IS-STD-018:** Password Policy.
*   **IS-STD-028:** Data Classification Standard.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name], CISO | Initial Draft aligned with NIST SC-12. |