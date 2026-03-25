### Law Enforcement Data Request Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | LEG-PRC-003 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Legal Officer / General Counsel |
| **Classification** | Public (Transparency) |

### 1. Purpose
The purpose of this procedure is to establish a standardized, legally compliant framework for responding to requests for user data from Law Enforcement Agencies (LEAs) and government entities. This document ensures that Study GRC Inc. (the "Organization") balances its duty to cooperate with valid legal process against its commitment to user privacy, data protection, and transparency as mandated by **Bylaws Article IX (Policies & Data Protection)** and **Article VIII (Records, Transparency & Finance)**.

### 2. Scope
This procedure applies to all employees, contractors, officers, and volunteers of the Organization who may receive, process, or fulfill requests for user data.

*   **In Scope:** Subpoenas, search warrants, court orders, National Security Letters (NSLs), and emergency disclosure requests regarding user data.
*   **Out of Scope:** Civil litigation requests (handled under *LEG-PRC-002 Subpoena Response Procedure*), internal investigations, and requests for public-facing non-user data.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **LEA** | Law Enforcement Agency (e.g., FBI, local police, Sheriff, District Attorney). |
| **Valid Legal Process** | A writ, warrant, mandate, or order issued by a court of competent jurisdiction that strictly adheres to the Stored Communications Act (SCA) and relevant state laws. |
| **Non-Content Data** | Basic subscriber information (name, email, IP logs, registration date). |
| **Content Data** | The substance of communications (e.g., private messages, forum posts in private groups, stored files). |
| **MLAT** | Mutual Legal Assistance Treaty; the mechanism by which foreign (non-US) LEAs must request data from US companies. |
| **Gag Order** | A court order (Non-Disclosure Order) prohibiting the Organization from notifying the target user of the data request. |

### 4. Procedures

#### 4.1 Intake and Verification
Any individual receiving a request from an LEA must immediately escalate it to the Chief Legal Officer (CLO) or designated Legal Counsel. Do **not** respond to the LEA directly before legal review.

1.  **Submission Method:** LEAs must submit requests via the dedicated legal email (`legal@[domain].org`) or via registered mail to the Registered Agent listed in **Bylaws Section 1.2**.
2.  **Identity Verification:** The CLO or CISO must verify the identity of the requester.
    *   Confirm the request comes from an official government email domain (e.g., `.gov`, `.police.uk`).
    *   If received by phone, instruct the officer to submit a formal written request on official letterhead.
    *   Call the agency's main switchboard (not the number provided in the signature) to verify the agent's employment if the request appears suspicious.

#### 4.2 Legal Review and Classification
The CLO shall review the request to determine its validity, scope, and jurisdiction.

1.  **Jurisdiction Check:**
    *   **US Requests:** Must be issued by a US court with jurisdiction over Study GRC Inc. (Texas) or federal jurisdiction.
    *   **International Requests:** Study GRC Inc. responds to foreign requests only when issued via a US court through the **MLAT** process, unless an emergency involving imminent threat to life exists.
2.  **Validity Check:** Ensure the document is signed by a judge or magistrate (for warrants/orders) or a clerk/attorney (for subpoenas) and has not expired.
3.  **Classification of Data Requested:**
    *   **Subpoena:** May compel disclosure of *Basic Subscriber Information* only (Name, Email, IP logs).
    *   **Court Order (18 U.S.C. § 2703(d)):** May compel disclosure of *Transactional Records* (metadata, message headers) but not content.
    *   **Search Warrant:** Required for the disclosure of *Content Data* (private messages, files). Must be issued upon a showing of probable cause.

#### 4.3 Data Minimization and Preservation
Upon verifying the request is valid:

1.  **Preservation:** If a **Preservation Request** is received, the CISO must immediately snapshot the relevant user data to prevent deletion or modification. This snapshot is held for 90 days (renewable) pending the issuance of formal legal process.
2.  **Scope Limitation:** The Organization shall interpret requests narrowly. We provide only the specific data fields explicitly requested. We do not volunteer additional data.
3.  **Overbroad Requests:** If a request is overly broad (e.g., "All data on all users"), the CLO will file a motion to quash or negotiate with the LEA to narrow the scope.

#### 4.4 User Notification Policy
In accordance with our commitment to transparency, Study GRC Inc. notifies users of requests for their data **prior** to disclosure, unless:

1.  **Prohibited by Law:** A valid statutory prohibition or court-issued Non-Disclosure Order (Gag Order) exists.
2.  **Emergency:** The request involves an imminent threat of death or serious physical injury (see Section 4.5).
3.  **Counterproductive:** The account is clearly compromised or belongs to a known bad actor (e.g., malware distribution), and notification would impede the investigation.

*Procedure:* If no exception applies, the CLO sends a standard notification email to the user, providing them 7 days to seek a protective order before data is released.

#### 4.5 Emergency Disclosure Requests (EDR)
Under 18 U.S.C. § 2702(b)(8) and (c)(4), the Organization may voluntarily disclose data if we have a good faith belief that an emergency involving **danger of death or serious physical injury** requires immediate disclosure.

1.  **EDR Form:** The LEA must complete the "Emergency Disclosure Request Form" certifying the nature of the emergency.
2.  **Expedited Review:** The CLO and CISO review these requests immediately (24/7 basis).
3.  **Limitation:** Only data necessary to resolve the emergency is released.

#### 4.6 Production and Transmission
1.  **Secure Transfer:** Data must never be sent via plain text email.
2.  **Method:** Use a secure, encrypted file transfer system (e.g., password-protected ZIP via secure link, with password sent via separate channel).
3.  **Chain of Custody:** The CISO maintains a log of exactly what files were generated, hash values of the files, and the timestamp of transmission.

#### 4.7 Transparency Reporting
To maintain public trust and comply with **Bylaws Section 8.2 (Transparency)**:

1.  **Tracking:** All requests are logged in the *Law Enforcement Request Register* (LEG-REG-001).
2.  **Reporting:** The Organization publishes an annual Transparency Report summarizing:
    *   Number of requests received.
    *   Types of requests (Subpoena, Warrant, Order).
    *   Percentage of requests where data was produced.
    *   Number of users affected.
    *   *Note: Reporting is subject to delays required by Gag Orders.*

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Intake Officer (Support/IT)** | Receives initial request; validates sender domain; escalates immediately to Legal; does NOT reply with data. |
| **Chief Legal Officer (CLO)** | Reviews legal validity; negotiates scope; determines user notification status; authorizes final release. |
| **Chief Info. Security Officer (CISO)** | Executes data preservation; retrieves data securely; ensures data minimization; manages secure transmission. |
| **Board of Directors** | Reviews and approves the Annual Transparency Report; provides oversight on high-profile or sensitive requests. |

### 6. Compliance and Enforcement
**Strict Compliance Required:** Unauthorized disclosure of user data to law enforcement without following this procedure is a violation of the Organization's **Privacy Policy** and **Bylaws Article IX**.

*   **Internal:** Employees found violating this procedure may face disciplinary action, up to and including termination.
*   **External:** Providing data without a warrant where one is required may subject the Organization and the individual to civil liability under the Stored Communications Act.
*   **Obstruction:** Destroying data after receiving a Preservation Request or Legal Process is a federal crime.

### 7. References
*   **Bylaws of Study GRC Inc.**
    *   Article VIII (Records, Transparency & Finance)
    *   Article IX (Policies & Data Protection)
*   **Stored Communications Act** (18 U.S.C. § 2701 et seq.)
*   **Texas Code of Criminal Procedure** (Art. 18.02 - Search Warrants)
*   **GDPR Article 48** (Transfers or disclosures not authorized by Union law)
*   **LEG-POL-001 Master Data Privacy Policy**

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Legal Officer | Initial Release |