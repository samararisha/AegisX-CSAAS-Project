<table width="100%">
  <tr>
    <td align="left" style="border: none;">
      <img src="https://github.com/AbdallahKhaledAmmar/AegisX-CSAAS-Project/raw/9d83c27c2ad3ac3043ec7ad421efadad589faeaf/WhatsApp%20Image%202026-02-23%20at%209.36.22%20PM.jpeg" width="220" alt="AegisX Logo" />
    </td>
    <td align="center" style="border: none;">
      <img src="https://img.shields.io/badge/ASA%20BANK-SECURITY%20ARCHITECTURE-blue?style=for-the-badge&logo=target" /><br />
      <img src="https://img.shields.io/badge/DESIGN-14%20SECURITY%20ZONES-orange?style=flat-square" />
      <img src="https://img.shields.io/badge/STATUS-v2.0%20APPROVED-blue?style=flat-square" />
    </td>
    <td align="right" style="border: none;">
      <img src="https://github.com/AbdallahKhaledAmmar/AegisX-CSAAS-Project/raw/9c135b0528a78bc7a35a836e2a464274597c2ff0/Green%20and%20Dark%20Blue%20Modern%20Gradient%20Banking%20Finance%20Logo.png" width="280" alt="ASA Bank Logo" />
    </td>
  </tr>
</table>

<div align="center">
  <h1>🛡️ ASA Bank: Security Architecture Suite</h1>
  <p><b>Lead Architect: Samara Risha</b></p>
  <i>A comprehensive defense-in-depth framework for mission-critical banking systems.</i>
</div>

---

## 📖 Project Overview
This repository contains the full security architecture and GRC (Governance, Risk, and Compliance) suite for **ASA Bank**[cite: 436, 533]. The architecture implements a rigid defence-in-depth strategy across **14 distinct security zones**, protecting assets from the internet perimeter to the air-gapped Disaster Recovery site[cite: 371, 447, 544].

---

## 🗺️ Security Zone Architecture
The network is segmented into 14 functional zones to ensure minimal blast radius and strict access control[cite: 371, 422].

### 🌐 Perimeter & Public Facing
* **Internet Zone**: Untrusted external space for clients and API consumers[cite: 374, 471].
* **Perimeter Security**: High-risk entry point featuring ISP/Border routers and DDoS protection[cite: 378, 514].
* **DMZ Network**: Secure segment for WAF, Reverse Proxy, Load Balancer, and Email Gateway[cite: 380, 471].
* **DMZ Web Servers**: Dedicated sub-zone for internet-facing Web and API servers[cite: 374, 471].

### 🏗️ Internal & Management
* **Internal Firewall Zone**: Second-tier security boundary enforcing HTTPS/API-only traffic[cite: 382, 492].
* **Application Services**: Hosting the core Banking App, Mobile Backend, IAM, and MFA servers[cite: 384, 477].
* **Identity Services**: High-trust zone for Active Directory (LDAPS), RADIUS, and DHCP[cite: 386, 573].
* **Core Network**: Redundant backbone with dual routers and switches[cite: 388, 514].
* **VLAN Segments**: Isolated user/system VLANs (HR, Finance, IT, SOC, and OOB Management)[cite: 393, 468, 480].

### 💰 Specialized Banking & SOC
* **ATM Network**: Hard-isolated infrastructure with a dedicated ATM Gateway[cite: 408, 471].
* **Payment Processing**: PCI-DSS scoped zone for card processing and transaction servers[cite: 410, 477].
* **Data Centre**: Dual-firewall protected zone for core banking databases and storage[cite: 413, 586].
* **SOC**: Centralized monitoring zone for Wazuh SIEM and Log Collection[cite: 256, 417].
* **Disaster Recovery**: Warm standby site with RTO 4h / RPO 1h[cite: 25, 415, 591].

---

## 📄 Documentation Index
| Ref | Document Title | Version | Status |
| :--- | :--- | :--- | :--- |
| **SEC-DOC-001** | Security Architecture Overview | v2.0 | ✅ Published [cite: 435] |
| **SEC-DOC-002** | Network Segmentation & VLAN Design | v1.0 | ✅ Published [cite: 354] |
| **SEC-DOC-003** | Firewall Policy & Rules | v1.0 | ✅ Published [cite: 128] |
| **SEC-DOC-004** | Log Collection & SIEM Architecture | v1.0 | ✅ Published [cite: 245] |
| **SEC-DOC-007** | Disaster Recovery & Backup Plan | v1.0 | ✅ Published [cite: 4] |
| **SEC-DOC-008** | Security Hardening Checklist | v2.0 | ✅ Published [cite: 533] |

---

## ⚙️ Key Technical Parameters
* **RTO / RPO**: 4 Hours / 1 Hour overall; 15-minute RPO for Tier 1 Databases[cite: 25, 26, 27].
* **Encryption**: AES-256 at rest and TLS 1.3 in transit enforced[cite: 378, 514, 583].
* **Monitoring**: Wazuh SIEM mapping alerts to **MITRE ATT&CK** (60% current coverage)[cite: 265, 297].
* **Log Retention**: 6 months online (Targeting 12 months for PCI compliance in Q2 2026)[cite: 304, 307, 343].


## 📜 Compliance Frameworks
This architecture is mapped against and complies with[cite: 536, 560]:
* **ISO/IEC 27001:2022** (A.12.4, A.13, A.17) [cite: 341, 560]
* **PCI-DSS v4.0** (Req 1, 4, 7, 8, 10, 11) [cite: 341, 560]
* **CIS Controls v8** (Controls 4, 5, 6, 8, 12, 13) [cite: 558, 560]
* **NIST SP 800-53 Rev 5** (AC, AU, CP, SC families) [cite: 341, 560]

---

<div align="center">
  <p><b>Samara Risha - Abdallah Khaled - Aya reda </b><br />Computer Science | Cybersecurity Specialization</p>
</div>


