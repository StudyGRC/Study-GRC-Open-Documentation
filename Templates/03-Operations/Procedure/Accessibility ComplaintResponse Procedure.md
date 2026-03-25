### Accessibility Complaint/Response Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | ACC-PRC-005 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | VP of Education & Training / CISO |
| **Classification** | Public |

### 1. Purpose
The purpose of this procedure is to establish a standardized, transparent, and effective mechanism for receiving, investigating, and resolving complaints regarding digital accessibility. As a Federal Grantee and 501(c)(3) organization, Study GRC Inc. is committed to ensuring our digital assets are accessible to individuals with disabilities in accordance with the Americans with Disabilities Act (ADA), Section 504 of the Rehabilitation Act, and the Web Content Accessibility Guidelines (WCAG) 2.2 Level AA.

This procedure ensures that when barriers are identified by users, the Organization provides:
1.  Prompt acknowledgment of the issue.
2.  Immediate reasonable accommodation (alternative access).
3.  A timeline for technical remediation.

### 2. Scope
This procedure applies to all digital assets owned or controlled by Study GRC Inc., including but not limited to:
*   Public-facing websites (studygrc.org).
*   Learning Management Systems (LMS) and courseware.
*   Digital documents (PDFs, Word docs, Slides) distributed to the public or members.
*   Third-party platforms where the Organization controls the content.

**Exclusions:** This procedure does not apply to third-party websites linked from our assets that are not under our control, though the Organization will make reasonable efforts to advocate for accessibility with those vendors.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Accessibility Barrier** | Any technical or design element that prevents a user with a disability from navigating, understanding, or interacting with digital content. |
| **Complainant** | The individual (member, student, parent, or public user) reporting the accessibility issue. |
| **Interim Accommodation** | A temporary solution provided to the user to access the information or service while the technical fix is being implemented (e.g., providing a transcript for a video that lacks captions). |
| **Remediation** | The technical process of fixing code, design, or content to meet WCAG 2.2 AA standards. |
| **Section 504** | Part of the Rehabilitation Act of 1973 prohibiting discrimination based on disability in programs receiving federal financial assistance. |

### 4. Procedures

#### 4.1 Complaint Intake Channels
The Organization must maintain visible and accessible channels for reporting barriers.
1.  **Dedicated Email:** The address `accessibility@studygrc.org` must be monitored daily by the Support Team.
2.  **Website Footer:** A link titled "Accessibility Feedback" must be present in the footer of all web properties, linking to the Accessibility Statement and a simple submission form.
3.  **Phone/Voice:** Users may report issues via the Organization’s primary contact number. Staff receiving these calls must transcribe the complaint into the ticketing system immediately.

#### 4.2 Step 1: Acknowledgment and Triage (0-2 Business Days)
Upon receipt of a complaint, the designated Support Lead must:
1.  **Log the Ticket:** Create a ticket in the IT Service Management system tagged as `CATEGORY: ACCESSIBILITY` and `PRIORITY: HIGH`.
2.  **Send Acknowledgment:** Send a non-automated, empathetic response to the Complainant within two (2) business days.
    *   *Standard Language:* "Thank you for bringing this to our attention. We are investigating the issue and will follow up with you shortly. If you need immediate access to this specific information, please let us know how we can assist you right now."
3.  **Initial Assessment:** Determine if the issue is:
    *   **Critical Blocker:** Prevents access to core services (e.g., "I cannot register for a class").
    *   **Major Barrier:** Makes access difficult but not impossible.
    *   **Minor/Cosmetic:** Does not prevent understanding or operation.

#### 4.3 Step 2: Investigation and Validation (2-5 Business Days)
The Technical Team (Web Developer or CISO) must:
1.  **Reproduce the Issue:** Attempt to replicate the barrier using assistive technology (e.g., NVDA, VoiceOver, keyboard-only navigation) or automated testing tools.
2.  **Confirm Validity:** Verify if the issue violates WCAG 2.2 AA standards.
3.  **Determine Root Cause:** Identify if the issue is content-based (e.g., missing alt text), code-based (e.g., bad ARIA labels), or platform-based (vendor issue).

#### 4.4 Step 3: Interim Accommodation (Immediate)
If the barrier cannot be fixed within 24 hours, the Director of Kindness and Generosity (DKG) or designee must contact the Complainant to offer an alternative way to access the service.
*   **Examples:**
    *   Reading a document over the phone.
    *   Emailing a text-only version of a PDF.
    *   Manually processing a registration that failed online.
*   **Documentation:** The specific accommodation provided must be recorded in the ticket.

#### 4.5 Step 4: Remediation Plan and Execution
Based on the severity, the Technical Team must schedule the fix:

| Severity | Target Resolution Time | Action |
| :--- | :--- | :--- |
| **Critical Blocker** | 1 - 5 Business Days | Immediate hotfix deployment. |
| **Major Barrier** | 10 Business Days | Prioritized in current development sprint. |
| **Minor/Cosmetic** | 30 - 60 Business Days | Scheduled for next major maintenance release. |
| **Vendor Issue** | Variable | Ticket logged with vendor; follow-up every 14 days until resolved. |

#### 4.6 Step 5: Verification and Closure
Once the fix is deployed:
1.  **QA Testing:** The fix must be tested against the specific assistive technology used by the Complainant (if known) and general WCAG standards.
2.  **User Notification:** The Support Lead must notify the Complainant that the issue has been resolved.
    *   *Invitation to Retest:* "We have deployed a fix for the issue you reported. Please let us know if this resolves the barrier for you."
3.  **Ticket Closure:** Close the ticket only after verification.

#### 4.7 Record Keeping
To ensure compliance with Federal Grant requirements and potential OCR (Office for Civil Rights) audits, the Organization must retain the following for a period of three (3) years:
1.  Original complaint (email/transcript).
2.  Record of interim accommodation offered/provided.
3.  Technical details of the remediation.
4.  Final communication with the Complainant.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Executive Director** | Ultimate accountability for compliance; approves budget for necessary remediation tools or vendors. |
| **Director of Kindness & Generosity (DKG)** | Manages communication with the Complainant; ensures tone is empathetic and non-defensive; facilitates interim accommodations. |
| **CISO / IT Lead** | Oversees technical investigation; validates WCAG compliance; manages vendor relationships for third-party platform issues. |
| **Web Developer** | Implements code-level fixes; performs regression testing to ensure fixes do not break other accessibility features. |
| **All Staff** | Responsible for forwarding any accessibility complaints received via personal email or phone to the dedicated channel immediately. |

### 6. Compliance and Enforcement
Failure to adhere to this procedure may result in:
1.  **Legal Liability:** Exposure to lawsuits under the ADA or loss of federal funding under Section 504.
2.  **Reputational Damage:** Loss of trust within the GRC community.
3.  **Disciplinary Action:** Staff members who willfully ignore accessibility complaints or fail to report them may face disciplinary action, up to and including termination, in accordance with the *Progressive Discipline Policy*.

### 7. References
*   **ACC-POL-001:** Digital Accessibility Policy
*   **GOV-POL-012:** Document Retention and Destruction Policy
*   **External:** Web Content Accessibility Guidelines (WCAG) 2.2
*   **External:** Section 504 of the Rehabilitation Act of 1973
*   **External:** Americans with Disabilities Act (ADA) Title III

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Compliance Architect | Initial Release |