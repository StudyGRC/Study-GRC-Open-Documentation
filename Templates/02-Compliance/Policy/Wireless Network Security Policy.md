### Wireless Network Security Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-012 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this policy is to establish the technical standards and behavioral requirements necessary to secure Study GRC Inc.’s wireless networking infrastructure and to protect Organization data when transmitted over wireless networks.

As a remote-first organization that frequently hosts educational events and manages sensitive community data, Study GRC Inc. faces significant risks from wireless interception, rogue access points, and "Evil Twin" attacks. This policy mandates the use of the WPA3 security standard to mitigate these risks and ensure compliance with Bylaws Article IX (Policies & Data Protection).

### 2. Scope
This policy applies to:
1.  **Infrastructure:** All wireless access points (APs), routers, and networking equipment owned, leased, or managed by Study GRC Inc., including temporary infrastructure deployed for events (e.g., hackathons, training sessions).
2.  **Devices:** All Organization-owned laptops, mobile devices, and tablets.
3.  **Personnel:** All Directors, Officers, employees, contractors, and volunteers accessing Organization resources via wireless networks.

**Exclusions:**
*   Personal home networks of remote staff are excluded from direct management but must adhere to the minimum connectivity standards defined in Section 4.2.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **WPA3 (Wi-Fi Protected Access 3)** | The latest security certification for Wi-Fi networks, providing stronger encryption (192-bit) and protection against brute-force attacks via Simultaneous Authentication of Equals (SAE). |
| **SAE (Simultaneous Authentication of Equals)** | A secure key exchange protocol used in WPA3 that replaces the Pre-Shared Key (PSK) method, preventing offline dictionary attacks. |
| **Rogue Access Point** | An unauthorized wireless access point installed on the Organization’s network, creating a security backdoor. |
| **Evil Twin** | A fraudulent Wi-Fi access point that appears to be legitimate but is set up to eavesdrop on wireless communications. |
| **SSID (Service Set Identifier)** | The primary name associated with an 802.11 wireless local area network (WLAN). |
| **VPN (Virtual Private Network)** | An encrypted tunnel between a device and a server, protecting data privacy over unsecured networks. |

### 4. Policy Statements

#### 4.1 Organization-Controlled Infrastructure Standards
All wireless infrastructure deployed by Study GRC Inc. (e.g., at the registered office, co-working spaces, or temporary event venues) must adhere to the following configuration standards:

*   **4.1.1 Mandatory WPA3 Encryption:** All wireless networks must utilize **WPA3-Enterprise** (192-bit security) for internal staff operations. Where Enterprise authentication is not feasible (e.g., small temporary setups), **WPA3-Personal (SAE)** is the absolute minimum standard.
    *   **Legacy Protocol Prohibition:** The use of WEP, WPA, and WPA2 (TKIP/AES) is strictly prohibited on Organization-controlled infrastructure unless a formal risk exception is signed by the CISO.
*   **4.1.2 SSID Configuration:**
    *   Default SSIDs and default manufacturer passwords must be changed immediately upon device provisioning.
    *   SSIDs must not identify the manufacturer, model, or specific location of the equipment (e.g., do not use "StudyGRC_Finance_Room202").
*   **4.1.3 Network Segmentation:**
    *   **Guest Networks:** A separate "Guest" network utilizing Client Isolation must be configured for non-organizational devices. Guest networks must be logically separated (VLAN) from the internal network containing sensitive Organization data.
    *   **Management Interfaces:** Wireless management interfaces (admin consoles) must not be accessible via the wireless network itself; they must be restricted to wired connections or secure VPN access only.

#### 4.2 Remote and Field Connectivity
Given the Organization's remote-first nature, personnel frequently connect from uncontrolled environments.

*   **4.2.1 Public Wi-Fi Usage:** Personnel are prohibited from accessing sensitive Organization data (including member databases, financial systems, or donor records) over public, open, or unsecured Wi-Fi networks (e.g., cafes, airports, hotels) unless a **Virtual Private Network (VPN)** approved by the CISO is active and encrypted.
*   **4.2.2 Home Office Standards:** Remote staff and volunteers handling sensitive data must ensure their home wireless networks use, at a minimum, WPA2-AES encryption, though WPA3 is strongly recommended. Default router passwords must be changed.

#### 4.3 Event and Training Environment Security
During Study GRC Inc. events (e.g., training workshops, conferences):

*   **4.3.1 Temporary Infrastructure:** Any temporary Wi-Fi deployed for educational purposes must be isolated from the administrative network used for processing registrations or payments.
*   **4.3.2 Youth Protection:** In accordance with the *Child and Youth Safeguarding Policy*, wireless networks provided for youth programs must employ content filtering (DNS-based or firewall-level) to block inappropriate content.

#### 4.4 Prohibited Activities
The following activities are strictly prohibited:

*   **4.4.1 Rogue APs:** Connecting unauthorized wireless access points (e.g., bringing a personal router to an event) to the Organization’s wired network.
*   **4.4.2 Ad-Hoc Networks:** Creating peer-to-peer (ad-hoc) wireless networks between Organization assets without CISO approval.
*   **4.4.3 Credential Sharing:** Sharing Wi-Fi Pre-Shared Keys (PSKs) or Enterprise credentials with unauthorized individuals.
*   **4.4.4 Attacking Networks:** Using Organization resources to crack, sniff, or attack external wireless networks, except during authorized penetration testing exercises sanctioned by the Board.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Defined in Bylaws Art. V §5.2. Responsible for the strategic oversight of this policy, approving WPA3 exceptions, and managing wireless security architecture. |
| **IT / Event Operations Staff** | Responsible for the physical configuration, deployment, and decommissioning of wireless hardware according to WPA3 standards. |
| **Employees & Volunteers** | Responsible for securing their remote connections via VPN when using public Wi-Fi and refraining from setting up unauthorized APs. |
| **Internal Audit Committee** | Responsible for periodically reviewing wireless configurations and exception logs for compliance. |

### 6. Compliance and Enforcement
Failure to comply with this policy may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action depending on the severity of the violation.

Any device found to be non-compliant or interfering with the security of the wireless network may be disconnected or quarantined by the CISO without prior notice.

### 7. References
*   **Bylaws of Study GRC Inc.** (Article V: Operational Leadership; Article IX: Policies & Data Protection)
*   **NIST SP 800-153:** Guidelines for Securing Wireless Local Area Networks (WLANs)
*   **NIST SP 800-97:** Establishing Wireless Robust Security Networks
*   **IS-POL-001:** Master Information Security Policy
*   **IS-STD-005:** Remote Work Technology Requirements

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | CISO | Initial Policy Release; WPA3 Mandate Established. |