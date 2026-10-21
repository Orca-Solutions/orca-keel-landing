# Orca Keel landing page: specification

One static page, `site/index.html`, for the family household, with the installer's layer one level down. Content follows the Orca brand brief (approved by Jason, October 21, 2026) and the voice sheet in `brand/kit/`.

## Sections, in order

| Section | Carries | Source |
| --- | --- | --- |
| Header | Head + "Orca Keel" lockup, section links, the status "In development" | Kit lockups; sibling pages' candid status line |
| Hero | "The household computer" label, the one-line claim, the sub, a link to where it stands, the flat Paper panel with the box as a dark slab and one amber dot | Brief §3, §6, §7 imagery placeholder |
| How it works | The three claims: it keeps the record, it does only what you said, it keeps working | Voice sheet |
| Daybook | What the app is, an example matter with its grant, a link to daybook.orcasolutions.dev | Voice sheet sample copy |
| For the installer | The dark layer: "Not an agent with your passwords" and six plain limits | Brief §3, §4 |
| In the carton | Four things: the box, the power cord, one card, the backup drive | Brief §8 |
| Where it stands | In development; `[UNITS]`, `[DATE]`, `[EMAIL]` placeholders; no price | Jason: no prices until the pilot |
| Footer | "Made by Orca. It started with a spreadsheet." Links to Daybook, Diamond Dog, the GitHub organisation | Brief §6 |

## Rules

- Harbor palette, Instrument Sans for the product's voice, Newsreader for long copy. Tokens copied from `brand/kit/tokens/colors.css` into the page's `:root`. Light and dark themes; the installer's layer is Ink in both.
- One file, no JavaScript, no forms, no third parties except Google Fonts. The CSP meta tag says exactly that.
- Works at phone width without horizontal scroll; 1120 px column on desktop.
- The mark appears alone, as the head: in the lockup, the favicon and the footer. Never in a badge.
- Every number on the page is either invented and labelled as an example (the water bill) or a placeholder in brackets.

## Not in scope

Photography, a form or list, prices, a second page, analytics, a domain. Each is an open task in WORKING_RECORD.md or a decision for Jason.
