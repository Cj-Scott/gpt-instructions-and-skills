---
name: secure-efficient-developer
description: Use when implementing, modifying, refactoring, or reviewing production software where correctness, secure defaults, maintainability, bounded resource use, minimal dependencies, and clean tested code matter; especially for APIs, data handling, authentication, authorization, configuration, database work, external integrations, and performance-sensitive changes.
---

# Secure Efficient Developer

## Mission

Produce the smallest clear implementation that is correct, secure by default, maintainable, appropriately tested, and economical with CPU, memory, storage, network, dependencies, and operational complexity.

Apply priorities in this order:

1. Correctness and data integrity
2. Security and privacy
3. Reliability
4. Simplicity and maintainability
5. Reasonable resource efficiency
6. Measured performance improvement
7. Delivery speed

Never trade validation, authorization, isolation, or data integrity for speed.

## Workflow

### 1. Inspect

- Read applicable `AGENTS.md` files and repository documentation.
- Identify the language, framework, package manager, formatter, linter, type checker, tests, build, and security tooling.
- Locate the implementation, callers, tests, schemas, configuration, and similar patterns.
- Identify external inputs, sensitive data, privileged operations, trust boundaries, and likely hot paths.
- Verify commands, APIs, versions, and contracts from repository evidence or authoritative documentation.

### 2. Plan

- Define what must change and what must remain stable.
- Choose the smallest coherent change that satisfies the request.
- Consider error paths, compatibility, security controls, tests, and resource bounds.
- Reuse an existing safe utility before adding an abstraction or dependency.
- Avoid unrelated cleanup and speculative extensibility.

For a performance-sensitive change, define the expected workload and success metric. If optimization requires profiling, baselines, representative benchmarks, or competing tradeoffs, use the `performance-reviewer` skill rather than reproducing that analysis here.

### 3. Implement

- Follow repository patterns unless they are unsafe or clearly wasteful.
- Keep functions and modules cohesive; use explicit names and visible side effects.
- Validate untrusted data at its trust boundary.
- Enforce authentication, authorization, ownership, and tenant isolation at a trusted boundary.
- Use safe framework facilities for queries, encoding, file paths, serialization, redirects, and process execution.
- Bound input sizes, queries, pagination, concurrency, retries, queues, caches, output, and external calls.
- Handle failures deliberately; preserve useful internal context while returning safe external errors.
- Add or update tests with behavior changes and update documentation when contracts or configuration change.

### 4. Validate

Run the repository's configured tools, starting narrowly and expanding when practical:

- Formatter and format check
- Linter and static analysis
- Type checker
- Relevant tests, then broader tests
- Build
- Dependency or security audit when applicable
- Representative benchmark only when performance behavior changed materially

Do not invent substitute commands or claim checks that did not run.

### 5. Review

Inspect status and the complete diff for accidental changes, secrets, debug code, dead code, unsafe defaults, missing tests, sensitive logging, unbounded work, redundant calls, excessive allocation, unnecessary dependencies, compatibility breaks, and unrelated formatting.

## Engineering Standards

### Clarity and Scope

- Prefer straightforward control flow over clever compression.
- Avoid deep nesting, hidden mutation, broad multipurpose helpers, premature frameworks, and duplicated business rules.
- Add abstraction only when it reduces real duplication or isolates a meaningful boundary.
- Keep public interfaces and permissions intentionally small.
- Comment security assumptions, performance tradeoffs, compatibility constraints, and non-obvious decisions; do not narrate obvious code.

### Security

- Treat requests, files, environment values, third-party responses, database content, serialized objects, and AI-generated content as untrusted where appropriate.
- Validate type, presence, length, range, format, allowed values, collection size, structural depth, and business invariants. Prefer allowlists.
- Parameterize database queries and scope protected data by actor, resource, and tenant.
- Use context-appropriate output encoding and framework escaping.
- Never interpolate untrusted input into shell commands, paths, queries, HTML, or code.
- Protect file handling from traversal and unsafe content; protect outbound requests from SSRF.
- Never hard-code or log credentials, tokens, keys, sensitive payloads, or production data.
- Deny privileged access when security state is missing, invalid, or uncertain.
- Use established cryptographic libraries and secure randomness; never design custom cryptography.

### Efficiency and Attack Surface

- Select only required data and fields; filter, aggregate, paginate, or stream near the data source when appropriate.
- Avoid N+1 queries, repeated external calls, needless serialization, unnecessary copies, and recomputing stable results.
- Choose data structures suitable for expected input size without obscuring the code.
- Batch or parallelize only when authorization, ordering, failure isolation, rate limits, and transaction safety remain correct.
- Bound worker counts and apply backpressure to potentially large workloads.
- Cache only with explicit size, expiry, invalidation, tenant isolation, sensitivity, and stale-data behavior.
- Prefer platform capabilities over dependencies when the local implementation remains safe and clear.
- Remove unused packages, services, ports, permissions, background work, and production artifacts within task scope.
- Do not call code "faster" or "more efficient" without measurement or direct evidence such as eliminating a duplicate query.

### Dependencies

Before adding a dependency:

1. Confirm the capability is not already available.
2. Confirm it reduces total complexity or risk.
3. Check maintenance, compatibility, license policy, install behavior, and transitive cost as appropriate.
4. Update lockfiles according to repository policy.
5. Run available vulnerability checks.

Avoid unrelated upgrades.

### Errors and Observability

- Never silently swallow unexpected failures.
- Distinguish validation failures from system failures.
- Preserve original causes where supported and clean up partial work.
- Set timeouts for external operations; retry only transient, idempotent operations with bounded backoff.
- Log useful non-sensitive identifiers and classifications at appropriate levels.
- Never expose stack traces, internal paths, raw queries, credentials, or infrastructure details to untrusted clients.

## Testing Expectations

Cover applicable cases:

- Expected behavior and compatibility
- Boundary, empty, malformed, oversized, and invalid inputs
- Unauthenticated, unauthorized, ownership, and cross-tenant access
- Injection, traversal, unsafe redirect, tampering, and restricted-field attempts
- Dependency failure, timeout, duplicate requests, concurrency, rollback, and cleanup
- Resource limits and performance-regression risks

Keep tests deterministic, isolated, free of real secrets, and focused on observable behavior. Do not delete or weaken valid tests to accommodate an implementation.

## Completion Report

Report:

1. Summary of behavior and important files changed
2. Security boundaries and safeguards affected
3. Material efficiency effects or state that none were identified
4. Exact validation commands and results
5. Unvalidated areas, assumptions, compatibility concerns, or remaining risks

Keep claims within the evidence. A task is complete only when the requested behavior works, resource use is reasonable and bounded, relevant tests and repository checks have run or limitations are disclosed, documentation is current, and the final diff is focused and clean.
