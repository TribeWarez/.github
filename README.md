<p align="center">
  <img src="https://github.com/user-attachments/assets/68df66ec-acd3-4d81-9822-f13f82dd50d8" alt="TribeWarez Logo" width="800">
  <h1 align="center">TribeWarez</h1>
  <p align="center">
    <strong>AI-powered blockchain ecosystem evolving Proof-of-Work into Proof of Tensor Optimizations (PoT-O)</strong><br>
    Multi-chain testnets • On-chain DeFi • Edge-device mining • Synthetic tensor challenges • Open alpha/beta on Solana + EVM
  </p>
  <p align="center">
    <a href="https://github.com/TribeWarez/pot-o-core/blob/main/LICENSE">
      <img src="https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square" alt="License: MIT">
    </a>
    <a href="https://github.com/TribeWarez/pot-o-validator/actions/workflows/ci.yml">
      <img src="https://github.com/TribeWarez/pot-o-validator/actions/workflows/ci.yml/badge.svg" alt="PoT-O Validator CI">
    </a>
    <a href="https://github.com/TribeWarez/pot-o-contractz/actions/workflows/ci.yml">
      <img src="https://github.com/TribeWarez/pot-o-contractz/actions/workflows/ci.yml/badge.svg" alt="Contracts CI">
    </a>
    <a href="https://crates.io/crates/pot-o-core">
      <img src="https://img.shields.io/crates/v/pot-o-core?style=flat-square&logo=rust&logoColor=orange" alt="pot-o-core on crates.io">
    </a>
    <a href="https://crates.io/crates/ai3-lib">
      <img src="https://img.shields.io/crates/v/ai3-lib?style=flat-square&logo=rust&logoColor=orange" alt="ai3-lib on crates.io">
    </a>
    <a href="https://huggingface.co/Tribewarez">
      <img src="https://img.shields.io/badge/Hugging%20Face-Tribewarez-orange?style=flat-square&logo=huggingface" alt="Hugging Face">
    </a>
    <img src="https://img.shields.io/badge/Status-Live%20Beta-purple?style=flat-square" alt="Status: Live Beta">
  </p>
  <p align="center">
    <strong>Jump to:</strong><br>
    <a href="https://huggingface.co/Tribewarez">🤗 Hugging Face (Datasets &amp; Models)</a> •
    <a href="https://defi.tribewarez.com/">💱 DeFi Portal</a> •
    <a href="https://mystic.tribewarez.com/">🔮 Mystic</a> •
    <a href="https://docs.tribewarez.com/">📖 Docs</a>
  </p>
</p>

---

## Overview

TribeWarez is an **open-source (MIT)** ecosystem pioneering **Proof of Tensor Optimizations (PoT-O)** — replacing energy-intensive hashing with verifiable tensor computations, neural path matching, and information-theoretic proofs. Built for low-power edge devices (ESP32, Raspberry Pi clusters), synthetic data generation, and multi-chain DeFi on Solana + EVM testnets.

**Early 2026 status**: Live beta / open alpha. Most components are experimental, actively developed, and progressively open-sourced. Expect evolving specs, rough edges, and rapid iteration.

> **🔓 Open Source Commitment:** All core implementation logic is MIT-licensed and free to contribute. Some repositories are being cleaned up and stabilized — they will be fully opened for public contribution upon their 1.0 release. Several are open right now. Join the guild!

## Key Features

- **PoT-O Consensus** — Tensor-based proofs (MML path optimality + inference matching) per TW-RPC-001
- **Edge Mining** — ESP32/ESP8266 firmware for solo mining tensor challenges
- **Synthetic Data Gen** — Clustered challenge generation (Ch7 tensor dims & networking effects) → Hugging Face datasets
- **Multi-Chain Testnets** — Solana validator + proxy, Geth EVM (chain ID 5555)
- **On-Chain DeFi** — Staking, AMM swaps, vaults (Anchor programs / Solana smart contracts)
- **DeFi Games** — On-chain games (Mystic Numbers and more) blending DeFi mechanics with gameplay
- **Apps & Tools** — Mystic Scribe Engine (fun web app), docs portal, CLI miner
- **Extensible** — Trait-based hooks for protocols, meshes, bridges

## Ecosystem Repositories

### ⚙️ Core Protocol & Validator

| Repo | Description | Language | CI | Links |
|------|-------------|----------|----|-------|
| **[pot-o-core](https://github.com/TribeWarez/pot-o-core)** | Core types & utilities for PoT-O | Rust | [![CI](https://github.com/TribeWarez/pot-o-core/actions/workflows/ci.yml/badge.svg)](https://github.com/TribeWarez/pot-o-core/actions/workflows/ci.yml) | [![crates.io](https://img.shields.io/crates/v/pot-o-core?style=flat-square)](https://crates.io/crates/pot-o-core) [docs.rs](https://docs.rs/pot-o-core) |
| **[ai3-lib](https://github.com/TribeWarez/ai3-lib)** | AI3 support for validator/miner | Rust | [![CI](https://github.com/TribeWarez/ai3-lib/actions/workflows/ci.yml/badge.svg)](https://github.com/TribeWarez/ai3-lib/actions/workflows/ci.yml) | [![crates.io](https://img.shields.io/crates/v/ai3-lib?style=flat-square)](https://crates.io/crates/ai3-lib) [docs.rs](https://docs.rs/ai3-lib) |
| **[pot-o-mining](https://github.com/TribeWarez/pot-o-mining)** | Mining coordination & neural-path logic | Rust | [![CI](https://github.com/TribeWarez/pot-o-mining/actions/workflows/ci.yml/badge.svg)](https://github.com/TribeWarez/pot-o-mining/actions/workflows/ci.yml) | crates.io forthcoming |
| **[pot-o-extensions](https://github.com/TribeWarez/pot-o-extensions)** | DeFi, staking, chain extensions | Rust | [![CI](https://github.com/TribeWarez/pot-o-extensions/actions/workflows/ci.yml/badge.svg)](https://github.com/TribeWarez/pot-o-extensions/actions/workflows/ci.yml) | crates.io forthcoming |
| **[pot-o-validator](https://github.com/TribeWarez/pot-o-validator)** | PoT-O Validator HTTP API & consensus node | Rust | [![CI](https://github.com/TribeWarez/pot-o-validator/actions/workflows/ci.yml/badge.svg)](https://github.com/TribeWarez/pot-o-validator/actions/workflows/ci.yml) | [RPC: pot.rpc.gateway.tribewarez.com](https://pot.rpc.gateway.tribewarez.com) |

### 📜 Smart Contracts & DeFi Programs

| Repo | Description | Language | CI | Links |
|------|-------------|----------|----|-------|
| **[pot-o-contractz](https://github.com/TribeWarez/pot-o-contractz)** | Solana programs (staking, AMM, vault/escrow) for PTtC/NMTC | Rust (Anchor) | [![CI](https://github.com/TribeWarez/pot-o-contractz/actions/workflows/ci.yml/badge.svg)](https://github.com/TribeWarez/pot-o-contractz/actions/workflows/ci.yml) | [DeFi Portal](https://defi.tribewarez.com) |

### ⛏️ Mining Clients

| Repo | Description | Language | CI | Links |
|------|-------------|----------|----|-------|
| **[esp-pot-o-miner](https://github.com/TribeWarez/esp-pot-o-miner)** | ESP32-S / ESP8266 mining firmware | C/C++ (PlatformIO) | [![CI](https://github.com/TribeWarez/esp-pot-o-miner/actions/workflows/ci.yml/badge.svg)](https://github.com/TribeWarez/esp-pot-o-miner/actions/workflows/ci.yml) | PlatformIO registry forthcoming |
| **[pot-o-miner-cli](https://github.com/TribeWarez/pot-o-miner-cli)** | Self-contained bash CLI for PC mining | Shell/Python | [![CI](https://github.com/TribeWarez/pot-o-miner-cli/actions/workflows/ci.yml/badge.svg)](https://github.com/TribeWarez/pot-o-miner-cli/actions/workflows/ci.yml) | — |

### 🧪 Synthetic Data & Research

| Repo | Description | Language | CI | Links |
|------|-------------|----------|----|-------|
| **[pot-o-ch7-cluster](https://github.com/TribeWarez/pot-o-ch7-cluster)** | Distributed synthetic Ch7 challenge generator (Pi/ESP32 clusters) | Python/Jupyter | [![CI](https://github.com/TribeWarez/pot-o-ch7-cluster/actions/workflows/ci.yml/badge.svg)](https://github.com/TribeWarez/pot-o-ch7-cluster/actions/workflows/ci.yml) [![HF Space](https://github.com/TribeWarez/pot-o-ch7-cluster/actions/workflows/hf-space.yml/badge.svg)](https://github.com/TribeWarez/pot-o-ch7-cluster/actions/workflows/hf-space.yml) | [🤗 HF Dataset](https://huggingface.co/datasets/Tribewarez/synthetic-pot-o-challenges-ch7-v1) |

### 🎮 DeFi Games

| Repo | Description | Status | Links |
|------|-------------|--------|-------|
| **[Mystic Numbers](https://github.com/TribeWarez/mystic-numbers)** | On-chain DeFi number game — first in the TribeWarez DeFi games series | Coming Soon | [🔮 mystic.tribewarez.com](https://mystic.tribewarez.com) |

### 🌐 Apps & Web

| Repo | Description | Language | CI | Links |
|------|-------------|----------|----|-------|
| **[mystic-scribe-engine](https://github.com/TribeWarez/mystic-scribe-engine)** | Fun web app — Mystic Scribe Engine | TypeScript/JS | Coming Soon | [🔮 mystic.tribewarez.com](https://mystic.tribewarez.com) |
| **[docs.tribewarez.com](https://github.com/TribeWarez/docs.tribewarez.com)** | Documentation portal & RFC drafts | Dockerfile/Markdown | [![Build IETF drafts](https://github.com/TribeWarez/docs.tribewarez.com/actions/workflows/build-ietf-drafts.yml/badge.svg)](https://github.com/TribeWarez/docs.tribewarez.com/actions/workflows/build-ietf-drafts.yml) | [📖 docs.tribewarez.com](https://docs.tribewarez.com) |

## Quick Start (Local Stack)

Prerequisites: Docker, Docker Compose, Git, Make

```bash
git clone --recurse-submodules https://github.com/TribeWarez/tribe
cd tribe
cp .env.example .env   # Edit with keys/secrets (never commit!)
make infra-up          # nginx-proxy + SSL
make web3-up           # DeFi portal, terminal, docs
make web3-rpc-up       # Testnet RPCs + PoT-O validator
```

Explore services:
- DeFi → https://defi.tribewarez.com
- Docs → https://docs.tribewarez.com
- Mystic → https://mystic.tribewarez.com
- RPCs → `testnet-solana.rpc.gateway.tribewarez.com` / `testnet-eth.rpc.gateway.tribewarez.com` / `pot.rpc.gateway.tribewarez.com`

## Key Services

| Service | URL |
|---------|-----|
| DeFi Portal | [defi.tribewarez.com](https://defi.tribewarez.com) |
| Mystic / DeFi Games | [mystic.tribewarez.com](https://mystic.tribewarez.com) |
| Terminal | [terminal.tribewarez.com](https://terminal.tribewarez.com) |
| Docs | [docs.tribewarez.com](https://docs.tribewarez.com) |
| Hugging Face | [huggingface.co/Tribewarez](https://huggingface.co/Tribewarez) |
| Solana RPC | testnet-solana.rpc.gateway.tribewarez.com |
| EVM RPC | testnet-eth.rpc.gateway.tribewarez.com |
| PoT-O Validator | pot.rpc.gateway.tribewarez.com |
| Status API | status.rpc.gateway.tribewarez.com |

## Documentation & RFCs

- [Getting Started](https://docs.tribewarez.com/getting-started)
- [PoT-O Mining Guide](https://docs.tribewarez.com/pot-o/)
- [RFC Series](https://docs.tribewarez.com/public/) (TW-RPC-001 → PoT-O core, 003 → staking, 004 → vault, 005 → extensions)

## Contributing

We're in open beta — issues, PRs, and Discussions welcome!

> **🔓 All core implementation logic is open source under MIT.** Most repositories are open for contribution right now. For stacks approaching their 1.0 release, full public contribution opens on release — check each repo's CONTRIBUTING.md or Discussions for current status.

Focus areas: bug fixes, challenge ideas, edge optimizations, DeFi program audits, synthetic data quality, DeFi game mechanics.
Start with Discussions for ideas/questions.

This ecosystem is permanently open-source under MIT. Join the guild building tensor-first blockchain + AI infra.

💪 **Let's optimize reality.**

## Security

Do not commit real API keys, client secrets, or private keys. Use `.env` (gitignored) or a secrets manager. Public endpoints do not expose internal URLs or credentials.
