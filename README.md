# 🚀 Shelby Testnet RPC Node Guide

A complete step-by-step guide to **install and run a Shelby Testnet RPC Node**.

Shelby provides **verifiable global object storage for AI workloads**, designed to power the next generation of **AI and decentralized infrastructure**.

This guide helps you deploy and run a **Shelby RPC node** using Docker.

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

# 📦 System Requirements

## Minimum Requirements

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

Update your server packages.

```bash
sudo apt update && sudo apt upgrade -y
```

---

# ⚙️ Step 2 — Install Dependencies

Install required packages.

```bash
sudo apt install curl git docker.io docker-compose -y
```

Enable Docker service.

```bash
sudo systemctl enable docker
sudo systemctl start docker
```

Verify Docker installation.

```bash
docker --version
```

---

# 📥 Step 3 — Clone Shelby Node Repository

Clone the official Shelby node repository.

```bash
git clone https://github.com/shelbyxyz/shelby-node.git
```

Enter the project directory.

```bash
cd shelby-node
```

---

# ⚙️ Step 4 — Configure Node

Copy the environment configuration file.

```bash
cp .env.example .env
```

Edit the configuration file.

```bash
nano .env
```

Modify the parameters if needed.

Save and exit.

---

# 🚀 Step 5 — Start Shelby RPC Node

Run the Shelby node using Docker.

```bash
docker compose up -d
```

Check running containers.

```bash
docker ps
```

If the container appears in the list, the node is running successfully.

---

# 📜 Step 6 — Check Node Logs

Monitor node logs to ensure everything is working correctly.

```bash
docker logs -f shelby-node
```

Press **CTRL + C** to exit logs.

---

# 🔎 Step 7 — Verify RPC Endpoint

Test your RPC endpoint in the browser.

```
http://YOUR_SERVER_IP:8545
```

If the endpoint responds, your **RPC node is operational**.

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

Check container logs.

```bash
docker logs shelby-node
```

---

# 🧠 About Shelby

Shelby is building **verifiable infrastructure for AI data storage**.

The protocol enables:

* Global data availability
* Verifiable storage proofs
* Infrastructure for AI workloads
* Scalable decentralized data systems

Shelby aims to become a **data layer for AI and crypto applications**.

---

# 🤝 Contributing

Contributions are welcome.

You can help by:

* Improving documentation
* Submitting pull requests
* Reporting issues

---

# ⭐ Support the Project

If this guide helped you:

⭐ Star this repository
🍴 Fork the repository
📢 Share it with the community

---

# 👤 Author

Manh100k Web3

Web3 Contributor
Testnet Hunter
Community Builder

---

# ⚠️ Disclaimer

This guide is for educational purposes.
Always verify commands and official documentation before running nodes.
