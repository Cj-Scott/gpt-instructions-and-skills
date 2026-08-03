# GPT Instructions and Skills Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Create and publish a cataloged repository for reusable GPT instructions and skills.

**Architecture:** Keep `C:\GitRepo` as a container and initialize only `gpt-instructions-and-skills` as a Git repository. Use Markdown catalogs at the container and repository levels for deterministic discovery.

**Tech Stack:** Git, GitHub CLI, Markdown

## Global Constraints

- Do not initialize `C:\GitRepo` as a Git repository.
- Use `main` as the initial branch.
- Publish the `gpt-instructions-and-skills` subdirectory as a new GitHub repository.

---

### Task 1: Create and publish the repository

**Files:**
- Create: `README.md`
- Create: `instructions/pure-css-rotating-glow-border.md`
- Create: `skills/README.md`

**Interfaces:**
- Consumes: the approved directory design and rotating-glow-border instruction
- Produces: a discoverable GitHub repository with a tracked `main` branch

- [ ] **Step 1: Initialize the subdirectory on `main`**

Run `git init -b main` from `C:\GitRepo\gpt-instructions-and-skills`.

- [ ] **Step 2: Verify repository boundaries and Markdown content**

Confirm `C:\GitRepo\.git` does not exist, all Markdown files are readable, and the instruction appears in the repository catalog.

- [ ] **Step 3: Commit the repository content**

Stage only files inside `C:\GitRepo\gpt-instructions-and-skills` and commit them as `Add GPT instructions and skills library`.

- [ ] **Step 4: Create and push the GitHub repository**

Run `gh repo create gpt-instructions-and-skills --public --source . --remote origin --push` from the subrepository.

- [ ] **Step 5: Verify publication**

Confirm the local branch tracks `origin/main`, the working tree is clean, and `gh repo view` resolves the published repository.
