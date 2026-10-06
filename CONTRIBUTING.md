# Contributing to project-next

Purpose: how the three of us (Marcus, Alex, Nehi) work together in this repo. Read it once, come back when unsure.

## Why we document

Three people, three PCs, and each of us also runs AI coding sessions on this repo. Nobody can see what the others did on their machine, in chat or in their head. So the rule is simple: **whatever is not in the repo does not exist.** Decisions, ideas, tasks, meeting outcomes and session results all land here, in writing, in English.

## Where things live

| Content | File |
|---|---|
| Product vision | `docs/vision.md` |
| Meeting notes | `docs/meetings/YYYY-MM-DD-topic.md` |
| Decisions (ADRs) | `docs/decisions/NNNN-short-title.md` |
| Ideas | `docs/ideas.md` |
| To-dos | `docs/todo.md` |
| Work log | `docs/log.md` |
| App sketch (roles, flows, screens, data model) | `docs/app-sketch.md`, interactive version in `docs/index.html` |
| Code (later) | `apps/` (deployable apps), `packages/` (shared code) |
| Index of all docs | `docs/README.md` |

## Branching & PRs

- `main` is protected. Nobody pushes to it directly, neither humans nor AI sessions.
- Branch prefixes: `feat/` (features), `docs/` (documentation), `fix/` (bug fixes), `chore/` (tooling, config). Example: `docs/update-vision`.
- One topic per PR. Keep a PR small enough to review in ten minutes.
- One other person reviews and approves before merge.
- Squash-merge. The squash commit message follows the commit rules below.
- Delete the branch after merge.
- Fill in the PR template (`.github/pull_request_template.md`).

## Commit messages

Conventional commits: `type: short description`. Imperative mood, English, no trailing period.

Types: `docs:`, `feat:`, `fix:`, `chore:`.

Examples:

```
docs: add kickoff meeting summary
feat: add provider onboarding form
fix: correct queue position after a skip
chore: add editorconfig and gitignore
```

Small commits. One logical change per commit.

## Documentation rules

- Every doc starts with a one-line purpose statement at the top.
- Dates are written as `YYYY-MM-DD`.
- Decisions are never only in chat, WhatsApp or a meeting. They go into an ADR in `docs/decisions/` or, for small things, into the meeting notes and `docs/todo.md`.
- Meeting notes go to `docs/meetings/YYYY-MM-DD-topic.md`. Use the template at the bottom of this file.
- Anything undecided is marked "proposal". Never write a proposal as if it were agreed.
- Use the role terms consistently: Platform (us), Provider (shop, salon, independent or mobile stylist), Stylist (staff of a Provider), Client (end customer).

## Ideas & to-dos

**Ideas** go to `docs/ideas.md`. Copy the template entry, add yours at the bottom, open a PR. Status starts as `new`. We move it to `discussing`, `accepted` or `parked` in the weekly sync.

**To-dos** go to `docs/todo.md`. Copy a checkbox line, put it under the right phase, set an owner or `open`. Only the owner ticks a box.

**Owners:** whoever adds a to-do can propose an owner. Owners are confirmed in the weekly sync. Do not assign work to someone without asking them.

**GitHub Issues:** convert a to-do into an issue when it needs discussion, has more than a few steps, or an AI session will work on it. Use the templates in `.github/ISSUE_TEMPLATE/` (`idea.md`, `todo.md`) and link the issue from the to-do line.

## Working with AI coding sessions

We use Claude Code (local and cloud sessions) and may use similar tools. Rules:

- Each session reads `CLAUDE.md` automatically. Keep that file short and current.
- Start a session with a clear task that references a to-do or issue. "Implement the queue join flow, Phase 1 in docs/todo.md" is good. "Improve the app" is not.
- Review the AI's diff before merging, like any other PR. You are responsible for what you merge.
- Never let an AI session push to `main`. Sessions work on branches and open PRs.
- Every AI session ends with an entry in `docs/log.md`. If the session forgot, add it yourself.
- Keep secrets out of the repo. Use `.env` files; they are listed in `.gitignore`. Never paste keys into prompts or files that end up in commits.
- If an AI session proposes a product or architecture decision, it goes into an ADR or `docs/ideas.md` as "proposal", not straight into code.

## Meeting rhythm

- Short weekly sync, 30 minutes max. Day and time: to be fixed.
- Notes go to `docs/meetings/` the same day.
- Three fixed agenda points:
  1. Progress since last time.
  2. Decisions needed.
  3. Next to-dos and owners.

## Language

Everything in the repo is in English: docs, code, comments, commits, file names. German is fine in chat and in PR comments. This choice can be revisited.

## Meeting notes template

Copy this into `docs/meetings/YYYY-MM-DD-topic.md`.

```markdown
# Meeting YYYY-MM-DD – Topic

Purpose: one line.

- **Date:** YYYY-MM-DD
- **Attendees:** names
- **Notes by:** name

## Progress since last time

- ...

## Decisions needed / taken

- Decision: ... (link the ADR if there is one)
- Proposal: ... (not yet decided)

## Next to-dos

- [ ] ... – owner: name

## Open points

- ...
```
