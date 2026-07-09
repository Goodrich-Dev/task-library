---
name: verify-xml-sitemap-exists-and-in-robotstxt
description: Confirms a current XML sitemap exists, is referenced in robots.txt, and is submitted to Google Search Console so every page can be found and indexed.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Verify XML sitemap exists and in robots.txt

**Use this when** running Layer 1 (Digital Plumbing Checks) of the Website QA Audit — Google can't rank pages it never discovers.

## Inputs
- Site URL and WordPress admin access (RankMath handles the sitemap on standard builds)
- Google Search Console access for the verified property
- The audit report/spreadsheet for logging results

## Steps
1. Fetch the sitemap directly in a browser — try `/sitemap_index.xml` (RankMath default) and `/sitemap.xml` — and confirm it returns valid XML, not a 404.
2. Open the sitemap and spot-check that it lists the live posts and pages, with no deleted URLs, staging URLs, or noindexed pages included.
3. Fetch `/robots.txt` and confirm it contains a `Sitemap:` line pointing at the exact sitemap URL from step 1.
4. In Google Search Console → Sitemaps, confirm the sitemap is submitted with status Success and a recent "last read" date.
5. Compare the sitemap URL count against the site's real page count; flag big gaps (sections missing) or bloat (tag/archive junk).
6. Log sitemap URL, robots.txt line, GSC status, and URL counts in the audit report.

## Definition of done (QA checklist)
- [ ] Sitemap loads with valid XML and lists current live URLs only
- [ ] robots.txt contains a correct `Sitemap:` reference and GSC shows status Success
- [ ] URL count sanity-checked and results logged, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent Fable 5 agent (or comparable OpenAI/Google model) goes past spot-checks: it diffs every sitemap URL against a full crawl of the live site, looping until zero live pages are missing, zero dead or noindexed URLs remain listed, and GSC reports Success on a fresh read.
It self-verifies after each fix by re-fetching the sitemap and robots.txt, and memory holds the last-known URL counts so any drift between runs triggers an automatic re-audit.
Each run logs one worked example to ## Example(s), compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /seo-audit · /digital-plumbing · previous: test-mobile-load-time-under-3-seconds · next check: verify-person-schema-with-sameas-links
