# orca-keel-landing working record

Current state, open tasks, verification and review dispositions. Newest first.

## 2026-10-22: which models it works with

**State.** Jason asked for a brief mention, as Otto's page has, of how the box works with Claude, ChatGPT and the like. The Daybook section gains one paragraph: reading and drafting take a model, the box works with Claude, ChatGPT or another provider the household picks, each provider gets only the part of a matter the job needs under a grant, and the record, deadlines and reminders need no model. The installer's list gains a seventh limit: no model runs on the box. Both follow the plan set (doc 08 R12, R13, R19; doc 05 OH7, no local inference). Who pays for model use (own keys or a service) is open (doc 05 Q11), so the page does not say.

Jason also settled how the name is written (2026-10-22): "Orca Keel" in full where it stands alone or first appears on the page, "Keel" alone for every later mention and inside the product, never "Keel by Orca". Three later mentions on the page change to "Keel"; the rule is in CLAUDE.md and docs/SPEC.md.

**Verification.** Rendered with headless Chromium at 1280 px and 390 px in light and dark mode: no horizontal overflow, no console errors. Routine copy; author check only.

## 2026-10-22: GitHub Pages and the domain

**State.** Jason enabled GitHub Pages (Source: GitHub Actions) and set the custom domain `orcakeel.orcasolutions.dev`; the DNS check was in progress when this was written. This change adds the canonical URL and `og:url` to the page, `site/CNAME` so the domain survives a redeploy, and the agreed values in `docs/DEVOPS.md`. DNS for the domain is a CNAME to `orca-solutions.github.io` on the studio's Cloudflare zone, set by Jason; "Enforce HTTPS" can be ticked once GitHub has issued the certificate.

**Verification.** Author check of the three changed files. The deployed page is verified in the handoff record, not here.

## 2026-10-21: repository created

**State.** Jason decided the landing page gets its own public repository under a proprietary licence, separate from the Orca Keel code, so GitHub Pages can serve it without a Cloudflare project ([ADR-0001](docs/decisions/0001-own-public-repository.md)). The page was drafted from the landing board on the brand canvas and the final brand kit (name Orca Keel, Signal mark as the seal, Harbor palette, approved by Jason the same day), with the prices removed since pricing waits for the pilot. The brand kit was copied in from the Orca Keel plan set (`plans/orca-home/brand/kit/`, draft 0.2) without the studio's Signal source package or the internal brand brief. The operating documents were copied from the maintainer's project scaffold (policy v3.1.4, October 11, 2026) and filled in; its private companion guides stay Git-ignored in the local clone. Commits are in Jason's name with no agent attribution, at his instruction.

The page has the hero, the three claims, the Daybook section with an example matter and grant, the installer's dark layer, the carton, a "where it stands" section with placeholders, and the footer.

**Open tasks.**
- Record the first deployment in `docs/handoffs/` once the custom domain's DNS check passes and HTTPS is enforced.
- Jason replaces the `LICENSE` placeholder with the licence text he wants.
- Fill `[UNITS]` and `[DATE]` when they exist. The contact address is jason@orcasolutions.dev (Jason, 2026-10-22). Pricing stays off the page until the pilot.
- Photography, when there is some. Until then the hero shows the flat Paper panel with the box drawn as a dark slab and the single amber dot.

**Verification.** The page was rendered with headless Chromium at 1280 px and 390 px in light and dark mode before this push: no horizontal overflow, no console errors, both themes legible. No JavaScript, so nothing to syntax-check. The CSP meta tag allows only inline styles, the two Google Fonts hosts and same-origin images. Author verification only; routine copy and a static page need no independent review.
