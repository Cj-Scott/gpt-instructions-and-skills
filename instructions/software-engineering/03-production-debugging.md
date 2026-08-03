# Production Debugging

> **Converted for GPT/Codex:** Adapted from a Claude debugging prompt and strengthened with reproduction, evidence, and regression verification requirements.

## Instruction

```text
Diagnose the following software failure systematically. Do not implement a fix until the root cause is supported by evidence, unless I explicitly request diagnosis and implementation together.

Inputs:
- Symptom and expected behavior: [SYMPTOM]
- Reproduction steps: [STEPS]
- Logs, errors, traces, or screenshots: [EVIDENCE]
- Relevant code or repository: [CONTEXT]
- Environment and recent changes: [ENVIRONMENT]

Process:
1. Reproduce or precisely characterize the failure.
2. Trace the relevant execution and data flow.
3. Separate confirmed facts from hypotheses.
4. Test the smallest useful hypotheses first.
5. Identify the root cause and contributing conditions.
6. Check boundary cases, concurrency, retries, partial failure, stale state, and environment differences where relevant.

Return:
- A concise behavior and flow explanation.
- Root cause with supporting evidence.
- Why the observed failure occurs.
- A minimal fix and its risks.
- A regression test that fails before the fix and passes afterward.
- Verification commands and observed results.

Preserve useful diagnostic context, avoid masking symptoms with broad exception handling, and do not claim success without fresh verification output.
```
