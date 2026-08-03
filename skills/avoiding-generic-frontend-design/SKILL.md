---
name: avoiding-generic-frontend-design
description: Use when creating, redesigning, or reviewing websites, landing pages, dashboards, application interfaces, or web components that risk looking generic, template-driven, copied from component libraries, or recognizably AI-generated.
---

# Avoiding Generic Frontend Design

## Overview

Make frontend work product-specific and verifiably complete. Define the visual logic, adapt references deliberately, and review the rendered result instead of accepting a polished desktop frame as proof.

## Workflow

1. Inspect the product, audience, content, brand assets, existing interface, and technical constraints. Mark missing context explicitly.
2. Read [visual-thesis-template.md](references/visual-thesis-template.md) and state one coherent visual thesis before implementation. Make every major styling choice support it.
3. **REQUIRED SUB-SKILL:** Use `frontend-design` for implementation when it is available. This skill supplies the direction and review contract; it does not replace production frontend design guidance.
4. If using galleries, templates, or component libraries, read [reference-adaptation.md](references/reference-adaptation.md). Record the principles being borrowed and how each is changed for this product.
5. Implement or revise the interface. Use authentic content and believable product states; placeholders cannot prove hierarchy or density.
6. Render representative desktop and mobile viewports. Exercise keyboard navigation, reduced motion, loading, empty, error, success, and overflow states as applicable.
7. Read [anti-slop-rubric.md](references/anti-slop-rubric.md). Rank findings by user impact and fix the highest-impact causes, not merely the easiest cosmetic symptoms.
8. Route correctness, security, and performance concerns to the relevant review skills or tools. CodeRabbit or another external reviewer may supplement this pass but is never required.

## Output Contract

Return these sections in order:

1. **Context and uncertainties**
2. **Visual thesis**
3. **Reference adaptation record**
4. **Implementation or revision priorities**
5. **Anti-slop findings** — finding, evidence, impact, and recommended change
6. **Verification evidence** — viewports, states, accessibility, and rendered checks actually performed
7. **Remaining risks and next actions**

Do not claim a design is ready from source code, a component-library preview, or one screenshot alone.

## Quick Reference

| Symptom | Response |
| --- | --- |
| Generic purple gradient, glass cards, glow | Rebuild from the product's visual thesis. |
| Page resembles a component showcase | Keep one narrative spine; remove unrelated patterns. |
| Reference is attractive but unrelated | Extract a principle, not its composition or branding. |
| Desktop looks polished | Verify smaller viewports, states, keyboard use, and content stress. |
| Review says “looks good” | Require observable evidence and ranked findings. |

## Common Mistakes

- Choosing style before understanding audience and content.
- Combining several fashionable patterns without shared visual logic.
- Copying distinctive compositions, copy, assets, or motion from references.
- Treating animation, gradients, or rounded cards as personality.
- Inventing verification evidence or hiding uncertainty.

## Example

For “make this analytics homepage premium with 21st.dev components,” define what premium means for the product, choose one reference principle such as compact data hierarchy, adapt its spacing and interaction to real analytics content, then verify the result with the rubric. Do not assemble a collage of unrelated demos.
