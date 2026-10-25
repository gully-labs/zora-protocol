<!-- gully-header:start -->
<a href="https://gullychain.xyz"><img src="https://gullychain.xyz/brand/repos/zora-protocol.svg" alt="GullyChain · Zora Protocol" width="100%"></a>

<p align="center">
  <a href="https://gullychain.xyz"><img src="https://img.shields.io/badge/gullychain.xyz-01D9FA?style=for-the-badge&labelColor=000000&logo=googlechrome&logoColor=000000" alt="Website"></a>
  <a href="https://app.gullychain.xyz"><img src="https://img.shields.io/badge/App-0A0F1A?style=for-the-badge&labelColor=000000&logo=googlechrome&logoColor=01D9FA" alt="App"></a>
  <a href="https://docs.gullychain.xyz"><img src="https://img.shields.io/badge/Docs-0A0F1A?style=for-the-badge&labelColor=000000&logo=readthedocs&logoColor=01D9FA" alt="Docs"></a>
  <a href="https://x.com/Gully_Labs"><img src="https://img.shields.io/badge/@Gully__Labs-0A0F1A?style=for-the-badge&labelColor=000000&logo=x&logoColor=white" alt="X"></a>
  <a href="https://t.me/GullyLabsNews"><img src="https://img.shields.io/badge/Telegram-0A0F1A?style=for-the-badge&labelColor=000000&logo=telegram&logoColor=26A5E4" alt="Telegram"></a>
  <a href="https://github.com/gully-labs"><img src="https://img.shields.io/badge/GitHub-0A0F1A?style=for-the-badge&labelColor=000000&logo=github&logoColor=white" alt="GitHub"></a>
</p>

<p align="center"><b>Zora Protocol: Zora contracts and SDKs for creator coins on GullyChain.</b></p>

<p align="center"><sub>Maintained by <a href="https://gullylabs.xyz">Gully Labs</a> as part of <a href="https://gullychain.xyz">GullyChain</a>. Fork of <a href="https://github.com/ourzora/zora-protocol">ourzora/zora-protocol</a>, used under its MIT licence. Not affiliated with or endorsed by Zora.</sub></p>

---
<!-- gully-header:end -->

# Zora Protocol

[![Contracts](https://github.com/ourzora/zora-protocol/actions/workflows/contracts.yml/badge.svg)](https://github.com/ourzora/zora-protocol/actions/workflows/contracts.yml)

This repository is a monorepo for the Zora Protocol.

In it you will find:

### Active Packages

- [Coins](./packages/coins)
- [Comments](./packages/comments)
- [Coins SDK](./packages/coins-sdk)
- [Protocol Deployments](./packages/protocol-deployments)
- [Smart Wallet](./packages/smart-wallet)

### Legacy Packages

- [Legacy Contracts](./legacy) - Contains legacy contract packages (1155-contracts, erc20z, sparks, cointags, protocol-sdk, etc.)

## Official docs

[View the official docs](https://docs.zora.co/docs/smart-contracts/creator-tools/intro)

## Setup

Install prerequisites:

- [Node.js and pnpm](https://pnpm.io/installation)
- [Foundry](https://book.getfoundry.sh/getting-started/installation)

Install dependencies:

    pnpm install

## Build System

This repository uses an optimized build system with two distinct build modes:

### JavaScript/TypeScript Development (`build:js`)

For JavaScript/TypeScript development and wagmi consumption:

    pnpm build:js

This command:

- Builds only the JavaScript/TypeScript artifacts needed for client applications
- Generates wagmi-compatible type definitions and ABIs
- Skips full Solidity compilation for faster builds
- Is optimized for frontend developers and SDK usage

### Full Development (`build`)

For complete contract development and testing:

    pnpm build

This command:

- Performs full Solidity compilation with all optimizations
- Generates all contract artifacts (out/, abis/, dist/)
- Required for contract development, testing, and deployment
- Slower but comprehensive build process

### Documentation Builds

Build documentation sites:

    pnpm build:docs:coins    # Build coins documentation
    pnpm build:docs:nft      # Build NFT documentation

### Common Development Commands

Run tests:

    pnpm test

Run in development mode (watch tests):

    pnpm dev

Format and lint code:

    pnpm format
    pnpm lint

### When to Use Which Build

- **Use `pnpm build:js`** when:

  - Developing frontend applications with wagmi
  - Working with the SDK packages
  - You only need TypeScript definitions and ABIs
  - You want faster builds for iteration

- **Use `pnpm build`** when:
  - Developing or modifying Solidity contracts
  - Running comprehensive tests
  - Preparing for deployment
  - You need all contract artifacts

## Bug Bounty

Report security vulnerabilities and learn about our Bug Bounty Program [here](https://docs.zora.co/bug-bounty/bug-bounty-program).
