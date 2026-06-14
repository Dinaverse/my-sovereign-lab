# 🛠️ Laboratory Operations & Security Reference

This document serves as the technical reference for the operations, maintenance, and security protocols of the laboratory infrastructure.

## 1. Introduction
This document defines the methodology for managing the laboratory infrastructure, ensuring it remains sovereign, automated, and secure. All modifications must adhere to these established principles.

## 2. Logical Topology (Nodes & Roles)
Communication across the lab relies exclusively on the encrypted Tailscale tunnel.

| Host Name | Role | Tailscale IP | SSH Method |
| :--- | :--- | :--- | :--- |
| Kali Station | Orchestrator/Controller | 100.72.84.77 | SSH CA/Key |
| Arch Cluster | Compute IA (4x P106-100) | 100.69.65.101 | SSH CA/Key |
| Raspberry Pi | Pi-hole/Services | 100.80.155.45 | SSH CA/Key |
| Dell Precision | Monitoring/Orchestrator | N/A | SSH CA/Key |
| Canwork189 | Storage/General | 100.118.171.116 | SSH CA/Key |
| Canwork164 | Storage/General | 100.65.232.81 | SSH CA/Key |

## 3. Security Posture (Hardening)
- **Transport:** Encrypted tunnel (Tailscale) is mandatory for all remote access.
- **Firewall:** SSH access restricted to Tailscale interfaces via `nftables`/`iptables`.
- **Authentication:**
    - Routine password authentication is disabled.
    - SSH CA is enabled; connections rely on certificates signed by the lab's master Certificate Authority.
- **Intrusion Protection:** Fail2Ban configured on control stations.

## 4. Orchestration & Automation
Laboratory management is powered by custom skills integrated with Gemini CLI:
- **Auditing:** `lab-auditor` (Material/Software state).
- **Control:** `agent-controller` (Systemd service management).
- **Deployment:** `deploy-docker-stack` (Docker/Compose orchestration).
- **Archiving:** `log-archiver` (Automated log backup).

## 5. Maintenance Procedures
- **Adding a Node:**
    1. Install Tailscale.
    2. Configure SSH CA trust (`TrustedUserCAKeys`).
    3. Harden firewall rules.
- **Certificate Renewal:** Periodically sign keys using the master CA.
- **Agent Persistence:** Utilize `systemd` user-level services with `linger` enabled for resilience.

---
*Technical Reference Version 1.0 (2026-06-14)*
