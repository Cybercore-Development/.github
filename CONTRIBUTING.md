# Contributing Guidelines

Thank you for contributing to Cybercore Development projects.  
We operate with a big-tech style workflow: **Tasks** are assigned to a single **DRI (Directly Responsible Individual)**, reviewed by a **Peer Reviewer**, and approved by a **Final Approver** (maintainer) before merge.

---

## Work Model

- **Tasks** are the unit of work (created as GitHub Issues with a TaskID).
- Each Task has one **DRI** (owner) and one **Peer Reviewer**.
- A **Final Approver** (from the core maintainers team) must approve before merge.
- All work happens on **feature branches**; `main` is protected.

**Lifecycle:** Task → Branch → Draft PR (within 24h) → Peer Review → Final Approval (Core Maintainer) → Merge

---

## Branching

- Always branch from `main`.
- Branch naming:
  - `feature/TASK-<id>-<yourname>`
  - `fix/TASK-<id>-<yourname>`
- Example: `feature/TASK-123-cyber`

---

## Commits

- Follow [Conventional Commits](https://www.conventionalcommits.org/).
- All commits must reference a TaskID.
- Examples:
  - `feat(TASK-123): add GET /users/:id endpoint`
  - `fix(TASK-456): handle null user email`

---

## Pull Requests

- Open a **Draft PR within 24 hours** of starting work.  
  Draft PRs are not expected to be complete — they are for visibility, discussion, and early feedback.
- Convert to “Ready for Review” when the Task is implemented and tests are passing.
- Every PR must:
  - Target `main`
  - Fill the PR template completely
  - Be reviewed first by a **Peer Reviewer**, then approved by a **Final Approver**
  - Pass CI (lint, tests, build)
- **PR size:** Keep changes small and focused (< 300 LOC changed is the guideline). Split large work into smaller PRs.

---

## Code Style

- **Naming:**
  - Variables/functions: `camelCase`
  - Classes/types: `PascalCase`
  - Constants: `SCREAMING_SNAKE_CASE`
  - Files: `kebab-case`
- **Formatting:** Prettier + ESLint enforced.

---

## Testing

- **Unit tests are required** for all new code. Update/extend tests when behavior changes.
- **Location & structure:** Place all tests under `tests/`, mirroring the `src/` path.  
  Rule: `src/path/to/File.js` → `tests/path/to/File.test.js`
- **Naming:** Use the same base name as the source file, with `.test.js`.
- **Coverage:** Overall coverage must not decrease. Changed lines/branches must be covered.
- **PR Testing Plan:** Each PR must include test cases covered and the commands to run them.
- **Scope by size:**
  - **S:** unit tests for functions/modules
  - **M:** unit tests + boundary/error cases
  - **L:** unit + integration/contract tests
- **Stability:** Flaky tests are not allowed. Mark and fix (or quarantine) immediately.

---

## Acceptance Criteria & Definition of Done (DoD)

A Task is “Done” when:
1. Acceptance criteria in the Task are met.  
2. CI passes (lint/tests/build) and coverage ≥ threshold.  
3. PR approved by Peer Reviewer and Final Approver.  
4. Docs/changelog updated if relevant.  
5. No secrets or credentials are committed.

---

## Sizing & Timelines

- **S (1–2 days):** small change, localized tests  
- **M (3–5 days):** multiple files/components, new tests  
- **L (design summary required):** significant scope; align with PM/Approver first

For **L** Tasks, include a **Design Summary** in the PR:
- Problem & constraints
- Proposed approach (APIs, data, errors)
- Test strategy
- Risks / rollback plan

---

## Communication

- Follow the **Code of Conduct** and **Security Policy** at all times.
- Use Issues for task scope and discussion.
- Use PR comments for code-specific discussion.
- Keep all project communication inside official channels (GitHub, Telegram).

---

By contributing, you agree to follow these guidelines.
