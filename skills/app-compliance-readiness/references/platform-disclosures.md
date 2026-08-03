# Platform Disclosure Worksheet

Use only after completing the app data inventory. Recheck current Apple and Google definitions before preparing answers.

## Apple App Privacy

For each data type determine:

- Whether it is collected under Apple's current definition
- Whether an optional-disclosure exception applies
- Purpose or purposes
- Whether it is linked to the user's identity
- Whether it is used for tracking
- Whether third-party partners or SDKs collect it

Do not assume on-device processing is collection. Do not infer tracking solely from the presence of an advertising SDK; verify configuration, consent, contracts, and actual transfers.

## Google Play Data Safety

For each data type determine:

- Whether it is collected
- Whether it is shared, including whether a current exception applies
- Required versus optional collection
- Purpose or purposes
- Ephemeral-processing status
- Encryption in transit across all applicable flows
- User deletion mechanisms and scope

Treat third-party SDK behavior as the developer's responsibility. Do not answer that all data is encrypted merely because common SDKs normally use HTTPS; verify every relevant flow.

## Reconciliation checks

- Compare forms with the privacy policy, consent UI, ATT behavior, permissions, account-deletion flow, and backend behavior.
- Include custom analytics parameters, crash logs, support attachments, server-side events, advertising identifiers, and inferred attributes.
- Explain intentional Apple/Google differences using each platform's definitions.
- Mark each answer `Confirmed`, `Conditional`, or `Unknown` and cite its evidence.

## Submission boundary

Prepare a worksheet for review. Do not submit store declarations or change production consent flows without explicit user authorization.
