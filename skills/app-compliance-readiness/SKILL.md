---
name: app-compliance-readiness
description: Use when assessing whether a web or mobile app is ready for privacy, AI disclosure, app-store data-safety, terms, user-generated content, DMCA, CCPA, or related compliance review, especially before launch or after adding SDKs, analytics, advertising, uploads, or AI features.
---

# App Compliance Readiness

## Overview

Produce an evidence-based readiness assessment, not legal certification. Verify current requirements from official sources and separate confirmed facts from assumptions and attorney-review items.

## Workflow

1. Establish scope before evaluating compliance:
   - Business entity, operating locations, user jurisdictions, age groups, platforms, stores, and launch date.
   - App features, AI behavior and claims, user-generated content, monetization, advertising, and sensitive-data use.
   - Deployed SDK versions and configuration, backend processors, data retention, deletion, and existing legal documents.
2. Build the data map using [app-data-inventory.md](references/app-data-inventory.md). Treat source code, runtime configuration, network behavior, vendor terms, and user flows as evidence. Do not infer exact collection or encryption from an SDK name.
3. Route the review:
   - Apple or Google distribution: read [platform-disclosures.md](references/platform-disclosures.md).
   - Uploads, hosting, linking, or search: read [ugc-dmca-checklist.md](references/ugc-dmca-checklist.md).
   - Legal, regulatory, or platform claims: read [official-sources.md](references/official-sources.md).
4. Browse current official sources. Record jurisdiction, effective date or retrieval date, applicability conditions, and direct link. Distinguish laws, regulator guidance, platform policy, and vendor documentation.
5. Classify every conclusion as:
   - **Confirmed requirement:** supported by current official authority and established facts.
   - **Likely gap:** authority applies if a stated assumption is true.
   - **Unknown:** evidence is missing.
   - **Attorney review:** legal interpretation, contract enforceability, litigation exposure, or jurisdiction-specific drafting.
6. Produce the output contract below. Stop short of filing, submitting forms, registering agents, or publishing legal text unless the user separately authorizes that action.

## Output Contract

1. Scope and assumptions
2. Evidence inventory and missing evidence
3. Prioritized findings table: area, status, authority, evidence, risk, next action, owner
4. Apple and Google declaration worksheet when applicable
5. AI disclosure and claims review when applicable
6. UGC and DMCA operational checklist when applicable
7. Attorney-review questions
8. Launch blockers, post-launch work, and source list with retrieval dates

## Quick Reference

| Situation | Required response |
| --- | --- |
| User asks for a compliance guarantee | Decline the guarantee; provide evidence, gaps, and counsel questions. |
| SDK behavior is uncertain | Mark unknown; inspect configuration and current vendor documentation. |
| A form answer depends on facts | Provide a conditional worksheet, not a guessed submission value. |
| Requirements may have changed | Browse current official sources before answering. |
| User requests a legal clause | Label it a draft and route enforceability to qualified counsel. |

## Common Mistakes

- Treating a privacy policy sentence, arbitration clause, or DMCA registration as blanket immunity.
- Assuming every app is covered by the same law or threshold.
- Confusing Apple App Privacy with Google Play Data Safety terminology.
- Omitting third-party SDK, server-side, inferred, or custom-event data.
- Calling an app compliant when important evidence remains unknown.

## Example

For “Does Firebase Analytics, Crashlytics, and Meta SDK make my store forms compliant?”, first inventory versions, toggles, custom events, identifiers, consent, server transfers, retention, and deletion. Return conditional Apple and Google worksheets with official citations; do not submit guessed declarations.
