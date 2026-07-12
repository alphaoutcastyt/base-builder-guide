# Base Builder Guide

Base Builder Guide is an AI-focused starter guide for builders who want to create apps, smart contracts, payment flows, wallet integrations, or AI-agent-powered products on Base.

This repository is not just a collection of links. It is a practical operating guide that tells an AI where to look in the Base ecosystem, which official sources to prioritize, which SDKs, contracts, and features to use, and how to ship from idea to testnet to mainnet.

## Table of Contents

- [Why This Exists](#why-this-exists)
- [How To Use](#how-to-use)
- [What It Covers](#what-it-covers)
- [Base App And Mobile Note](#base-app-and-mobile-note)
- [Important Security Principles](#important-security-principles)
- [Official Sources](#official-sources)
- [Files](#files)

## Why This Exists

When building on Base, AI agents can sometimes drift into outdated docs, incomplete SDK examples, wrong chain information, or generic blockchain advice. This guide gives the AI a clear route:

- Which official Base docs should it check first?
- Which GitHub repositories should it use as references?
- When should it use Base App, Base Account, Base Pay, Builder Codes, B20, Basenames, OnchainKit, or Base MCP?
- How should it convert an idea into an MVP, frontend, backend, smart contracts, tests, and deployment plan?
- Which security checks are mandatory for payments, wallets, agents, and contracts?

## How To Use

### For Brainstorming Project Ideas

Give this repository (or directly `base-builder-ai-guide.md`) to an AI assistant and use a prompt like:

```
Read this guide. Give me strong project ideas I can build on Base.
For each idea, include the target user, why Base is the right chain,
which Base features it uses, MVP scope, contract requirements,
and a testnet build plan.
```

### For Existing Ideas

If you already have an idea, use:

```
Read this guide. Turn this idea into a working Base project:
[write your idea]

Include frontend, backend, smart contracts, wallet integration,
payment verification, Builder Code attribution, Base Sepolia deployment plan,
and tests where needed.
```

### For Coding Agents

If you are giving this to a coding agent:

```
Read base-builder-ai-guide.md first. Then inspect this repository and build the MVP on Base.
Use Base Sepolia by default, include required contracts, wallet integration,
payment verification if needed, Builder Code attribution, tests, and run instructions.
```

## What It Covers

The guide brings the following Base builder topics into one AI operating file:

### Network & Infrastructure
- Base Chain network information
- Base Mainnet, Base Sepolia, and Vibenet differences
- RPC, node provider, and production infrastructure rules

### Smart Contracts & Deployment
- Smart contract deployment with Foundry
- Base Account and Sign In With Base
- B20 token/precompile rules

### Payments & Transactions
- Base Pay and server-side payment verification
- Base Subscriptions
- Sponsored gas and paymaster flows
- Batch transactions, sub-accounts, and spend permissions
- Commerce Payments
- Flashblocks and transaction UX

### Features & Integrations
- Builder Codes and ERC-8021 attribution
- Basenames
- OnchainKit
- Base MCP, agents, x402 payments, and plugin architecture

### Frontend & Distribution
- Base App's standard web app model
- Mobile-friendly Base apps and PWA guidance

### Quality & Security
- Testing, security, and mainnet readiness checklists

## Base App And Mobile Note

For Base App, the right target is a mobile-friendly standard web app or PWA. A product meant to open inside Base App should not be treated as a native iOS/Android mini-runtime. It should be designed as a responsive web application that works well on mobile browsers.

You can also build native iOS or Android apps that interact with Base. That is a separate distribution model from a Base App-discoverable web app.

## Important Security Principles

- **Do not put private keys, seed phrases, CDP secrets, paymaster URLs, or RPC secrets in the repository.**
- Use Base Sepolia as the default target for new projects.
- Payment apps must not rely on frontend success alone; backend verification is mandatory.
- Payment and order fulfillment must include replay protection.
- Smart wallet features must check wallet capabilities before use.
- Builder Codes should be considered for transaction attribution in apps that send transactions.
- Time-sensitive information must be checked against official docs and status pages.

## Official Sources

- **Base Docs**: https://docs.base.org/
- **Base Docs LLM Index**: https://docs.base.org/llms-full.txt
- **Base Website**: https://www.base.org/
- **Base Blog**: https://blog.base.dev/
- **Base Status**: https://status.base.org/
- **Base GitHub**: https://github.com/base
- **Base Agents Quickstart**: https://docs.base.org/agents/quickstart
- **Base MCP**: https://mcp.base.org
- **Coinbase Developer Platform Docs**: https://docs.cdp.coinbase.com/
- **OnchainKit**: https://onchainkit.xyz/

## Files

- **README.md**: Purpose and usage of this repository.
- **base-builder-ai-guide.md**: The main Base Builder AI Guide to give to an AI assistant.

## Note

This guide does not mean an AI should never check official sources. It tells the AI which official source to check and when. SDK signatures, API limits, plugin lists, B20 activation status, and network status must always be verified against official Base docs and status pages before deployment.
