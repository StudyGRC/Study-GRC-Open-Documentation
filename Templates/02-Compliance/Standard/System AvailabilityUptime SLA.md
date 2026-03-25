### System Availability and Uptime Service Level Agreement (SLA)

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-004 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Director of IT Operations |
| **Classification** | Public |

### 1. Purpose
The purpose of this Standard is to define the acceptable levels of system availability and reliability for Study GRC Inc.'s digital assets. As a remote-first, digital-native non-profit dedicated to "removing financial barriers" and "empowering learners" (Bylaws Art. 1.3), continuous access to our open-source resources and community platforms is critical to our mission. This document establishes the metrics for uptime, the protocols for maintenance, and the transparency requirements regarding service interruptions.

### 2. Scope
This Standard applies to all production-level, public-facing digital services owned or managed by Study GRC Inc.

**In Scope:**
*   **Core Website:** (e.g., studygrc.org) and associated subdomains.
*   **Learning Management System (LMS):** The platform hosting curriculum and quizzes.
*   **Community Platform:** Forums, chat servers, or collaboration tools managed directly by the Organization.
*   **API Services:** Public or partner-facing Application Programming Interfaces.

**Out of Scope:**
*   Development, Staging, or QA environments.
*   Third-party services not under the direct control of the Organization (e.g., GitHub, Discord, upstream ISP outages), though these are monitored.
*   User-side issues (e.g., a member’s local internet connection or browser incompatibility).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Availability** | The percentage of time a specific service is operational and accessible to users over a defined period. |
| **Downtime** | A period during which the service is unavailable to users due to failure. This excludes Scheduled Maintenance. |
| **Scheduled Maintenance** | Planned outages for updates, patches, or hardware upgrades, communicated to the membership in advance. |
| **Uptime Target** | The minimum acceptable percentage of availability (e.g., 99.9%). |
| **Incident** | An unplanned interruption to a service or reduction in the quality of a service. |
| **RCA** | Root Cause Analysis; a retrospective process to identify why an outage occurred. |

### 4. Standards and Requirements

#### 4.1 Availability Targets
Study GRC Inc. commits to a **99.9% ("Three Nines")** availability target for all In-Scope services, measured on a monthly basis.

*   **99.9% Uptime** allows for approximately:
    *   43 minutes of downtime per month.
    *   8.7 hours of downtime per year.

#### 4.2 Calculation of Uptime
Availability is calculated using the following formula:

$$ \text{Availability \%} = \left( \frac{\text{Total Minutes in Month} - \text{Unplanned Downtime Minutes}}{\text{Total Minutes in Month}} \right) \times 100 $$

*Note: Scheduled Maintenance windows are deducted from the "Total Minutes" and do not count as Unplanned Downtime.*

#### 4.3 Scheduled Maintenance
To maintain system security and performance, periodic maintenance is required.
1.  **Notification:** The IT Operations team must provide at least **48 hours' notice** to the membership via the Community Platform and/or email for any maintenance expected to exceed 15 minutes.
2.  **Scheduling:** Whenever possible, maintenance must be scheduled during "off-peak" hours based on global traffic analytics (typically 02:00 UTC to 06:00 UTC).
3.  **Status Page:** All scheduled maintenance must be logged on the Organization’s public System Status Page.

#### 4.4 Emergency Maintenance
In the event of a critical security vulnerability (e.g., a Zero-Day exploit) requiring immediate remediation:
1.  The CISO or Executive Director may authorize **Emergency Maintenance** without the standard 48-hour notice.
2.  Communication to members should be sent as soon as safely possible, explaining the urgency of the security action.

#### 4.5 Monitoring and Alerting
1.  **Automated Monitoring:** The Organization must utilize automated synthetic monitoring tools (e.g., UptimeRobot, Datadog, Pingdom) to check service health at intervals no longer than 5 minutes.
2.  **Alerting:** Downtime events must trigger immediate alerts to the IT Operations team and the CISO via email and instant messaging.

#### 4.6 Transparency and Reporting
In alignment with **Bylaws Article VIII (Records, Transparency & Finance)**, the Organization values trust.
1.  **Public Status Page:** A real-time status page must be publicly accessible, showing the current health of all In-Scope services.
2.  **Incident Reporting:** For any unplanned outage exceeding 60 minutes, a "Post-Incident Review" summary must be published to the Community within 5 business days, detailing:
    *   What happened.
    *   Why it happened (Root Cause).
    *   Steps taken to prevent recurrence.

#### 4.7 Service Credits (Non-Monetary)
As Study GRC Inc. provides resources at zero cost (Bylaws Art 1.3), financial service credits are not applicable. However, in the event of significant downtime affecting timed certifications or course deadlines:
1.  **Deadline Extensions:** The VP of Education & Training shall extend assignment or exam deadlines by a period equal to or greater than the duration of the outage.
2.  **Community Acknowledgment:** The Organization will issue a formal apology to the membership for significant disruptions.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Approves this Standard; authorizes Emergency Maintenance; reviews monthly uptime reports. |
| **Director of IT Operations** | Ensures monitoring tools are active; executes maintenance; manages vendor relationships (hosting providers). |
| **VP of Education & Training** | Determines impact on learners; authorizes deadline extensions during outages. |
| **Director of Kindness & Generosity (DKG)** | Manages community communications during outages to ensure members feel heard and supported. |

### 6. Compliance and Enforcement
**System Reliability:** Failure to meet the 99.9% target for three (3) consecutive months will trigger a mandatory architectural review by the CISO and the Advisory Board to determine necessary infrastructure changes.

**Personnel:** Failure to adhere to the Notification or Reporting requirements defined in this Standard may result in disciplinary action, up to and including termination of employment or volunteer assignment.

### 7. References
*   **Bylaws of Study GRC Inc.** (Specifically Art. 1.3 Purpose & Art. VIII Transparency)
*   **IS-POL-001:** Master Information Security Policy
*   **IS-PRC-015:** Incident Response Plan (IRP)
*   **IS-PRC-020:** Business Continuity Plan (BCP)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name] | Initial Release |