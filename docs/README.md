# Docs index

Purpose: index of everything in `docs/`, with the reading order for newcomers.

## Reading order for newcomers

1. [`../CONTRIBUTING.md`](../CONTRIBUTING.md) – how we work together.
2. [`vision.md`](vision.md) – what we build and why.
3. [`meetings/2026-09-kickoff.md`](meetings/2026-09-kickoff.md) – where the vision comes from.
4. [`app-sketch.md`](app-sketch.md) – roles, flows, screens, architecture, data model, MVP scope.
5. [`index.html`](index.html) – the same sketch as an interactive page. Live at https://mdbeatzxf.github.io/project-next/docs/index.html (GitHub Pages).
6. [`design/round-one/`](design/round-one/) – the UI design (Claude Design export) and [`design/round-one-decisions.md`](design/round-one-decisions.md) – what to confirm.
7. [`decisions/0001-tech-stack.md`](decisions/0001-tech-stack.md) – the proposed tech stack.
8. [`todo.md`](todo.md) – what is next and who owns it.
9. [`log.md`](log.md) – the last entries, to see what happened recently.

## All docs

| File | What it is |
|---|---|
| `vision.md` | Product vision: problem, solution, roles, business model, open questions. |
| `app-sketch.md` | App sketch: roles, flows, screens, architecture, data model, MVP vs later. Mermaid diagrams, GitHub renders them. |
| `index.html` | Interactive version of the app sketch. Self-contained, GitHub Pages-ready. |
| `ideas.md` | Idea backlog. Anyone adds via PR. |
| `todo.md` | To-do list with owners, grouped by phase. |
| `log.md` | Append-only work log. Every session, human or AI, adds one entry at the end. |
| `meetings/` | Meeting notes, one file per meeting: `YYYY-MM-DD-topic.md`. |
| `meetings/2026-09-kickoff.md` | Kickoff meeting summary: what was said, advice, decisions, next steps. |
| `decisions/README.md` | How ADRs (architecture decision records) work. |
| `decisions/0000-template.md` | ADR template. |
| `decisions/0001-tech-stack.md` | Tech stack proposal. Status: proposed. |
| `design/README.md` | Where UI designs live, how they link back to the sketch. |
| `design/claude-design-prompt.md` | The prompt we use in Claude Design to produce the UI. |
| `design/round-one/` | Design round one, exported 1:1 from Claude Design: design system, Client app, Provider dashboard, flows, prototype. PNG renders in `exports/`. |
| `design/round-one-decisions.md` | The 20 decisions the design made where the brief was silent, with the question for the team on each. Status: proposal. |

## Related files outside `docs/`

| File | What it is |
|---|---|
| `../README.md` | Short project overview. |
| `../CLAUDE.md` | Instructions read automatically by AI coding sessions. |
| `../CONTRIBUTING.md` | Human guidelines: branches, commits, PRs, docs rules, AI sessions, meetings. |
| `../.github/` | Issue templates (`idea.md`, `todo.md`) and the PR template. |
