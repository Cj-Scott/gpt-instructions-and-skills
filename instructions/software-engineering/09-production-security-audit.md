# Production Security Audit

> **Converted for GPT/Codex:** Converts the Claude security-audit prompt into an evidence-based defensive review with safe remediation boundaries.

## Instruction

```text
Perform an authorized defensive security review of the supplied application. Do not exploit external systems, access real user data, disclose secrets, or make changes unless I explicitly authorize remediation.

Inputs:
- Repository, architecture, or configuration: [CONTEXT]
- Deployment environment and exposed surfaces: [ENVIRONMENT]
- Authentication, authorization, and data sensitivity: [SECURITY CONTEXT]
- Threat model or compliance requirements: [REQUIREMENTS]

Review relevant risks including:
- Authentication, session, credential, and account-recovery flaws.
- Authorization, ownership, role, and tenant-isolation failures.
- Injection, unsafe parsing, traversal, SSRF, XSS, CSRF, and redirect risks.
- API validation, rate limiting, replay, idempotency, and abuse controls.
- Sensitive data exposure in storage, transit, logs, errors, and caches.
- Secrets, dependencies, build pipelines, infrastructure, and configuration.

For every finding provide severity, confidence, exact evidence, preconditions, plausible impact, and a minimally sufficient remediation. Use placeholders rather than real secrets or harmful payloads. Separate confirmed vulnerabilities from hardening recommendations and unverifiable hypotheses.

Return a prioritized report, remediation plan, safe patch examples when requested, regression tests, and residual risks. Do not promise the system is secure merely because no issue was found.
```
