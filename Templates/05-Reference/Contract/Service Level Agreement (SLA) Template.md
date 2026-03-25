### Service Level Agreement (SLA) Template

| Document Control | |
| :--- | :--- |
| **Document ID** | LEG-TMP-025 |
| **Document Type** | Template / Contract Attachment |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Executive Director / CFO |
| **Document Owner** | General Counsel / Procurement Officer |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Service Level Agreement (SLA) Template is to define the specific performance metrics, responsibilities, and expectations between **Study GRC Inc.** ("Customer") and third-party service providers ("Provider"). This document ensures that the Organization receives the value and reliability required to maintain its remote-first operations and educational mission. It establishes a mechanism for measuring performance and applying remedies (Service Credits) in the event of underperformance, ensuring fiscal responsibility and operational continuity.

### 2. Scope
This template applies to all significant service contracts entered into by Study GRC Inc., particularly those involving:
*   IT Infrastructure (Hosting, Cloud Services).
*   Software as a Service (SaaS) platforms critical to operations.
*   Managed Security Services.
*   Consulting or Support Services with recurring deliverables.

**Exclusions:** This template does not apply to employment contracts, one-time transactional purchases of goods (hardware), or volunteer agreements.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Uptime / Availability** | The percentage of time the Service is functional and accessible to Study GRC Inc. users, excluding Scheduled Maintenance. |
| **Downtime** | Any period where the Service is unavailable or fails to perform its material functions. |
| **Scheduled Maintenance** | Planned outages for updates or repairs where the Provider has given at least 48 hours prior written notice. |
| **Response Time** | The time elapsed between the Customer reporting an incident and the Provider acknowledging the receipt of the report. |
| **Resolution Time** | The time elapsed between the reporting of an incident and the restoration of the Service to full functionality. |
| **Service Credit** | A financial credit applied to future invoices as a remedy for failure to meet SLA targets. |
| **RCA** | Root Cause Analysis; a report detailing why a failure occurred and how it will be prevented in the future. |

### 4. Agreement Clauses (Template Content)

*Note to Drafter: The following sections must be customized and included as an addendum or exhibit to the Master Service Agreement (MSA).*

#### 4.1. Service Availability Target
The Provider shall ensure the Service is available **[Insert Percentage, e.g., 99.9%]** of the time during each calendar month ("Availability Target").

**Calculation:**
$$ \text{Availability} = \left( \frac{\text{Total Minutes in Month} - \text{Downtime Minutes}}{\text{Total Minutes in Month}} \right) \times 100 $$

**Exclusions:** Downtime caused by the following shall not count against the Availability Target:
1.  Scheduled Maintenance (conducted within the window of [Time Window, e.g., Saturday 02:00 AM - 06:00 AM CST]).
2.  Force Majeure events (as defined in the MSA).
3.  Issues caused solely by Study GRC Inc.'s negligence or hardware.

#### 4.2. Incident Priority and Response Standards
In the event of a Service issue, the Provider shall adhere to the following response and resolution times based on severity:

| Priority Level | Description | Response Time Target | Resolution Time Target |
| :--- | :--- | :--- | :--- |
| **P1 - Critical** | Service is down; critical business functions (e.g., Learning Platform, Donation Portal) are inaccessible. No workaround exists. | < 30 Minutes | < 4 Hours |
| **P2 - High** | Service is severely degraded; major functions are impaired. Operations can continue with difficulty. | < 2 Hours | < 8 Hours |
| **P3 - Medium** | Minor bug or issue; specific non-critical functions are impaired. Workaround exists. | < 8 Business Hours | < 3 Business Days |
| **P4 - Low** | Cosmetic issue, information request, or feature request. | < 24 Business Hours | Next Release / TBD |

#### 4.3. Service Credits (Performance Remedies)
If the Provider fails to meet the Availability Target or Resolution Time Targets in any given calendar month, Study GRC Inc. is entitled to Service Credits calculated as a percentage of the monthly fees.

**Availability Credits:**
*   **99.0% – 99.89%:** [5]% Credit
*   **95.0% – 98.99%:** [15]% Credit
*   **Below 95.0%:** [30]% Credit

**Support Credits:**
*   Failure to meet P1 Resolution Time: [5]% Credit per incident.

*Total credits in a single month shall not exceed [100]% of the monthly fee.*

#### 4.4. Reporting and Root Cause Analysis (RCA)
1.  **Monthly Reporting:** Provider must submit a monthly performance report detailing Uptime, Downtime minutes, and Ticket Resolution metrics by the [5th] business day of the following month.
2.  **RCA Requirement:** For any P1 (Critical) incident or any Downtime exceeding [1 hour], Provider must submit a formal Root Cause Analysis within [5] business days, detailing the cause and preventative measures taken.

#### 4.5. Data Backup and Recovery (If Applicable)
*   **RPO (Recovery Point Objective):** Data shall be backed up such that no more than [e.g., 1 hour] of data is lost.
*   **RTO (Recovery Time Objective):** Services shall be restored from backup within [e.g., 4 hours] of a catastrophic failure.

#### 4.6. Termination for Chronic Failure
Study GRC Inc. reserves the right to terminate the Master Service Agreement for cause, without penalty, if:
1.  Availability falls below [90]% in any single month; OR
2.  Availability falls below the Availability Target for [three] consecutive months.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Provider** | Monitor systems 24/7, provide support within defined timeframes, issue credits automatically or upon request, and provide RCAs. |
| **Study GRC Contract Owner** | Verify monthly performance reports, report incidents with appropriate severity levels, and formally request Service Credits when due. |
| **Chief Financial Officer (CFO)** | Ensure Service Credits are accurately applied to invoices and monitor the financial impact of vendor underperformance. |
| **Chief Info. Security Officer (CISO)** | Review RCAs for security implications and ensure vendor compliance with data protection standards during outages. |

### 6. Compliance and Enforcement
**Failure to Enforce:** Failure by Study GRC Inc. to demand Service Credits for a specific breach does not constitute a waiver of rights for future breaches.

**Dispute Resolution:** Disputes regarding the classification of incidents (e.g., whether an event was P1 or P2) or the calculation of Uptime shall be resolved via the Dispute Resolution process outlined in the Master Service Agreement.

**Regulatory Alignment:** This SLA supports compliance with **2 CFR 200.318(b)**, which requires non-federal entities to maintain oversight to ensure contractors perform in accordance with the terms, conditions, and specifications of their contracts.

### 7. References
*   **LEG-POL-022:** Procurement Policy (Federal Standards)
*   **IS-POL-058:** Vendor/Third-Party Risk Policy
*   **IS-PRC-045:** Incident Response Plan (IRP)
*   **Master Service Agreement (MSA)** [Linked per specific vendor]

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Legal Officer | Initial Template Release |