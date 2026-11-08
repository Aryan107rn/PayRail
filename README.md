# PayRail

### Payment Orchestration, Reliability & Observability Platform

**One Integration. Multiple Providers. Reliable Payments.**

PayRail is a developer-first payment infrastructure platform that provides a unified interface for integrating multiple payment service providers (PSPs). It enables businesses to orchestrate payment execution, configure intelligent routing, handle provider failures, maintain financial consistency and monitor the complete lifecycle of transactions.

It also features a dedicated Payment Testing Lab that allows developers to simulate real-world failure scenarios and validate payment reliability.

---

## Overview

Managing multiple payment providers introduces engineering challenges such as inconsistent APIs, provider outages, duplicate transactions, uncertain payment outcomes and reconciliation complexity.

PayRail addresses these challenges through a centralized orchestration and reliability layer between merchants and payment providers.

### Core Capabilities

- **Unified Payment API** — Integrate multiple payment providers through a single interface.
- **Intelligent Routing** — Route transactions using configurable provider selection policies.
- **Failure Recovery** — Handle timeouts, provider outages and uncertain payment outcomes safely.
- **Idempotency** — Prevent duplicate payment processing.
- **Payment Observability** — Track transaction execution, provider responses and failure history.
- **Financial Ledger** — Maintain consistent financial records and support reconciliation.
- **Payment Testing Lab** — Simulate payment failures and validate recovery mechanisms.

---

## System Architecture

PayRail follows a modular monolith architecture with asynchronous background processing, designed for maintainability, consistency and scalability.

### High-Level Design
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/88946978-c420-4d6b-a11e-2454f9bf25a0" />


### Payment Execution Flow

<!-- Add Payment Execution Flow Diagram Here -->

![PayRail Payment Flow](docs/architecture/payment-flow.png)

### Payment Lifecycle

<!-- Add Payment State Machine Diagram Here -->

![PayRail Payment State Machine](docs/architecture/payment-state-machine.png)

### Database Design

<!-- Add Database ER Diagram Here -->

![PayRail Database ER Diagram](docs/architecture/database-erd.png)

---

## Technology Stack

| Layer | Technology |
|---|---|
| Frontend | React, TypeScript |
| Styling | Tailwind CSS |
| Backend | Node.js, Fastify, TypeScript |
| ORM | Drizzle ORM |
| Database | PostgreSQL |
| Queue & Cache | Redis, BullMQ |
| Reverse Proxy | Nginx |
| Containerization | Docker |
| Observability | OpenTelemetry, Prometheus, Grafana |
| Testing | Vitest, k6 |

---

## Engineering Concepts

PayRail focuses on practical backend engineering and distributed systems concepts:

- Distributed systems and fault tolerance.
- Idempotency and concurrency control.
- Database transactions and financial consistency.
- Payment state machines.
- Circuit breakers and retry strategies.
- Asynchronous processing and background workers.
- Event-driven architecture and webhooks.
- Double-entry accounting and reconciliation.
- Multi-tenant security.
- Observability and distributed tracing.
- Fault injection and failure recovery.

---

## Payment Testing Lab

A dedicated environment for testing payment infrastructure under controlled failure conditions.

**Supported simulation scenarios:**

- Provider timeouts and outages.
- Delayed payment responses.
- Duplicate webhooks.
- Concurrent payment requests.
- Worker failures.
- Unknown payment outcomes.

<!-- Add Payment Testing Lab Screenshot Here -->

![PayRail Payment Testing Lab](docs/images/testing-lab.png)

---

## Dashboard Preview

<!-- Add Dashboard Screenshots Here -->

| Overview Dashboard | Transaction Management |
|---|---|
| ![Dashboard](docs/images/dashboard.png) | ![Transactions](docs/images/transactions.png) |

| Provider Management | Payment Observability |
|---|---|
| ![Providers](docs/images/providers.png) | ![Observability](docs/images/observability.png) |

---

## Project Structure

```text
payrail/
├── apps/
│   ├── api/
│   └── dashboard/
├── packages/
│   ├── database/
│   ├── shared/
│   └── provider-sdk/
├── docs/
│   ├── architecture/
│   ├── api/
│   ├── database/
│   └── images/
├── infrastructure/
├── tests/
├── docker-compose.yml
├── pnpm-workspace.yaml
├── .env.example
├── LICENSE
└── README.md
```

---

## Development Roadmap

| Phase | Milestone | Status |
|---|---|---|
| 1 | Core API and merchant management | Planned |
| 2 | Payment engine and mock providers | Planned |
| 3 | Routing and reliability engine | Planned |
| 4 | Webhooks, recovery and ledger | Planned |
| 5 | Payment Testing Lab | Planned |
| 6 | Dashboard and observability | Planned |
| 7 | Real provider integrations and deployment | Planned |

---

## Documentation

Detailed technical documentation will be maintained separately.

- High-Level Design (HLD)
- Low-Level Design (LLD)
- Database Schema and ER Diagram
- API Documentation
- Payment Lifecycle and State Transitions
- Failure Handling and Recovery Strategies
- Security and Engineering Decisions

---

## Security

PayRail is designed with security and financial correctness in mind.

- Merchant-level authentication and authorization.
- Tenant data isolation.
- Secure API key management.
- Webhook signature verification.
- Encrypted provider credentials.
- Idempotent payment operations.
- Immutable financial records.
- Rate limiting and audit logging.

The initial project is a development and testing platform. Production payment operations require appropriate provider agreements, security reviews and regulatory assessment.

---

## License

Distributed under the **MIT License**. See [LICENSE](LICENSE) for details.

---

<p align="center">
  <strong>PayRail</strong><br/>
  Making Payment Infrastructure Reliable, Observable and Developer-Friendly.
</p>
