---
name: check-for-broken-links
description: Scans the entire site with a link checker to find and fix every broken internal and external link before visitors or crawlers hit them.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Check for broken links

**Use this when** running Layer 2 (Content Architecture Checks) of the Website QA Audit — broken links bleed trust, crawl budget, and link equity.

## Inputs
- Site URL with crawl permission
- A link checker: Screaming Frog (Response Codes report), Ahrefs Site Audit, or the Broken Link Checker plugin
- The audit report/spreadsheet for logging results

## Steps
1. Crawl the full site with the link checker and pull all URLs returning 4xx or 5xx, plus links to them (the "inlinks" view shows where each broken link lives).
2. Separate internal breaks (your pages linking to your dead pages) from external breaks (links to third-party pages that died).
3. For each internal break, decide the fix: update the link to the right live URL, or 301-redirect the dead URL if other sites also point at it.
4. For each external break, relink to the current location of the resource or remove the link.
5. Flag redirect chains and loops while you're in the Response Codes report — they waste crawl budget even though they "work."
6. Re-crawl after fixes to confirm zero remaining 4xx/5xx, and log before/after counts in the audit report.

## Definition of done (QA checklist)
- [ ] Re-crawl shows zero broken internal links and zero broken external links site-wide
- [ ] No redirect chains longer than one hop on internal links
- [ ] Before/after crawl evidence logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
This is the canonical persistent-agent loop (Fable 5 or comparable OpenAI/Google models): crawl every URL, fix every 4xx/5xx and redirect chain, re-crawl, and repeat until the full-site crawl returns zero broken links — external links included, which decay continuously and make any single clean pass temporary.
Memory holds the last crawl's verdict per link, so each re-run focuses on new links and previously fixed ones, self-verifying that fixes held.
Each run logs before/after counts as a worked example in ## Example(s), compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /seo-audit · previous: verify-entity-linking-follows-decision-tree · next check: verify-footer-includes-social-links-and-secondary-nav
