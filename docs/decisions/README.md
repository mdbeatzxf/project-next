# Architecture Decision Records (ADRs)

Purpose: how we record decisions, so that they are never only in chat, WhatsApp or a meeting.

## Rules

- One file per decision: `NNNN-short-title.md`, numbered in order (`0001`, `0002`, ...). `0000-template.md` is the template.
- Status is one of `proposed`, `accepted`, `superseded`.
- A new ADR starts as `proposed`. It becomes `accepted` when the team agrees, in the weekly sync or by PR approval from the others. Record the date of acceptance.
- Never edit an accepted ADR. If the decision changes, write a new ADR and set the old one to `superseded by ADR-NNNN`.
- Typo and link fixes are fine. Changes to the decision itself are not.
- Every architectural or product-structure decision gets an ADR: tech stack, data model changes, hosting, payment approach, and so on.

## How to write one

1. Copy `0000-template.md` to `NNNN-short-title.md` with the next free number.
2. Fill in Context, Decision, Alternatives considered, Consequences. Keep it to facts.
3. Open a PR on a branch `docs/adr-NNNN-short-title`.
4. Add the ADR to the list below.

## List

| # | Title | Status | Date |
|---|---|---|---|
| 0001 | Tech stack | proposed | 2026-10-06 |
