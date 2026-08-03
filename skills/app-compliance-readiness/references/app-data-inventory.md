# App Data Inventory

Build this inventory before answering privacy or app-store questions. Use `Unknown` when evidence is missing.

## Scope intake

- Legal entity, business model, annual revenue, data-volume thresholds, and operating locations
- User locations, age groups, children or teen access, and sensitive-user populations
- Web, iOS, Android, desktop, browser extension, or other distribution
- AI features, automated decisions, generated output, and user-facing claims
- User uploads, messaging, profiles, public content, linking, search, and moderation
- Advertising, analytics, attribution, payments, authentication, support, and marketing

## Data-flow fields

For every first-party feature, backend service, SDK, API, and processor record:

| Field | Required detail |
| --- | --- |
| Data | Exact field or category, including custom-event parameters and inferred data |
| Source | User, device, app event, server, partner, public source, or inference |
| Purpose | Specific operational, analytics, advertising, security, or account purpose |
| Required | Required, optional, consent-gated, or configuration-dependent |
| Destination | On-device, first-party server, processor, advertising partner, or other third party |
| Identity | Anonymous, pseudonymous, device-linked, account-linked, or directly identifying |
| Retention | Duration, trigger, deletion path, backups, and legal holds |
| Security | Transport, storage, access control, logging, and secret handling evidence |
| User control | Consent, opt-out, access, correction, deletion, and appeal mechanisms |
| Evidence | File/config location, runtime observation, network trace, contract, or vendor documentation |

## Evidence priority

1. Runtime and network behavior in the relevant production configuration
2. Source code and deployed configuration
3. Current vendor documentation for the exact version
4. Contracts and data-processing terms
5. Existing disclosures and internal statements

Existing privacy text is a claim to verify, not proof of actual behavior.
