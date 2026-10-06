# Vision: project-next

**Working title:** project-next
**In one line:** Booking & walk-in queue platform for barbers and hairdressers.

> Draft, based on the [kickoff meeting](meetings/2026-09-kickoff.md) in September 2026. Correct and extend via pull request. See also the [app sketch](app-sketch.md), the [ideas list](ideas.md) and the [to-do list](todo.md).

## What we are building

project-next is a booking and walk-in queue platform for barbers and hairdressers. It brings the delivery-app model to barbershops: a client finds a provider nearby, sees their work and prices, books a slot or joins the walk-in queue from their phone, and is notified when it is their turn. Providers get a simple dashboard for calendar, queue and portfolio. We start in German cities, focused on African and Turkish barbers and on mobile stylists. Cash stays the default. Online payment is never forced.

**Pitch:** "Lieferando for barbers and hairdressers" – the delivery-app model applied to barbershops.

## The problem

- Many barbershops and hairdressers have no structure for booking: personal phone numbers, WhatsApp or Instagram DMs, cash, no fixed slots. This is especially true for African and Turkish barbers in German cities and for mobile hairdressers and braiders who work from home or come to you.
- Clients walk in and do not know how long they will wait or how many people are ahead of them.
- Clients, especially Gen Z, do not want to hand out their phone number to book a haircut.
- Clients in a new city do not know where to find a barber for their hair type or style ("I want an African hairdresser, where can I go?").
- Existing platforms (Check24, eBay Kleinanzeigen, Google, Facebook Marketplace, generic booking tools) do not serve this niche. Barbers do not use them.
- Many barbers are not formally registered. A platform that forces online payment or invoicing will not get them on board.

## Who it is for

We use exactly these terms in docs, code and UI.

| Term | Meaning |
|---|---|
| **Platform** | Us. The admin side of the product. |
| **Provider** | The platform's customer: a barbershop, a hair salon, or an independent or mobile stylist (barber, braider, hairdresser). |
| **Stylist** | A person who does the hair. A provider has one or more stylists (staff); an independent stylist is both provider and stylist. |
| **Client** | The provider's customer: the end customer who gets the haircut. |

In short: Provider = the platform's customer, i.e. the shop or stylist; Client = the provider's customer.

## What makes it different

- **Walk-in queue with "people ahead of me".** The key feature. Join the queue remotely, see how many people are in front of you and the estimated wait, get notified when it is nearly your turn.
- **Niche focus.** African and Turkish barbers in German cities, plus mobile stylists and braiders. Generic booking tools ignore this group. We build for it first.
- **No forced online payment.** Cash is the default. Online payment is optional and comes later, if at all. Otherwise most providers will not join.
- **No phone numbers exchanged.** Clients and providers communicate through in-app notifications and messages.

## Core features

### Client side (mobile-first web app, native app later)

1. **Discover** providers nearby by city or address. Filter by specialty (African hair, Turkish barber, braids, locs, extensions, beard, women's/men's, kids), by "comes to your place" vs "you go there", price range, and "open now".
2. **Provider profile:** portfolio photos as evidence of their work, services with prices set by the provider, opening hours, location or service radius, ratings and reviews.
3. **Book an appointment:** pick a service or hairstyle, a stylist (optional), and a time slot.
4. **Walk-in queue:** join remotely, see position and estimated wait, get notified when it is nearly your turn.
5. **Booking management:** reminders, cancel or reschedule, history, favourites.
6. **Privacy:** no phone numbers exchanged; in-app notifications and messages.
7. **Payment:** cash by default. Optional PayPal, bank transfer or in-app payment later. Never required.

### Provider side (web dashboard)

1. **Onboarding:** profile, address or mobile service radius, specialties, photos, services with prices, opening hours, staff (stylists).
2. **Calendar:** appointments per stylist, block times, queue management ("next", "skip", "done"), live wait-time estimate.
3. **Booking requests:** accept or decline, no-show handling.
4. **Portfolio management:** upload photos, tag by style.
5. **Simple stats:** bookings per week, popular services, revenue estimate (cash tracked optionally).
6. **Verification badge:** ID or business verification. Trust comes from reviews and the portfolio.

### Platform side (admin)

- Provider verification, content moderation (photos, reviews), support, metrics, pricing configuration.

## Business model & go-to-market

- The product must be able to make money from the start, but it begins **free for providers** to seed usage.
- Revenue options: a **small fee per booking** (a haircut costs roughly 10–25 EUR depending on the city, so the fee must be small), later a **subscription for shops**, and **premium placement**.
- **Seed strategy:** pick a few cities, get key barbers to use it for free, and let the barber network spread it. One barber with influence changes everything.
- **Networking over marketing:** go to barbers and ask what their biggest hassle is. If 50 say the same thing, start there. First vendors, starting with a hairdresser the team knows, validate the idea.
- **Niche first, then expand:** barbers and hairdressers first, Germany first (the team is here). Later: other service categories and other countries. Nigeria and Ghana were mentioned as possible later markets with less competition.
- **Know the competition.** A niche with no structure can be won without big capital. A general marketplace in Germany cannot.

## Scope

### MVP (v0.1)

- Provider profile with services, prices and portfolio
- Client discovery by city and specialty
- Simple appointment booking (no payment)
- Walk-in queue with "people ahead of me"
- Notifications (push and email)
- Provider dashboard (calendar and queue)
- Reviews after a completed booking
- Admin verification of providers

### Later

- Online payment (optional)
- Multi-stylist scheduling optimisation
- Loyalty features
- Product sales (for example ordering hair extensions or colour)
- Other service categories, other countries
- Native apps
- WhatsApp integration

The technical approach (monorepo, web-first PWA, proposed stack, data model) is in the [app sketch](app-sketch.md). It is a proposal; the decision is pending.

## Open questions

- Name and brand. A naming brainstorm belongs in the [ideas list](ideas.md).
- Legal form, and who owns what.
- Time budget per person. All three have other commitments.
- Build fresh, or reuse Alex's existing general service-marketplace code (Service Scout)?
- First cities. First 5–10 pilot providers. Survey questions for barbers.
- Pricing model, and when to switch from free to paid.
- Legal: GDPR, Impressum, terms, handling providers who are not registered businesses, review law.
- Tech stack: proposal in the [app sketch](app-sketch.md) and [ADR-0001](decisions/0001-tech-stack.md), to be decided at the next meeting.
