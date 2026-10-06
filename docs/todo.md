# To-do

Purpose: the shared task list with owners, grouped by phase. Anyone adds via PR.

## How to add a to-do

1. Copy a line in this format: `- [ ] Task – owner: Name` (use `open` if nobody owns it yet).
2. Put it under the right phase, at the bottom of that list.
3. Open a PR. Owners are confirmed in the weekly sync.
4. Only the owner ticks a box. Mention what was done in `log.md`.
5. Convert a to-do into a GitHub Issue (template `To-do`) when it needs discussion, has more than a few steps, or an AI session will work on it. Link it from the line, e.g. `(#12)`.

Ticked items stay in their phase. We clean up at the end of each phase.

## Phase 0: concept & planning (now)

- [ ] Confirm the follow-up meeting date – owner: Marcus
- [ ] Everyone reads the docs and comments via PR – owner: all
- [ ] Decide the product name – owner: all – see idea 2 in `ideas.md`
- [ ] Decide the tech stack: accept or change ADR-0001 – owner: all – `decisions/0001-tech-stack.md`
- [ ] Decide reuse of the existing marketplace code vs fresh build – owner: Alex + Marcus
- [ ] List 5–10 pilot barbers/stylists and contact them – owner: all – Marcus has one hairdresser contact
- [ ] Write the barber survey questions – owner: open – see idea 3 in `ideas.md`
- [ ] Pick first city/cities – owner: all
- [ ] Legal basics check: GDPR, Impressum, terms, Providers who are not registered businesses – owner: open
- [ ] Confirm or overturn the 20 decisions from design round one – owner: all – `design/round-one-decisions.md`
- [ ] Legal check: hair type and "specialists in" preference in onboarding vs DSGVO Art. 9 – owner: open – decision 06 in `design/round-one-decisions.md`
- [ ] Decide red vs blue for the "You're next" queue state – owner: all – decision 02 in `design/round-one-decisions.md`

## Phase 1: MVP build

Starts after the Phase 0 decisions. Scope: MVP section in `app-sketch.md`.

- [ ] Repo scaffolding (monorepo, `apps/`, `packages/`, CI) – owner: open
- [ ] Data model – owner: open
- [ ] Provider onboarding (profile, address or radius, specialties, photos, services + prices, opening hours, Stylists) – owner: open
- [ ] Discovery (by city, specialty, mobile vs on-site, price, open now) – owner: open
- [ ] Booking (service, optional Stylist, time slot; accept/decline; cancel/reschedule) – owner: open
- [ ] Walk-in queue (join remotely, position, "people ahead of me", wait estimate, next/skip/done) – owner: open
- [ ] Notifications (web push + email) – owner: open
- [ ] Provider dashboard (calendar + queue) – owner: open
- [ ] Reviews after a done booking – owner: open
- [ ] Admin verification of Providers – owner: open

## Phase 2: pilot

- [ ] Pilot with the first Providers – owner: open
- [ ] Feedback loop with pilot Providers and Clients – owner: open
- [ ] Pricing switch: decide when and how to move from free to paid – owner: open
