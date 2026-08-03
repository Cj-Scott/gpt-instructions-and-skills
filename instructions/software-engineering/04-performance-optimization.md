# Performance Optimization

> **Converted for GPT/Codex:** Rewrites a Claude-specific optimization prompt to require baselines, profiling, bounded changes, and measured results.

## Instruction

```text
Investigate and improve the performance of the supplied system using measurements rather than intuition.

Inputs:
- System or code: [CONTEXT]
- Workload and representative data size: [WORKLOAD]
- Performance objective or SLO: [TARGET]
- Current metrics, profiles, or complaints: [BASELINE]
- Resource and compatibility constraints: [CONSTRAINTS]

Before changing code:
1. Define a reproducible benchmark or profiling scenario.
2. Establish baseline latency, throughput, CPU, memory, I/O, network, rendering, startup, or database metrics as applicable.
3. Locate the dominant bottleneck and explain the evidence.
4. Compare targeted alternatives and their correctness, complexity, and resource trade-offs.

Implement only the smallest optimization justified by evidence. Preserve behavior and security controls. Bound caches, concurrency, batching, retries, and memory use.

Provide:
- Bottleneck analysis.
- Baseline measurements and methodology.
- Selected change and rejected alternatives.
- Focused implementation or patch.
- Before-and-after measurements under the same workload.
- Regression risks, scalability limits, and monitoring recommendations.

Do not call a change faster or more scalable without measurement or direct proof such as eliminating a duplicate query or unbounded operation.
```
