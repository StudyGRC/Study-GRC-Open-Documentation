### ARIA Landmark/Role Usage Guidelines

| Document Control | |
| :--- | :--- |
| **Document ID** | IT-GUD-015 |
| **Document Type** | Guideline |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Bi-Annual) |
| **Approving Authority** | VP of Education & Training |
| **Document Owner** | Lead Web Developer / Accessibility Coordinator |
| **Classification** | Public |

### 1. Purpose
The purpose of this guideline is to standardize the implementation of WAI-ARIA (Web Accessibility Initiative - Accessible Rich Internet Applications) landmarks and roles across Study GRC Inc. digital properties.

As an organization dedicated to removing barriers to GRC knowledge (Bylaws Article I, Section 1.3), ensuring our digital resources are navigable by assistive technology users is a core operational requirement. Proper use of landmarks allows screen reader users to programmatically navigate page sections (e.g., jumping directly to the main content or navigation) without wading through repetitive links, satisfying **WCAG 2.2 Criteria 1.3.1 (Info and Relationships)** and **2.4.1 (Bypass Blocks)**.

### 2. Scope
This guideline applies to all web-based technologies developed, maintained, or procured by Study GRC Inc., including but not limited to:
*   The public-facing website (studygrc.org).
*   The Learning Management System (LMS).
*   Community forums and collaboration platforms.
*   Open-source tools and repositories managed by the Organization.

**Audience:** This document is intended for Front-End Developers, UI/UX Designers, Content Managers, and third-party vendors delivering digital products.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **ARIA (WAI-ARIA)** | A technical specification that provides a framework for adding attributes to HTML elements to make web content and applications more accessible to people with disabilities. |
| **Landmark** | A type of ARIA role that programmatically identifies significant sections of a page (e.g., banner, navigation, main, search) to assistive technologies. |
| **Semantic HTML** | HTML elements that clearly describe their meaning in a human- and machine-readable way (e.g., using `<nav>` instead of `<div class="nav">`). |
| **Screen Reader** | Assistive software (e.g., NVDA, JAWS, VoiceOver) that reads text and code structure aloud to users with visual impairments. |
| **DOM** | Document Object Model; the data representation of the objects that comprise the structure and content of a document on the web. |

### 4. Guidelines

#### 4.1 The First Rule of ARIA
Developers must adhere to the **First Rule of ARIA**: *If you can use a native HTML element or attribute with the semantics and behavior you require already built in, then do so instead of repurposing an element and adding an ARIA role, state, or property.*

*   **Preferred:** `<nav>`
*   **Avoid:** `<div role="navigation">` (Unless strictly necessary due to legacy constraints).

#### 4.2 Top-Level Landmark Structure
Every web page within the Study GRC ecosystem should contain the following high-level structural landmarks to ensure consistent navigation.

| HTML5 Element | Implicit ARIA Role | Usage Requirement |
| :--- | :--- | :--- |
| `<header>` | `banner` | **Mandatory.** Must contain the site logo and global tools. Limit to one per page (top level). |
| `<nav>` | `navigation` | **Mandatory.** Used for primary site navigation. |
| `<main>` | `main` | **Mandatory.** Must contain the unique content of the document. **Strictly limited to one per page.** |
| `<footer>` | `contentinfo` | **Mandatory.** Contains copyright, privacy links, and contact info. Limit to one per page. |
| `<aside>` | `complementary` | **Conditional.** Used for sidebars or content related to the main content but separate from it. |
| `<form>` | `search` | **Conditional.** Specifically used for the site search functionality. |

#### 4.3 Labeling Multiple Landmarks
When multiple landmarks of the same type exist on a page (e.g., a primary navigation bar and a footer navigation list), developers **must** distinguish them using `aria-label` or `aria-labelledby`.

**Incorrect Implementation (Ambiguous):**
```html
<nav> ... </nav> <!-- Screen reader says "Navigation" -->
<nav> ... </nav> <!-- Screen reader says "Navigation" -->
```

**Correct Implementation (Distinguishable):**
```html
<nav aria-label="Main"> ... </nav> <!-- Screen reader says "Main Navigation" -->
<nav aria-label="Social Media"> ... </nav> <!-- Screen reader says "Social Media Navigation" -->
```

#### 4.4 The `main` Landmark
To facilitate the "Skip to Content" mechanism required by WCAG 2.4.1:
1.  Each page must have exactly **one** element with the role of `main` (or the `<main>` tag).
2.  The `main` region must not be nested within `header`, `footer`, or `nav` elements.
3.  The `main` region should be the target of the visible "Skip to Main Content" link at the top of the DOM.

#### 4.5 `search` Role Usage
The search functionality is critical for accessibility.
*   Use `<form role="search">` or a `<form>` element containing an `<input type="search">`.
*   Ensure the submit button is clearly labeled.

#### 4.6 `complementary` (Aside) Usage
Use the `complementary` role (via `<aside>`) for content that is meaningful but not critical to the main flow (e.g., "Related Courses," "Upcoming Events").
*   If the content is critical for understanding the main content, it should be part of the `main` region, not an `aside`.

#### 4.7 Prohibited Practices
*   **Redundant Roles:** Do not add default roles to HTML5 elements (e.g., `<nav role="navigation">` is generally unnecessary in modern browsers, though harmless; `<button role="button">` is redundant).
*   **Landmark Overload:** Do not wrap every small section of a page in a landmark. Too many landmarks create "noise" for screen reader users, defeating the purpose of quick navigation.
*   **Orphaned Content:** Ensure all perceptible content resides within a landmark region. Text should not exist outside of `banner`, `main`, `navigation`, or `contentinfo`.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Front-End Developers** | Implement semantic HTML and ARIA landmarks according to this guideline during the coding phase. |
| **UI/UX Designers** | Define the page structure in wireframes to support logical landmark placement (e.g., defining what is "Main" vs. "Complementary"). |
| **QA / Testers** | Verify landmark presence and labeling using automated tools (e.g., WAVE, Axe) and manual screen reader testing. |
| **VP of Education & Training** | Ensure all educational platforms (LMS) adhere to these guidelines to maintain an inclusive learning environment. |

### 6. Compliance and Enforcement
While this document is a *Guideline*, adherence is critical for meeting the mandatory requirements set forth in the **Digital Accessibility Policy**.

Failure to implement proper landmarks results in a violation of WCAG 2.2 Level A criteria. Code submissions (Pull Requests) that fail to meet these structural standards may be rejected by the Chief Information Security Officer (CISO) or the designated accessibility lead until remediated.

### 7. References
*   **Internal:** Digital Accessibility Policy (IT-POL-009)
*   **Internal:** Website Accessibility Statement
*   **External:** [W3C WAI-ARIA Authoring Practices Guide (APG) - Landmarks](https://www.w3.org/WAI/ARIA/apg/practices/landmark-regions/)
*   **External:** [WCAG 2.2 Recommendation](https://www.w3.org/TR/WCAG22/)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Compliance Architect | Initial Release |