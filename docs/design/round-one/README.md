# Design round one (Claude Design export)

Purpose: the first UI design round, exported 1:1 from Claude Design. Do not edit these files by hand; change the design in Claude Design and re-export.

- Source: https://claude.ai/design/p/8793adfc-8910-4925-87a8-7667aed3dc07?via=share
- Exported: 2026-10-06
- Made from: `../claude-design-prompt.md`

## How to open

Start at `index.html`, the overview of all pages with thumbnails and the prototype. Live via GitHub Pages: https://mdbeatzxf.github.io/project-next/docs/design/round-one/

The pages link to each other. They load React and Babel from unpkg.com at runtime, so you need internet access.

| Page | What |
|---|---|
| `index.html` | Overview of all pages with thumbnails and the prototype (added by us, not part of the export) |
| `00 Cover and Direction.dc.html` | Cover, visual direction, colour roles |
| `01 Design System.dc.html` | Tokens, type, parts |
| `02 Client App.dc.html` | 32 client frames, iPhone 390 × 844, dark first plus light samples |
| `03 Provider Dashboard.dc.html` | 12 provider frames, desktop 1440 × 900 and tablet 1024 × 768 |
| `04 Flows.dc.html` | Client book a slot, client join the queue, provider first day |
| `05 Open Questions.dc.html` | Decisions made in the design and the question for the team on each |
| `Client Prototype.dc.html` | Click-through prototype of the client app |
| `Client Screen.dc.html`, `Provider Screen.dc.html` | The live screen components used by the pages above |
| `pn.css`, `icons.js`, `support.js`, `.thumbnail` | Shared styles, icons, runtime and preview image |

PNG renders of every page are in `exports/` so they can be viewed on GitHub without a browser runtime; `exports/thumbs/` holds the small previews used by `index.html`.
