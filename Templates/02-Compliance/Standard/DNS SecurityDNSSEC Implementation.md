### DNS Security and DNSSEC Implementation Standard

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-017 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Director of IT Infrastructure |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Standard is to establish mandatory technical requirements for the configuration, management, and security of Study GRC Inc.’s Domain Name System (DNS) infrastructure. As a remote-first organization relying heavily on digital platforms to deliver open-source resources, the **Availability** and **Integrity** of our domains are critical to our mission.

This Standard mitigates risks associated with DNS hijacking, cache poisoning, Man-in-the-Middle (MitM) attacks, and Denial of Service (DoS) events, ensuring compliance with federal grant security requirements (2 CFR 200) and industry best practices (NIST SP 800-81-2).

### 2. Scope
This Standard applies to:
*   All Second-Level Domains (SLDs) registered to Study GRC Inc. (e.g., `studygrc.org`).
*   All subdomains created under these SLDs.
*   All personnel (employees, contractors, and volunteers) with administrative access to DNS registrars or DNS hosting providers.

**Exclusions:**
*   Ephemeral test domains used in isolated sandbox environments that do not process public traffic or member data.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **DNS (Domain Name System)** | The hierarchical decentralized naming system for computers, services, or other resources connected to the Internet or a private network. |
| **DNSSEC (DNS Security Extensions)** | A suite of extensions to DNS that provides cryptographic authentication of data origin, denial of existence, and data integrity, but not confidentiality. |
| **Registrar** | An organization (e.g., Cloudflare, Namecheap, AWS Route53) that manages the reservation of Internet domain names. |
| **Registry Lock** | A status code set at the registry level that prevents a domain from being transferred, deleted, or having its details modified without manual verification. |
| **TTL (Time to Live)** | A setting for each DNS record that tells the DNS resolver how long to cache a query before requesting a new one. |
| **CAA Record** | Certificate Authority Authorization record; specifies which Certificate Authorities (CAs) are allowed to issue certificates for a domain. |

### 4. Standards

#### 4.1 Registrar Account Security
To prevent unauthorized domain takeovers, the following controls must be applied to all Registrar accounts:
*   **4.1.1 Multi-Factor Authentication (MFA):** Hardware-based MFA (FIDO2/YubiKey) or Time-based One-Time Password (TOTP) **must** be enforced for all accounts with access to DNS management. SMS-based MFA is prohibited.
*   **4.1.2 Role-Based Access Control (RBAC):** Access to modify DNS records must be restricted to the specific personnel defined in the *Access Control Policy*.
*   **4.1.3 Registrar Locking:** The "ClientTransferProhibited" (Registrar Lock) status must be enabled for all production domains to prevent unauthorized transfers.
*   **4.1.4 Contact Information:** WHOIS contact information must use role-based email addresses (e.g., `hostmaster@studygrc.org`) rather than individual personal emails to ensure continuity.

#### 4.2 DNSSEC Implementation
In accordance with the CISO's mandate for data integrity (Bylaws Article V, Section 5.2), DNSSEC must be enabled on all primary public-facing domains.
*   **4.2.1 Signing:** All zones must be cryptographically signed.
*   **4.2.2 Algorithm:** The signing algorithm must be ECDSA Curve P-256 with SHA-256 (Algorithm 13) or stronger. RSA/SHA-1 is strictly prohibited.
*   **4.2.3 Chain of Trust:** The Delegation Signer (DS) record must be published to the parent zone (Registry) to establish a complete chain of trust.
*   **4.2.4 Key Management:** If using a managed DNS provider (e.g., Cloudflare, AWS), automated key rotation must be enabled. If managing keys manually, Zone Signing Keys (ZSK) must be rotated quarterly, and Key Signing Keys (KSK) annually.

#### 4.3 Zone Configuration and Hygiene
*   **4.3.1 CAA Records:** All domains must publish CAA records restricting SSL/TLS certificate issuance to authorized Certificate Authorities (e.g., Let's Encrypt, DigiCert) to prevent rogue certificate issuance.
*   **4.3.2 Dangling DNS:** A quarterly audit must be conducted to identify and remove CNAME records pointing to decommissioned resources (e.g., an old S3 bucket or Azure instance) to prevent subdomain takeovers.
*   **4.3.3 Email Authentication:** To protect the organization's reputation, all domains must have valid SPF, DKIM, and DMARC records (set to `p=quarantine` or `p=reject`).

#### 4.4 Availability and Redundancy
To satisfy the **Availability** regulatory mapping:
*   **4.4.1 Anycast Network:** DNS services must be hosted on a provider utilizing an Anycast network architecture to ensure low latency and resilience against DDoS attacks.
*   **4.4.2 TTL Settings:**
    *   **Static Records (A, MX, TXT):** TTL should be set between 1 hour (3600s) and 24 hours (86400s) to maximize caching efficiency.
    *   **Failover Records:** Records used for active failover mechanisms must have a TTL of no more than 5 minutes (300s).
*   **4.4.3 Secondary DNS:** Where technically feasible without breaking DNSSEC chains, a secondary DNS provider should be configured as a fallback.

#### 4.5 Monitoring and Alerting
*   **4.5.1 Expiration Monitoring:** Automated alerts must be configured to notify the IT team 60, 30, and 7 days prior to domain registration expiration.
*   **4.5.2 Configuration Change Alerting:** Any modification to NS (Name Server) or MX (Mail Exchange) records must trigger an immediate high-priority alert to the Security Operations team.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Approves this Standard; ensures alignment with NIST guidelines; reviews annual DNS audit reports. |
| **Director of IT Infrastructure** | Owns the relationship with Registrars; ensures MFA enforcement; manages budget for domain renewals. |
| **SysAdmins / DevOps Engineers** | Implement DNSSEC signing; configure records (A, CNAME, TXT); respond to availability alerts. |
| **Director of Finance** | Ensures payment methods for Registrars are valid to prevent involuntary domain expiration (Availability risk). |

### 6. Compliance and Enforcement
Failure to adhere to this Standard can result in service outages, reputational damage, and loss of donor trust.

*   **Technical Enforcement:** Non-compliant configurations identified during automated scans will be flagged for immediate remediation.
*   **Disciplinary Action:** Personnel found circumventing security controls (e.g., disabling MFA on Registrar accounts) are subject to disciplinary action, up to and including termination of employment or volunteer assignment, in accordance with the *Employee Handbook*.

### 7. References
*   **NIST SP 800-81-2:** Secure Domain Name System (DNS) Deployment Guide.
*   **CISA Cybersecurity Performance Goals (CPG):** Goals 2.1 (MFA) and 5.1 (Asset Management).
*   **Study GRC Bylaws:** Article V (Operational Leadership - CISO Duties).
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-POL-005:** Access Control Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Legal Officer | Initial release of standard. |