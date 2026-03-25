### Consent Management Platform (CMP) Configuration Standard

| Document Control | |
| :--- | :--- |
| **Document ID** | PRIV-STD-012 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Data Protection Officer (DPO) |
| **Classification** | Public |

### 1. Purpose
The purpose of this Standard is to define the mandatory technical and functional configuration requirements for the Consent Management Platform (CMP) deployed across Study GRC Inc. digital properties. This Standard ensures compliance with the **ePrivacy Directive (2002/58/EC)**, **GDPR**, and the **Texas Data Privacy and Security Act (TDPSA)** by enforcing a "Prior Consent" model for non-essential data collection technologies. It aligns with **Bylaws Article IX**, which mandates the protection of member and learner data.

### 2. Scope
This Standard applies to all public-facing websites, subdomains, mobile applications, and learning management systems (LMS) owned or operated by Study GRC Inc.

*   **In Scope:** Main website (`studygrc.org`), community forums, open-source repositories, and third-party integrations (e.g., analytics, marketing pixels, embedded video players).
*   **Exclusions:** Internal-only administrative portals that utilize strictly necessary cookies for authentication and security purposes only, provided no third-party tracking occurs.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **CMP (Consent Management Platform)** | Software used to inform visitors about data collection and manage their consent choices regarding cookies and trackers. |
| **Prior Consent (Zero Load)** | The technical state where no cookies (other than Strictly Necessary) are set on the user's device until the user explicitly clicks "Accept." |
| **Strictly Necessary Cookies** | Cookies essential for the website to function (e.g., security, load balancing, preserving cart items). Exemption from consent applies. |
| **Dark Patterns** | User interface designs that trick or manipulate users into making decisions that are not in their best interest (e.g., making the "Reject" button invisible). |
| **Granular Consent** | The ability for a user to consent to specific categories of data processing (e.g., Analytics) while rejecting others (e.g., Marketing). |

### 4. Standard Requirements

#### 4.1. Implementation Architecture
To ensure effective blocking of unauthorized trackers, the CMP script must be implemented as follows:
*   **4.1.1 Execution Order:** The CMP script tag must be the **first** script loaded in the HTML `<head>` section of the web property.
*   **4.1.2 Tag Management Integration:** If a Tag Management System (e.g., GTM) is used, the CMP must control the firing triggers of all tags. No tags may fire on "Page Load" or "DOM Ready" unless they are classified as Strictly Necessary.
*   **4.1.3 Asynchronous Loading:** The CMP must load asynchronously to prevent latency in rendering the core content, aligning with our mission to provide accessible resources.

#### 4.2. Cookie Categorization and Auto-Blocking
All cookies and tracking technologies must be scanned monthly and categorized into the following buckets. Uncategorized cookies are strictly prohibited.

*   **4.2.1 Strictly Necessary:** (Always Active) - Security, authentication, and CMP preference storage.
*   **4.2.2 Functional:** (Default: Off) - Enhanced personalization (e.g., language settings, video player preferences).
*   **4.2.3 Performance/Analytics:** (Default: Off) - Aggregated data on site usage (e.g., Google Analytics, Matomo).
*   **4.2.4 Targeting/Advertising:** (Default: Off) - Building user profiles for marketing. **Note:** Given our non-profit status and youth focus, Targeting cookies are prohibited on pages specifically designated for K-12 audiences.

#### 4.3. User Interface (UI) and Experience
The Consent Banner (Notice) must adhere to the following design standards to avoid "Dark Patterns" and ensure valid consent under the ePrivacy Directive:

*   **4.3.1 Equal Weight:** The "Accept All" and "Reject All" (or "Decline") buttons must be presented with equal prominence (same size, color contrast, and visibility).
*   **4.3.2 No Pre-Ticked Boxes:** Checkboxes for non-essential categories must be unchecked by default.
*   **4.3.3 Clear Language:** The banner must clearly state that cookies are used and provide a link to the **Privacy Policy** and **Cookie Policy**.
*   **4.3.4 Granular Control:** A "Preferences" or "Settings" button must be available on the first layer of the banner, allowing users to toggle specific categories.
*   **4.3.5 Persistent Withdrawal:** A floating icon or clearly visible footer link ("Cookie Preferences") must be available on every page to allow users to withdraw or modify consent as easily as they gave it.

#### 4.4. Consent Records and Audit Trail
The CMP must maintain an immutable log of user consent to satisfy regulatory audit requirements:
*   **4.4.1 Log Data:** The log must capture the unique Consent ID, Timestamp, IP Address (anonymized/hashed), User Agent, and the specific categories consented to.
*   **4.4.2 Retention:** Consent logs shall be retained for 12 months in accordance with the **Records Retention Schedule**.

#### 4.5. Cross-Domain and Cross-Device Consent
*   **4.5.1 Scope:** Where technically feasible, consent shall be managed at the root domain level to prevent user fatigue, provided the purposes of processing are identical across subdomains.
*   **4.5.2 Re-Consent:** Users must be prompted to renew consent at least every 12 months, or immediately if the Privacy Policy or Cookie Categorization changes significantly.

#### 4.6. Youth Protection Configuration
In alignment with the **Child and Youth Safeguarding Policy**:
*   **4.6.1 Age Gating:** If the CMP detects a user is accessing a designated "Youth Resource" section, all Targeting/Advertising cookies must be hard-blocked regardless of user choice.
*   **4.6.2 Clarity:** For youth-oriented pages, the CMP language must be simplified to an 8th-grade reading level.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Approves the selection of the CMP vendor and validates security configurations. |
| **Data Protection Officer (DPO)** | Reviews and approves cookie categorizations and banner text to ensure legal compliance. |
| **Web Development Team** | Implements the CMP script, ensures "Zero Load" functionality, and manages Tag Manager triggers. |
| **Marketing/Content Team** | Ensures no new third-party tools are added to the website without prior vetting and categorization in the CMP. |

### 6. Compliance and Enforcement
Failure to comply with this Standard may result in the Organization violating the ePrivacy Directive and GDPR, leading to significant financial penalties and reputational damage.
*   **Technical Enforcement:** The CISO reserves the right to disable any web property or third-party integration that bypasses the CMP.
*   **Personnel:** Employees found circumventing the CMP (e.g., hardcoding tracking pixels) are subject to disciplinary action up to and including termination.

### 7. References
*   **ePrivacy Directive (2002/58/EC)** - Article 5(3)
*   **General Data Protection Regulation (GDPR)** - Article 7 (Conditions for Consent)
*   **Texas Data Privacy and Security Act (TDPSA)**
*   **Bylaws of Study GRC Inc.** - Article IX (Policies & Data Protection)
*   **PRIV-POL-001:** Master Data Privacy Policy
*   **IS-POL-005:** Acceptable Use Policy

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Compliance Architect | Initial Release aligned with ePrivacy Directive. |