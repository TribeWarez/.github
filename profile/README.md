# TribeWarez

**AI-powered blockchain ecosystem for PoT-O mining, DeFi, and decentralized applications on Solana and EVM testnets.**

---

## Overview

TribeWarez is a blockchain ecosystem that replaces traditional proof-of-work with **Proof of Tensor Optimizations (PoT-O)**, and provides multi-chain testnets, on-chain DeFi programs, and a token economy designed for mining, staking, and swaps. Many of our repositories are currently undergoing cleanup and validation; **most will be released to the public** once that work is complete.

## Ecosystem Components

- **Proof of Tensor Optimizations (PoT-O)** — Replaces SHA-256 mining with tensor computation proofs validated by MML path optimality and neural inference path matching (standardized in TW-RPC-001).
- **Multi-Chain Testnets** — Solana test validator with RPC proxy and Helius fallback, plus a Geth PoW EVM testnet (chain ID 5555).
- **DeFi Programs** — On-chain staking, AMM swap, and vault/escrow programs built with Anchor on Solana (TW-RPC-003 staking, TW-RPC-004 vault).
- **ESP-Ready Mining** — Tensor challenges sized for ESP32-S and ESP8266 microcontrollers for IoT solo mining.
- **Token Economy** — PTtC (Pumped TRIB€-test Coin) and NMTC (Numerologic Master Coin) with mining rewards, staking, and swap capabilities.
- **Extensible Architecture** — Trait-based extension points for device protocols, multi-node VPN mesh, pool strategies, and cross-chain bridges (TW-RPC-005).

## Running the Stack Locally

**Prerequisites:** Docker, Docker Compose, Make, Git.

```bash
git clone https://github.com/TribeWarez/tribe tribe
cd tribe
cp .env.example .env
# Edit .env with your API keys and secrets (never commit real values)

make infra-up      # Base infrastructure (nginx-proxy, SSL)
make web3-up       # Web3 stack (DeFi, terminal, docs)
make web3-rpc-up   # Testnet RPC (Solana, EVM, PoT-O validator)
```

## Key Services

| Service        | URL |
|----------------|-----|
| DeFi Portal    | [defi.tribewarez.com](https://defi.tribewarez.com) |
| Terminal       | [terminal.tribewarez.com](https://terminal.tribewarez.com) |
| Docs           | [docs.tribewarez.com](https://docs.tribewarez.com) |
| Solana RPC     | testnet-solana.rpc.gateway.tribewarez.com |
| EVM RPC        | testnet-eth.rpc.gateway.tribewarez.com |
| PoT-O Validator| pot.rpc.gateway.tribewarez.com |
| Status API     | status.rpc.gateway.tribewarez.com |

## Docs and RFCs

- [Getting Started](https://docs.tribewarez.com/getting-started) — Prerequisites and quick start.
- [PoT-O Mining](https://docs.tribewarez.com/pot-o/) — How Proof of Tensor Optimizations works.
- [PoT-O RFC Series](https://docs.tribewarez.com/public/) — TW-RPC-001 (PoT-O core), TW-RPC-003 (staking), TW-RPC-004 (vault), TW-RPC-005 (extensions).

## Security

Do not commit real API keys, client secrets, or private keys. Use `.env` (gitignored) or a secrets manager. Public endpoints do not expose internal URLs or credentials.

## Contributing

The ecosystem is in **testnet/experimental** phase. As repositories are cleaned up and validated, they will be opened for public contribution. We welcome issues, pull requests, and discussion around the RFC series. Get in touch via the repositories and docs linked above.
