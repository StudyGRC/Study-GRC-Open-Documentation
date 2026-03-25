### WCAG 2.2 Level AA Compliance Checklist

| Document Control | |
| :--- | :--- |
| **Document ID** | ACC-CHK-001 |
| **Document Type** | Standard / Checklist |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-04-25 (Bi-Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | VP of Education & Training |
| **Classification** | Public |

### 1. Purpose
The purpose of this document is to establish the technical standards required for Study GRC Inc. to meet the **Web Content Accessibility Guidelines (WCAG) 2.2 Level AA**. As an organization dedicated to removing barriers to GRC knowledge (Bylaws Article I, Section 1.3), ensuring our digital ecosystem is accessible to individuals with disabilities is a mission-critical mandate. This checklist serves as the primary auditing tool for all web properties, learning management systems (LMS), and digital resources to mitigate legal risk under the ADA and Section 508 of the Rehabilitation Act.

### 2. Scope
This standard applies to all digital content and technology assets owned, developed, or maintained by Study GRC Inc., including but not limited to:
*   Public-facing websites and portals.
*   The Learning Management System (LMS) and course materials.
*   Internal administrative dashboards.
*   Third-party integrations (where configurable).
*   Electronic documents (PDFs, slide decks) distributed to the community.

**Exclusions:** Archived content published prior to [Date] that is not currently being used for active instruction, unless a specific request for accommodation is made.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **WCAG 2.2** | Web Content Accessibility Guidelines version 2.2, the international standard for web accessibility. |
| **Level AA** | The intermediate level of conformance, which satisfies all Level A and Level AA success criteria. This is the target standard for Study GRC Inc. |
| **POUR** | The four principles of accessibility: Perceivable, Operable, Understandable, and Robust. |
| **ARIA** | Accessible Rich Internet Applications; a set of attributes that define ways to make web content and web applications more accessible to people with disabilities. |
| **Focus Indicator** | A visual effect (usually a ring or outline) that indicates which element on a webpage currently has the keyboard focus. |
| **Assistive Technology (AT)** | Software or hardware used by people with disabilities to interact with digital content (e.g., screen readers, braille displays, switch devices). |

### 4. Compliance Standards & Checklist

All digital assets must be evaluated against the following Success Criteria (SC). "Pass" indicates full compliance; "Fail" requires immediate remediation.

#### 4.1 Principle 1: Perceivable
*Information and user interface components must be presentable to users in ways they can perceive.*

| ID | Success Criteria | Requirement | Status (P/F) |
| :--- | :--- | :--- | :--- |
| **1.1.1** | **Non-text Content** (Level A) | All images, icons, and non-text elements have equivalent alternative text (alt text). Decorative images are hidden from screen readers (empty alt attribute). | |
| **1.2.1** | **Audio-only and Video-only (Prerecorded)** (Level A) | Transcripts are provided for audio-only content. Text descriptions or audio tracks are provided for video-only content. | |
| **1.2.2** | **Captions (Prerecorded)** (Level A) | Synchronized captions are provided for all prerecorded video content. | |
| **1.2.3** | **Audio Description or Media Alternative** (Level A) | A transcript or audio description is provided for video content to describe visual information not conveyed through audio. | |
| **1.2.4** | **Captions (Live)** (Level AA) | Live training sessions and webinars include real-time captioning (CART or automated with high accuracy). | |
| **1.2.5** | **Audio Description (Prerecorded)** (Level AA) | Audio description is provided for all prerecorded video content. | |
| **1.3.1** | **Info and Relationships** (Level A) | Information, structure, and relationships conveyed through presentation (e.g., headings `<h1>`-`<h6>`, lists, tables) can be programmatically determined. | |
| **1.3.2** | **Meaningful Sequence** (Level A) | The reading order of content is logical and intuitive when navigated by a screen reader. | |
| **1.3.3** | **Sensory Characteristics** (Level A) | Instructions do not rely solely on sensory characteristics (e.g., "click the green button" or "look at the right column"). | |
| **1.3.4** | **Orientation** (Level AA) | Content does not restrict its view and operation to a single display orientation (portrait or landscape). | |
| **1.3.5** | **Identify Input Purpose** (Level AA) | Input fields collecting personal data have correct `autocomplete` attributes to allow browsers to autofill user data. | |
| **1.4.1** | **Use of Color** (Level A) | Color is not used as the only visual means of conveying information, indicating an action, prompting a response, or distinguishing a visual element. | |
| **1.4.3** | **Contrast (Minimum)** (Level AA) | Text and images of text have a contrast ratio of at least 4.5:1 (large text 3:1). | |
| **1.4.4** | **Resize Text** (Level AA) | Text can be resized without assistive technology up to 200 percent without loss of content or functionality. | |
| **1.4.5** | **Images of Text** (Level AA) | Text is used to convey information rather than images of text, except where a specific presentation is essential (e.g., logos). | |
| **1.4.10** | **Reflow** (Level AA) | Content can be presented without loss of information or functionality, and without requiring scrolling in two dimensions (vertical scrolling only at 320 CSS pixels). | |
| **1.4.11** | **Non-text Contrast** (Level AA) | User interface components (buttons, inputs) and graphical objects have a contrast ratio of at least 3:1 against adjacent colors. | |
| **1.4.12** | **Text Spacing** (Level AA) | No loss of content or functionality occurs when users override text spacing (line height, paragraph spacing, letter spacing, word spacing). | |
| **1.4.13** | **Content on Hover or Focus** (Level AA) | Where hover or focus triggers additional content (tooltips), the content is dismissible, hoverable, and persistent. | |

#### 4.2 Principle 2: Operable
*User interface components and navigation must be operable.*

| ID | Success Criteria | Requirement | Status (P/F) |
| :--- | :--- | :--- | :--- |
| **2.1.1** | **Keyboard** (Level A) | All functionality is available from a keyboard (no mouse required). | |
| **2.1.2** | **No Keyboard Trap** (Level A) | Keyboard focus does not get "trapped" within a component; the user can navigate away using standard keys. | |
| **2.1.4** | **Character Key Shortcuts** (Level A) | If single-key shortcuts are implemented, they can be turned off, remapped, or are active only on focus. | |
| **2.2.1** | **Timing Adjustable** (Level A) | If a time limit is set (e.g., quiz timer), the user can turn off, adjust, or extend the limit (exceptions apply for real-time events). | |
| **2.2.2** | **Pause, Stop, Hide** (Level A) | Moving, blinking, or scrolling information that starts automatically, lasts more than 5 seconds, and is presented in parallel with other content can be paused, stopped, or hidden. | |
| **2.3.1** | **Three Flashes or Below Threshold** (Level A) | Web pages do not contain anything that flashes more than three times in any one second period. | |
| **2.4.1** | **Bypass Blocks** (Level A) | A mechanism is available to bypass blocks of content that are repeated on multiple Web pages (e.g., "Skip to Content" link). | |
| **2.4.2** | **Page Titled** (Level A) | Web pages have titles that describe topic or purpose. | |
| **2.4.3** | **Focus Order** (Level A) | If a Web page can be navigated sequentially, the focus order preserves meaning and operability. | |
| **2.4.4** | **Link Purpose (In Context)** (Level A) | The purpose of each link can be determined from the link text alone or from the link text together with its programmatically determined link context. | |
| **2.4.5** | **Multiple Ways** (Level AA) | More than one way is available to locate a Web page within a set of Web pages (e.g., search, sitemap). | |
| **2.4.6** | **Headings and Labels** (Level AA) | Headings and labels describe topic or purpose. | |
| **2.4.7** | **Focus Visible** (Level AA) | Any keyboard operable user interface has a mode of operation where the keyboard focus indicator is visible. | |
| **2.4.11** | **Focus Not Obscured (Minimum)** (Level AA) **[New in 2.2]** | When a user interface component receives keyboard focus, the component is not entirely hidden due to author-created content (e.g., sticky headers/footers). | |
| **2.5.1** | **Pointer Gestures** (Level A) | All functionality that uses multipoint or path-based gestures (e.g., pinch-to-zoom, swiping) can be operated with a single pointer without a path-based gesture. | |
| **2.5.2** | **Pointer Cancellation** (Level A) | For functionality that can be operated using a single pointer, completion of the function is on the up-event (release), and there is a mechanism to abort or undo. | |
| **2.5.3** | **Label in Name** (Level A) | For user interface components with labels that include text or images of text, the name contains the text that is presented visually. | |
| **2.5.4** | **Motion Actuation** (Level A) | Functionality that can be operated by device motion or user motion can also be operated by user interface components (e.g., shaking device to undo). | |
| **2.5.7** | **Dragging Movements** (Level AA) **[New in 2.2]** | All functionality that uses a dragging movement for operation can be achieved by a single pointer without dragging (e.g., drag-and-drop has a click-based alternative). | |
| **2.5.8** | **Target Size (Minimum)** (Level AA) **[New in 2.2]** | The size of the target for pointer inputs is at least 24x24 CSS pixels, unless there is sufficient spacing or it is inline text. | |

#### 4.3 Principle 3: Understandable
*Information and the operation of user interface must be understandable.*

| ID | Success Criteria | Requirement | Status (P/F) |
| :--- | :--- | :--- | :--- |
| **3.1.1** | **Language of Page** (Level A) | The default language of each Web page can be programmatically determined (e.g., `<html lang="en">`). | |
| **3.1.2** | **Language of Parts** (Level AA) | The human language of each passage or phrase in the content can be programmatically determined (if different from default). | |
| **3.2.1** | **On Focus** (Level A) | When any component receives focus, it does not initiate a change of context. | |
| **3.2.2** | **On Input** (Level A) | Changing the setting of any user interface component does not automatically cause a change of context unless the user has been advised of the behavior before using the component. | |
| **3.2.3** | **Consistent Navigation** (Level AA) | Navigational mechanisms that are repeated on multiple Web pages occur in the same relative order each time they are repeated. | |
| **3.2.4** | **Consistent Identification** (Level AA) | Components that have the same functionality within a set of Web pages are identified consistently. | |
| **3.2.6** | **Consistent Help** (Level A) **[New in 2.2]** | If a help mechanism (e.g., contact info, chat) is available, it appears in the same relative place across pages. | |
| **3.3.1** | **Error Identification** (Level A) | If an input error is automatically detected, the item that is in error is identified and the error is described to the user in text. | |
| **3.3.2** | **Labels or Instructions** (Level A) | Labels or instructions are provided when content requires user input. | |
| **3.3.3** | **Error Suggestion** (Level AA) | If an input error is automatically detected and suggestions for correction are known, then the suggestions are provided to the user. | |
| **3.3.4** | **Error Prevention (Legal, Financial, Data)** (Level AA) | For pages that cause legal commitments or financial transactions, submissions are reversible, checked, or confirmed. | |
| **3.3.7** | **Redundant Entry** (Level A) **[New in 2.2]** | Information previously entered by or provided to the user that is required to be entered again in the same process is either auto-populated or available for the user to select (e.g., Shipping same as Billing). | |
| **3.3.8** | **Accessible Authentication (Minimum)** (Level AA) **[New in 2.2]** | A cognitive function test (e.g., solving a puzzle, memorizing a password) is not required for any step in an authentication process unless an alternative or help mechanism is provided (e.g., copy/paste allowed, password managers supported). | |

#### 4.4 Principle 4: Robust
*Content must be robust enough that it can be interpreted reliably by a wide variety of user agents, including assistive technologies.*

| ID | Success Criteria | Requirement | Status (P/F) |
| :--- | :--- | :--- | :--- |
| **4.1.1** | **Parsing** (Level A) | *Note: This criteria is obsolete in WCAG 2.2 but maintained for legacy alignment.* Ensure HTML is well-formed (start/end tags, unique IDs). | |
| **4.1.2** | **Name, Role, Value** (Level A) | For all user interface components (form elements, links, components generated by scripts), the name and role can be programmatically determined; states, properties, and values that can be set by the user can be programmatically set; and notification of changes to these items is available to user agents (ARIA usage). | |
| **4.1.3** | **Status Messages** (Level AA) | In content implemented using markup languages, status messages can be programmatically determined through role or properties such that they can be presented to the user by assistive technologies without receiving focus (e.g., `role="status"` or `aria-live`). | |

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **VP of Education & Training** | Owner of this standard. Ensures all curriculum and LMS platforms meet Level AA compliance prior to release. |
| **Chief Information Security Officer (CISO)** | Ensures authentication mechanisms (SC 3.3.8) and security tools do not violate accessibility standards. |
| **Developers / Engineering** | Responsible for technical implementation (ARIA, keyboard navigation, focus management, code structure). |
| **Content Creators** | Responsible for semantic structure, alt text, captions, and readability of content within the LMS and website. |
| **QA / Testers** | Conducts audits using this checklist prior to any major release or update. |

### 6. Compliance and Enforcement
Failure to comply with this standard may result in disciplinary action, up to and including termination of employment or volunteer assignment. Non-compliant code or content will be rejected during the Quality Assurance (QA) phase and must be remediated before deployment to production.

Per **Bylaws Article IX**, all intellectual property and open-source contributions created for the Organization must adhere to these standards to ensure they remain accessible to the community.

### 7. References
*   [W3C WCAG 2.2 Recommendation](https://www.w3.org/TR/WCAG22/)
*   [Study GRC Digital Accessibility Policy (ACC-POL-001)]
*   [Section 508 of the Rehabilitation Act]
*   [Americans with Disabilities Act (ADA)]

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Compliance Architect | Initial Draft aligned with WCAG 2.2 release. |