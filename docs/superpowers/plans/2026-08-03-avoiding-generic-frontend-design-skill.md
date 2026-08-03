# Avoiding Generic Frontend Design Skill Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build, publish, and locally install a Codex-native skill that prevents generic AI-generated frontend design.

**Architecture:** A concise `SKILL.md` coordinates visual-thesis creation, reference adaptation, implementation routing, and anti-slop review. Three progressively loaded references hold the detailed design record, review rubric, and pattern-adaptation guidance; repository catalogs expose the skill for discovery.

**Tech Stack:** Markdown, YAML, Codex skill-creator scripts, Git, GitHub CLI.

## Global Constraints

- Complement the existing `frontend-design` skill instead of duplicating its implementation guidance.
- Convert Claude-specific recommendations into Codex-native routing.
- Keep CodeRabbit and external component libraries optional.
- Do not copy third-party designs wholesale.
- Validate, forward-test, merge, and install the merged `main` package locally.

---

### Task 1: Establish the Failing Baseline

**Files:**
- Read: `docs/superpowers/specs/2026-08-03-avoiding-generic-frontend-design-skill-design.md`
- Create later: `skills/avoiding-generic-frontend-design/SKILL.md`

**Interfaces:**
- Consumes: Three frontend design scenarios without the new skill.
- Produces: A list of observable baseline failures that the skill must correct.

- [ ] **Step 1: Run a landing-page scenario without the skill**

Prompt an agent to propose a fast AI-security SaaS landing page under time pressure and record whether it defaults to generic gradients, cards, typography, or claims.

- [ ] **Step 2: Run a dashboard scenario without the skill**

Prompt an agent to improve a dense operations dashboard using a component library and record whether it copies patterns without a product-specific visual thesis.

- [ ] **Step 3: Run a review scenario without the skill**

Prompt an agent to review an attractive screenshot under launch pressure and record whether it omits responsiveness, accessibility, states, or implementation evidence.

- [ ] **Step 4: Confirm the baseline fails for relevant reasons**

Expected: At least one scenario lacks a coherent visual thesis, deliberate reference adaptation, or a complete verification rubric.

### Task 2: Create the Minimal Skill Package

**Files:**
- Create: `skills/avoiding-generic-frontend-design/SKILL.md`
- Create: `skills/avoiding-generic-frontend-design/agents/openai.yaml`
- Create: `skills/avoiding-generic-frontend-design/references/anti-slop-rubric.md`
- Create: `skills/avoiding-generic-frontend-design/references/visual-thesis-template.md`
- Create: `skills/avoiding-generic-frontend-design/references/reference-adaptation.md`

**Interfaces:**
- Consumes: Baseline failure list from Task 1.
- Produces: `$avoiding-generic-frontend-design`, a self-contained Codex skill.

- [ ] **Step 1: Initialize the package**

Run `init_skill.py avoiding-generic-frontend-design --path C:\GitRepo\gpt-instructions-and-skills\skills --resources references` with interface metadata for the display name, description, and default prompt.

- [ ] **Step 2: Write the minimal workflow**

Use `apply_patch` to define concrete triggers, the visual-thesis and review sequence, required routing to `frontend-design` when available, an output contract, quick reference, common mistakes, and one compact example.

- [ ] **Step 3: Write focused references**

Use `apply_patch` to add observable rubric criteria, the visual-thesis record, and rules for adapting reference patterns without cloning them.

- [ ] **Step 4: Verify structural constraints**

Run `quick_validate.py skills/avoiding-generic-frontend-design` with UTF-8 enabled. Expected: `Skill is valid!`

### Task 3: Forward-Test and Refine

**Files:**
- Modify if needed: `skills/avoiding-generic-frontend-design/SKILL.md`
- Modify if needed: `skills/avoiding-generic-frontend-design/references/*.md`

**Interfaces:**
- Consumes: The same three scenarios from Task 1 with the new skill loaded.
- Produces: Pressure-tested guidance that corrects the observed failures.

- [ ] **Step 1: Re-run all scenarios with the skill**

Expected: Each response states a product-specific visual thesis, adapts references deliberately, and includes responsive, accessibility, state, and code-quality verification without requiring CodeRabbit.

- [ ] **Step 2: Inspect every response manually**

Compare each response against the baseline failure list and the output contract.

- [ ] **Step 3: Patch any discovered gaps**

Use `apply_patch` only for behavior required by a failed scenario; do not add hypothetical scope.

- [ ] **Step 4: Re-run affected scenarios and validation**

Expected: Corrected scenarios pass and `quick_validate.py` still reports `Skill is valid!`

### Task 4: Catalog, Publish, and Install

**Files:**
- Modify: `README.md`
- Modify: `skills/README.md`
- Install to: `C:\Users\cjsco\.codex\skills\avoiding-generic-frontend-design`

**Interfaces:**
- Consumes: Validated skill package.
- Produces: A merged GitHub skill and an identical locally installed package.

- [ ] **Step 1: Add catalog entries**

Use `apply_patch` to link the skill from both catalog files with a one-sentence purpose.

- [ ] **Step 2: Run repository verification**

Run `quick_validate.py`, `git diff --check`, placeholder scans, referenced-file checks, and a complete package inventory. Expected: zero failures.

- [ ] **Step 3: Commit and publish**

Commit the plan, skill, references, and catalog changes; push the feature branch; open a ready pull request; merge it; switch to `main`; and pull with `--ff-only`.

- [ ] **Step 4: Install through the official helper**

Run `install-skill-from-github.py --repo Cj-Scott/gpt-instructions-and-skills --ref main --path skills/avoiding-generic-frontend-design`.

- [ ] **Step 5: Verify the installed copy**

Normalize line endings and compare every installed file with the merged repository package, then validate the installed directory. Expected: identical normalized content and `Skill is valid!`

- [ ] **Step 6: Commit checkpoint**

No additional commit is required after installation because local Codex deployment is outside the repository.
