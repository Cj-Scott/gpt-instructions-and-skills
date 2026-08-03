# Avoiding Generic Frontend Design Skill

## Purpose

Create a Codex-native skill that prevents generic, interchangeable AI-generated frontend design. The skill will turn the Instagram reel's three-part advice—design intelligence, automated review, and strong premade patterns—into a reusable workflow that complements the existing `frontend-design` skill.

## Scope

The skill applies when Codex creates or substantially redesigns a website, landing page, dashboard, application interface, or reusable web component. It focuses on visual distinctiveness and review quality; it does not replace implementation, security, performance, or framework-specific skills.

## Workflow

1. Inspect the product context, audience, content, existing brand system, and current interface before proposing a direction.
2. Define a compact visual thesis covering typography, color, composition, density, imagery, and interaction character.
3. Use `frontend-design` as the required implementation-oriented design skill when it is available.
4. Study relevant component and layout references for principles, then adapt them to the product rather than copying a template wholesale.
5. Review the result against an explicit anti-slop rubric: hierarchy, specificity, typography, composition, repetition, states, responsiveness, accessibility, and consistency.
6. Route code correctness and security findings to the appropriate review skill or tool. External services such as CodeRabbit remain optional.
7. Iterate on the highest-impact findings and verify the rendered interface at representative viewport sizes.

## Skill Package

- `SKILL.md`: triggers, core workflow, output contract, quick reference, common failure patterns, and one compact example.
- `agents/openai.yaml`: Codex display metadata and a default invocation prompt.
- `references/anti-slop-rubric.md`: observable review criteria and severity guidance.
- `references/visual-thesis-template.md`: a compact decision record for visual direction.
- `references/reference-adaptation.md`: rules for learning from premade designs without producing a copied or incoherent collage.

## Output Contract

When reviewing or designing an interface, the skill produces:

1. Product and audience context.
2. Visual thesis.
3. Reference principles being adapted.
4. Implementation or revision priorities.
5. Anti-slop review findings ranked by impact.
6. Viewport and accessibility verification evidence.
7. Remaining uncertainties and next actions.

## Testing

Baseline scenarios will test whether an agent naturally reaches for generic gradients, repeated rounded cards, default typography, arbitrary animation, or unadapted component-library patterns. Forward tests will reuse the same scenarios with the skill loaded and verify that the agent produces a coherent visual thesis, adapts references deliberately, and applies the review rubric without making external tools mandatory.

## Deployment

After validation, add the skill to both repository catalogs, merge it through a pull request, and install the merged package into `C:\Users\cjsco\.codex\skills` for local Codex use.
