### Cookie Policy and Consent Banner

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-013 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Bi-Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Public |

### 1. Purpose
The purpose of this policy is to define the standards and requirements for the use of cookies and similar tracking technologies on all digital properties owned and operated by Study GRC Inc. ("the Organization"). This policy ensures compliance with the General Data Protection Regulation (GDPR), the ePrivacy Directive, and the Texas Data Privacy and Security Act (TDPSA), while upholding the Organization’s commitment to transparency and user trust as outlined in Article IX of the Bylaws.

### 2. Scope
This policy applies to:
*   **Digital Assets:** All websites, subdomains (e.g., `community.studygrc.org`), mobile applications, and learning management systems (LMS) operated by the Organization.
*   **Personnel:** All employees, volunteers, contractors, and third-party vendors involved in web development, marketing, or data analysis.
*   **Users:** All visitors to the Organization's digital properties, regardless of their geographic location.

**Exclusions:**
*   Third-party websites linked to from Organization properties where the Organization has no control over the cookies set by those external sites.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Cookie** | A small text file stored on a user's device by a website to remember information about the user, such as login status, language preference, or behavioral data. |
| **Strictly Necessary Cookies** | Cookies essential for the website to function (e.g., security tokens, load balancing). These do not require consent. |
| **Non-Essential Cookies** | Cookies used for analytics, marketing, or enhanced functionality that are not technically required for the site to operate. |
| **Consent Management Platform (CMP)** | Software used to automate the cookie consent process, block cookies prior to consent, and record user preferences. |
| **First-Party Cookie** | A cookie set by the domain the user is visiting (e.g., `studygrc.org`). |
| **Third-Party Cookie** | A cookie set by a domain other than the one the user is visiting (e.g., Google Analytics, Facebook Pixel). |

### 4. Policy Statements

#### 4.1. Principle of Prior Consent (Opt-In)
In accordance with GDPR Article 6 and the ePrivacy Directive, Study GRC Inc. operates under a strict **"Prior Consent"** model.
*   **Default State:** All non-essential cookies (Analytics, Marketing, Functional) must be **blocked by default** until the user explicitly grants consent.
*   **No Implied Consent:** Scrolling, browsing, or continuing to use the site does *not* constitute valid consent.
*   **Granularity:** Users must be able to consent to specific categories of cookies rather than being forced to accept "all or nothing."

#### 4.2. Cookie Categorization
All cookies deployed on Organization assets must be categorized into one of the following four groups within the CMP:

1.  **Strictly Necessary:** Essential for page navigation, access to secure areas (Member Portal), and security functions. *Consent is not required, but transparency is mandatory.*
2.  **Functional:** Enable the website to provide enhanced functionality and personalization (e.g., remembering a username or region).
3.  **Performance/Analytics:** Allow the Organization to count visits and traffic sources to improve the performance of our open-source resources. All data collected must be aggregated and anonymized where possible.
4.  **Targeting/Marketing:** Used to track visitors across websites to display relevant advertisements. *Note: Given the Organization's non-profit status, the use of these cookies is minimized and strictly regulated.*

#### 4.3. Consent Banner Requirements
The website must display a Consent Banner to all new visitors. The banner must adhere to the following UI/UX standards:

*   **Clear Language:** Must state clearly that cookies are used and for what purpose.
*   **Equal Weight Buttons:** The "Reject All" button must be as visible, accessible, and easy to click as the "Accept All" button. "Dark patterns" (e.g., making the Reject button grey or hidden) are strictly prohibited.
*   **Configuration:** A "Cookie Settings" or "Preferences" button must be available to allow granular selection.
*   **Accessibility:** The banner must be accessible via keyboard navigation and screen readers (WCAG 2.2 AA compliant).

#### 4.4. Youth Protection (COPPA Compliance)
Pursuant to the Organization's *Child and Youth Safeguarding Policy*:
*   If a user is identified or reasonably believed to be under the age of 13 (e.g., via age-gating on specific youth-oriented pages), **Targeting and Performance cookies must be disabled automatically**, regardless of the consent banner interaction.
*   No behavioral profiling data may be collected on known minors.

#### 4.5. Withdrawal of Consent
Users must have the ability to withdraw or modify their consent as easily as they gave it.
*   A persistent "Cookie Settings" link or icon must be visible in the website footer or lower corner of the screen on every page.
*   Upon withdrawal, the CMP must immediately cease processing data and attempt to delete relevant cookies where technically feasible.

#### 4.6. Cookie Lifetime and Data Retention
*   **Expiration:** Cookies should not have an expiration date exceeding 12 months from the date of consent.
*   **Consent Renewal:** Users must be asked to renew their consent at least every 12 months, or sooner if the Policy changes significantly.

#### 4.7. Third-Party Auditing
The CISO or designee must conduct a quarterly scan of the website using the CMP or external tools to identify:
*   New cookies ("Cookie Creep").
*   Unclassified cookies.
*   Cookies setting prior to consent (Compliance failure).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Owns this policy; selects the CMP vendor; conducts quarterly compliance audits. |
| **Web Developer / IT Admin** | Implements the CMP code; ensures cookies are correctly tagged and blocked prior to consent; ensures banner accessibility. |
| **VP of Education & Training** | Ensures LMS platforms comply with cookie categorization and do not track students unnecessarily. |
| **Marketing / Comms Team** | Requests approval from CISO before adding any new tracking pixels or analytics scripts to the website. |
| **All Employees/Volunteers** | Must not implement "shadow IT" or unauthorized tracking tools on Organization web properties. |

### 6. Compliance and Enforcement
Failure to comply with this policy may result in disciplinary action, up to and including termination of employment or volunteer assignment.
*   **Technical Violations:** Unauthorized tracking scripts found during audits will be removed immediately.
*   **Legal Risk:** Non-compliance puts the Organization at risk of significant fines under GDPR (up to €20 million or 4% of global revenue) and reputational damage to our 501(c)(3) status.

### 7. References
*   **GDPR Articles 4(11), 6(1)(a), and 7:** Conditions for Consent.
*   **ePrivacy Directive 2002/58/EC:** Rules on storage of information on user equipment.
*   **Study GRC Bylaws Article IX:** Policies & Data Protection.
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-POL-012:** Master Data Privacy Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name] | Initial Draft created for GDPR compliance. |

---

### Appendix A: Standard Consent Banner Text

**Headline:** We Value Your Privacy

**Body Text:**
"Study GRC Inc. uses cookies to enhance your experience, analyze our traffic, and ensure the security of our community resources. Because we respect your right to privacy, you can choose not to allow some types of cookies. However, blocking some types of cookies may impact your experience of the site and the services we are able to offer."

**Buttons:**
1.  [Accept All Cookies]
2.  [Reject Non-Essential Cookies]
3.  [Cookie Settings]

**Footer Link:**
"Cookie Policy | Privacy Policy"