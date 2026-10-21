# orca-keel-landing working record

Current state, open tasks, verification and review dispositions. Newest first.

## 2026-10-21: repository created

**State.** Jason decided the landing page gets its own public repository under a proprietary licence, separate from the Orca Keel code, so GitHub Pages can serve it without a Cloudflare project ([ADR-0001](docs/decisions/0001-own-public-repository.md)). The page was drafted from the landing board on the brand canvas and the final brand kit (name Orca Keel, Signal mark as the seal, Harbor palette, approved by Jason the same day), with the prices removed since pricing waits for the pilot. The brand kit was copied in from the Orca Keel plan set (`plans/orca-home/brand/kit/`, draft 0.2) without the studio's Signal source package or the internal brand brief. The operating documents were copied from the maintainer's project scaffold (policy v3.1.4, October 11, 2026) and filled in; its private companion guides stay Git-ignored in the local clone. Commits are in Jason's name with no agent attribution, at his instruction.

The page has the hero, the three claims, the Daybook section with an example matter and grant, the installer's dark layer, the carton, a "where it stands" section with placeholders, and the footer.

**Open tasks.**
- Jason enables GitHub Pages for the repository (Settings › Pages › Source: GitHub Actions) so the workflow in `.github/workflows/pages.yml` deploys `site/`; then record the first deployment in `docs/handoffs/`.
- Jason chooses the domain; then add the canonical URL and `og:url` to `site/index.html` and a `CNAME` file under `site/` ([docs/DEVOPS.md](docs/DEVOPS.md)).
- Jason replaces the `LICENSE` placeholder with the licence text he wants.
- Fill `[UNITS]`, `[DATE]` and `[EMAIL]` when they exist. Pricing stays off the page until the pilot.
- Photography, when there is some. Until then the hero shows the flat Paper panel with the box drawn as a dark slab and the single amber dot.

**Verification.** The page was rendered with headless Chromium at 1280 px and 390 px in light and dark mode before this push: no horizontal overflow, no console errors, both themes legible. No JavaScript, so nothing to syntax-check. The CSP meta tag allows only inline styles, the two Google Fonts hosts and same-origin images. Author verification only; routine copy and a static page need no independent review.
