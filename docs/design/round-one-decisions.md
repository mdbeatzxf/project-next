# Design round one: decisions to confirm

Purpose: the design in `round-one/` made decisions where the brief was silent. They are listed here, taken from page 05 of the export, so the team can confirm or overturn each one. Status of every item: **proposal** until the team decides. Confirmed items move into `../vision.md` or `../app-sketch.md`; overturned items go back into the next Claude Design run via `claude-design-prompt.md`.

| # | Area | Decision in the design | Question for the team | Team answer |
|---|---|---|---|---|
| 01 | Visual system | Neutral style for now: black, white, greys, Geist, 12 px corners. Blue for action and selection, red for decline and "You're next". | When the name is chosen, does the brand colour replace blue, or sit next to it? | |
| 02 | Visual system | "You're next" turns the whole queue screen red because it is the one moment the Client must act. | Is red right here, or does it read as an error? Alternative: blue field. | |
| 03 | Visual system | Photos show in full colour; placeholders mark where they go. | Who supplies the first real photos for the example Providers? | |
| 04 | Visual system | Dark is default for the app; light is a full alternative. | Should the Provider dashboard default to light, since shops are often bright? | |
| 05 | Onboarding profile | New step 3 asks: cuts for (Men's, Women's, Kids, No preference), hair type, specialists wanted, styles. All optional, editable in Profile. | Use it only to sort results, or also to hide non-matching Providers? | |
| 06 | Onboarding profile | We ask hair type and "specialists in" (African hair, Turkish barber, ...) instead of origin. Ethnic origin is special-category data under DSGVO Art. 9. | Legal check: is the specialist preference fine without explicit consent? | |
| 07 | Onboarding profile | Shops never see these answers. | Would Providers benefit from seeing hair type before a booking (e.g. braids length)? | |
| 08 | Client app | Queue join requires a service choice so the shop can plan; Stylist is optional. | Do shops want to restrict the queue to certain services (no braids by walk-in)? | |
| 09 | Client app | A client may be in one queue at a time and must be within ~15 min walk (soft hint, not enforced). | Enforce distance with location, or trust? | |
| 10 | Client app | Free cancellation until 2 h before; no fee in v1 because there is no payment. | What happens after repeated no-shows? Warning, then block from bookings at that Provider? | |
| 11 | Client app | At the desk the Client says their display name. No codes or QR. | Is a name enough when two Yusufs are in the queue? Add a 2-digit number? | |
| 12 | Client app | Mobile Providers take requests, not instant bookings, and show "from" prices. | Who sets the final price for braids, and when does the Client see it? | |
| 13 | Client app | Reviews only after a booking or queue visit marked Done by the Provider. | Can Providers reply to reviews? Can they report one? | |
| 14 | Provider dashboard | Next calls the first person to the first free Stylist; Skip moves them one place down, not to the end. | Should Skip ask why (not here, wrong service) to feed the wait estimate? | |
| 15 | Provider dashboard | Wait estimate = people ahead × average service time of their chosen services, per free chair. | Is the dashboard allowed to show this estimate to Clients from day one, or only after a week of data? | |
| 16 | Provider dashboard | Verification needs an ID plus a shop photo; business registration is optional. | Legal check: what does the platform need to list unregistered Providers in DE? | |
| 17 | Provider dashboard | Booking requests auto-decline after 24 h. | Shorter for same-day requests? | |
| 18 | Scope and handover | Frame names follow the brief; `docs/app-sketch.md` was not available in Claude Design. | Confirmed below: names match, with two differences. | see below |
| 19 | Scope and handover | Exports: PNG per page and the flows page are produced from these files. | Folder layout under `docs/design/`: one folder per round (`round-one/`), renders in `round-one/exports/`. | done |
| 20 | Scope and handover | Platform admin is out of scope; Stats is marked Later. | Which stats does a Provider need in v1, if any? | |

## Differences to `../app-sketch.md`

Checked after the export, by comparing the frame lists with the screen tables in the sketch.

- **Client onboarding** (4 screens plus login) and **empty / loading / error states** are frames in the design. The sketch tables did not list them as screens. The sketch now does.
- **Queue board** is not a separate provider screen in the design. The live queue with Next, Skip, Done and "add walk-in" lives inside **Today**. The sketch now says so.
- Everything else matches: Home / Search with map, Provider profile, booking as a five-step sheet, Queue status with states, My bookings, Review, Profile and settings; Onboarding wizard, Today, Calendar, Services and prices, Portfolio, Stylists, Settings and verification, Stats (later).
- New in the design and not yet in the vision: the **"About your hair"** onboarding step (decisions 05 to 07). Treat as a proposal.
