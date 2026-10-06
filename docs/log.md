# Work log

Purpose: append-only work log. Every session, human or AI, adds one entry at the END of this file. Never edit or reorder old entries.

## How to add an entry

Copy the template, fill it in, append it at the bottom. Keep it short: what changed, what is open. Link PRs or commits where useful.

## Template

```markdown
## YYYY-MM-DD – Name – human|AI session

**What changed**
- ...

**Open points / next**
- ...
```

---

## 2026-10-06 – Marcus – AI session

**What changed**
- Repo scaffolded: vision, kickoff summary, guidelines (`README.md`, `CLAUDE.md`, `CONTRIBUTING.md`), app sketch (`docs/app-sketch.md` + `docs/index.html`), ideas, to-dos, ADR template and tech-stack proposal (ADR-0001, status proposed), issue and PR templates, `.gitignore`, `.editorconfig`.

**Open points / next**
- Team reviews all docs and comments via PR.
- Next meeting: confirm the date; decide name, tech stack, fresh build vs reuse.

## 2026-10-06 – Marcus – AI session

**What changed**
- Team member name corrected to Naayi.
- Added `docs/design/` with the Claude Design prompt and the rules for storing design links and exports.
- Pull request #1 opened for the whole scaffolding.

**Open points / next**
- Run the prompt in Claude Design, store the link and exports in `docs/design/`.
- Team reviews PR #1.

## 2026-10-06 – Marcus – AI session

**What changed**
- Design round one from Claude Design added 1:1 under `docs/design/round-one/` (HTML export) with PNG renders in `exports/`.
- `docs/design/round-one-decisions.md`: the 20 decisions the design made, as proposals with the team question on each, plus the differences to the app sketch (onboarding and state screens added, queue board lives inside Today).
- App sketch, docs index, README and the sketch page link to the design. Three new Phase 0 to-dos, one new idea.

**Open points / next**
- Team confirms or overturns the design decisions (to-do in Phase 0).
- Next design round only via a new Claude Design run from `claude-design-prompt.md`; never edit the export by hand.

## 2026-10-06 – Marcus – AI session

**What changed**
- GitHub Pages enabled by Marcus (branch `main`, folder `/`). Site: https://mdbeatzxf.github.io/project-next/
- Removed the Actions-based Pages workflow again; the branch deployment makes it redundant. Links in README, docs index, CONTRIBUTING and the design README point to the live URLs.

**Open points / next**
- Team review of the docs and the design decisions before the next meeting.
