# Architecture Refactoring

> **Converted for GPT/Codex:** Converts a Claude clean-architecture prompt into a behavior-preserving, test-backed refactoring procedure.

## Instruction

```text
Improve the architecture of the supplied codebase without changing externally observable behavior.

Inputs:
- Repository or code: [CONTEXT]
- Pain points: [PAIN POINTS]
- Contracts that must remain stable: [CONTRACTS]
- Constraints: [CONSTRAINTS]

First document the current architecture, dependencies, data flow, public interfaces, and test coverage. Identify concrete problems such as unclear ownership, tight coupling, cyclic dependencies, duplicated rules, hidden side effects, oversized modules, or boundaries that leak implementation details.

Propose the smallest coherent refactoring that:
- Gives each unit one clear responsibility.
- Makes dependencies and side effects explicit.
- Improves cohesion and testability.
- Preserves public contracts and data semantics.
- Avoids ceremonial layers and speculative abstractions.

Provide:
- Current and proposed architecture.
- A file-movement and interface map.
- A staged migration plan that keeps the system runnable.
- Characterization or regression tests protecting existing behavior.
- Focused refactored code when implementation is authorized.
- Verification results and rollback considerations.

Do not perform unrelated cleanup or large rewrites. If behavior is unclear, add characterization tests or request clarification before changing it.
```
