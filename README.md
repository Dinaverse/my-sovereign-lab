# 🧪 My Sovereign Lab

> *A self-hosted, bare-metal computing environment engineered for resilience, data sovereignty, and high-performance local AI inference with zero cloud dependencies.*

---

## 🎯 Vision

This laboratory is the physical and logical backbone of all my infrastructure projects. It converts repurposed enterprise-grade hardware into a distributed, multi-node computing cluster capable of running local LLMs, security tooling, network monitoring, and containerized services entirely on-premises.

---

## 🖥️ Node Inventory

| Node | Hostname | Role | Hardware |
|------|----------|------|----------|
| 🧠 | **Arch Linux** | GPU Compute / LLM Inference | 4x NVIDIA P106-100 (24 GB VRAM) |
| 🔴 | **Kali Linux** | Master Orchestrator / SecOps | x86 workstation |
| 🥧 | **Raspberry Pi** | IDS / DNS / Network Services | ARM SBC |
| 🖧 | **Dell Server** | Gateway / Monitoring | Enterprise rack unit |
| 💾 | **AMD Machine** | Storage Worker / CPU Compute | Canwork189 |

---

## 🔗 Ecosystem Repositories

| Repository | Description |
|------------|-------------|
| [`arch-linux-multi-gpu-llm`](https://github.com/Dinaverse/arch-linux-multi-gpu-llm) | 4x GPU cluster for local LLM inference |
| [`sovereign-ai-infrastructure`](https://github.com/Dinaverse/sovereign-ai-infrastructure) | Architecture & node documentation |
| [`local-ai-sovereign-stack`](https://github.com/Dinaverse/local-ai-sovereign-stack) | Docker-based AI stack (Ollama + Grafana) |
| [`sovereign-lab-orchestration`](https://github.com/Dinaverse/sovereign-lab-orchestration) | Orchestration principles & IaC methodology |
| [`cybersecurity-lab-automation`](https://github.com/Dinaverse/cybersecurity-lab-automation) | Security automation & monitoring scripts |
| [`sovereign-ai-security`](https://github.com/Dinaverse/sovereign-ai-security) | AI-driven security tooling |

---

## ⚙️ Core Infrastructure Stack

```text
🐧 OS Layer        ::  Arch Linux, Kali Linux, Debian, Raspbian
🐳 Containers      ::  Docker, Docker Compose
🤖 AI Runtime      ::  Ollama (local LLM), CUDA, Multi-GPU VRAM pooling
📊 Monitoring      ::  Prometheus, Grafana, custom Python agents
🛡️ Security        ::  Suricata IDS, custom log analytics, Morpheus (AI SecOps)
🌐 Networking      ::  VLAN segmentation, custom DNS, SSH hardening
```

---

## 🏗️ Lab Topology

```
[Internet]
     │
  [Dell Gateway / Monitoring]
     │
  [LAN Switch]
     ├── [Kali Master Orchestrator]
     ├── [Arch GPU Cluster (4x P106-100)]
     ├── [Raspberry Pi IDS / DNS]
     └── [AMD Canwork189 Storage / CPU]
```

---

## 📈 Status

| Service | Status |
|---------|--------|
| Multi-GPU LLM Inference (Qwen 3.5:27B) | ✅ Operational |
| Grafana / Prometheus Monitoring | ✅ Operational |
| Suricata IDS | ✅ Operational |
| Docker Containerized Services | ✅ Operational |
| n8n Workflow Automation | ✅ Operational |

---

*Built with a research-and-development mindset repurposing hardware, not renting cloud.*
