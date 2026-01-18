# SubNFT: The Subscription NFT Engine

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Ecosystem: Stellar/EVM](https://img.shields.io/badge/Ecosystem-Stellar%20%7C%20EVM-purple.svg)](https://stellar.org)
[![Model: Recurring Revenue](https://img.shields.io/badge/Model-Recurring%20Revenue-orange.svg)](#)

**SubNFT** is a protocol-agnostic engine for creating time-locked, subscription-based NFTs. Designed specifically for open-source developers and researchers, SubNFT provides a sustainable revenue model by turning digital assets into expiring access keys.

---

### 1. Executive Summary
One-time NFT sales rarely support long-term maintenance. SubNFT introduces **Time-Locked Metadata**. Developers can issue NFTs that grant access to private GitHub repositories, specialized documentation, or premium Discord channels for a specific duration. Once the "subscription" period ends, the NFT metadata dynamically updates to a "revoked" or "expired" state until a renewal payment is made.

### 2. The Problem
The "Starving Developer" problem is real in Web3:
* **One-and-Done Revenue:** Standard NFTs provide a burst of initial liquidity but no recurring support for maintenance.
* **Proprietary Gating:** Existing subscription tools are often "Black Box" solutions that take high platform fees (10-20%).
* **Complexity:** Setting up an expiring access system requires complex smart contract logic that many developers don't have time to build.

### 3. Key Features
* **⏳ Time-Locked Metadata:** NFTs that "expire" on-chain, triggering a change in access rights across integrated platforms.
* **🔓 Decentralized Gating:** Native integrations for GitHub (via GitHub Apps) and Discord (via Bot) to automate member management.
* **🔄 Auto-Renewal Logic:** Optional smart contract hooks that allow users to "top up" their NFT duration using stablecoins.
* **🌌 Multi-Chain Support:** Optimized for **Stellar/Soroban** (using Contract Storage) and **EVM** (using EIP-5643 or similar standards).

### 4. Roadmap for this Wave
* **Phase 1:** Core Subscription Smart Contract for Soroban and Solidity.
* **Phase 2:** Launch the "Access Watcher" service—a middleware that checks NFT expiration before granting GitHub/Discord access.
* **Phase 3:** Create a No-Code Dashboard for developers to launch their own Subscription NFT collections.

### 5. Why SubNFT belongs in Drips Wave
SubNFT is a **Sustainability Tool** for the public good.
* **Empowering Creators:** We provide the infrastructure for developers to fund their own work independently.
* **Sustainability:** We use Drips to stream 15% of our funding back to the NFT metadata standards and decentralized storage providers (like IPFS/Arweave) we utilize.

---

## 🛠 Project Structure (Monorepo)

```text
SubNFT/
├── contracts/
│   ├── soroban/       # Rust-based subscription logic
│   └── evm/           # Solidity (EIP-5643) implementation
├── apps/
│   ├── dashboard/     # UI for creators to manage subscriptions
│   └── watcher/       # Middleware for GitHub/Discord gating
├── libs/
│   └── metadata/      # Logic for generating expiring JSON metadata
└── LICENSE            # MIT Licensed
