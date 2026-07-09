---
name: ensure-robots-meta-not-blocking-indexing--qa-audit
description: Confirms no robots meta tags, headers, or WordPress settings are silently blocking search engines from indexing the site's money pages.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Ensure robots meta not blocking indexing

**Use this when** closing Layer 1 (Digital Plumbing Checks) of the Website QA Audit — one leftover noindex from the dev phase can erase the entire site from Google.

## Inputs
- Site URL plus a full page list (XML sitemap or crawl export)
- WordPress admin access and Google Search Console access for the verified property
- Chrome DevTools (or curl) to read response headers
- The audit report/spreadsheet for logging results

## Steps
1. In WordPress → Settings → Reading, confirm "Discourage search engines from indexing this site" is UNCHECKED.
2. View source on the homepage and every key template (service page, blog post, about, contact) and search for `<meta name="robots"` — flag any `noindex` or `nofollow` on pages that should rank.
3. Check response headers in DevTools → Network (or `curl -I`) for an `X-Robots-Tag: noindex` header — a server-level block invisible in the HTML.
4. Fetch `/robots.txt` and confirm no `Disallow: /` or rules blocking core content paths (intentional blocks like /wp-admin/ are fine).
5. Run the homepage and one money page through GSC URL Inspection; confirm verdict "URL is on Google" or at minimum "Indexing allowed: Yes."
6. Log every page checked, where any block was found (meta, header, robots.txt, or WP setting), and the GSC verdicts in the audit report.

## Definition of done (QA checklist)
- [ ] Zero unintended noindex/nofollow directives in meta tags, X-Robots-Tag headers, or robots.txt across checked pages
- [ ] WordPress "Discourage search engines" is off and GSC URL Inspection shows indexing allowed on money pages
- [ ] Findings logged per page in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent Fable 5 agent (or comparable OpenAI/Google model) checks every URL, not just key templates: it fetches each page's robots meta and X-Robots-Tag header across the full sitemap, looping until zero unintended noindex/nofollow directives survive anywhere and GSC confirms indexing allowed on the money pages.
It self-verifies after fixes with fresh fetches, and memory keeps the per-URL verdict so re-runs only re-inspect failures and newly published pages — plus a standing watch for the WordPress "Discourage" box flipping back on.
Each run logs one example to ## Example(s), compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /seo-audit · /digital-plumbing · previous: check-favicon-is-set · next: Layer 2 begins with verify-all-pages-written-in-first-person
