# ADR-0001: the landing page has its own public repository

Date: 2026-10-21. Status: accepted (Jason).

## Context

Orca Keel's code and plans are private. The landing page needs to be served from somewhere, and the studio's other landing pages (`daybook-landing`, `diamond-dog-landing`, `gg-landing`) each live in their own repository, served by Cloudflare Pages.

## Decision

The landing page lives in `Orca-Solutions/orca-keel-landing`, a public repository under a proprietary licence, so GitHub Pages can serve it without a Cloudflare project. The page carries only what is already public-facing: the page, the brand kit it is built from, and these operating documents. The product's plans, the brand brief's internal notes and the studio's Signal source package stay out.

## Consequences

- Anyone can read the page's source and the brand kit. The licence and NOTICE say what may not be done with them.
- Deploys are a GitHub Actions workflow, not a Cloudflare project; `site/_headers` is inert here.
- Moving to Cloudflare later costs nothing: the `site/` folder and `_headers` already fit its layout.
