### Endpoint Detection and Response (EDR) Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-073 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-26 |
| **Next Review Date** | 2024-10-26 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Director of Security Operations |
| **Classification** | Internal |

### 1. Purpose
The purpose of this policy is to mandate the deployment, management, and utilization of Endpoint Detection and Response (EDR) technologies within Study GRC Inc. As a remote-first organization, traditional perimeter defenses (firewalls) are insufficient. This policy ensures that the Organization maintains visibility into endpoint activities to detect, investigate, and respond to advanced cyber threats, malware, and unauthorized access attempts in real-time, thereby protecting member data and intellectual property.

### 2. Scope
This policy applies to:
*   **Organization-Owned Assets:** All laptops, desktops, servers, and virtual machines owned or leased by Study GRC Inc.
*   **Privileged BYOD Assets:** Personal devices used by staff or volunteers that have been granted privileged access (e.g., Administrator, Root, or access to sensitive PII/Financial data) and are enrolled in the Organization’s Mobile Device Management (MDM) or security program.
*   **Users:** All employees, contractors, Board members, and volunteers who utilize the devices described above.

**Exclusions:**
*   Personal devices of Community Participants or General Members who access public-facing resources only.
*   Personal devices of volunteers used strictly for web-based access (e.g., email, Slack) without local data synchronization, provided they meet the *Minimum Security Standards*.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **EDR (Endpoint Detection and Response)** | An integrated security solution that combines real-time continuous monitoring and collection of endpoint data with rules-based automated response and analysis capabilities. |
| **Endpoint** | Any device that connects to the Organization's network or accesses Organization data, including laptops, desktops, servers, and mobile devices. |
| **Telemetry** | Data collected by the EDR agent regarding system activity, including process execution, network connections, file modifications, and user behavior. |
| **Isolation** | The automated or manual process of severing an endpoint's network access (except to the EDR management console) to prevent the spread of a threat. |
| **Tamper Protection** | Security controls that prevent unauthorized users (including local administrators) from disabling, uninstalling, or modifying the EDR agent. |

### 4. Policy Statements

#### 4.1 Mandatory Deployment
An approved EDR agent must be installed, active, and reporting telemetry on all in-scope endpoints prior to the device being permitted to access Study GRC Inc. production networks or sensitive data repositories.
*   **4.1.1** Devices found without a functioning EDR agent will be automatically blocked from accessing organizational resources via Conditional Access policies.
*   **4.1.2** The EDR solution must be configured to start automatically upon system boot and run continuously in the background.

#### 4.2 Configuration and Tamper Protection
To ensure the integrity of the Organization's security posture:
*   **4.2.1** **Tamper Protection:** Tamper protection features must be enabled on all agents. Users, including those with local administrative privileges, are strictly prohibited from disabling, modifying, or uninstalling the EDR agent.
*   **4.2.2** **Exclusions:** Any exclusions to EDR scanning (e.g., for specific developer tools or performance-sensitive applications) must be formally requested, risk-assessed, and approved by the Security Operations team.
*   **4.2.3** **Updates:** EDR agents must be configured to automatically update signatures and software versions. Devices that fall behind the minimum supported version by more than 30 days will be quarantined.

#### 4.3 Automated Response and Isolation
To mitigate threats at machine speed:
*   **4.3.1** The EDR system is authorized to take automated actions based on pre-defined logic approved by the CISO. This includes killing malicious processes, quarantining files, and isolating the host from the network.
*   **4.3.2** The Security Operations team reserves the right to remotely isolate any endpoint displaying indicators of compromise (IOCs) without prior user notification to prevent lateral movement of threats.

#### 4.4 Data Privacy and Collection
Study GRC Inc. respects the privacy of its workforce while maintaining security.
*   **4.4.1** **Security Focus:** EDR telemetry is collected solely for the purpose of information security, incident response, and system health monitoring. It must not be used for employee productivity monitoring or surveillance unrelated to security investigations.
*   **4.4.2** **Data Types:** Collected data typically includes process names, file hashes, network destination IPs, and command-line arguments. The Organization minimizes the collection of content (e.g., the text inside a Word document) unless specifically triggered by a malicious event.

#### 4.5 Incident Response Integration
The EDR solution serves as the primary source of truth for forensic investigations.
*   **4.5.1** In the event of a confirmed security incident, the Incident Response Team is authorized to utilize the EDR "Live Response" capabilities to remotely access the endpoint for forensic data gathering, regardless of the user's physical location.
*   **4.5.2** Users must cooperate fully with Security Operations during an EDR-flagged investigation.

#### 4.6 Interference Prohibited
Any attempt to block EDR communications (e.g., via host file modification or firewall rules) or to "spoof" EDR telemetry is considered a severe violation of the *Acceptable Use Policy* and will be treated as a potential insider threat activity.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Selects the EDR vendor; approves automated response policies; authorizes host isolation during major incidents. |
| **Security Operations (SecOps)** | Monitors EDR consoles; investigates alerts; tunes detection rules to minimize false positives; performs threat hunting. |
| **IT Systems Administration** | Deploys EDR agents to endpoints; ensures agents are healthy and updating; manages compatibility with OS updates. |
| **End Users** | Ensures the device connects to the internet regularly to send telemetry; reports any EDR error messages to the Help Desk; does not attempt to disable the agent. |

### 6. Compliance and Enforcement
**Monitoring:** The Security Operations team will continuously monitor EDR health dashboards to ensure 100% coverage of in-scope assets.

**Enforcement:** Failure to comply with this policy—specifically attempts to disable or tamper with EDR agents—may result in disciplinary action, up to and including termination of employment or volunteer assignment. Devices found non-compliant will be immediately disconnected from Organization resources.

### 7. References
*   **NIST CSF 2.0:** DE.CM (Continuous Monitoring), RS.AN (Analysis), RS.MI (Mitigation).
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-POL-044:** Incident Response Plan.
*   **IS-POL-022:** Bring Your Own Device (BYOD) Policy.
*   **HR-POL-001:** Employee Handbook (Acceptable Use).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-26 | Director of SecOps | Initial Policy Drafting and Approval. |