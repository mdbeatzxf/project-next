# Claude Design prompt

Purpose: the prompt we paste into Claude Design to get real UI designs for the Client app and the Provider dashboard. Keep it in sync with `../vision.md` and `../app-sketch.md`. Exports and the link to the design file go into this folder (see `README.md`).

---

## Prompt (copy everything below the line)

You are designing the first real UI for **project-next** (working title, no brand name yet): a booking and walk-in queue platform for barbers and hairdressers. Think "Lieferando for barbers": a client finds a barber nearby, sees their work and prices, books a slot or joins the walk-in queue from their phone, and gets a push when it is nearly their turn. Start in German cities with African and Turkish barbers and mobile stylists (braiders, home hairdressers). Cash stays the default; online payment is never forced; no phone numbers are exchanged.

### Roles (use exactly these words in the UI and in layer names)

- **Client**: the person who gets the haircut. Uses the mobile app.
- **Provider**: our customer: a barbershop, a salon, or an independent or mobile stylist. Uses the dashboard.
- **Stylist**: a person who cuts hair at a Provider. A one-person Provider is their own Stylist.
- **Platform**: us, the admin side. Not in scope for this design round.

### Design direction

- Mobile-first, made for the street: big tap targets, readable in sunlight, fast to scan while walking.
- Audience is young and multicultural (Gen Z and millennials in Berlin, Cologne, Frankfurt, Saarbrücken). The look should feel like a good barbershop: confident, warm, a bit raw, proud of craft. Not a clinical SaaS tool, not a beauty-spa pastel look.
- One bold accent colour on a dark-neutral or warm-neutral base. Strong typographic hierarchy. Photos of real haircuts are the hero content everywhere, so the UI should get out of their way.
- Light and dark mode, dark first.
- Same design language for the Provider dashboard, but calmer and denser: it runs all day on a tablet or laptop next to the chair.
- Provide a small design system first (colour tokens, type scale, spacing, buttons, chips, cards, list rows, bottom sheet, toasts, status pills), then build every screen from it.
- German locale: prices as "15 €", 24-hour times, dates like "Fr 10.10.".
- Accessibility: contrast AA, min 44 px tap targets, visible focus, no colour-only states.

### Client app: screens to design (iPhone 390 × 844)

1. **Onboarding** (3 short screens): what it does, choose city, allow notifications. Login via email or Apple/Google. No phone number required.
2. **Home / Search**: location field ("Berlin, Neukölln"), search, filter chips (specialty: African hair, Turkish barber, braids, locs, extensions, beard, women's, men's, kids; "comes to you"; "open now"; price), result cards with photo, name, specialty tags, rating, distance, price from, and a live queue hint ("3 waiting · ~35 min"). Map toggle.
3. **Provider profile**: cover photo, verified badge, name, specialties, rating, address or "mobile · comes to you · 10 km", opening hours, portfolio grid (photos tagged by style), services with duration and price, stylists, reviews. Two primary actions pinned at the bottom: **Book** and **Join queue**.
4. **Booking flow** (bottom sheets or steps): choose service, optional stylist, day and time slot, note to the shop, review and confirm. State the payment clearly: "Pay cash at the shop. No phone number shared." Confirmation screen with add-to-calendar.
5. **Queue status**: the hero screen. Big position number, "people ahead of you", estimated wait, "your turn around 14:40", live status (waiting, you're next, serving), address and walking time, **Leave queue**. Also design the push notification and the lock-screen live activity for "You're next".
6. **My bookings**: upcoming and past, cancel or reschedule, rebook in one tap, favourites.
7. **Review**: 1 to 5 stars, text, optional photo of the result, only after a done booking.
8. **Profile and settings**: display name, home city, notifications, delete account.
9. **Empty, loading and error states** for search, queue and bookings.

### Provider dashboard: screens to design (desktop 1440 × 900 and tablet 1024 × 768)

1. **Onboarding wizard**: Provider type (shop, independent, mobile), address or service radius, specialties, services and prices, opening hours, photos, stylists, verification upload. Ask for the minimum; many Providers are not registered businesses.
2. **Today**: the one screen for a working day. Calendar per Stylist on the left, live walk-in queue on the right with big **Next**, **Skip**, **Done** buttons, "now serving", "add walk-in by name", live wait estimate. Must work with one hand on a tablet.
3. **Calendar**: week view per Stylist, block times, booking requests to accept or decline, no-show marking.
4. **Services and prices**: table with name, category, duration, price, "at client's home" flag.
5. **Portfolio**: upload, tag by style and Stylist, reorder.
6. **Stylists**: add, deactivate, specialties, working hours.
7. **Settings and verification**: profile, verification status, notifications.
8. Optional, mark as "later": **Stats** with bookings per week, no-shows, top services, revenue estimate.

### Example data (use this, mark nothing as real)

Providers: "Kings Cuts Neukölln" (Turkish barber, fade, beard, 4.8 ★, 132 reviews, Sonnenallee 112), "Ama's Braids" (mobile, braids, locs, comes to you, from 60 €), "Salon Nadia" (women's, extensions, colour), "Afro Lounge" (African hair, kids). Services: Fade 30 min 15 €, Beard trim 15 min 8 €, Fade + beard 45 min 20 €, Kids cut 20 min 12 €, Braids 120 min from 60 €. Stylists: Murat, Deniz, Ama. Queue: position 3, 2 ahead, ~25 min.

### Deliverables and how to organise the file

- Pages in this order: **00 Cover and direction** (3 mood directions, pick one and say why), **01 Design system**, **02 Client app**, **03 Provider dashboard**, **04 Flows** (client: discover → book or join queue → notified → visit → review; provider: onboarding → Today → done), **05 Open questions for the team**.
- Name frames with the screen names above so they match `docs/app-sketch.md` in our repo.
- Make the client app flow clickable as a prototype.
- Export every screen as PNG (2x) and the flows as one PDF, so we can store them in the repo under `docs/design/exports/`.
- Where the briefing is silent, make a decision and list it on page 05 instead of asking first. Do not invent a brand name; use "project-next" as placeholder wordmark and propose three naming directions on page 00 if you want.
