### Domain Name Management

| Document Control | |
| :--- | :--- |
| **Document ID** | IT-PRC-016 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | IT Systems Administrator |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a standardized process for the acquisition, maintenance, security, and retirement of internet domain names owned by Study GRC Inc. This procedure ensures that domain names—critical intellectual property and brand assets—are protected against expiration, hijacking, unauthorized transfer, and reputational damage.

### 2. Scope
This procedure applies to all internet domain names registered, purchased, or managed by Study GRC Inc.
*   **Applies to:** All employees, Board Directors, and volunteers authorized to manage IT assets or marketing channels.
*   **Exclusions:** Personal domain names owned by members or volunteers that are not used for official Organization business.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Registrar** | An accredited organization (e.g., Namecheap, Cloudflare, GoDaddy) that manages the reservation of internet domain names. |
| **Registrant** | The legal entity or individual who owns the domain name. For all Organization assets, this must be "Study GRC Inc." |
| **DNS (Domain Name System)** | The system that translates human-readable domain names (studygrc.org) into IP addresses. |
| **Registrar Lock** | A security setting that prevents a domain from being transferred to another registrar without explicit authorization. |
| **WHOIS Privacy** | A service that redacts the contact details of the domain owner from public records to protect privacy. |

### 4. Procedures

#### 4.1 Acquisition and Registration
To ensure legal ownership and brand consistency, the following steps must be taken when acquiring new domains:

1.  **Authorization:** Prior to purchase, the requesting party must obtain approval from the Executive Director or the VP of Education & Training to ensure the domain aligns with the Organization's mission.
2.  **Registrant Information:**
    *   The **Registrant Organization** must always be listed as "Study GRC Inc."
    *   The **Registrant Email** must be a generic, managed distribution list (e.g., `domains@studygrc.org` or `it-admin@studygrc.org`), never a personal email address or a specific employee's individual work email.
    *   The **Mailing Address** must match the Organization’s Registered Office as defined in **Bylaws Article 1.2**.
3.  **Defensive Registration:** To satisfy Brand Protection requirements, the Organization shall prioritize acquiring the `.org`, `.com`, and `.net` variations of its primary trademarks where budget permits.

#### 4.2 Account Security and Access Control
Domain registrars control the "keys to the kingdom." Access must be strictly guarded.

1.  **Approved Registrars:** The Organization shall consolidate domains under a single, enterprise-grade registrar approved by the CISO to centralize management.
2.  **Multi-Factor Authentication (MFA):** MFA is **mandatory** for any account with access to domain management. Hardware keys (e.g., YubiKey) are the preferred method; SMS 2FA is prohibited unless no other option exists.
3.  **Access Limitation:** Access to the registrar account is restricted to the CISO, the IT Systems Administrator, and the Executive Director (as an emergency backup).
4.  **API Access:** If API keys are generated for DNS automation, they must be rotated annually and restricted by IP address where possible.

#### 4.3 Maintenance and Renewal
To prevent accidental expiration and service outages:

1.  **Auto-Renewal:** All active domain names must be set to **Auto-Renew** within the registrar portal.
2.  **Payment Methods:** The Chief Financial Officer (CFO) must ensure a valid corporate credit card or bank account is linked to the registrar account. A backup payment method must be configured.
3.  **Expiration Monitoring:** The IT Systems Administrator must configure alerts to notify the IT team 60, 30, and 7 days prior to any domain expiration date, regardless of auto-renew status.

#### 4.4 Configuration and Privacy
1.  **Registrar Lock:** The "ClientTransferProhibited" (Registrar Lock) status must be enabled for all domains to prevent unauthorized transfers.
2.  **WHOIS Privacy:** Due to the remote nature of the Organization and to protect the privacy of volunteers/staff, WHOIS Privacy (Redaction) must be enabled for all domains unless legally required otherwise.
3.  **DNSSEC:** Domain Name System Security Extensions (DNSSEC) must be enabled on primary domains to prevent DNS spoofing and cache poisoning.

#### 4.5 Termination and Transfer
1.  **Non-Renewal Decision:** A decision to let a domain expire must be approved in writing by the Executive Director.
2.  **Safe Landing:** If a domain is no longer needed for active services but carries brand weight, it should be redirected to the primary website rather than released to the public pool.
3.  **Transfer Out:** Transferring a domain out of the Organization’s possession constitutes a transfer of assets and must comply with **Bylaws Article X (Fundamental Actions)** if the domain constitutes a "substantial asset," or otherwise requires Board notification.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **CISO** | Ultimate accountability for domain security; approves registrar selection; enforces MFA policies. |
| **IT Systems Administrator** | Executes purchases; manages DNS records; monitors expiration dates; ensures WHOIS accuracy. |
| **Executive Director** | Approves new domain acquisitions; authorizes non-renewal of assets. |
| **CFO** | Maintains valid payment methods on file with the registrar; reviews renewal invoices. |

### 6. Compliance and Enforcement
Failure to comply with this procedure—specifically the use of personal email addresses for registration or disabling MFA—may result in disciplinary action, up to and including termination of employment or volunteer assignment.

Unauthorized transfer or sale of the Organization's domain names is considered theft of Intellectual Property (as defined in **Bylaws Article 9.3**) and will result in immediate legal action.

### 7. References
*   **Bylaws Article 1.2:** Registered Office and Agent
*   **Bylaws Article 9.3:** Intellectual Property
*   **IS-POL-001:** Master Information Security Policy
*   **FIN-POL-022:** Procurement Policy

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | IT Systems Admin | Initial Draft |