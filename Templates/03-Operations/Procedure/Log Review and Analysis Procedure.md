### Log Review and Analysis Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-054 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-26 |
| **Next Review Date** | 2024-10-26 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Security Operations Lead |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a standardized methodology for the review, analysis, and escalation of system logs within Study GRC Inc. This procedure ensures the Organization proactively identifies security incidents, policy violations, and operational anomalies.

This document supports the Organization’s obligation to maintain **Threat Detection** capabilities as required by the **Master Information Security Policy** and federal grant compliance standards (2 CFR 200.303 Internal Controls). It specifically addresses the requirement to monitor for unauthorized access to sensitive data, including donor information and youth participant records.

### 2. Scope
This procedure applies to all Information Systems owned, operated, or leased by Study GRC Inc. that generate audit logs. This includes, but is not limited to:
*   **Cloud Infrastructure:** AWS, Azure, or GCP environments.
*   **SaaS Applications:** Google Workspace, Slack, GitHub, Donor Management Systems (CRM).
*   **Network Security Devices:** Firewalls, VPN concentrators, and Zero Trust Network Access (ZTNA) gateways.
*   **Endpoints:** Workstations and servers (via EDR/Antivirus logs).
*   **Identity Providers:** SSO and MFA logs (e.g., Okta, Google Identity).

**Exclusions:** Debug-level logs on non-production development environments that do not contain PII or sensitive intellectual property are excluded from mandatory daily review but must still be retained per the *Data Retention Policy*.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **SIEM** | Security Information and Event Management system; a tool that aggregates and analyzes log data. |
| **IOC** | Indicator of Compromise; a piece of forensic data (e.g., IP address, file hash) that identifies potentially malicious activity. |
| **False Positive** | An alert that incorrectly indicates a vulnerability or malicious activity exists. |
| **Privileged Account** | An account with elevated permissions (e.g., Administrator, Root, Super Admin). |
| **Triage** | The process of determining the priority and validity of a security alert. |

### 4. Procedures

#### 4.1 Log Ingestion and Configuration
To ensure effective analysis, logs must be centralized and formatted correctly.
1.  **Centralization:** All critical systems defined in the Scope must be configured to forward logs to the Organization’s designated central log repository or SIEM.
2.  **Time Synchronization:** All log sources must be synchronized via Network Time Protocol (NTP) to Coordinated Universal Time (UTC) to ensure accurate forensic timelines.
3.  **Log Integrity:** Access to modify or delete logs within the central repository must be restricted to the CISO and designated Security Operations personnel only.

#### 4.2 Automated Alerting Rules
Due to the volume of logs, automated analysis is the primary detection method. The Security Operations Team must configure the SIEM/Log Aggregator to trigger alerts on the following events:
1.  **Multiple Failed Login Attempts:** More than five (5) failures within 10 minutes for a single account.
2.  **Privileged Access Anomalies:** Login to a Super Admin account outside of standard business hours or from a geolocation not associated with the user.
3.  **Malware Detection:** Any "Not Cleaned" or "Quarantined" event from Endpoint Detection and Response (EDR) agents.
4.  **Data Exfiltration Indicators:** Large file transfers (>1GB) to unauthorized cloud storage or external IP addresses.
5.  **Policy Violations:** Installation of unauthorized software or disabling of security controls (e.g., turning off the firewall).

#### 4.3 Manual Review Cadence
While automation handles real-time threats, human review is required for trend analysis and complex threats.

**4.3.1 Daily Review (Business Days)**
*   **Responsibility:** Security Analyst
*   **Scope:**
    *   Review all alerts classified as "High" or "Critical" generated in the previous 24 hours.
    *   Review "Top Talkers" (highest bandwidth users) on the VPN/Network.
    *   Review any account lockouts.

**4.3.2 Weekly Review**
*   **Responsibility:** Security Operations Lead
*   **Scope:**
    *   Review a summary report of all "Medium" severity alerts.
    *   Analyze trends in failed login attempts (brute force campaigns).
    *   Review access logs for the **Donor CRM** and **Youth Data Repositories** to ensure access aligns with business needs.
    *   Review changes to Group Policy or Cloud IAM roles.

**4.3.3 Monthly Review**
*   **Responsibility:** CISO
*   **Scope:**
    *   Review the "Privileged User Activity Report" for all System Administrators.
    *   Validate that log ingestion rates are consistent (identifying broken log forwarders).
    *   Review the list of "suppressed" or "whitelisted" alerts to ensure they are still valid.

#### 4.4 Analysis and Triage Workflow
When an anomaly or alert is identified during automated or manual review:

1.  **Validation:** The Analyst must verify if the activity is a False Positive by cross-referencing with Change Management tickets or contacting the user via an out-of-band method (e.g., Slack/Phone).
2.  **Classification:** If the activity is valid and suspicious, classify the severity based on the *Incident Classification Matrix*.
3.  **Documentation:** Open a ticket in the IT Service Management (ITSM) system. Record the:
    *   Time of detection.
    *   Source IP/User.
    *   Nature of the anomaly.
    *   Evidence (screenshots or log snippets).
4.  **Escalation:**
    *   **Low/Medium:** Remediate per standard operating procedures (e.g., reset password, re-image machine).
    *   **High/Critical:** Immediately activate the **Incident Response Plan (IRP)** and notify the CISO.

#### 4.5 Youth Protection Monitoring
Pursuant to the *Child and Youth Safeguarding Policy*, logs related to systems storing minor's data must be reviewed for:
1.  **Bulk Exports:** Any export of youth participant lists.
2.  **Unauthorized Viewing:** Access to youth records by personnel without a valid background check or business justification.
3.  **After-Hours Access:** Access to youth data between 10:00 PM and 6:00 AM local time, unless part of a scheduled event.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Accountable for the overall log management strategy; approves alerting rules; conducts monthly executive reviews. |
| **Security Operations Lead** | Responsible for configuring the SIEM; conducting weekly reviews; tuning alert thresholds to reduce noise. |
| **Security Analyst** | Responsible for daily log monitoring; initial triage of alerts; documenting findings in the ticketing system. |
| **System Administrators** | Responsible for ensuring their respective systems (servers, apps) are correctly forwarding logs to the central repository. |

### 6. Compliance and Enforcement
Failure to adhere to this procedure can result in undetected breaches, loss of 501(c)(3) status due to data mismanagement, or loss of federal funding.

**Enforcement:**
*   **Tampering:** Any employee found intentionally disabling logging, modifying log files to conceal activity, or deleting audit trails will be subject to immediate disciplinary action, up to and including termination and legal prosecution.
*   **Negligence:** Failure by assigned IT staff to perform required daily/weekly reviews may result in performance improvement plans or disciplinary action.

### 7. References
*   **IS-POL-001:** Master Information Security Policy
*   **IS-PLN-001:** Incident Response Plan
*   **IS-POL-053:** Log Management and Retention Policy
*   **HR-POL-020:** Child and Youth Safeguarding Policy
*   **NIST SP 800-92:** Guide to Computer Security Log Management
*   **2 CFR 200.303:** Federal Uniform Guidance - Internal Controls

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-26 | Security Operations Lead | Initial release of procedure. |