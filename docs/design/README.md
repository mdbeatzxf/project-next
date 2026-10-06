# Design

Purpose: where UI design work lives and how it links back to the docs.

## Rules

- The source of truth for *what* the app does is `../vision.md` and `../app-sketch.md`. Design follows them; if a design changes a flow, update the sketch in the same PR.
- Designs are made in Claude Design (or Figma) from the prompt in `claude-design-prompt.md`. Keep that prompt current when the sketch changes.
- Each design round gets its own folder: `round-one/`, `round-two/`, ... with the 1:1 export from Claude Design and a `README.md`. Decisions the design made on its own go into `round-<n>-decisions.md` as proposals for the team.
- Store the link to the design file in the table below. Store exports (PNG 2x per screen, PDF per flow) under `exports/<YYYY-MM-DD>-<topic>/` so everyone, including AI sessions, can see the current state without opening the design tool.
- Name frames and exports exactly like the screens in `../app-sketch.md` (for example `client-queue-status.png`, `provider-today.png`).
- Open design questions go to `../ideas.md` or `../todo.md`, not into the design file only.

## Design files

| Date | What | Tool | Link | Exports |
|---|---|---|---|---|
| 2026-10-06 | Round one: design system, 32 Client frames, 12 Provider frames, flows, prototype. From `claude-design-prompt.md`. Decisions to confirm: `round-one-decisions.md` | Claude Design | https://claude.ai/design/p/8793adfc-8910-4925-87a8-7667aed3dc07?via=share | `round-one/` (HTML export, 1:1, overview in `index.html`) and `round-one/exports/` (PNG per page). Live: https://mdbeatzxf.github.io/project-next/docs/design/round-one/ |
