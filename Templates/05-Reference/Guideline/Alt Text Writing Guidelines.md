### Alt Text Writing Guidelines

| Document Control | |
| :--- | :--- |
| **Document ID** | COM-GUD-010 |
| **Document Type** | Guideline |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Vice President of Education & Training |
| **Document Owner** | Director of Kindness and Generosity (DKG) |
| **Classification** | Public |

### 1. Purpose
The purpose of this document is to provide clear, actionable instructions for creating Alternative Text ("Alt Text") for non-text content across Study GRC Inc.'s digital platforms.

This guideline supports the Organization’s mission as defined in **Bylaws Article I, Section 1.3**, specifically the commitment to "empowering learners" and "removing barriers." Furthermore, this document ensures compliance with the **Web Content Accessibility Guidelines (WCAG) 2.2, Success Criterion 1.1.1 (Non-text Content)**, ensuring that individuals utilizing assistive technology have equal access to our educational resources.

### 2. Scope
This guideline applies to all visual media published, hosted, or distributed by Study GRC Inc.

**Applies to:**
*   **Website Content:** Images, icons, and buttons on the main website and subdomains.
*   **Educational Resources:** Diagrams, charts, and screenshots within the Learning Management System (LMS) or downloadable PDFs.
*   **Social Media:** Images posted on LinkedIn, Twitter/X, Discord, and other platforms.
*   **Marketing Materials:** Email newsletters and digital brochures.
*   **Personnel:** All employees, volunteers, Board members, and third-party contractors creating content.

**Exclusions:**
*   Audio-only content (covered under Transcription Standards).
*   Video content (covered under Captioning/Audio Description Standards).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Alt Text (Alternative Text)** | A text description of an image that is read by screen readers or displayed when an image fails to load. It conveys the *meaning* and *function* of the image. |
| **Assistive Technology (AT)** | Software or hardware used by individuals with disabilities to access digital content (e.g., Screen Readers like JAWS, NVDA, or VoiceOver). |
| **Decorative Image** | An image that serves only an aesthetic purpose, provides no information, and has no function (e.g., a visual divider or background texture). |
| **Functional Image** | An image that initiates an action (e.g., a magnifying glass icon for "Search" or a printer icon for "Print"). |
| **Complex Image** | Images containing substantial information, such as GRC frameworks, risk heat maps, flowcharts, or data graphs. |
| **WCAG** | Web Content Accessibility Guidelines; the international standard for web accessibility. |

### 4. Guidelines

#### 4.1 General Principles of Alt Text
When writing Alt Text, the goal is to provide the **equivalent user experience** to someone who cannot see the image.
*   **Be Accurate:** The text must accurately describe the content or function.
*   **Be Concise:** Aim for 125 characters or fewer for simple images. Screen readers may cut off lengthy descriptions.
*   **Context Matters:** The same image may need different Alt Text depending on the surrounding content.
*   **Avoid Redundancy:** Do not repeat information already provided in the caption or adjacent text.
*   **No "Picture of...":** Do not start with "Image of," "Photo of," or "Graphic of." Screen readers announce "Graphic" automatically.

#### 4.2 Informative vs. Decorative Images
Content creators must determine the purpose of the image before writing text.

**4.2.1 Informative Images**
If the image adds new information, it requires descriptive Alt Text.
*   *Example:* A photo of a specific GRC conference speaker.
*   *Bad:* "Man in suit."
*   *Good:* "John Doe presenting on ISO 27001 at the Annual GRC Summit."

**4.2.2 Decorative Images**
If the image is purely for visual flair and adds no context, it should be hidden from screen readers to reduce noise.
*   **Implementation:** Use a null attribute (`alt=""`) in HTML or mark as "Decorative" in CMS/Social Media tools.
*   *Examples:* Stock photos of generic laptops, visual page dividers, or background gradients.

#### 4.3 Functional Images
For images that act as buttons or links, describe the **function**, not the appearance.
*   *Example:* A magnifying glass icon used for a search button.
*   *Bad:* "Magnifying glass."
*   *Good:* "Search website."

#### 4.4 Complex Images (GRC Specific)
Study GRC Inc. frequently utilizes complex diagrams (e.g., Risk Heat Maps, NIST Framework flows). These cannot be fully described in 125 characters.

**4.4.1 Two-Part Strategy**
1.  **Short Alt Text:** Provide a brief label. (e.g., "Chart showing the NIST Cybersecurity Framework Core Functions.")
2.  **Long Description:** Provide the full data in the adjacent text, a caption, or a link to a text-based version.

**4.4.2 Text Embedded in Images**
Avoid using images of text whenever possible. If unavoidable (e.g., a screenshot of a CLI terminal or a specific log entry):
*   The Alt Text must contain the **exact text** shown in the image.
*   If the text is too long, transcribe it in the main body of the article.

#### 4.5 Social Media Specifics
*   **LinkedIn/Twitter/Facebook:** Always use the specific "Add Description" or "ALT" feature before posting. Do not put the Alt Text in the post body unless the platform lacks an accessibility feature.
*   **Hashtags:** If hashtags are used within the Alt Text, use CamelCase (e.g., #StudyGRC) to ensure screen readers pronounce them correctly.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Content Creator / Author** | Responsible for drafting accurate Alt Text at the time of content creation. Must identify if an image is decorative or informative. |
| **Editor / Reviewer** | Verifies that Alt Text is present, accurate, and free of spelling errors before publication. Checks for "image of" redundancy. |
| **Web Developer / IT** | Ensures the CMS (Content Management System) supports Alt Text fields and that the code renders `alt` attributes correctly. |
| **Director of Kindness (DKG)** | Conducts periodic audits of digital content to ensure alignment with inclusivity goals. |

### 6. Compliance and Enforcement
While this document is a Guideline, adherence is critical for legal compliance and fulfilling our 501(c)(3) charitable mission.

*   **Content Rejection:** Content submitted to the VP of Education & Training or the Marketing team without proper Alt Text will be rejected and returned for remediation.
*   **Remediation:** Existing content identified as non-compliant during audits must be updated within 30 days of discovery.
*   **Persistent Non-Compliance:** Volunteers or staff who repeatedly ignore accessibility guidelines may be subject to retraining or removal from content creation duties, as their actions create legal risk and exclude community members.

### 7. References
*   **WCAG 2.2 Recommendation:** [https://www.w3.org/TR/WCAG22/](https://www.w3.org/TR/WCAG22/)
*   **Study GRC Inc. Digital Accessibility Policy (IS-POL-009)**
*   **Study GRC Inc. Brand Identity and Style Guide (OPS-GUD-005)**

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Compliance Architect | Initial Release aligned with WCAG 2.2 |