# ADR-0001: Tech stack

Purpose: propose the technical stack for the MVP. Nothing here is decided yet.

- **Status:** PROPOSED
- **Date:** 2026-10-06

## Context

- Three part-time people. We need to move fast with little setup and little operations work.
- Web-first: Clients and Providers use a responsive web app (PWA). Native apps come later, if at all.
- The walk-in queue is the hero feature. Queue position and wait time must update on screen without a reload. That means realtime from day one.
- Providers upload portfolio photos. We need file storage.
- Discovery is by city/address and radius, so we need simple geo queries.
- Alex has an existing general service-marketplace codebase. Reusing it is one of the alternatives.

## Decision (proposal)

- **Monorepo** in this GitHub repo. Web-first (responsive PWA), native apps later.
- **Frontend:** TypeScript + React (Next.js) for the Client app and the Provider dashboard. Two apps or one app with roles, to be decided when we scaffold.
- **Backend:** Supabase – Postgres, Auth, Realtime (for the live queue), Storage (for photos). Chosen to move fast with three part-time people.
- **Notifications:** web push + email first. SMS/WhatsApp later.
- **Maps/geo:** PostGIS, or simple lat/lng + radius to start. Map tiles via OpenStreetMap/Leaflet.
- **Payments (later, optional):** Stripe or PayPal. Cash stays the default; online payment is never required.
- **Hosting:** Vercel (frontend) + Supabase. CI via GitHub Actions.

## Alternatives considered

- **Flutter for everything (mobile + web).** One codebase for native and web. Trade-off: a weaker fit for a web-first PWA and for pages that should be found via search. Still an option if the team prefers it.
- **Node/NestJS + Postgres + WebSockets.** Full control, no dependence on a backend-as-a-service vendor. Trade-off: more setup and operations work (auth, realtime, storage, hosting) for a three-person part-time team.
- **Reuse the existing marketplace code (Alex's codebase).** Could save time on generic marketplace parts. Open: fit for the booking and queue flows, its stack, and how much adapting is needed. This is a separate Phase 0 to-do (Alex + Marcus) and may change this ADR.

## Consequences

- Positive: little backend code at the start; auth, realtime and storage come built in; free tiers are enough for a pilot; one language (TypeScript) across the stack.
- Negative / risks: dependence on Supabase and Vercel; realtime and row-level security need care; a later move to a custom backend costs effort.
- Follow-ups: scaffold the monorepo only after this ADR is accepted; a data model ADR comes next; decide two apps vs one app with roles.

## To be decided at the next meeting

Accept this proposal, change it, or replace it. On acceptance, set the status to `accepted` and update the date. If the direction changes after acceptance, write ADR-0002 and mark this one superseded.
