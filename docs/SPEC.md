# Orca Keel landing page: specification

One static page, `site/index.html`, for the household, with the installer's layer one level down. The current creative candidate is described in `WORKING_RECORD.md` (2026-10-23); publication follows Jason's acceptance and merge. Content follows the approved Orca brand kit and existing public product description.

## Sections, in order

| Section | Carries |
| --- | --- |
| Header | Desktop sticky bar with the keel line, Paper head on Depth tile, lowercase lockup, section links and “In development” status. Static at 760 px and below. A keyboard skip link precedes it. |
| Hero | “The household computer”; the mental-load benefit; what Keel is; the phone setup line above “Where it stands” and “See how it works”. The illustrative household record and box form one portrait: Paper record, Harbor wall, Shallows shelf, Ink box and Shallows seal, Amber light. Caption labels it as illustration and invented examples. A short strip names record ownership, explicitly allowed actions and local reminders. |
| How it works | Three steps: capture a letter/email/spoken note into Daybook; understand the matter/deadline/next action; give a specific grant. Sources: the previous public page and kit voice sheet. |
| For the household | Daybook's calendar, reminders, notes and ideas. An illustrative water-bill matter keeps source, amount and grant together. The grant's purpose, cap and expiry are separately legible. Plain files on the household's drive. Below: model choice (Claude, ChatGPT or another provider), limited per-job disclosure under a grant, no local inference, record/deadlines/reminders independent of a model. |
| For the installer | The second Depth band. Specific grants and traceable actions; no shell for routines or third-party skill store at launch; local filing/reminders/deadlines; planned rollback and backup; press-to-listen and phone pairing with no public ports. Diamond Dog's existing mark and landing-page link explain the underlying limits. |
| In the carton | The box, power cord, one card and backup drive. Setup remains about fifteen minutes; the product is in development. No unmeasured electricity comparison. |
| Where it stands | Built in one house first; intended-product status; no dates or prices. The existing waiting-list link opens a public GitHub issue template, with the public/account-required disclosure beside it. |
| Footer | Ink ground, Shallows lockup, studio origin, sibling landing pages and the GitHub organisation. |

## Presentation rules

- The existing sea palette and two Depth bands remain. Paper and white are the light-mode page surfaces; Ink and dark surfaces serve dark mode. Shallows is never a page-wide wash. Amber marks the hardware light, the final period of each section headline, the development-status dot and the grant dot.
- Instrument Sans is the product voice; Newsreader is the record and long-copy voice. The hero's second sentence uses Newsreader as a deliberate editorial treatment. No new fonts.
- The content column is capped at 1248 px. At 760 px and below, paired sections stack and the header stops sticking. The hardware illustration uses content-driven height; its record stays clear of the box even when text wraps.
- Primary and secondary marks retain the approved geometry and colours. The icon exception allows the existing header/footer tiles. The separate favicon work is not part of this change.
- “Orca Keel” in standalone positions and the first running mention; “Keel” thereafter. The lockup stays lowercase with the kit spacing.
- Examples are synthetic, explicitly labelled, and not represented as shipped product screenshots. The page describes an in-development product, not verified implementation.
- Power-loss and failed-update guarantees are not absolute: explain local operation, planned rollback and the backup drive. No guessed performance, price, shipping date or production count.

## Runtime and boundaries

Static HTML/CSS only, no JavaScript, analytics, forms or embeds. Google Fonts remains the only runtime third party. Existing CSP, canonical URL, headers and deployment workflow are unchanged. The waiting list remains the Jason-approved GitHub issue template; no live household/product endpoint is linked.

Photography, product functionality, signup infrastructure, prices, domain/hosting changes and new pages are outside this creative pass.
