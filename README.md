<div align="center">
  <img src="https://img.shields.io/badge/ASA%20BANK-SECURITY%20ARCHITECTURE-blue?style=for-the-badge&logo=appveyor" />
  <img src="https://img.shields.io/badge/STATUS-V2.0%20APPROVED-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/COMPLIANCE-PCI--DSS%20%7C%20ISO%2027001-green?style=for-the-badge" />
</div>

<br />

<div align="center">
  <h1>🛡️ ASA Bank: Enterprise Security Infrastructure</h1>
  <p><b>Lead Architect: Abdallah Khaled - Samara Risha - Aya Reda</b></p>
  <i>Comprehensive Defence-in-Depth Architecture for Critical Banking Systems</i>
</div>

---

### 📖 Overview
This repository contains the authoritative security architecture documentation for **ASA Bank**[cite: 436]. The design implements a multi-layered defense strategy across **14 distinct security zones**, protecting assets from the internet perimeter to the air-gapped Disaster Recovery (DR) site[cite: 371, 514].

---

### 🗺️ Network Segmentation & Zones
The architecture utilizes strict VLAN and firewall-based isolation to minimize blast radius[cite: 366, 369]:

* **Perimeter & DMZ**: Three-legged firewall design (`FW-01`) separating public traffic from internal services[cite: 147, 459].
* **Application Services**: Banking App, Mobile Backend, and IAM/MFA servers[cite: 471].
* **Identity Services**: Centralized AD, RADIUS, and DNS with LDAPS enforced[cite: 386].
* **PCI Zone**: Hard-isolated ATM and Payment processing infrastructure with a dedicated `FW-05`[cite: 406, 583].
* **Data Centre**: Dual-firewall design protecting the Core Banking and Transaction databases[cite: 413, 587].

---

### 📄 Documentation Suite
| Ref | Document Title | Version | Status |
| :--- | :--- | :--- | :--- |
| **SEC-DOC-001** | Security Architecture Overview | v2.0 | ✅ Published [cite: 435] |
| **SEC-DOC-003** | Firewall Policy & Rules | v1.0 | ✅ Published [cite: 128] |
| **SEC-DOC-004** | Log Collection & SIEM Architecture | v1.0 | ✅ Published [cite: 245] |
| **SEC-DOC-007** | Disaster Recovery & Backup Plan | v1.0 | ✅ Published [cite: 4] |
| **SEC-DOC-008** | Security Hardening Checklist | v2.0 | ✅ Published [cite: 533] |

---

### ⚙️ Technical Specifications
* **Recovery Objectives**: Overall RTO of **4 hours** and RPO of **1 hour**[cite: 6, 25, 26].
* **Database RPO**: 15 minutes via continuous async log shipping[cite: 24, 27, 48].
* **SIEM Pipeline**: **Wazuh XDR** (`172.16.66.10`) receiving logs from 16 network devices and 23 agents[cite: 247, 274, 277].
* **MITRE ATT&CK**: Currently covering 60% of relevant techniques, targeting 80% by Q3 2026[cite: 297, 298].

---

### 🚩 Flag Resolution Register (v2.0 Update)
Initial architecture vulnerabilities identified in v1.0 have been fully remediated[cite: 516]:
* **F-01**: DMZ segment fully implemented between perimeter and core[cite: 517].
* **F-04**: Dedicated PCI Firewall added for ATM/Payment isolation[cite: 517].
* **F-05**: Out-of-Band (OOB) Management network established (VLAN 50)[cite: 517] (Partially Implmented).
* **F-07**: Verified log collection paths for all zones to the SOC[cite: 517].

---

### 📂 Repository Structure
```text
banking-security-architecture/
├── docs/           # Technical Specification Documents (SEC-DOC series)
├── diagrams/       # Verified Architecture Screenshots & Native Files
└── README.md       # Project Executive Summary
