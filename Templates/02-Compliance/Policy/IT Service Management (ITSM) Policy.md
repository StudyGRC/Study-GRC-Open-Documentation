### IT Service Management (ITSM) Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IT-POL-001 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2025-10-27 (Bi-Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this policy is to establish a formal framework for the design, delivery, management, and improvement of IT services within Study GRC Inc. This policy ensures that IT services align with the Organization’s charitable mission, support a remote-first workforce, and adhere to the **ITIL (Information Technology Infrastructure Library)** framework. It mandates a structured approach to service delivery to maximize reliability, security, and cost-effectiveness in compliance with 2 CFR 200 (Uniform Guidance) for federal grantees.

### 2. Scope
This policy applies to all Information Technology resources, services, and personnel (including employees, volunteers, and contractors) associated with Study GRC Inc.

*   **In Scope:**
    *   All cloud-based services (SaaS, PaaS, IaaS).
    *   End-user computing support and device management.
    *   Network infrastructure (where applicable in a remote context).
    *   Software development and deployment lifecycles.
*   **Exclusions:**
    *   Personal devices (BYOD) not used for accessing Organizational Data, unless specifically enrolled in the Mobile Device Management (MDM) program.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Change Management** | The process of controlling the lifecycle of all changes, enabling beneficial changes to be made with minimum disruption to IT services. |
| **Incident** | An unplanned interruption to an IT service or reduction in the quality of an IT service. |
| **Problem** | A cause, or potential cause, of one or more Incidents. |
| **Service Catalog** | A centralized database or structured document containing accurate information on all operational IT services available to the organization. |
| **SLA (Service Level Agreement)** | A documented agreement between the IT function and the business (or users) that defines the level of service expected. |
| **CISO** | Chief Information Security Officer, as defined in **Bylaws Article V, Section 5.2**. |

### 4. Policy Statements

#### 4.1 Service Strategy and Governance
4.1.1 **Alignment with Mission:** All IT services must directly support the Organization’s mission to foster a GRC community and provide open-source resources. IT investments must be justified by business value and approved in accordance with the **Budget Development and Approval Policy**.
4.1.2 **Service Catalog:** The CISO must maintain an up-to-date **Service Catalog** detailing all approved software, hardware standards, and support services available to staff and volunteers. Shadow IT (unauthorized services) is strictly prohibited.

#### 4.2 Service Design
4.2.1 **Security by Design:** In accordance with the **Master Information Security Policy**, all new IT services must undergo a security review prior to procurement or deployment.
4.2.2 **Availability and Capacity:** Service designs must account for the remote nature of the workforce, ensuring accessibility across distributed geographies. Capacity planning must be conducted annually to prevent over-provisioning (waste of donor funds) or under-provisioning (performance degradation).
4.2.3 **SLA Definition:** Critical services (e.g., Learning Management System, Donor CRM) must have defined Service Level Agreements (SLAs) regarding uptime and support response times.

#### 4.3 Service Transition (Change Management)
4.3.1 **Change Control:** To minimize disruption, all changes to production systems, critical infrastructure, or public-facing platforms must follow the **Change Control and Management Procedure**.
4.3.2 **Change Authority:**
*   **Standard Changes:** Pre-authorized, low-risk changes (e.g., password resets) do not require specific approval.
*   **Normal Changes:** Require approval from the CISO or designated IT Manager.
*   **Emergency Changes:** Require immediate approval from the CISO or Executive Director and must be documented retroactively.
4.3.3 **Testing:** No change may be deployed to production without successful testing in a non-production environment, where feasible.

#### 4.4 Service Operation
4.4.1 **Incident Management:** All IT issues must be logged as "Incidents" in the Organization’s designated ticketing system. Incidents must be prioritized based on impact and urgency.
4.4.2 **Problem Management:** The IT function must perform Root Cause Analysis (RCA) for all "Major Incidents" (as defined in the **Incident Response Plan**) to prevent recurrence.
4.4.3 **Access Management:** Access to IT services is granted strictly on a Principle of Least Privilege basis, in accordance with **Bylaws Article IX (Data Protection)** and the **Access Control Policy**.
4.4.4 **Service Desk:** The Organization shall maintain a centralized point of contact (Help Desk) for users to report issues and request services.

#### 4.5 Continual Service Improvement (CSI)
4.5.1 **Performance Metrics:** The CISO shall report key performance indicators (KPIs) to the Executive Director quarterly. Metrics may include System Uptime, Ticket Resolution Time, and User Satisfaction.
4.5.2 **Annual Review:** This policy and the Service Catalog must be reviewed annually to ensure they remain relevant to the Organization's evolving needs and technological landscape.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Executive Director (CEO)** | Provides strategic direction and budgetary approval for IT services; acts as the final escalation point for critical IT disputes. |
| **Chief Information Security Officer (CISO)** | Owns the ITSM process; acts as the Change Manager; ensures security integration into all service lifecycles; reports on IT performance to the Board. |
| **IT Staff / Volunteers** | Execute service operations (ticket resolution, maintenance); adhere to Change Management protocols; identify potential improvements. |
| **Employees / Members** | Report incidents via official channels; adhere to the **Acceptable Use Policy**; participate in User Acceptance Testing (UAT) when requested. |

### 6. Compliance and Enforcement
Failure to comply with this policy—specifically the bypassing of Change Management controls or the deployment of unauthorized Shadow IT—may result in disciplinary action, up to and including termination of employment or volunteer assignment.

Significant disruptions caused by negligence or willful misconduct may also result in legal action to recover damages, in accordance with **Bylaws Article VII (Indemnification)** limitations.

### 7. References
*   **Bylaws of Study GRC Inc.** (specifically Articles V and IX)
*   **IS-POL-001:** Master Information Security Policy
*   **IS-PRC-010:** Change Control and Management Procedure
*   **IS-POL-005:** Access Control Policy
*   **ITIL Foundation Framework v4**
*   **2 CFR 200.318:** General Procurement Standards (Technology acquisition)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | CISO | Initial Policy Draft based on ITIL v4 standards. |