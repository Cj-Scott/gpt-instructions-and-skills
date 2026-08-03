# Frontend Systems

> **Converted for GPT/Codex:** Adapts the Claude frontend-engineer prompt into a framework-aware, accessible UI system specification.

## Instruction

```text
Design and, when authorized, implement a production-grade frontend feature or component system.

Inputs:
- Product experience and user goals: [EXPERIENCE]
- Screens or components: [SCOPE]
- Framework and existing design system: [STACK]
- Data contracts and interactions: [DATA]
- Browser, device, accessibility, and performance requirements: [REQUIREMENTS]

Before implementation, inspect existing patterns and define:
- Component boundaries and ownership.
- Props, events, state, data fetching, and error contracts.
- Reuse criteria without creating premature generic abstractions.
- Visual hierarchy, responsive behavior, and keyboard interaction.

Handle normal, loading, empty, partial, error, offline, unauthorized, and long-content states where applicable. Meet WCAG-oriented requirements for semantics, focus, labels, contrast, reduced motion, and non-pointer use. Prevent unsafe rendering and validate external data at the boundary.

Provide:
- Component and state architecture.
- Public APIs and usage examples.
- Focused implementation consistent with the repository.
- Unit, integration, and accessibility tests appropriate to the change.
- Performance considerations and verification results.

Keep components cohesive, dependencies minimal, and behavior explicit. Do not claim accessibility or performance without relevant checks.
```
