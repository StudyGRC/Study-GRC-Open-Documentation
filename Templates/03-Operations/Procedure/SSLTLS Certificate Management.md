### SSL/TLS Certificate Management Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-020 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Lead Systems Administrator |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a standardized process for the issuance, installation, monitoring, renewal, and revocation of Secure Sockets Layer (SSL) and Transport Layer Security (TLS) certificates within Study GRC Inc. This procedure ensures the confidentiality and integrity of data in transit, prevents service interruptions caused by expired certificates, and maintains user trust by eliminating browser security warnings.

### 2. Scope
This procedure applies to all Study GRC Inc. information systems, applications, and network devices that utilize encryption for data in transit.
*   **In Scope:** Public-facing websites (e.g., studygrc.org), learning management systems, API endpoints, mail servers, and internal administrative dashboards.
*   **Exclusions:** Local development environments not accessible from the public internet, provided they do not process live Member data.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **CA (Certificate Authority)** | A trusted entity that issues digital certificates (e.g., Let's Encrypt, DigiCert, AWS ACM). |
| **CSR (Certificate Signing Request)** | A message sent from an applicant to a CA to apply for a digital certificate. It contains the public key and identity information. |
| **Private Key** | A secret cryptographic key used to decrypt data and sign digital communications. **Must never be shared.** |
| **ACME Protocol** | Automated Certificate Management Environment; a protocol for automating interactions between certificate authorities and web servers. |
| **Wildcard Certificate** | A public key certificate that can be used with multiple subdomains of a domain (e.g., `*.studygrc.org`). |
| **HSTS** | HTTP Strict Transport Security; a web security policy mechanism that forces web browsers to interact with websites only via secure HTTPS connections. |

### 4. Procedures

#### 4.1. Approved Standards and Protocols
To ensure compliance with the *Master Information Security Policy* and NIST guidelines, all certificates must adhere to the following technical standards:
1.  **Protocol Version:** Only **TLS 1.2** or **TLS 1.3** are permitted. SSL v2/v3 and TLS 1.0/1.1 are strictly prohibited and must be disabled on the server side.
2.  **Key Length:**
    *   RSA keys must be at least **2048-bit**.
    *   ECDSA (Elliptic Curve) keys must be at least **256-bit**.
3.  **Hashing Algorithm:** SHA-256 or higher is required. SHA-1 is prohibited.
4.  **Validity Period:** Certificates shall not have a validity period exceeding 398 days. Automated short-lived certificates (e.g., 90 days via Let's Encrypt) are preferred.

#### 4.2. Certificate Acquisition and Issuance
**4.2.1 Automated Issuance (Preferred)**
Whenever feasible, Study GRC Inc. utilizes automated issuance via the ACME protocol (e.g., Let's Encrypt) or Cloud Provider Managers (e.g., AWS Certificate Manager).
1.  **Configuration:** The Systems Administrator configures the web server or load balancer to request a certificate via the approved ACME client (e.g., Certbot).
2.  **Validation:** Domain validation is performed automatically via HTTP-01 or DNS-01 challenges.
3.  **Storage:** Private keys generated during this process must be stored with strict file permissions (read-only by root/service account).

**4.2.2 Manual Issuance (Exception)**
If automation is not possible (e.g., specific vendor requirements or EV certs):
1.  **CSR Generation:** The Systems Administrator generates a CSR on the target server.
    *   *Warning:* The Private Key must be generated on the server and **never** transmitted via email, Slack, or ticketing systems.
2.  **Submission:** The CSR is submitted to an approved Commercial CA by the IT Department.
3.  **Verification:** The CISO or designee approves the domain ownership verification email.

#### 4.3. Installation and Configuration
1.  **Chain of Trust:** Administrators must install the Intermediate CA certificates alongside the server certificate to ensure a complete chain of trust.
2.  **Cipher Suites:** Servers must be configured to prioritize secure cipher suites (Forward Secrecy preferred). Weak ciphers (e.g., RC4, NULL, 3DES) must be disabled.
3.  **HSTS Implementation:** All public-facing web services must enable HSTS with a minimum max-age of 31536000 seconds (1 year) to prevent protocol downgrade attacks.
4.  **Testing:** Post-installation, the configuration must be tested using a tool such as SSL Labs (Qualys) to ensure a grade of "A" or higher.

#### 4.4. Monitoring and Renewal
**4.4.1 Automated Renewal**
1.  Systems using ACME/Certbot must have a cron job or systemd timer configured to check for renewal twice daily.
2.  Renewal triggers when the certificate is within 30 days of expiration.
3.  Services (e.g., Nginx, Apache) must be reloaded automatically upon successful renewal.

**4.4.2 Manual Renewal Monitoring**
For certificates that cannot be automated:
1.  **Inventory:** All manual certificates must be logged in the *IT Asset Register*.
2.  **Alerting:** The monitoring system (e.g., Nagios, Uptime Robot, or CloudWatch) must be configured to send alerts to the IT Distribution List at the following intervals prior to expiration:
    *   30 Days (Warning)
    *   14 Days (Urgent)
    *   7 Days (Critical)
    *   1 Day (Emergency)

#### 4.5. Certificate Revocation
A certificate must be revoked immediately if:
1.  The Private Key is lost, stolen, or compromised.
2.   The domain name is no longer owned by Study GRC Inc.
3.  The service is decommissioned.

**Revocation Steps:**
1.  **Notification:** The Systems Administrator notifies the CISO of the compromise/change.
2.  **Action:** The Administrator logs into the CA portal or uses the ACME client to issue a revocation command.
3.  **Verification:** Verify that the certificate serial number appears on the CA’s Certificate Revocation List (CRL) or OCSP responder.
4.  **Replacement:** If the service is still active, a new certificate with a new Private Key must be generated and installed immediately.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Approves CA vendors; authorizes manual certificate purchases; oversees the encryption strategy in accordance with Bylaws Article V. |
| **Lead Systems Administrator** | Executes CSR generation, installation, and configuration; maintains automation scripts; responds to expiration alerts. |
| **DevOps Engineer** | Configures automated certificate management for cloud infrastructure and CI/CD pipelines. |
| **All Staff** | Reports any "Not Secure" browser warnings or certificate errors to the IT Help Desk immediately. |

### 6. Compliance and Enforcement
Failure to comply with this procedure may result in disciplinary action, up to and including termination of employment or volunteer assignment. Negligence leading to a Private Key compromise or a public service outage due to expiration is considered a serious violation of the *Master Information Security Policy*.

### 7. References
*   **IS-POL-001:** Master Information Security Policy
*   **IS-POL-012:** Encryption Policy
*   **NIST SP 800-52 Rev. 2:** Guidelines for the Selection, Configuration, and Use of TLS Implementations
*   **Bylaws of Study GRC Inc.:** Article V (Operational Leadership)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Lead Systems Admin | Initial release of procedure. |