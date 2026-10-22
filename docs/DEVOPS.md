# Project deployment agreement

Status: **Agreed for a static page on GitHub Pages at orcakeel.orcasolutions.dev; first deployment pending**

| Record | Value |
| --- | --- |
| Project / repository | Orca Keel landing page, `Orca-Solutions/orca-keel-landing` (public, proprietary licence) |
| App development owner | Jason |
| DevOps owner / coordination chat | Jason, through the Orca Keel project |
| Frontend and domain owner | Jason |
| Product / budget / launch owner | Jason |
| Template source | Orca-Solutions/dev-ops, `templates/project-devops/DEVOPS.md` |
| Copied template commit | 205908e1dbacf86b0e050a4830322a8ff42f121f |
| Platform brief date | October 9, 2026; revalidated for this project October 21, 2026 |
| Custom domain | `orcakeel.orcasolutions.dev`, a CNAME to `orca-solutions.github.io` in the studio's Cloudflare zone; set in Settings › Pages by Jason on October 22, 2026 |
| First development review / latest contract review | October 21, 2026, at repository creation |
| Release handoff / accepted deployment evidence | Not yet available; the first GitHub Pages deployment goes in `docs/handoffs/` |

This file records choices that development and operations must agree on. It contains configuration key names and credential ownership only, never secret values or customer data.

## Platform brief supplied by DevOps

The studio's default for a static landing page is Cloudflare Pages; existing suitable GitHub Pages sites can remain. Jason chose GitHub Pages for this page on October 21, 2026 so that a public repository under a proprietary licence serves it without a Cloudflare project ([ADR-0001](decisions/0001-own-public-repository.md)). Static output only. A Pages site does not configure the production domain by itself.

## Project declaration

- Selected pattern and reason: **GitHub Pages from `site/` on `main`, through `.github/workflows/pages.yml`.** Zero cost, deploys on push, no second platform to manage.
- Users and data: public page, a handful of visitors. No real data; the example matter is invented. No sensitive categories.
- Components: static HTML and CSS, one page. Fonts from Google Fonts (`fonts.googleapis.com`, `fonts.gstatic.com`) with system fallbacks. No runtime, build, database, jobs or other external services.
- State: none.
- Public and private routes: `/` serves `index.html`; `/favicon.svg`, `/robots.txt`. No private routes, health checks, callbacks or WebSockets. The page is at `https://orcakeel.orcasolutions.dev/` (and, until the DNS check passes, `https://orca-solutions.github.io/orca-keel-landing/`); links in the page are relative so it works at either address.
- Deployment budget and approved services: $0. GitHub Pages on a public repository.
- Availability and recovery: that of an ordinary personal landing page. Recovery is a revert on `main` or re-running the last good workflow run.

## Decisions and early flags

| Topic | App requirement or proposed choice | Status / question / impact | Decision owner and resolution |
| --- | --- | --- | --- |
| Runtime, ARM64 and image delivery | None; static files | N/A (no runtime) | — |
| Database roles, storage and migrations | None | N/A (no state) | — |
| Singleton, background jobs and graceful shutdown | None | N/A | — |
| Domains, authentication and browser origins | `orcakeel.orcasolutions.dev`; no auth | Agreed. `site/CNAME`, canonical and `og:url` in `index.html`; enforce HTTPS once the certificate is issued | Jason, October 22, 2026 |
| Cache and service-worker update behavior | GitHub Pages defaults; no service worker | Agreed | — |
| Resource limits, load, disk growth and cost | A handful of visitors; $0 | Agreed | — |
| Backup, restore, deletion and retention | The repository is the backup | Agreed | — |
| Secrets, mail and external providers | None. The workflow uses `GITHUB_TOKEN` with `pages: write` and `id-token: write` | Agreed | — |
| Release triggers, fallbacks and approval | Push to `main` deploys; PRs do not. Jason merges | Agreed. Pages source set to GitHub Actions by Jason, October 22, 2026 | Jason |

## Implementation contract

**Runtime and operations.** None. `site/` is uploaded as the Pages artifact by `actions/upload-pages-artifact` and deployed by `actions/deploy-pages`. `site/.nojekyll` stops Jekyll from processing the folder.

**Security and browser behavior.** The Content Security Policy is the meta tag in `index.html`: `default-src 'none'`, inline styles and the two Google Fonts hosts, same-origin and `data:` images, no scripts, no forms, no framing base. `site/_headers` carries the same policy plus `nosniff`, referrer and permissions policies for Cloudflare Pages, should the host ever change; GitHub Pages ignores it and sends no custom headers.

**Updates and fallback.** A merge to `main` deploys. Fallback is a revert commit or re-running a previous successful workflow run from the Actions tab. No schema, clients or state.

**Recovery and privacy.** Nothing is stored or collected. Nothing to back up beyond the repository.

## Before first deployment

- Settings › Pages › Source is **GitHub Actions** (done October 22, 2026).
- The DNS check for `orcakeel.orcasolutions.dev` passes and **Enforce HTTPS** is ticked.
- The workflow run on `main` succeeds and the page loads at the `github.io` address.
- Check the page in light and dark mode at desktop and phone widths; confirm fonts load or fall back.
- Record the deployment in `docs/handoffs/` with the commit and the address.

## Changes affecting the other team

| Date / source or infrastructure revision | Change and reason | Affected code/config and rollout action | Owners / decision link |
| --- | --- | --- | --- |
| 2026-10-21, repository creation | GitHub Pages chosen over Cloudflare Pages | `.github/workflows/pages.yml`, `site/.nojekyll`; Jason enables Pages | Jason, [ADR-0001](decisions/0001-own-public-repository.md) |
