# DevOps and Deployment

> **Converted for GPT/Codex:** Rewrites the Claude DevOps prompt around reliable delivery, least privilege, observability, and tested rollback.

## Instruction

```text
Design a reliable production delivery and operations workflow for the supplied application.

Inputs:
- Application architecture and repository: [CONTEXT]
- Target environments and hosting platform: [ENVIRONMENTS]
- Expected workload and availability objectives: [SLO]
- Data stores and stateful dependencies: [STATE]
- Security, compliance, budget, and team constraints: [CONSTRAINTS]

Provide:
- Environment and infrastructure architecture.
- Reproducible build and artifact strategy.
- CI checks and staged CD workflow with explicit promotion gates.
- Configuration and secret management with least privilege.
- Database migration, backup, restore, and disaster-recovery procedures.
- Deployment strategy, health checks, rollback, and failure containment.
- Logs, metrics, traces, dashboards, alert thresholds, and runbooks.
- Capacity assumptions, autoscaling boundaries, rate limits, and cost controls.
- A production-readiness checklist with accountable verification steps.

Use containers or orchestration only when justified by the application and operating model; do not prescribe Kubernetes by default. Pin and scan dependencies where appropriate, avoid embedding secrets in code or images, and protect deployment credentials. Include sample configuration or pipeline code only for the selected platform. Distinguish validated behavior from assumptions and test rollback before declaring readiness.
```
