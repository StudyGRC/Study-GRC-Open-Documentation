### VPN Configuration and Usage Standard

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-026 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this standard is to define the mandatory technical requirements and usage protocols for Virtual Private Network (VPN) connections within Study GRC Inc. As a remote-first organization, Study GRC relies on VPN technology to establish a secure, encrypted perimeter around our data and administrative interfaces, mitigating risks associated with unsecured networks (e.g., public Wi-Fi) and Man-in-the-Middle (MitM) attacks. This standard aligns with the data protection mandates outlined in **Article IX** of the Bylaws.

### 2. Scope
This standard applies to:
*   **Users:** All employees, contractors, Board Directors, and volunteers with access to Restricted or Confidential data.
*   **Devices:** All Organization-owned devices and any personal devices (BYOD) used to access internal administrative systems, financial records, or member databases.
*   **Systems:** All VPN gateways, concentrators, and client software managed or authorized by Study GRC Inc.

**Exclusions:**
*   General public access to the Study GRC public-facing website.
*   Volunteers whose access is limited strictly to public-facing collaboration platforms (e.g., Discord public channels) where no sensitive data is processed.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **VPN (Virtual Private Network)** | A technology that creates a safe, encrypted connection over a less secure network, such as the public internet. |
| **Split Tunneling** | A network configuration that allows a user to access dissimilar security domains like a public network (e.g., the Internet) and a local LAN or WAN at the same time, using the same or different network connections. |
| **Kill Switch** | A security feature that automatically disconnects the device from the internet if the VPN connection drops, preventing data leaks. |
| **AES-256** | Advanced Encryption Standard with a 256-bit key length; the industry standard for securing data. |
| **Handshake** | The process by which the VPN client and server establish a connection and agree on encryption keys. |

### 4. Standards

#### 4.1 Approved Protocols and Technology
To ensure the integrity and confidentiality of data in transit, only modern, secure protocols are permitted.
*   **4.1.1 Permitted Protocols:** The VPN solution must utilize WireGuard, OpenVPN, or IKEv2/IPsec.
*   **4.1.2 Prohibited Protocols:** The use of PPTP (Point-to-Point Tunneling Protocol) and L2TP/IPsec (without IKEv2) is strictly prohibited due to known security vulnerabilities.
*   **4.1.3 Vendor Selection:** All VPN client software must be approved by the CISO. Free, ad-supported, or "consumer-grade" VPNs that monetize user data are strictly prohibited.

#### 4.2 Cryptographic Standards (Encryption)
In accordance with NIST SP 800-53 (SC-13) and Bylaws Article IX, all VPN connections must meet the following cryptographic requirements:
*   **4.2.1 Data Channel Encryption:** Traffic must be encrypted using **AES-256-GCM** or **ChaCha20-Poly1305**.
*   **4.2.2 Control Channel Encryption:** The control channel must use TLS 1.2 or higher, or an equivalent secure handshake mechanism (e.g., Noise protocol framework for WireGuard).
*   **4.2.3 Perfect Forward Secrecy (PFS):** The VPN configuration must support PFS to ensure that compromise of a long-term key does not compromise past session keys.

#### 4.3 Authentication and Access Control
*   **4.3.1 Multi-Factor Authentication (MFA):** All VPN access must require MFA. Single-factor authentication for VPN entry is prohibited.
*   **4.3.2 Identity Integration:** Where feasible, VPN authentication must integrate with the Organization’s primary Identity Provider (IdP) via SAML or OIDC to ensure centralized account management.
*   **4.3.3 Least Privilege:** VPN access permissions must be segmented. Users must only be granted network routes to the specific resources required for their role (e.g., a volunteer should not have network routes to the Finance server).

#### 4.4 Client Configuration Requirements
*   **4.4.1 Kill Switch:** All VPN clients must have a "Kill Switch" feature enabled. If the VPN tunnel collapses, all network traffic must be blocked immediately to prevent data leakage over the unencrypted interface.
*   **4.4.2 DNS Leak Protection:** Clients must be configured to force DNS queries through the encrypted VPN tunnel to prevent ISP snooping or DNS hijacking.
*   **4.4.3 Auto-Connect:** For Organization-managed devices, the VPN client must be configured to auto-connect upon detection of an untrusted network (e.g., public coffee shop Wi-Fi).

#### 4.5 Split Tunneling Configuration
To balance security with network performance (specifically for video conferencing), Study GRC employs a defined Split Tunneling strategy:
*   **4.5.1 Restricted Traffic (Must Tunnel):** All traffic destined for internal administrative panels, cloud infrastructure management consoles (e.g., AWS/Azure), and financial banking portals must be routed through the VPN.
*   **4.5.2 Direct Access (May Bypass):** High-bandwidth, latency-sensitive, and already-encrypted public SaaS traffic (specifically Zoom, Slack, and Microsoft Teams video) may be routed directly to the internet, bypassing the VPN tunnel, provided the endpoint device has an active firewall and EDR agent.

#### 4.6 Logging and Monitoring
*   **4.6.1 Session Logging:** The VPN gateway/server must log the following for a minimum of 90 days:
    *   User ID.
    *   Source IP Address.
    *   Timestamp of connection start and end.
    *   Bytes transferred.
*   **4.6.2 Anonymization:** While metadata is logged for security, the VPN solution must not inspect or log the *content* of user traffic (packet payloads) unless required by a specific legal investigation authorized by the Board.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Defines the VPN standard; selects approved vendors; reviews VPN logs for anomalies. |
| **IT Administrator** | Configures VPN gateways/servers; manages user groups and routing rules; ensures client software is patched. |
| **Employees & Volunteers** | Ensure VPN is active when accessing restricted resources; report any connection failures or suspected compromises immediately. |
| **Executive Director** | Approves the budget for enterprise VPN licensing. |

### 6. Compliance and Enforcement
Failure to comply with this standard may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action depending on the severity of the violation.

**Bylaws Reference:** Violation of this standard by a Director constitutes "cause" for removal under **Bylaws Section 3.6**.

### 7. References
*   **NIST SP 800-53 Rev. 5:** AC-17 (Remote Access), SC-13 (Cryptographic Protection).
*   **NIST SP 800-113:** Guide to SSL VPNs.
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-POL-008:** Remote Access Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | CISO | Initial Standard creation and approval. |