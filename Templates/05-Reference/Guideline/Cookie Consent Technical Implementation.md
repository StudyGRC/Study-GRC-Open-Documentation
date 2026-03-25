### Cookie Consent Technical Implementation

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-GUD-014 |
| **Document Type** | Guideline (Technical Standard) |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-04-25 (Bi-Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Web Development Lead |
| **Classification** | Public |

### 1. Purpose
The purpose of this guideline is to define the technical specifications and configuration requirements for the Consent Management Platform (CMP) and cookie handling mechanisms across Study GRC Inc. digital properties. This document bridges the gap between the **Master Data Privacy Policy** and actual code implementation, ensuring that user consent is captured, recorded, and respected in compliance with GDPR, CCPA/CPRA, the Texas Data Privacy and Security Act (TDPSA), and the ePrivacy Directive.

### 2. Scope
This guideline applies to all public-facing websites, the Learning Management System (LMS), and community forums owned or operated by Study GRC Inc.

*   **Applies to:** Web Development Team, Marketing Operations, Third-Party Vendors, and any personnel with access to website tag managers (e.g., Google Tag Manager).
*   **Exclusions:** Backend server-side session management that does not utilize client-side storage mechanisms, provided no personal data is processed.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **CMP (Consent Management Platform)** | Software used to request, receive, and store users' consent for the use of cookies and tracking scripts. |
| **Zero-Load (Prior Consent)** | The technical state where **no** cookies or trackers (except Strictly Necessary) are fired until the user explicitly grants consent. |
| **GPC (Global Privacy Control)** | A browser signal that communicates a user's preference to opt-out of data selling or sharing. |
| **Tag Manager** | A system (e.g., GTM) that manages JavaScript and HTML tags used for tracking and analytics on websites. |
| **Dark Patterns** | User interface designs that trick or manipulate users into making decisions that are not in their best interest (e.g., making the "Reject" button invisible). |

### 4. Technical Guidelines

#### 4.1 Consent Management Platform (CMP) Configuration
The Organization utilizes a designated CMP to handle consent signaling. The CMP must be the **first script** loaded in the `<head>` of the document to ensure it can intercept and block other scripts.

*   **4.1.1 IAB TCF Compliance:** The CMP must be configured to support the IAB Transparency and Consent Framework (TCF) v2.2 or higher to communicate consent status to advertising vendors programmatically.
*   **4.1.2 Cross-Domain Consent:** Where technically feasible and legally permissible, consent should persist across `studygrc.org` and its subdomains (e.g., `learn.studygrc.org`) to improve user experience.
*   **4.1.3 Accessibility:** The CMP banner and preference center must comply with **WCAG 2.2 Level AA** standards, ensuring full keyboard navigability and screen reader compatibility.

#### 4.2 Cookie Categorization and Blocking
All cookies and tracking scripts must be classified into one of four categories. Unclassified cookies are strictly prohibited in the production environment.

*   **Category 1: Strictly Necessary:** Essential for site function (e.g., login session, cart, security).
    *   *Default State:* **Active**. Cannot be disabled.
*   **Category 2: Functional/Preferences:** Stores user choices (e.g., language, region).
    *   *Default State:* **Inactive** (GDPR/EU); **Active** (US/TX - Opt-out).
*   **Category 3: Analytics/Performance:** Aggregated data on site usage (e.g., Google Analytics).
    *   *Default State:* **Inactive** (GDPR/EU); **Active** (US/TX - Opt-out).
*   **Category 4: Marketing/Targeting:** Tracks users across websites to build profiles.
    *   *Default State:* **Inactive** (Global Best Practice for Study GRC).

**Implementation Rule:** Scripts associated with Categories 2, 3, and 4 must be wrapped in conditional logic or managed via the Tag Manager's "Consent Mode" to ensure they **do not fire** until the CMP returns a positive consent signal.

#### 4.3 Geo-Fencing and Regional Logic
To balance compliance with user experience, the CMP must utilize IP-based geo-location to serve the appropriate consent model:

*   **Zone A (EEA/UK/Brazil):** Explicit Opt-In Model (GDPR). No non-essential cookies load before the "Accept" click.
*   **Zone B (California/Virginia/Colorado/Connecticut):** Opt-Out Model with explicit "Do Not Sell/Share" link.
*   **Zone C (Texas - TDPSA):** Study GRC treats Texas residents with the same high standard as Zone B, recognizing Universal Opt-Out Mechanisms.
*   **Zone D (Rest of World):** Implied Consent (Banner notification only), subject to the Organization's ethical stance on data minimization.

#### 4.4 User Interface (UI) Requirements
The consent banner must adhere to the Organization's commitment to transparency and "Kindness" (per Bylaws Article V).

*   **4.4.1 Equal Prominence:** The "Reject All" or "Decline" button must be displayed with the same size, color contrast, and visibility as the "Accept All" button.
*   **4.4.2 No Pre-Ticked Boxes:** In Opt-In zones, checkboxes for non-essential categories must be unchecked by default.
*   **4.4.3 Persistent Re-Consent:** A floating icon or footer link labeled "Cookie Preferences" must be available on every page to allow users to withdraw consent as easily as they gave it.

#### 4.5 Signal Handling (GPC and DNT)
The technical implementation must listen for browser-based privacy signals.

*   **Global Privacy Control (GPC):** If the HTTP header or JavaScript property `navigator.globalPrivacyControl` is detected as `true`, the CMP must automatically treat this as a valid request to opt-out of Sale/Sharing (Category 4) and Targeted Advertising.
*   **Do Not Track (DNT):** While not legally binding in all jurisdictions, Study GRC honors DNT signals by disabling Category 4 cookies by default.

#### 4.6 Youth Protection (COPPA/GDPR-K)
In alignment with the **Child and Youth Safeguarding Policy**:

*   **Age-Gating:** If a user is identified as a minor (under 13 in US, under 16 in EU) via account login or age-gate:
    1.  The CMP must suppress **all** Category 3 (Analytics) and Category 4 (Marketing) cookies regardless of banner interaction.
    2.  Third-party data sharing must be technically severed.

#### 4.7 Data Retention
*   **Consent Log:** The CMP must store a record of the consent (Timestamp, Consent ID, Categories Accepted) for 12 months to demonstrate compliance during an audit.
*   **Cookie Lifespan:** First-party cookies set by Study GRC should not exceed a lifespan of 12 months.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Web Development Lead** | Responsible for the technical integration of the CMP code, configuring Tag Manager triggers, and ensuring Zero-Load prior to consent. |
| **Marketing Operations** | Responsible for correctly classifying new tracking tags/pixels before requesting deployment. |
| **Chief Information Security Officer (CISO)** | Approves the selection of the CMP vendor and conducts annual technical audits of cookie behavior. |
| **Privacy Officer / DPO** | Reviews the UI/UX of the banner to ensure it meets current legal standards (avoiding Dark Patterns). |

### 6. Compliance and Enforcement
Failure to adhere to this guideline may result in data leakage, regulatory fines (GDPR/TDPSA), and reputational damage.
*   **Automated Scanning:** The Organization will employ automated scanning tools monthly to detect unclassified cookies or "cookie leakage" (cookies set before consent).
*   **Enforcement:** Developers or marketers found intentionally bypassing the CMP to deploy tracking scripts will be subject to disciplinary action under the **Code of Conduct**.

### 7. References
*   **IS-POL-007:** Master Data Privacy Policy
*   **IS-POL-008:** Online Privacy Policy
*   **IS-STD-005:** Digital Accessibility Standard (WCAG 2.2)
*   **External:** IAB Europe Transparency & Consent Framework v2.2 Policies
*   **External:** Texas Data Privacy and Security Act (TDPSA)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Legal Officer | Initial release of technical implementation guidelines. |