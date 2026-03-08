# 🚀 Shelby Testnet RPC Node Guide

<p align="center">

![GitHub stars](https://img.shields.io/github/stars/manhdz9990/shelby-testnet-node-guide?style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/manhdz9990/shelby-testnet-node-guide?style=for-the-badge)
![GitHub license](https://img.shields.io/github/license/manhdz9990/shelby-testnet-node-guide?style=for-the-badge)

</p>

A **complete step-by-step guide** to install and run a **Shelby Testnet RPC Node**.

Shelby provides **verifiable global object storage for AI workloads**, powering the next generation of **AI and decentralized infrastructure**.

This guide explains how to deploy a **Shelby RPC node using Docker**.

---

# 📑 Table of Contents

* Official Links
* System Requirements
* Step 1 — Update Server
* Step 2 — Install Dependencies
* Step 3 — Clone Shelby Node
* Step 4 — Configure Node
* Step 5 — Start RPC Node
* Step 6 — Check Logs
* Step 7 — Verify RPC
* Useful Commands
* About Shelby
* Contributing
* Support
* Author

---

# 🌐 Official Links

Documentation
https://docs.shelby.xyz/protocol/node-setup/testnet_rpc

Website
https://shelby.xyz

Twitter
https://twitter.com/shelbyserves

Discord
https://discord.gg/shelbyserves

---

# 💻 System Requirements

## Minimum

| Resource | Requirement  |
| -------- | ------------ |
| CPU      | 4 Cores      |
| RAM      | 8 GB         |
| Storage  | 100 GB SSD   |
| OS       | Ubuntu 22.04 |

## Recommended

| Resource | Requirement |
| -------- | ----------- |
| CPU      | 8 Cores     |
| RAM      | 16 GB       |
| Storage  | 500 GB SSD  |

---

# ⚙️ Step 1 — Update Server

Update system packages.

```bash
sudo apt update && sudo apt upgrade -y
```

---

# ⚙️ Step 2 — Install Dependencies

Install required packages.

```bash
sudo apt install curl git docker.io docker-compose -y
```

Enable Docker.

```bash
sudo systemctl enable docker
sudo systemctl start docker
```

Verify Docker installation.

```bash
docker version
```

---

# 📥 Step 3 — Clone Shelby Node Repository

Clone the official Shelby repository.

```bash
git clone https://github.com/shelbyxyz/shelby-node.git
```

Enter the directory.

```bash
cd shelby-node
```

---

# ⚙️ Step 4 — Configure Node

Copy the environment file.

```bash
cp .env.example .env
```

Edit configuration.

```bash
nano .env
```

Save and exit.

---

# 🚀 Step 5 — Start Shelby RPC Node

Run the node using Docker.

```bash
docker compose up -d
```

Check running containers.

```bash
docker ps
```

If the container appears in the list, your node is running successfully.

---

# 📜 Step 6 — Check Logs

Monitor node logs.

```bash
docker logs -f shelby-node
```

Press **CTRL + C** to exit logs.

---

# 🔎 Step 7 — Verify RPC Endpoint

Open the RPC endpoint in your browser.

```
http://YOUR_SERVER_IP:8545
```

If the endpoint responds, the **RPC node is operational**.

---

# 🛠 Useful Commands

## Stop Node

```bash
docker compose down
```

## Restart Node

```bash
docker compose restart
```

## Update Node

```bash
git pull
docker compose down
docker compose up -d
```

---

# 📊 Check Node Status

List running containers.

```bash
docker ps
```

View logs.

```bash
docker logs shelby-node
```

---

# 🧠 About Shelby

Shelby builds **verifiable infrastructure for AI data storage**.

The protocol enables:

• Global data availability
• Verifiable storage proofs
• Infrastructure for AI workloads
• Scalable decentralized storage

Shelby aims to become a **data layer for AI applications**.

---

# 🤝 Contributing

Contributions are welcome.

You can help by:

• Improving documentation
• Submitting pull requests
• Reporting issues

---

# ⭐ Support the Project

If this guide helped you:

⭐ Star this repository
🍴 Fork the repository
📢 Share it with the community

---

# 👤 Author

**Manh100k Web3**

Web3 Contributor
Testnet Hunter
Community Builder

---

# ⚠️ Disclaimer

This guide is provided for **educational purposes only**.

Always verify commands and refer to official documentation before running nodes.
