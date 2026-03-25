### Email Security/Anti-Phishing Controls

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-072 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-26 |
| **Next Review Date** | 2024-04-26 (Bi-Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Standard is to define the mandatory technical configurations and user behaviors required to protect Study GRC Inc. (the "Organization") from email-based threats. As a remote-first organization, email is a primary attack vector for ransomware, credential theft, and financial fraud. This document establishes controls to validate sender identity, filter malicious content, and protect the Organization’s reputation and the data of its community members, including minors, in alignment with the Organization's mission to foster a safe GRC ecosystem.

### 2. Scope
This Standard applies to:
*   **Systems:** All email domains owned or managed by the Organization (e.g., `@studygrc.org`), including cloud-based email infrastructure (e.g., Google Workspace, Microsoft 365).
*   **Users:** All Directors, Officers, employees, volunteers, contractors, and committee members utilizing Organization-provisioned email accounts.
*   **Exclusions:** Personal email accounts not associated with the Organization's infrastructure, though use of personal email for Organization business is restricted by the *Acceptable Use Policy (IS-POL-007)*.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Phishing** | A cybercrime in which a target is contacted by email by someone posing as a legitimate institution to lure individuals into providing sensitive data. |
| **Spear Phishing** | A targeted attempt to steal sensitive information such as account credentials or financial information from a specific victim. |
| **Whaling** | A specific form of spear phishing targeted at high-profile business executives (e.g., CEO, CFO) to authorize fraudulent wire transfers. |
| **SPF (Sender Policy Framework)** | An email authentication method that specifies the mail servers authorized to send email on behalf of a domain. |
| **DKIM (DomainKeys Identified Mail)** | An email authentication method that adds a cryptographic signature to emails to verify they were not forged or altered. |
| **DMARC (Domain-based Message Authentication, Reporting, and Conformance)** | A protocol that uses SPF and DKIM to determine the authenticity of an email message and specifies how receivers should handle failures. |
| **Sandboxing** | An isolated environment where suspicious file attachments are executed to analyze their behavior before being delivered to the user. |

### 4. Standards

#### 4.1 Technical Configuration: Inbound Protection
The Organization’s email infrastructure must be configured with the following automated protections:

*   **4.1.1 Malware and Virus Scanning:** All inbound and outbound messages must be scanned for known malware signatures.
*   **4.1.2 Attachment Sandboxing:** All executable, script, and document attachments (e.g., .exe, .ps1, .docx, .pdf) originating from external sources must undergo dynamic analysis (sandboxing) prior to delivery.
*   **4.1.3 URL Rewriting (Time-of-Click Protection):** The email gateway must rewrite URLs in inbound emails to route through a security proxy that verifies the destination's safety at the moment the user clicks the link.
*   **4.1.4 External Sender Tagging:** All emails originating from outside the Organization's domain must be visually flagged with a banner (e.g., "EXTERNAL") to alert the recipient.
*   **4.1.5 Anti-Spoofing:** The system must be configured to quarantine or reject messages that fail SPF, DKIM, or DMARC checks based on the sending domain's policy.

#### 4.2 Technical Configuration: Domain Reputation (Outbound)
To prevent the Organization’s domain from being used for fraud and to ensure deliverability, the CISO must enforce:

*   **4.2.1 SPF Records:** All domains must have a valid SPF record listing only authorized sending IP addresses/services. The record must end with `-all` (Hard Fail) or `~all` (Soft Fail), with a roadmap to `-all`.
*   **4.2.2 DKIM Signing:** All outbound email services (including third-party marketing tools like Mailchimp or HubSpot) must sign emails with a 2048-bit DKIM key.
*   **4.2.3 DMARC Enforcement:**
    *   **Phase 1 (Monitoring):** `p=none` (Current status).
    *   **Phase 2 (Quarantine):** `p=quarantine` (Target: 3 months from Effective Date).
    *   **Phase 3 (Reject):** `p=reject` (Target: 6 months from Effective Date).
*   **4.2.4 Open Relay Prohibition:** Mail servers must be configured to deny open relaying of messages.

#### 4.3 High-Risk Target Protections (Whaling)
Pursuant to Bylaws Article V, Operational Officers (CEO, CFO, CISO) are high-value targets.
*   **4.3.1 Impersonation Protection:** The email security gateway must be configured to flag emails using display names that match the names of Board Directors or Operational Officers but originate from external addresses (e.g., an email from "John Doe" at `gmail.com` where John Doe is the CEO).
*   **4.3.2 Financial Keyword Flagging:** Emails directed to the Treasurer or CFO containing keywords related to "wire transfer," "invoice," or "urgent payment" must undergo enhanced heuristic scanning.

#### 4.4 User Account Security
*   **4.4.1 Multi-Factor Authentication (MFA):** In accordance with *IS-POL-015*, MFA is mandatory for all email access. Legacy protocols (IMAP/POP3) that do not support Modern Auth/MFA must be disabled.
*   **4.4.2 Auto-Forwarding Restriction:** Automatic forwarding of Organization email to external personal domains (e.g., auto-forwarding to Yahoo/Gmail) is technically blocked to prevent Data Loss Prevention (DLP) violations.

#### 4.5 Reporting and Response
*   **4.5.1 Reporting Mechanism:** A "Report Phishing" button or add-in must be deployed to all email clients (Desktop, Web, Mobile) to allow users to report suspicious emails with a single click.
*   **4.5.2 User Notification:** Users who report a simulated phishing test correctly must receive immediate positive reinforcement. Users who fall for a simulated test must be automatically enrolled in remedial training.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Responsible for the technical configuration, maintenance, and monitoring of email security controls defined in this Standard. Reports compliance status to the Board. |
| **IT/System Administrators** | Implement SPF/DKIM/DMARC records; manage the email gateway; investigate reported phishing incidents. |
| **Operational Officers & Directors** | Set the "Tone at the Top" by adhering to security warnings and participating in anti-phishing training. |
| **All Users** | Responsible for verifying the identity of senders, avoiding suspicious links, and reporting potential phishing attempts via the designated reporting tool. |

### 6. Compliance and Enforcement
Failure to comply with this Standard may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action depending on the severity of the violation.

**Specific Enforcement Triggers:**
*   Disabling local security controls on endpoints.
*   Circumventing MFA or auto-forwarding blocks.
*   Repeated failure of phishing simulations (3+ failures in 12 months) will result in a formal review with the Director of Kindness and Generosity (HR function) and the CISO.

### 7. References
*   **NIST SP 800-53 Rev. 5:** Controls SI-3 (Malicious Code Protection), SI-4 (Information System Monitoring), IA-2 (Identification and Authentication).
*   **CISA Cybersecurity Performance Goals (CPG):** 2.1 (MFA), 2.2 (Phishing-Resistant MFA), 2.3 (Unique Credentials).
*   **Study GRC Bylaws:** Article V (Operational Leadership).
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-POL-007:** Acceptable Use Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-26 | CISO | Initial Draft and Standardization of DMARC roadmap. |