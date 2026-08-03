# Optional Codex Plugins

Snapshot date: 2026-08-03

This inventory tracks installed plugins that are not part of Codex's bundled or primary-runtime toolset. It records what to reinstall without copying generated plugin caches, authentication tokens, connector credentials, or other machine-specific state.

## Installed optional plugins

| Plugin | Installed version | Purpose | Source |
| --- | --- | --- | --- |
| [Superpowers](https://github.com/obra/superpowers) | 6.2.0 | Development workflows for brainstorming, planning, TDD, debugging, code review, and branch completion. | `openai-curated-remote/superpowers` |
| [GitHub](https://github.com/openai/plugins) | 0.1.8-2841cf9749ae | Repository, pull-request, issue, CI, review, and publishing workflows. | `openai-curated-remote/github` |
| [Gmail](https://github.com/openai/oai-maintained-plugins) | 0.1.5 | Gmail search, inbox triage, summaries, drafting, and message organization. | `openai-curated-remote/gmail` |

## Restore guidance

Install each plugin by name from the Codex plugin marketplace. Treat the versions above as a reproducibility snapshot rather than a requirement to downgrade a newer compatible release. Reconnect GitHub or Gmail through Codex after installation; credentials are intentionally not stored in this repository.

After upgrading or adding an optional plugin, update its version, purpose, and source here.

## Deliberately excluded

The following are considered native/default components for this inventory and are not tracked as optional installations:

- Bundled Codex plugins such as Browser, Sites, and Visualize.
- Primary artifact/runtime plugins such as Documents, PDF, Presentations, Spreadsheets, and Template Creator.
- OpenAI default document, presentation, and spreadsheet templates.
- Plugin cache files, generated installation metadata, and account credentials.
