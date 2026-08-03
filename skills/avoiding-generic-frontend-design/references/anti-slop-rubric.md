# Anti-Slop Review Rubric

Review rendered output and observed interaction. Source code alone is insufficient evidence.

## Severity

- **Blocker:** prevents task completion, accessibility, comprehension, or safe launch.
- **High:** makes the product misleading, generic, incoherent, or materially difficult to use.
- **Medium:** weakens hierarchy, consistency, responsiveness, or trust.
- **Low:** localized polish issue with limited user impact.

## Criteria

| Area | Evidence to inspect | Failure signals |
| --- | --- | --- |
| Product specificity | Thesis, copy, content, task flow | Could be relabeled for any startup without redesign |
| Hierarchy | First viewport, scan path, primary action | Everything has equal emphasis; decoration competes with action |
| Typography | Font roles, scale, measure, numerals | Default stack without rationale; excessive display styles |
| Composition | Grid, rhythm, section sequence | Repeated card bands; component-demo collage; arbitrary asymmetry |
| Color and surfaces | Tokens, contrast, state meaning | Generic gradient/glow; too many translucent panels; color-only status |
| Content realism | Labels, data, errors, long strings | Placeholder copy hides density and overflow problems |
| Interaction | Hover, focus, keyboard, feedback | Motion without purpose; missing focus; ambiguous controls |
| States | Loading, empty, error, success, permissions | Only the ideal state exists |
| Responsiveness | Representative narrow and wide renders | Desktop merely shrinks; clipped data; hidden primary actions |
| Accessibility | Semantics, contrast, zoom, reduced motion | Appearance-only review; inaccessible charts or forms |
| Consistency | Tokens, components, icon and copy rules | Each section follows a different reference style |
| Performance restraint | Asset, font, and animation cost | Decorative effects dominate load or runtime work |

## Finding Format

For every finding, report:

1. Severity and area.
2. Observable evidence and where it appears.
3. User or product impact.
4. Specific recommended change.
5. Verification needed after the change.

Do not invent observations. If a viewport, state, or interaction was not tested, list it under remaining risks.
