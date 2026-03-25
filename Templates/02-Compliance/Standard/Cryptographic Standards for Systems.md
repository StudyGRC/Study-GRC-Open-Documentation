### Cryptographic Standards for Systems

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-008 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Lead Security Architect |
| **Classification** | Public |

### 1. Purpose
The purpose of this Standard is to define the specific cryptographic algorithms, key lengths, and protocols required to protect Study GRC Inc. (the "Organization") data assets. This Standard ensures the confidentiality and integrity of sensitive information, including member data and youth protection records, by mandating compliance with Federal Information Processing Standards (FIPS) 140-3. This document supports the Organization's obligation to protect "Work Product" and maintain trust as outlined in **Article IX** of the Bylaws.

### 2. Scope
This Standard applies to all Information Systems, software applications, cloud infrastructure, and network devices owned, developed, or managed by the Organization.

*   **In Scope:**
    *   All production servers, databases, and workstations.
    *   Custom software developed by the Organization (Open Source and Internal).
    *   Third-party SaaS applications (vendor selection criteria).
    *   VPNs and remote access gateways.
*   **Exclusions:**
    *   Legacy systems explicitly documented in the Risk Register with an approved temporary exception.
    *   User-owned devices (BYOD), except regarding the specific cryptographic configurations of Organization-managed applications installed on them.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Symmetric Encryption** | A type of encryption where the same key is used for both encryption and decryption (e.g., AES). |
| **Asymmetric Encryption** | A type of encryption that uses a pair of keys (public and private) for encryption and digital signatures (e.g., RSA, ECDSA). |
| **FIPS 140-3** | Federal Information Processing Standards Publication 140-3. The current U.S. government standard for cryptographic modules. |
| **Salt** | Random data that is used as an additional input to a one-way function that hashes data, a password, or a passphrase. |
| **Work Factor** | The amount of effort (usually time/processing power) required to perform a cryptographic operation, often adjustable in hashing algorithms (e.g., iteration count). |
| **Approved Mode** | An operational state of a cryptographic module where only FIPS-approved algorithms are used. |

### 4. Standards

#### 4.1 Approved Cryptographic Algorithms
All systems must utilize algorithms validated by the NIST Cryptographic Algorithm Validation Program (CAVP).

**4.1.1 Symmetric Encryption (Data at Rest & Bulk Transfer)**
*   **Algorithm:** Advanced Encryption Standard (AES).
*   **Minimum Key Length:** 256-bit.
*   **Approved Modes:** GCM (Galois/Counter Mode) is preferred for performance and integrity. CBC (Cipher Block Chaining) is permitted only with proper padding (PKCS#7) and integrity checks (HMAC).
*   **Prohibited:** ECB (Electronic Codebook) mode is strictly prohibited.

**4.1.2 Asymmetric Encryption (Key Exchange & Digital Signatures)**
*   **RSA:** Minimum 3072-bit key length for all new keys. (2048-bit is permitted only for verification of legacy data).
*   **Elliptic Curve Cryptography (ECC):**
    *   **ECDSA/ECDH:** Curves P-256 (secp256r1) or P-384.
    *   **EdDSA:** Curve25519 (permitted for SSH/TLS where FIPS strict mode is not technically mandatory, but NIST curves are preferred for federal compliance).

**4.1.3 Hashing and Message Digests**
*   **Standard Hashing:** SHA-2 (SHA-256, SHA-384, SHA-512) or SHA-3.
*   **Prohibited:** MD5, SHA-1, RIPEMD.

**4.1.4 Password Hashing**
*   Passwords must **never** be stored in clear text or encrypted reversibly. They must be hashed with a salt.
*   **Approved Algorithms:** Argon2id (preferred), bcrypt (work factor $\ge$ 12), or PBKDF2 (HMAC-SHA256 with $\ge$ 600,000 iterations).
*   **Salt Requirement:** Unique, random salt of at least 16 bytes per user.

#### 4.2 Prohibited and Deprecated Algorithms
The following algorithms are considered broken or weak and must not be used in any new system. Existing instances must be remediated immediately.
*   **Symmetric:** DES, 3DES (Triple DES), RC4, Blowfish, CAST.
*   **Asymmetric:** RSA keys < 2048 bits, DSA < 2048 bits.
*   **Hashing:** MD5, SHA-1 (except for HMAC usage where collision resistance is not required), MD4.
*   **Protocols:** SSL v2/v3, TLS 1.0, TLS 1.1, WEP, WPA/WPA2-Personal (TKIP).

#### 4.3 Data in Transit Protocols
All network communications transmitting sensitive data must be encrypted.

*   **Web Traffic (HTTPS):**
    *   Must use TLS 1.2 or TLS 1.3.
    *   **Cipher Suites:** Must support Forward Secrecy (FS).
    *   **Prohibited:** Null ciphers, export-grade ciphers, and RC4 suites.
*   **Remote Access (SSH):**
    *   Protocol Version 2 (SSHv2) only.
    *   Disable password authentication; use Public Key authentication.
*   **VPN:**
    *   IPsec with AES-256-GCM or WireGuard (if FIPS compliance is not strictly enforced by specific grant requirements).

#### 4.4 Key Management
Proper management of cryptographic keys is critical to the security of the cryptosystem.

*   **4.4.1 Generation:** Keys must be generated using a FIPS-approved Deterministic Random Bit Generator (DRBG) or a cryptographically secure hardware entropy source.
*   **4.4.2 Storage:**
    *   **Production Keys:** Must be stored in a dedicated Secrets Manager (e.g., AWS KMS, HashiCorp Vault, Azure Key Vault) or a Hardware Security Module (HSM).
    *   **Hardcoding:** Cryptographic keys, secrets, and API tokens must **never** be hardcoded in source code, version control systems (e.g., GitHub), or configuration files.
*   **4.4.3 Rotation:**
    *   **Symmetric Keys:** Rotated at least annually or immediately upon suspected compromise.
    *   **Asymmetric Keys (Certificates):** Maximum validity period of 397 days (approx. 13 months).
*   **4.4.4 Destruction:** Keys must be destroyed using a method that ensures they are unrecoverable (crypto-shredding) when no longer needed.

#### 4.5 Implementation in Open Source Projects
As an organization dedicated to open-source resources (Bylaws Article I, Section 1.3), special care must be taken with public repositories.

*   **Scanning:** All repositories must utilize automated secret scanning tools (e.g., TruffleHog, GitGuardian) in the CI/CD pipeline to prevent accidental key commits.
*   **Public Keys:** Only public keys may be stored in repositories; private keys are strictly forbidden.

#### 4.6 FIPS 140-3 Compliance
For systems processing Federal Contract Information (FCI) or Controlled Unclassified Information (CUI) pursuant to federal grants:
*   Cryptographic modules used must be FIPS 140-2 or FIPS 140-3 validated.
*   Systems must operate in "FIPS Mode," ensuring only approved algorithms are available for use.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Owns this Standard; approves exceptions; ensures alignment with NIST/FIPS updates. |
| **Lead Security Architect** | Maintains the list of approved cipher suites; conducts cryptographic reviews of new system designs. |
| **DevOps / Engineering Teams** | Implement approved algorithms in code and infrastructure; ensure no secrets are committed to version control. |
| **IT Operations** | Manages certificate lifecycles (SSL/TLS) and ensures server configurations (web servers, load balancers) meet this standard. |
| **Internal Audit** | Verifies compliance with this standard during annual security assessments. |

### 6. Compliance and Enforcement
**6.1 Monitoring**
Compliance with this standard is monitored via automated vulnerability scanning, static application security testing (SAST), and periodic penetration testing.

**6.2 Enforcement**
Failure to comply with this standard constitutes a violation of the Organization's Information Security Policy.
*   **Employees/Volunteers:** Violations may result in disciplinary action, up to and including termination of employment or volunteer assignment.
*   **Code/Systems:** Non-compliant code will be rejected during the Pull Request (PR) review process. Non-compliant systems may be disconnected from the network until remediated.

### 7. References
*   **NIST FIPS 140-3:** Security Requirements for Cryptographic Modules.
*   **NIST SP 800-53r5:** Security and Privacy Controls (SC-12, SC-13).
*   **NIST SP 800-131A Rev 2:** Transitioning the Use of Cryptographic Algorithms and Key Lengths.
*   **Study GRC Bylaws:** Article IX (Intellectual Property & Data Protection).
*   **IS-POL-001:** Master Information Security Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Lead Security Architect | Initial release aligned with FIPS 140-3 and Bylaws. |