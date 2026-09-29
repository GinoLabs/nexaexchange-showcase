# NexaExchange — Public Architecture Overview

NexaExchange is currently a **simulated exchange engineering project**. This document describes the architecture at a public-safe level.

## High-level system

```text
             Browser
                |
                v
      React + TypeScript UI
                |
                v
          Node / Express API
           /             \
          v               v
    PostgreSQL          Redis
          |
          v
  Simulated accounts,
  ledger, orders,
  trades, sessions,
  audit information
```

## Core concepts demonstrated

### Accounts and sessions
The simulator includes account authentication and session-management concepts, including session hardening work.

### Double-entry ledger
Simulated balances are represented through ledger concepts rather than real customer assets.

### Trading
The simulator demonstrates:
- limit orders
- market orders
- price-time priority
- partial fills
- cancellations
- fee handling
- trade history

### Administrative controls
The project includes administrative and audit concepts intended for simulator operations and testing.

## Infrastructure boundary

The private operational project uses hosted staging infrastructure, but the public showcase must not expose:
- private hostnames
- cloud account identifiers
- SSH material
- environment files
- database URLs
- passwords
- tokens
- internal service identifiers
- incident evidence

## Simulator-only boundary

The public architecture must not imply that NexaExchange currently:
- accepts real cryptocurrency
- accepts fiat
- provides real-money trading
- provides customer custody
- operates as a licensed exchange

Any transition beyond simulation is a separate legal, compliance, custody, security, and operations program.

## Public technology overview

Safe technologies to mention publicly include:
- React
- TypeScript
- Vite
- Node.js
- Express
- PostgreSQL
- Redis
- Docker
- GitHub
- cloud-hosted staging infrastructure

## Public-release rule

The showcase explains architecture and engineering decisions without publishing the private operational source repository or secret-bearing configuration.
