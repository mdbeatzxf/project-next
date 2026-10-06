# Kickoff meeting – late September 2026

> This summary was written from an auto-generated, partly garbled recording of a mixed English/German conversation.
> Attributions and details may be imperfect; where something was unclear in the recording, it says so.
> Everyone who was there: please correct and extend this summary via pull request.

**When:** late September 2026, in person. The exact date is unclear in the recording.

## Participants

| Name | Role in this meeting |
|---|---|
| Marcus | Initiated and presented the idea. Owner of this repo. |
| Alex | Took part in the discussion. |
| Nehi | Took part in the discussion. |

## The idea in one paragraph

Marcus presented the idea as the delivery-app model applied to barbers and hairdressers: "Lieferando for barbers and hairdressers". A client opens the app, finds a barber or hairdresser nearby who can do their hair, sees photos and prices, and books a slot or joins the walk-in queue from their phone. The provider gets a simple tool for bookings and the queue. Marcus called these two levels "the customer, i.e. the shop or the hairdresser" and "the sub-customer, the shop's clients"; in the repo they are **Provider** and **Client** (see the [vision](../vision.md)). Cash stays the default. No brand name was chosen.

## Problems identified

- Many barbershops and hairdressers have no booking structure: personal phone numbers, WhatsApp or Instagram DMs, cash, no fixed slots. Especially true for African and Turkish barbers in German cities and for mobile hairdressers and braiders.
- Walk-in clients do not know how long they will wait or how many people are ahead of them.
- Clients, especially Gen Z, do not want to give out their phone number for a haircut.
- Clients in a new city do not know where to find a barber for their hair type ("I want an African hairdresser, where can I go?").
- Existing platforms (Check24, eBay Kleinanzeigen, Google, Facebook Marketplace, generic booking tools) do not serve this niche. Barbers do not use them.
- Many barbers are not formally registered. Forcing online payment or invoicing would keep them off the platform.

## Features discussed

The group saw the walk-in queue as the key feature.

### Client side

- Discover providers by city or address; filter by specialty (African hair, Turkish barber, braids, locs, extensions, beard, women's/men's, kids), "comes to you" vs "you go there", price range, open now.
- Provider profile: portfolio photos as "evidence", services with prices set by the provider, opening hours, location or radius, reviews.
- Book an appointment: service, stylist (optional), time slot.
- Walk-in queue: join remotely, see "how many people are in front of me" and the estimated wait, get notified when it is nearly your turn.
- Reminders, cancel or reschedule, history, favourites. No phone numbers exchanged; in-app messages instead.
- Cash by default. PayPal, bank transfer or in-app payment as a later option, never required.

### Provider side

- Onboarding: profile, address or mobile radius, specialties, photos, services and prices, opening hours, staff (stylists).
- Calendar per stylist, block times, queue management ("next", "skip", "done"), live wait-time estimate.
- Accept or decline booking requests; no-show handling.
- Portfolio management with style tags.
- Simple stats: bookings per week, popular services, revenue estimate (cash tracked optionally).
- Verification badge; trust through reviews and portfolio.

Mentioned for later: ordering hair extensions or colour through the app.

## Business model & go-to-market advice

- The platform should make money "from the get-go", but start free for the first barbers in a few cities to seed usage.
- A haircut costs roughly 10–25 EUR depending on the city (15 EUR was the example), so a per-booking fee must be small. A subscription for shops and premium placement are later options.
- Get key barbers on board for free and let the barber network spread it: "one barber with influence changes everything".
- "Networking over marketing": go to barbers and ask what their biggest hassle is. If 50 say the same thing, start there.
- A first vendor contact exists (a hairdresser the team knows); use the first vendors to validate.
- Know your competition. A niche with no structure can be won without big capital; a general marketplace in Germany cannot.
- Niche first: barbers and hairdressers, Germany first because the team is here. Later other services and countries; Nigeria and Ghana were mentioned as possible markets with less competition.

## Context

All three have other commitments and limited time. Alex already has a general service-marketplace codebase called Service Scout, aimed at a broader market than this project. Whether to reuse it or build fresh is an open decision.

## Decisions

- Alex and Marcus agreed to continue on this together. Nehi is involved.
- Cash is the default; online payment is never forced.
- Niche first (barbers and hairdressers), Germany first.
- A follow-up meeting was agreed (see next steps).
- This GitHub repo, working title "project-next", is the shared workspace.

## Open questions

- Name and brand; legal form; who owns what.
- Time budget per person. Marcus said he cannot pull this off alone.
- Build fresh, or reuse Alex's Service Scout code?
- First cities; first 5–10 pilot providers; survey questions for barbers.
- Pricing model, and when to switch from free to paid.
- Legal: GDPR, Impressum, terms, providers who are not registered businesses, review law.
- Tech stack: proposal in the [app sketch](../app-sketch.md) and [ADR-0001](../decisions/0001-tech-stack.md), to be decided at the next meeting.

## Next steps

| What | Who | When |
|---|---|---|
| Follow-up meeting: "next week Friday". The recording says "the 2nd"; date to be confirmed. | All | To be confirmed |
| Send an email with the follow-up date | Marcus | Before the meeting |
| Set up this GitHub repo as the shared workspace | Marcus | Done |
| Read the docs; add ideas to [ideas.md](../ideas.md) and to-dos to [todo.md](../todo.md) via PR | Everyone | Before the follow-up |
