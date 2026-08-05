# seo-god audit punch list — rentingradar.com — 2026-08-05

Site: https://rentingradar.com · Audit ID: `134dc7a3-e0c0-453d-87a9-d6ad3c0bfe0b` · 7/7 pages crawled, 0 blocked.

**No build/typecheck gate exists for this project** (hand-written static HTML, no toolchain). By
agreement with the site owner, all edits below are reported as **edited, unverified** rather than
**fixed** — nothing automatically confirmed they didn't break anything. Recommend a manual visual
check of the 7 pages, especially the two footer heading changes (visual regression risk is low —
CSS was updated alongside the tag change — but it wasn't machine-verified).

## Class 5 — performance: not assessed

All 10 Lighthouse runs failed during this crawl (`lighthouseCompleted: 0`, `lighthouseFailed: 10`).
This is **not** "no performance issues" — it's an absence of data. No performance findings exist for
this audit because none could be measured. Re-run `audit` to get a real read; if Lighthouse keeps
failing, that's worth investigating on its own (could be the Docker container's headless Chrome, a
resource limit, or something blocking Lighthouse from reaching the live site from inside the
container).

## Not crawled — outside this audit's scope

Only 7 pages were discovered by following internal links from the homepage. These exist on the site
but were never reached, so nothing about them was measured — not "clean," just unaudited:

- `https://rentingradar.com/404.html`
- `https://rentingradar.com/tutorial.html` and the `tutorials/` directory
- `https://app.rentingradar.com` (the product app itself — a separate deployment/domain, likely a
  separate audit target if you want it covered)

If you want these in scope, either link to them from an audited page or hand `run_site_audit` a
higher `maxPages` pointed at each starting URL directly.

## Everything else

All 13 issues OpenSEO found (2 missing meta descriptions, 5 overlong titles, 4 overlong meta
descriptions, 2 heading-order skips) were fixable in the repo and were edited in this run — see the
session summary for the file list. Nothing is being punted to a server admin, CMS editor, or hosting
provider this round; there were no broken links, no 4xx/5xx, no noindex mistakes, and no blocked
pages to report.
