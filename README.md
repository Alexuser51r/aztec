# ⚡ Aztec Node Setup — Quick Start

A clean and simplified guide for deploying the Aztec Sequencer node. All signal, no noise.

---

## 📌 System Requirements

**Recommended:**

- ✅ CPU: 8 cores
- ✅ RAM: 16 GB
- ✅ SSD: 100 GB+
- ✅ Internet Speed	25 Mbps Upload / Download
---

## 1️⃣ Prepare Your System

Update and install dependencies:

```bash
sudo apt update && sudo apt upgrade -y
```

```bash
sudo apt install -y curl git wget build-essential tmux htop nano \
  make gcc g++ unzip jq lz4 iptables \
  libssl-dev libleveldb-dev pkg-config \
  autoconf automake clang bsdmainutils
```

---

## 2️⃣ Install Docker

If Docker is not installed yet:

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh
```

---

## 3️⃣ Launch the Node

### 📥 Install Aztec:

```
bash -i <(curl -s https://install.aztec.network)
```
### Rpc  https://drpc.org 

### manually add a path to .bashrc
```
echo 'export PATH="$HOME/.aztec/bin:$PATH"' >> ~/.bashrc
```

###  Apply changes
```
source ~/.bashrc
```

### 🚀 Start:

```bash
aztec start --node --archiver --sequencer \
  --network alpha-testnet \
  --l1-rpc-urls RPC_URL  \
  --l1-consensus-host-urls BEACON_URL \
  --sequencer.validatorPrivateKey 0xYourPrivateKey \
  --sequencer.coinbase 0xYourAddress \
  --p2p.p2pIp you IP
```

---

## 4️⃣ Check Node Status

```bash
curl http://localhost:8080/status
```

Expected output: `OK`

---

## 🧽 Reset Node Data (if needed)

```bash
rm -rf ~/.aztec/alpha-testnet/
```

---

## 🧠 Useful Links

- [Aztec Official Site](https://aztec.network/)
- [Aztec GitHub](https://github.com/AztecProtocol)

