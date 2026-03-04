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

## Submodules (PoT-O crates, firmware, and CLI)

The PoT-O validator, ESP miner, and desktop miner use library crates, firmware, and the CLI that can live in separate GitHub repos and are consumed here as **git submodules**.

- **Rust library crates:** `pot-o-core`, `ai3-lib`, `pot-o-mining`, `pot-o-extensions` (under `gateway.tribewarez.com/testnet.rpc.gateway.tribewarez.com/pot-o-validator/`).
- **ESP firmware:** `esp-pot-o-miner` (under `.../pot-o-validator/firmware/esp-pot-o-miner`).
- **Desktop CLI miner:** [pot-o-miner-cli](https://github.com/TribeWarez/pot-o-miner-cli) (bash + Python 3) — under `gateway.tribewarez.com/testnet.rpc.gateway.tribewarez.com/pot-o-miner-cli` when used as a submodule of the testnet gateway repo.

**Clone with submodules:**

```bash
git clone --recurse-submodules https://github.com/TribeWarez/tribe tribe
cd tribe
```

**If you already cloned without submodules:**

```bash
git submodule update --init --recursive
```

**Converting in-repo crates/firmware to submodules (one-time):**  
Create the corresponding empty repos under your GitHub org (`tribewarez/pot-o-core`, `ai3-lib`, `pot-o-mining`, `pot-o-extensions`, `esp-pot-o-miner`), then from the repo root run:

```bash
./scripts/setup-crate-submodules.sh    # exports Rust crates and adds submodules
./scripts/setup-firmware-submodule.sh # exports esp-pot-o-miner and adds submodule
```

Commit the updated `.gitmodules` and submodule entries. Dependency versions between the validator and the library crates are aligned via the workspace and `[patch.crates-io]` in the validator `Cargo.toml` when building in-repo.

## Running the Stack Locally

**Prerequisites:** Docker, Docker Compose, Make, Git.

```bash
git clone --recurse-submodules https://github.com/TribeWarez/tribe tribe
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

## Status

[![PoT-O Validator](https://img.shields.io/github/actions/workflow/status/TribeWarez/tribe/pot-o-validator.yml?branch=main)](https://github.com/TribeWarez/tribe/actions/workflow/pot-o-validator.yml)
[![Solana Programs](https://img.shields.io/github/actions/workflow/status/TribeWarez/tribe/programs.yml?branch=main)](https://github.com/TribeWarez/tribe/actions/workflow/programs.yml)
[![Security scan](https://img.shields.io/github/actions/workflow/status/TribeWarez/tribe/security-scan.yml?branch=main)](https://github.com/TribeWarez/tribe/actions/workflow/security-scan.yml)
[![Deploy (production)](https://img.shields.io/github/deployments/TribeWarez/tribe/production)](https://github.com/TribeWarez/tribe/deployments)

## CI and releases

- **Main repo**
  - **PoT-O Validator** (`.github/workflows/pot-o-validator.yml`): on push/PR to `main`, checks out with submodules, runs `cargo test` and `cargo build --release` in the pot-o-validator workspace.
  - **Solana Programs** (`.github/workflows/programs.yml`): on push/PR to `main`, runs `cargo check --workspace` in the programs workspace (Anchor build can be added when needed).

- **Rust library crates** (when used as separate repos)
  - **CI** (`.github/workflows/ci.yml`): `cargo test`, `cargo clippy`, `cargo fmt --check` on push/PR to `main`.
  - **Release** (`.github/workflows/release.yml`): on tag `v*.*.*`, runs tests then `cargo publish` to crates.io (requires repo secret `CARGO_REGISTRY_TOKEN`), and creates a GitHub Release.

- **ESP firmware (esp-pot-o-miner)** (when used as a separate repo)
  - **CI** (`.github/workflows/ci.yml`): PlatformIO build for `esp32s` and `esp8266` on push/PR.
  - **Release** (`.github/workflows/release.yml`): on tag `v*.*.*`, builds both envs, uploads firmware artifacts, and creates a GitHub Release. Optional: set `PLATFORMIO_AUTH_TOKEN` to publish to the PlatformIO registry.

- **Desktop CLI miner (pot-o-miner-cli)** ([TribeWarez/pot-o-miner-cli](https://github.com/TribeWarez/pot-o-miner-cli))
  - **CI** (`.github/workflows/ci.yml`): checks bash/curl/jq/python3, runs `./pot-o-mine --help`, and validates Python syntax. No publish step; tag releases can be created manually from the Releases UI.

**Release playbooks**

- **Rust crates:** Bump `version` in `Cargo.toml`, commit, then `git tag v0.1.1 && git push origin v0.1.1`. CI publishes to crates.io and creates the GitHub Release.
- **Firmware:** Bump version in `platformio.ini` (e.g. `POT_O_VERSION`), commit, then tag and push as above; CI builds and attaches binaries to the GitHub Release.

## Security

Do not commit real API keys, client secrets, or private keys. Use `.env` (gitignored) or a secrets manager. Public endpoints do not expose internal URLs or credentials.

## Contributing

The ecosystem is in **testnet/experimental** phase. As repositories are cleaned up and validated, they will be opened for public contribution. We welcome issues, pull requests, and discussion around the RFC series. Get in touch via the repositories and docs linked above.
cd ~
