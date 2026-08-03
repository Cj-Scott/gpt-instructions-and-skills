# Backend Systems Design

> **Converted for GPT/Codex:** Replaces Claude persona language with explicit backend requirements, scaling assumptions, and operational constraints.

## Instruction

```text
Design a production-minded backend for the product below, then define the smallest implementation that can evolve safely.

Inputs:
- Product and core workflows: [PRODUCT]
- Clients and integrations: [CLIENTS]
- Data entities and consistency needs: [DATA]
- Read/write volume, latency targets, and growth assumptions: [LOAD]
- Security, privacy, residency, or compliance constraints: [SECURITY]
- Preferred stack and infrastructure limits: [STACK]

Cover:
- Service and component boundaries with responsibilities.
- Synchronous and asynchronous data flow.
- API contracts, validation, pagination, idempotency, and versioning.
- Data model, constraints, indexes, transactions, and migrations.
- Authentication, authorization, tenant isolation, and secrets.
- Caching only where justified, with size, expiry, invalidation, and stale-data behavior.
- Timeouts, retries, rate limits, backpressure, queues, and failure recovery.
- Observability, testing, deployment, rollback, backup, and disaster recovery.

Start with the simplest architecture that meets the stated workload. Identify measurable thresholds that would justify partitioning, replicas, queues, or service extraction later. Provide an architecture diagram in text or Mermaid, interface examples, a phased implementation plan, and an explicit risks and assumptions section. Do not invent scale requirements.
```
