### Children's Info Processing Limitation Standard

| Document Control | |
| :--- | :--- |
| **Document ID** | PRIV-STD-032 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Public |

### 1. Purpose
The purpose of this Standard is to strictly define the limitations on the collection of Personal Information from children under the age of 13. This document ensures Study GRC Inc. complies with the Children’s Online Privacy Protection Act (COPPA), specifically **16 CFR § 312.8**, by prohibiting the conditioning of a child's participation in an activity on the disclosure of more information than is reasonably necessary to participate in that activity.

### 2. Scope
This Standard applies to:
*   **Personnel:** All employees, Board Directors, Operational Officers, and volunteers of Study GRC Inc.
*   **Assets:** All websites, mobile applications, online services, and digital forms owned or operated by the Organization.
*   **Activities:** Any contest, game, educational course, newsletter, or community event directed to children under 13, or where the Organization has actual knowledge that it is collecting information from a child under 13.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Child** | An individual under the age of 13. |
| **Personal Information (PI)** | Individually identifiable information about an individual collected online, including: first and last name; home or other physical address; online contact information (email, IM handle); screen name or username where it functions as online contact information; telephone number; SSN; persistent identifier (cookie, IP address, device serial number); or a photograph, video, or audio file containing a child’s image or voice. |
| **Reasonably Necessary** | The absolute minimum amount of data required to technically and operationally facilitate a specific activity. If the activity can function without a specific data point, that data point is *not* reasonably necessary. |
| **Conditioning Participation** | Requiring a user to provide data as a prerequisite to access a service, game, prize, or resource (e.g., a mandatory form field). |

### 4. Standard Statements

#### 4.1 General Prohibition on Excessive Collection
In accordance with COPPA § 312.8 and the Organization's commitment to removing barriers to education (Bylaws Art. 1.3), Study GRC Inc. **must not** condition a child’s participation in a game, the offering of a prize, or another activity on the child disclosing more personal information than is reasonably necessary to participate in such activity.

#### 4.2 The "Reasonably Necessary" Test
Before adding any input field to a form or enabling any tracking technology on a child-directed resource, the Project Owner must apply the following test. If the answer to any question is "No," the data collection is prohibited.

1.  **Functional Requirement:** Is this specific piece of data required for the software to execute the immediate task? (e.g., An email is required to send a password reset; a phone number is *not*).
2.  **Immediate Utility:** Is the data used for the current activity, rather than a future, undefined marketing purpose?
3.  **No Less-Intrusive Alternative:** Is there a way to achieve the goal without this data? (e.g., Using a non-unique username instead of a real name).

#### 4.3 Activity-Specific Collection Limits
The following table defines the **maximum** allowable data collection for specific activity types involving children. Collection exceeding these limits requires written approval from the CISO and Legal Counsel.

| Activity Type | Allowable Data Elements (Maximum) | Prohibited Data (Examples) |
| :--- | :--- | :--- |
| **Educational Quiz/Game** | Session Cookie (Non-tracking), Anonymous Score. | Real Name, Email, Address, Persistent Trackers. |
| **Newsletter Subscription** | Parent’s Email Address (for notice/consent). | Child's Email, Child's Name, Phone Number. |
| **Contest Entry** | Parent’s Email (to notify winner). | Home Address (unless they win and shipping is required). |
| **Account Registration** | Username (non-PI), Password, Parent Email. | Real Name, School Name, Geolocation. |
| **One-Time Inquiry** | Online Contact Info (deleted after response). | Persistent storage of contact info. |

#### 4.4 Technical Implementation Requirements
To ensure compliance with this Standard, all digital assets must adhere to the following technical specifications:

*   **4.4.1 Optional Fields:** Forms directed at children must not mark non-essential fields as "Required" or "Mandatory." Ideally, non-essential fields should be removed entirely.
*   **4.4.2 Default Settings:** Privacy settings for child accounts must default to the most restrictive setting (High Privacy).
*   **4.4.3 Tracker Blocking:** Third-party behavioral advertising cookies and tracking pixels must be disabled on all URLs designated as "Child-Directed."
*   **4.4.4 Data Segregation:** Data collected from children must be stored in a manner that allows for immediate isolation and deletion upon parental request, separate from general adult membership data.

#### 4.5 Third-Party Vendor Restrictions
When utilizing third-party tools (e.g., survey platforms, learning management systems) for youth programs:
*   Vendors must be vetted to ensure they do not collect excessive data (e.g., building profiles on students).
*   Contracts must explicitly prohibit the vendor from using data for any purpose other than providing the specific service to Study GRC Inc.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **VP of Education & Training** | Ensures all curriculum and educational games are designed to function with minimal data input. |
| **Chief Information Security Officer (CISO)** | Conducts technical audits of forms and cookies to verify only "reasonably necessary" data is being collected. Approves exceptions. |
| **Director of Kindness & Generosity (DKG)** | Monitors community interactions to ensure moderators do not informally ask children for excessive personal details. |
| **Web Developers / IT Staff** | Implements form validation logic that prevents the submission of excessive data (e.g., blocking submission of phone numbers in text fields). |

### 6. Compliance and Enforcement
Failure to comply with this Standard may result in disciplinary action, up to and including termination of employment or volunteer assignment.
*   **Legal Risk:** Violations of COPPA § 312.8 can result in civil penalties of up to $50,120 per violation.
*   **Remediation:** Any data found to be collected in violation of this standard must be immediately and permanently destroyed (sanitized) in accordance with the *Data Retention and Destruction Policy*.

### 7. References
*   **External:** Children’s Online Privacy Protection Act (COPPA), 15 U.S.C. § 6501–6506.
*   **External:** 16 CFR § 312.8 (Prohibition on conditioning participation).
*   **Internal:** Bylaws Article IX (Policies & Data Protection).
*   **Internal:** PRIV-POL-001 (Master Data Privacy Policy).
*   **Internal:** PRIV-POL-030 (COPPA Compliance Policy).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Compliance Architect | Initial Release aligned with COPPA §312.8 requirements. |