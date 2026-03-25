### Software Installation Approval Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | IT-PRC-005 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a standardized process for the request, review, approval, and installation of software on Study GRC Inc. (the "Organization") information systems. This procedure is designed to:
1.  **Mitigate Security Risks:** Prevent the introduction of malware, spyware, and vulnerabilities associated with unvetted software.
2.  **Ensure Legal Compliance:** Guarantee that all software is properly licensed for organizational use, preventing copyright infringement and liability.
3.  **Maintain System Stability:** Ensure software compatibility with the Organization’s Standard Operating Environment (SOE).
4.  **Control Costs:** Prevent "Shadow IT" and unnecessary expenditure on redundant tools.

### 2. Scope
This procedure applies to:
*   **Personnel:** All employees, contractors, volunteers, and Board members utilizing Organization-owned assets.
*   **Assets:** All Organization-owned endpoints (laptops, desktops, mobile devices), servers, and cloud environments.
*   **Software:** All applications, including commercial off-the-shelf (COTS) software, Open Source Software (OSS), freeware, shareware, browser extensions, and SaaS applications requiring local agents.

**Exclusions:**
*   Software updates and patches managed centrally by IT via the Patch Management Policy.
*   Personal devices (BYOD) not connected to the Organization's internal network or VPN, provided no Organization data is processed on the unapproved software.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Allowlist (Standard Software List)** | A list of pre-approved software applications that are vetted for security and licensing and are authorized for installation without a new approval request. |
| **Shadow IT** | Information technology systems, software, and services managed without the knowledge or approval of the IT/Security department. |
| **Local Admin Rights** | User account privileges that allow the installation of software and modification of system settings. |
| **EULA** | End User License Agreement; the legal contract between the software author and the user. |
| **MDM** | Mobile Device Management; software used by IT to secure, monitor, and manage end-user mobile devices and laptops. |

### 4. Procedures

#### 4.1. Verification Against Allowlist
Before submitting a request, the Requester must check the Organization’s **Standard Software List** (published on the Intranet/Wiki).
*   **If the software is on the list:** The user may proceed to Step 4.5 (Installation) by requesting deployment via the IT Service Desk.
*   **If the software is NOT on the list:** The user must proceed to Step 4.2.

#### 4.2. Submission of Software Request
The Requester must submit a "Software Request Ticket" via the IT Help Desk system containing the following information:
1.  **Software Name and Version.**
2.  **Vendor/Developer Name and Website URL.**
3.  **Business Justification:** Specific explanation of why this software is necessary for the role or project.
4.  **Cost:** License cost (per user or flat rate) and funding source (Department Budget or Grant ID).
5.  **Data Usage:** Will this software process Personally Identifiable Information (PII) or Confidential data?

#### 4.3. Managerial Approval
The Requester’s direct manager receives the ticket for initial review. The manager must validate:
1.  **Necessity:** The software is required for job performance.
2.  **Budget:** Funds are available (if the software is not free).
3.  **Redundancy:** No existing approved tool performs the same function.

#### 4.4. Security and Licensing Review (IT/CISO)
Upon Manager approval, the CISO or designated IT Analyst performs a vetting process:

**4.4.1 Security Assessment**
*   Review the software for known vulnerabilities (CVEs).
*   Analyze the vendor's reputation and security posture (supply chain risk).
*   For Open Source Software: Verify the project is actively maintained and check for malicious code indicators.
*   Review requested permissions (e.g., does it require full disk access?).

**4.4.2 Licensing Compliance**
*   Review the EULA to ensure compliance with the Organization’s non-profit status.
*   **Critical Check:** Verify "Free for Personal Use" vs. "Commercial/Organizational Use." Many "free" tools require payment when used by an organization.
*   Confirm the license type (Perpetual, Subscription, Floating).

**4.4.3 Compatibility Check**
*   Ensure the software does not conflict with existing security agents (EDR, VPN) or the operating system version.

#### 4.5. Approval Decision
*   **Approved:** The ticket is updated with installation instructions. The software is added to the Asset Inventory.
*   **Denied:** The ticket is closed with a specific reason provided (e.g., "Security Risk," "Duplicate Functionality," "Licensing Incompatibility").
*   **Conditional Approval:** Approved for a specific timeframe or isolated environment (sandbox) only.

#### 4.6. Installation
To maintain the **Principle of Least Privilege**, users are generally not granted Local Admin rights. Installation occurs via one of the following methods:
1.  **Automated Deployment (Preferred):** IT pushes the software via the Organization’s MDM/RMM solution.
2.  **Remote Assisted Installation:** IT connects remotely to the user’s machine to enter Admin credentials and complete the installation.
3.  **Temporary Admin Access:** In rare cases, a temporary, time-bound elevation of privileges is granted to the user to perform the install, followed by immediate revocation.

#### 4.7. Post-Installation Documentation
The IT Department must:
1.  Record the license key and expiration date in the **Software Asset Management (SAM)** register.
2.  Retain proof of purchase/entitlement for audit purposes.
3.  If the software is to be widely used, add it to the **Standard Software List**.

#### 4.8. Periodic Audit and Removal
*   **Quarterly Scans:** IT will scan network endpoints to identify unauthorized software.
*   **Unused Software:** Software not used for 90 days may be reclaimed/uninstalled to free up licenses and reduce attack surface.
*   **Unauthorized Software:** Any software found that bypassed this procedure will be immediately removed, and the incident reported to the CISO.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Requester** | Verifies Allowlist status; submits complete requests with business justification; adheres to license terms. |
| **Department Manager** | Approves budget and validates business necessity; ensures staff do not install unauthorized software. |
| **IT Analyst** | Performs technical compatibility checks; executes installation via MDM/Remote tools; maintains the SAM register. |
| **CISO** | Conducts security risk assessments; reviews EULAs for compliance; holds final authority to deny software based on risk. |
| **Executive Director** | Approves significant software expenditures exceeding the CISO's delegation of authority. |

### 6. Compliance and Enforcement
Strict adherence to this procedure is required to maintain the Organization's security posture and legal standing.
*   **Disciplinary Action:** Installation of unauthorized software, particularly pirated software or hacking tools, constitutes a violation of the **Acceptable Use Policy** and **Code of Ethics**. Consequences may include removal of access rights, termination of employment/volunteer status, and legal action.
*   **Legal Liability:** Users who install unlicensed software may be held personally liable for copyright infringement under applicable laws.

### 7. References
*   **IS-POL-001:** Master Information Security Policy
*   **IS-POL-002:** Acceptable Use Policy (AUP)
*   **IS-POL-020:** Software Licensing Compliance Policy
*   **IS-STD-005:** Standard Software Allowlist
*   **NIST SP 800-53 (CM-11):** User-Installed Software

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | CISO | Initial Release |