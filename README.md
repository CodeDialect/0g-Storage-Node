# 0G Storage Node One-Click Installer

## What Is a Storage Node?

Unlike Validator Nodes that secure the blockchain, **Storage Nodes** manage and serve large datasets. They are essential to the decentralized storage layer of the 0G AI network.

---

## Features

- One-click install
- Auto dependency install (Rust, Go, tools)
- Minimal working config.toml (dynamic)
- Systemd service auto-restart

---

## Requirements

- Ubuntu 20.04 or 22.04
- 4+ cores, 16GB+ RAM, 500-1000GB SSD/NVMe
- Public IP

---

## Install Dependencies 
```bash
sudo apt update && sudo apt install git curl -y
```

## Quick Start

```bash
bash <(curl -sL https://raw.githubusercontent.com/CodeDialect/0g-Storage-Node/main/0g_node_setup.sh)
```
---

## Change RPC
```bash
bash <(curl -sL https://raw.githubusercontent.com/CodeDialect/0g-Storage-Node/main/change_rpc.sh)
```
---

## Faucet & Explorer

- [Chain Info](https://docs.0g.ai/run-a-node/testnet-information)
- [Faucet](https://faucet.0g.ai/)
- [Explorer](https://chainscan-galileo.0g.ai/)
- [Miner Stats](https://storagescan-galileo.0g.ai/miner/)
- [RPCs](https://www.astrostake.xyz/0g-status)

---

## Manage

| Task | Command |
|------|---------|
| Status | `sudo systemctl status zgs` |
| Logs   | `tail -f ~/0g-storage-node/run/log/zgs.log.$(date +%F)` |
| Stop   | `sudo systemctl stop zgs` |
| Remove | `sudo systemctl disable zgs && sudo rm /etc/systemd/system/zgs.service` |
