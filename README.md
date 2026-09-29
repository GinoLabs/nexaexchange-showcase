# NexaExchange Showcase

NexaExchange is a **simulated centralized-exchange development project** built to explore exchange architecture, trading workflows, ledger design, matching, operational controls, and security hardening without accepting real customer funds or real cryptocurrency.

> This public showcase is intentionally separate from the private operational/source repository. It must not contain production credentials, private infrastructure details, internal incident material, or secret-bearing configuration.

## Current safety boundary

NexaExchange is a simulator.

It does **not** accept:
- real cryptocurrency deposits or withdrawals
- fiat deposits or withdrawals
- real-money trading
- customer custody
- real customer assets

Any future move beyond simulation requires a separate legal, compliance, custody, security, and operational program.

## What the project demonstrates

- Account registration and authentication
- Simulated BTC and USDT balances
- Double-entry ledger concepts
- Limit and market orders
- Price-time-priority matching
- Partial fills and cancellations
- Trading fees
- Trade and order history
- Administrative controls and audit concepts
- Session-security hardening
- Staging / operational-readiness planning

## High-level architecture

```text
Browser / React + TypeScript
          |
          v
     Node / Express API
          |
   +------+------+
   |             |
PostgreSQL     Redis
   |
Simulated ledger,
orders, trades,
sessions & audit data
```

The public showcase should describe architecture at a high level only. Private hostnames, AWS account details, SSH material, environment values, passwords, tokens, database URLs, and private service identifiers stay out of this repository.

## Technology

- React
- TypeScript
- Vite
- Node.js
- Express
- PostgreSQL
- Redis
- Docker / containerized development
- GitHub
- AWS-hosted staging infrastructure

## Project status

The private project has implemented the core simulator, including accounts, simulated balances, ledger-backed trading, matching, fees, administrative controls, email-provider abstractions, and session-rotation work. Staging, operational validation, independent security review, and other readiness gates remain separate from any real-money production decision.

## Security approach

The public showcase must never include:
- `.env` files
- AWS credentials
- SSH private keys
- API keys
- access tokens
- database connection strings
- production cookies or session tokens
- internal incident evidence
- customer data
- private backend source copied wholesale from the operational repository

Before publication, every document, screenshot, diagram, and video should receive a public-release review.

## Roadmap

Public-facing roadmap items may include:
- simulator staging validation
- monitoring and backup exercises
- accessibility validation
- independent security review
- operational runbooks
- continued simulator UX improvements

Real-money features are intentionally outside the current public simulator scope.

## Sponsorship

❤️ **Support the project:** https://github.com/sponsors/Yoyogino

Sponsorship helps fund public documentation, simulator development, testing, security work, infrastructure exercises, and educational engineering resources.

Sponsorship does not represent an investment product, customer deposit, token sale, exchange account, or entitlement to financial returns.

## Public architecture

See [ARCHITECTURE.md](ARCHITECTURE.md) for the sanitized architecture overview.

## Repository guides

- [Architecture](ARCHITECTURE.md)
- [Public roadmap](ROADMAP.md)
- [Security policy](SECURITY.md)
- [Contributing](CONTRIBUTING.md)
- [Simulator disclaimer](DISCLAIMER.md)
- [Public release checklist](PUBLIC_RELEASE_CHECKLIST.md)
- [Public media register](MEDIA.md)

## Repository boundary

Public showcase repository: `nexaexchange-showcase`  
Private operational/source repository: `Yoyogino/NexaExchange`

Keep those roles separate.

---

NexaExchange · simulated exchange engineering project
