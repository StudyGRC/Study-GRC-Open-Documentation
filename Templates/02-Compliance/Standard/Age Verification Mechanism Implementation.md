### Age Verification Mechanism Implementation

| Document Control | |
| :--- | :--- |
| **Document ID** | DP-STD-054 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2024-05-01 |
| **Next Review Date** | 2024-11-01 (Bi-Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Public |

### 1. Purpose
The purpose of this Standard is to define the technical and procedural requirements for age verification and age assurance across Study GRC Inc.’s digital platforms. This document ensures compliance with the **Children’s Online Privacy Protection Act (COPPA) Rule (16 CFR Part 312)**, specifically the "COPPA 2.0" updates regarding mixed-audience platforms, and the **Texas Data Privacy and Security Act (TDPSA)**. It establishes the mechanism to prevent the unauthorized collection of personal information from children under 13 and to identify minor users (13–17) for enhanced privacy protections.

### 2. Scope
This Standard applies to all Study GRC Inc. digital properties, including the public website, Learning Management System (LMS), and community forums (e.g., Discord integrations) where user accounts are created or personal data is collected.

*   **In Scope:** User registration flows, newsletter sign-ups, event registration, and donation processing.
*   **Exclusions:** Passive browsing of public-facing, static educational content where no cookies, tracking pixels, or user input data are collected.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Neutral Age Gate** | An age screening mechanism that asks a user to input their date of birth (DOB) in a neutral manner, without suggesting the correct answer or defaulting to an age above 13. |
| **Mixed Audience Site** | A website or service directed to children but also used by a substantial number of adults, or a general audience site with a specific section directed to children. |
| **Verifiable Parental Consent (VPC)** | Any reasonable effort (taking into consideration available technology) to ensure that a parent of a child receives notice of the operator's personal information collection, use, and disclosure practices, and authorizes the collection. |
| **Session Lock** | A technical control (e.g., a temporary cookie) that prevents a user from immediately re-entering a different date of birth after being identified as underage. |
| **Zero-Data Collection State** | A mode of operation where the system disables all tracking, cookies, and input fields for a specific user session. |

### 4. Standards

#### 4.1 Neutral Age Gate Requirements
Pursuant to **Bylaws Article IX (Policies & Data Protection)** and COPPA regulations regarding mixed-audience platforms, all entry points requiring personal data collection must utilize a **Neutral Age Gate**.

1.  **Input Method:** The interface must require the user to manually enter their Month and Year of birth (or full Date of Birth).
2.  **Prohibited Designs:**
    *   The system **must not** use a checkbox stating "I am over 13."
    *   The system **must not** pre-populate the date fields to a qualifying age (e.g., defaulting to the year 2000).
    *   The system **must not** display text prompting the user to "Enter a valid date" if a minor age is entered; it must simply process the age as entered.
3.  **Placement:** The Age Gate must appear **before** any other personal information (email, name, username) is requested or collected.

#### 4.2 Technical Logic and Thresholds
The backend logic for the Age Verification Mechanism must classify users into three distinct categories based on the calculated age:

*   **Category A: Under 13 (Child)**
    *   **Action:** Immediate block of account creation flow.
    *   **Data Handling:** No personal information (PI) may be written to the database.
    *   **Redirect:** User must be redirected to a generic "Parental Information" page explaining that a parent must initiate the account creation via the *Verifiable Parental Consent* flow.
*   **Category B: 13 to 17 (Teen)**
    *   **Action:** Account creation permitted.
    *   **Data Handling:** Account flagged as `MINOR_TEEN`.
    *   **TDPSA Compliance:** Targeted advertising and data sale (if any) must be technically disabled by default for this flag.
*   **Category C: 18+ (Adult)**
    *   **Action:** Standard account creation permitted.

#### 4.3 Anti-Gaming Measures (Session Lock)
To comply with FTC guidance on preventing children from falsifying age after an initial rejection:

1.  **Cookie/Session Marker:** Upon a user entering a DOB that classifies them as **Category A (Under 13)**, the system must place a temporary session cookie or local storage marker indicating `AGE_FAIL`.
2.  **Block Duration:** This marker must persist for the duration of the browser session or a minimum of 24 hours.
3.  **Re-Entry Prevention:** If a user attempts to restart the registration process while the `AGE_FAIL` marker is present, the system must automatically redirect to the Parental Information page, regardless of the new date entered.

#### 4.4 Verifiable Parental Consent (VPC) Implementation
For users under 13 who require access to educational resources (e.g., K-12 programs), Study GRC Inc. utilizes the **"Email Plus"** method for internal operations and **Payment Verification** for transaction-based services, as defined in **DP-POL-053 (Children's Privacy Policy)**.

1.  **Initiation:** Access for a child under 13 must be initiated by an adult account holder.
2.  **Verification Transaction:** If the "Payment Verification" method is used, the system must process a nominal transaction (e.g., $1.00 donation) using a credit card, debit card, or online payment system that provides notification of each separate transaction to the primary account holder.
3.  **Data Retention:** The record of the VPC (the transaction ID or consent form) must be retained for the life of the child's account to prove compliance during an audit.

#### 4.5 Data Minimization of Date of Birth
In accordance with **Bylaws Article IX, Section 9.3 (Intellectual Property & Data)** and the principle of Data Minimization:

1.  **Storage:** The full Date of Birth (DOB) should **not** be stored in the production database unless legally required for specific grant reporting.
2.  **Derived Data:** The system should calculate the age, assign the appropriate Age Flag (`CHILD`, `TEEN`, `ADULT`), and store the **Month/Year** only if necessary for annual age incrementation.
3.  **Purge:** Raw DOB input data used solely for the Age Gate calculation must be discarded from memory immediately after the session flag is assigned.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Owns the technical architecture of the Age Gate; ensures anti-gaming cookies are secure and effective. |
| **Director of Web Development** | Implements the Neutral Age Gate code; ensures no default dates are set in the UI; maintains the "Session Lock" logic. |
| **Data Protection Officer (DPO)** | Conducts quarterly tests of the Age Gate to ensure it correctly blocks under-13 inputs and triggers VPC flows. |
| **VP of Education & Training** | Ensures K-12 specific curriculum pages are properly gated behind the VPC requirement. |

### 6. Compliance and Enforcement
Failure to comply with this Standard puts Study GRC Inc. at risk of violating federal law (COPPA) and state law (TDPSA), which carries significant financial penalties.

*   **Technical Non-Compliance:** Any deployment of code that bypasses the Neutral Age Gate or sets a default age will be treated as a **Critical Severity Incident** requiring immediate rollback.
*   **Personnel:** Staff found intentionally disabling age verification controls to boost enrollment numbers will be subject to disciplinary action, up to and including termination.

### 7. References
*   **16 CFR Part 312:** Children's Online Privacy Protection Rule (COPPA).
*   **Texas Business & Commerce Code § 541:** Texas Data Privacy and Security Act (TDPSA).
*   **DP-POL-053:** Children's Privacy (Under 16) Policy.
*   **DP-POL-001:** Master Data Privacy Policy.
*   **Bylaws of Study GRC Inc.:** Article IX (Policies & Data Protection).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2024-05-01 | Chief Legal Officer | Initial release aligned with COPPA 2.0 proposed rulemaking and TDPSA requirements. |