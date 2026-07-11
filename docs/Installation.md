# 🚀 Installation Guide

## Requirements

Before deployment, make sure you have:

- Linux environment
- Docker
- VMware or VirtualBox
- Python environment
- Minimum 8GB RAM recommended

---

# Clone Repository

```bash
git clone https://github.com/boullahmgy/devsecops-app.git
```

Move into the project:

```bash
cd devsecops-app
```

---

# Environment Setup

Configure the virtual machines:

- Kali Linux (Attack Simulation)
- Linux Server (Security Services)
- Wazuh Server
- Suricata IDS

---

# Verify Installation

Check running services:

```bash
systemctl status wazuh-manager
```

```bash
systemctl status suricata
```

---

# Deployment

Follow configuration instructions according to your environment.
