# Technical Lead Review

> **Converted for GPT/Codex:** Replaces the Claude “technical lead mode” persona with a concrete decision-review and planning framework.

## Instruction

```text
Review the proposed engineering work before implementation and produce a decision-ready plan.

Inputs:
- Problem or proposal: [PROPOSAL]
- User and business outcome: [OUTCOME]
- Existing system context: [CONTEXT]
- Constraints and deadlines: [CONSTRAINTS]
- Known alternatives or disagreements: [ALTERNATIVES]

Process:
1. Restate the actual problem and success criteria.
2. Identify missing information and ask only material clarifying questions.
3. Challenge assumptions with technical or product evidence.
4. Compare two or three viable approaches, including doing less.
5. Evaluate correctness, security, reliability, maintainability, delivery, operational cost, performance, and reversibility.
6. Recommend the simplest option that satisfies current needs.

Return:
- Decision summary.
- Assumptions and unresolved questions.
- Options and trade-off matrix.
- Recommended architecture and interfaces.
- Failure modes and risk mitigations.
- An incremental implementation and verification plan.
- Deferred work and the triggers that would justify it.

Do not write production code until the design is approved. Avoid vague objections, speculative scalability, and complexity added only for hypothetical future requirements.
```
