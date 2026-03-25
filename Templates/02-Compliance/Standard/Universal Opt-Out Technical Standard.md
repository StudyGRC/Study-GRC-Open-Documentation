### Universal Opt-Out Technical Standard

| Document Control | |
| :--- | :--- |
| **Document ID** | DP-STD-011 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Public |

### 1. Purpose
The purpose of this standard is to define the mandatory technical requirements for detecting, processing, and honoring Universal Opt-Out Mechanisms (UOOMs), specifically the Global Privacy Control (GPC), across all Study GRC Inc. digital properties.

This standard ensures compliance with the California Consumer Privacy Act (CCPA) §1798.135, the California Privacy Rights Act (CPRA), and the Texas Data Privacy and Security Act (TDPSA). It aligns with the Organization’s commitment to data transparency as outlined in **Bylaws Article IX (Policies & Data Protection)** and the "Director of Kindness and Generosity" mandate to maintain a respectful community culture.

### 2. Scope
This standard applies to:
*   **Assets:** All public-facing websites, web applications, and mobile applications owned or operated by Study GRC Inc.
*   **Personnel:** Web developers, DevOps engineers, and third-party marketing vendors managing tracking technologies.
*   **Data:** All user data collected via cookies, pixels, beacons, or server-side logging that constitutes "selling" or "sharing" for cross-context behavioral advertising.

**Exclusions:**
*   Internal administrative portals not accessible to the general public.
*   Transactional data strictly necessary for the fulfillment of a user's request (e.g., processing a donation or course registration), which is exempt from opt-out requests.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **UOOM (Universal Opt-Out Mechanism)** | A user-enabled signal sent by a platform, technology, or mechanism (such as a browser extension or operating system setting) that communicates the consumer’s choice to opt-out of the sale or sharing of personal data. |
| **GPC (Global Privacy Control)** | A specific technical specification for transmitting a UOOM via HTTP headers or JavaScript DOM properties. |
| **Sale/Sharing** | Under CCPA/CPRA, the exchange of personal information for monetary or other valuable consideration, or the disclosure of personal information to a third party for cross-context behavioral advertising. |
| **Frictionless Manner** | A method of processing opt-outs that does not charge a fee, change the user's experience, display a notification/pop-up (other than confirmation), or require the user to create an account. |

### 4. Technical Standards

#### 4.1 Signal Detection Requirements
All Study GRC Inc. web properties must automatically detect and parse UOOM signals. The system must listen for the signal in two locations:

1.  **HTTP Header:** The web server must inspect incoming HTTP requests for the header `Sec-GPC`.
    *   If `Sec-GPC: 1` is present, it must be treated as a valid opt-out request.
2.  **JavaScript DOM:** The client-side application must check the `navigator` or `window` object.
    *   If `navigator.globalPrivacyControl` or `window.globalPrivacyControl` evaluates to `true`, it must be treated as a valid opt-out request.

#### 4.2 Signal Processing and Conflict Resolution
Upon detecting a valid `true` or `1` signal:

1.  **Precedence:** The UOOM signal takes precedence over any conflicting "default" settings in the Consent Management Platform (CMP).
2.  **Logged-In Users:** If a user is logged into the Study GRC platform and their account profile previously consented to tracking, the incoming UOOM signal **overrides** the profile setting for that specific browser session. The system should prompt the user (non-intrusively) to update their global profile preferences to match the signal if technically feasible.
3.  **Pseudonymous Users:** For visitors without accounts, the opt-out must be applied immediately to the session ID or cookie ID associated with that browser.

#### 4.3 Downstream Propagation (The "Do Not Fire" Rule)
Detection of the signal must trigger the following technical actions immediately, prior to the loading of non-essential scripts:

1.  **Cookie Suppression:** Marketing, analytics, and social media tracking cookies (e.g., Meta Pixel, Google Ads, LinkedIn Insight Tag) must be blocked from firing.
2.  **Tag Manager Variables:** The Google Tag Manager (or equivalent) Data Layer must be updated.
    *   Example: Set `privacy_consent_marketing = false`.
3.  **Vendor Notification:** If data is passed to third-party processors (e.g., payment processors or email providers) during the session, the API call must include the appropriate privacy flag (e.g., passing `restricted_data_processing=true` to Google APIs).

#### 4.4 User Interface (UI) Feedback
To ensure transparency and reduce user confusion:

1.  **Visual Confirmation:** If a UOOM is detected, the "Do Not Sell or Share My Personal Information" toggle in the website footer or privacy preference center must automatically display as **"Opted Out"** or **"Off"**.
2.  **No Interruption:** The website must **not** display a pop-up, interstitial, or warning asking the user to confirm the signal or attempting to persuade them to change it (strictly prohibited by CCPA §1798.135).

#### 4.5 Persistence
The opt-out status derived from a UOOM must persist for the duration of the user's interaction with the website. If the user returns in a subsequent session with the signal still active, the opt-out remains.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Web Development Lead** | Implement the JavaScript and server-side logic to detect `Sec-GPC` and `navigator.globalPrivacyControl`. Ensure the CMP is configured to respect these signals. |
| **Chief Information Security Officer (CISO)** | Conduct quarterly audits using browser testing tools to verify that tracking pixels do not fire when GPC is enabled. |
| **VP of Education & Training** | Ensure that educational resources remain accessible to users who have opted out (no "privacy walls"). |
| **Marketing Manager** | Adjust analytics reporting to account for "untrackable" traffic resulting from UOOM compliance. |

### 6. Compliance and Enforcement
Failure to comply with this standard puts Study GRC Inc. at risk of regulatory fines under CCPA/CPRA and the Texas Data Privacy and Security Act.

**Technical Enforcement:** Code changes to the website header or Consent Management Platform (CMP) require a mandatory code review by the CISO or a designated Privacy Engineer to ensure UOOM logic is not accidentally disabled.

**Disciplinary Action:** Personnel found intentionally bypassing or disabling opt-out mechanisms may be subject to disciplinary action, up to and including termination of employment or contract.

### 7. References
*   **California Consumer Privacy Act (CCPA):** §1798.135 (Methods of Limiting Sale, Sharing, and Use of Personal Information).
*   **California Code of Regulations:** Title 11, § 7025 (Opt-Out Preference Signals).
*   **Texas Data Privacy and Security Act (TDPSA):** Requirements for recognizing universal opt-out mechanisms.
*   **Global Privacy Control (GPC) Specification:** https://globalprivacycontrol.org/
*   **Study GRC Inc. Bylaws:** Article IX (Policies & Data Protection).
*   **Study GRC Inc. Policy:** DP-POL-001 (Master Data Privacy Policy).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Legal Officer | Initial release to align with CCPA and TDPSA requirements. |