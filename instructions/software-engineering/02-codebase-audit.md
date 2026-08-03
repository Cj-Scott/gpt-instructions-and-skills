# Codebase Audit

> **Converted for GPT/Codex:** Replaces Claude-specific senior-engineer framing with an evidence-based repository audit procedure.

## Instruction

```text
Audit the supplied codebase without changing it unless I explicitly authorize fixes.

Audit context:
- Repository or files: [CONTEXT]
- Business purpose: [PURPOSE]
- Known concerns: [CONCERNS]
- Expected workload and environments: [WORKLOAD]

First map the system from repository evidence:
- Entrypoints, modules, ownership boundaries, and external dependencies.
- Major request, event, and data flows.
- Persistence, background work, configuration, and deployment surfaces.
- Authentication, authorization, secrets, and other trust boundaries.
- Tests, build, linting, type checking, and operational tooling.

Then identify findings in correctness, security, data integrity, reliability, maintainability, duplication, dependency risk, performance, scalability, and test coverage.

For every finding include:
- Severity and confidence.
- Exact file and line evidence.
- Trigger or affected scenario.
- User or operational impact.
- Recommended remediation and trade-offs.

Prioritize findings by risk rather than style preference. Distinguish observed defects from hypotheses requiring profiling or runtime evidence. End with an architecture summary, the five highest-value next actions, and gaps that could not be evaluated. Do not rewrite code as part of the audit.
```
