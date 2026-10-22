# Orca Keel landing page: specification

One static page, `site/index.html`, for the family household, with the installer's layer one level down. Content follows the Orca brand brief (approved by Jason, October 21, 2026) and the voice sheet in `brand/kit/`.

## Sections, in order

| Section | Carries | Source |
| --- | --- | --- |
| Header | The head in Paper on a Depth tile + "orca keel" lockup, section links, the status "In development" | Kit lockups; sibling pages' candid status line |
| Hero | "The household computer" label, the one-line claim, the sub, a link to where it stands, the headline's period in Amber, the box drawn on a Depth panel: an Ink slab on two short feet, the head in Shallows on its front, one amber dot, a shadow for the dimension; the button in Depth | Brief §3, §6, §7 imagery placeholder; the sea, B-13; Amber, B-14; `brand/kit/scenes/` |
| How it works | The three claims: it keeps the record, it does only what you said, it keeps working | Voice sheet |
| Daybook | Label "For the household", headline "The book of the house, kept for you."; Daybook's house mark beside the paragraph, the name linked to daybook.orcasolutions.dev; what the app is, which models it works with (Claude, ChatGPT or another provider; cloud only, one task's worth, under a grant), an example matter with its grant | Voice sheet sample copy; plan docs 08 (R12, R13, R19) and OH7 |
| For the installer | The dark layer: "Not an agent with your passwords", seven plain limits (the last: no model runs on the box), and Diamond Dog as the layer that makes them hold, its mark beside the paragraph and the name linked to diamonddog.orcasolutions.dev | Brief §2, §3, §4 |
| In the carton | Four things: the box, the power cord, one card, the backup drive | Brief §8 |
| Where it stands | "Coming soon." Built in one house first; a waiting list will open; no units, dates, price or address | Jason, 2026-10-22: no promises, no blanks, email waits for Keel's own domain |
| Footer | "Made by Orca. It started with a spreadsheet." Links to Daybook, Diamond Dog, the GitHub organisation | Brief §6 |

## Rules

- Harbor palette, Instrument Sans for the product's voice, Newsreader for long copy. Tokens copied from `brand/kit/tokens/colors.css` into the page's `:root`. Light and dark themes; the installer's layer is Ink in both.
- One file, no JavaScript, no forms, no third parties except Google Fonts. The CSP meta tag says exactly that.
- Works at phone width without horizontal scroll; 1120 px column on desktop.
- "Orca Keel" in full in the title, metadata, carton, footer line and the first mention on the page; "Keel" alone afterwards. Never "Keel by Orca". The lockup is lowercase, "orca keel", set live in CSS: "orca" at 600, "keel" at 400, 0.16 em apart, tracking -0.03 em, the head 6 px from the word.
- The mark appears alone, as the head: in the lockup, the favicon and the footer. Never in a badge.
- Depth #11404B is the product's colour: the panel behind the box in both modes, the button, the head's tile in the header and the favicon, and the head on light grounds (the footer). On dark grounds (dark mode, the installer's layer) the lockup, the marks, the installer label and links are Shallows #D8E6E4. Neither is a page ground; the page stays Paper and Ink. Amber is the box's light plus one point per page, the headline's period (B-14).
- Every number on the page is invented and labelled as an example (the water bill). Nothing else is counted, dated or priced.
- Sibling marks (Daybook's house, Diamond Dog's dog) appear once each, 32 px, beside the paragraph that names the product, in that product's own colour rules: Daybook's blue-black, Diamond Dog in Paper on Ink.

## Not in scope

Photography, a form or list, prices, a second page, analytics, a domain. Each is an open task in WORKING_RECORD.md or a decision for Jason.
