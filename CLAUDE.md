# CLAUDE.md – instructions for Claude Code sessions

project-next is a booking and walk-in queue platform for barbers and hairdressers (working title, Phase 0: concept & planning).
Providers (shops, salons, independent or mobile stylists, each with one or more Stylists) offer services; Clients discover them, book a slot or join the walk-in queue; the Platform (us) verifies Providers and runs the admin side.

## Before doing anything, read in this order

1. `CONTRIBUTING.md`
2. `docs/README.md`
3. `docs/vision.md`
4. `docs/todo.md`
5. The last 3 entries of `docs/log.md`

## Working rules

- Work on a branch named `feat/...`, `docs/...` or `fix/...`. Never commit directly to `main`.
- Small commits. Conventional-commit style messages: `docs: ...`, `feat: ...`, `fix: ...`, `chore: ...`. Imperative, English.
- Everything in English: docs, code, comments, commit messages, file names.
- Keep docs in sync with code. If you change behaviour, update the doc that describes it in the same PR.
- Every architectural decision becomes an ADR in `docs/decisions/` (copy `0000-template.md`, take the next free number, status `proposed`).
- New ideas go to `docs/ideas.md`. New tasks go to `docs/todo.md`.
- Never invent product decisions that are not in the docs. Ask, or add them marked as "proposal".
- Use the role terms exactly: Platform, Provider, Stylist, Client.
- No secrets in the repo. Use `.env` files; they are listed in `.gitignore`.

## At the end of every session

1. Append an entry to `docs/log.md` (date, who, session type human/AI, what changed, open points).
2. Update the checkboxes in `docs/todo.md`.
3. Push the branch. Open a PR if the work is done.

## Tech stack

The stack is only PROPOSED until the team accepts it. See `docs/decisions/0001-tech-stack.md`.
Do not add dependencies or scaffold apps as if it were decided.
