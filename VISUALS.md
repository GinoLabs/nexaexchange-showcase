# Public Visuals

These diagrams are intentionally sanitized for the public NexaExchange showcase.

> **Scope:** NexaExchange is a simulated exchange engineering project. These visuals do not represent a live licensed exchange, customer custody service, real-money trading venue, or deposit/withdrawal system.

## Simulator scope boundary

```mermaid
flowchart LR
    U[Public / Test User] --> UI[Simulator UI]
    UI --> API[Simulator API]
    API --> LEDGER[Simulated Ledger]
    API --> MATCH[Matching Engine]
    MATCH --> LEDGER

    X1[No real deposits]:::stop
    X2[No real withdrawals]:::stop
    X3[No customer custody]:::stop
    X4[No real-money trading]:::stop

    LEDGER -. outside current scope .-> X1
    LEDGER -. outside current scope .-> X2
    LEDGER -. outside current scope .-> X3
    MATCH -. outside current scope .-> X4

    classDef stop stroke-dasharray: 5 5;
```

## Sanitized architecture

```mermaid
flowchart TB
    B[Browser / React + TypeScript]
    A[Node / Express API]
    P[(PostgreSQL)]
    R[(Redis)]
    L[Simulated Ledger]
    O[Orders / Trades]
    S[Sessions / Audit Data]

    B --> A
    A --> P
    A --> R
    P --> L
    P --> O
    P --> S
```

No private hostnames, account identifiers, credentials, environment values, database URLs, SSH material, or internal incident details are included.

## Public engineering milestones

```mermaid
flowchart LR
    A[Core simulator] --> B[Public documentation]
    B --> C[Staging validation]
    C --> D[Monitoring + backup exercises]
    D --> E[Accessibility validation]
    E --> F[Independent security review]

    G[Future real-money decision]:::future
    F -. requires separate legal, compliance, custody, security and operational program .-> G

    classDef future stroke-dasharray: 5 5;
```

## Screenshot publication rule

Simulator screenshots can be added only after a separate public-release review confirms that they contain no credentials, private infrastructure identifiers, personal/customer data, sensitive URLs, session material, or language implying that real deposits, withdrawals, custody, or real-money trading are live.
