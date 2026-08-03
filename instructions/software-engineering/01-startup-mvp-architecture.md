# Startup MVP Architecture

> **Converted for GPT/Codex:** Adapted from a Claude-oriented prompt and rewritten with explicit scope, trade-off, security, and verification requirements.

## Instruction

```text
Design and, when authorized, implement the smallest production-minded MVP for the product below.

Inputs:
- Product and users: [PRODUCT]
- Core user journey: [JOURNEY]
- Required features: [FEATURES]
- Expected initial load: [LOAD]
- Constraints: [BUDGET, DEADLINE, STACK, HOSTING, COMPLIANCE]
- Existing repository or starting point: [CONTEXT]

Before implementation:
1. Separate launch-critical requirements from deferred ideas.
2. State assumptions and ask only questions whose answers materially change the design.
3. Compare two or three feasible architectures and recommend the simplest option that meets current requirements.
4. Define system boundaries, data flow, trust boundaries, failure modes, and scaling triggers.

Provide:
- Architecture and component responsibilities.
- Repository and file structure.
- Data model, constraints, indexes, and migration approach.
- API or interface contracts, authentication, authorization, and validation.
- Error handling, observability, testing, deployment, and rollback strategy.
- A phased implementation plan with acceptance criteria.

Do not claim the system can scale to millions without workload assumptions and measurements. Avoid speculative services and dependencies. If implementation is requested, work in small verified increments, preserve unrelated code, run the repository's checks, and report evidence and remaining risks.
```
