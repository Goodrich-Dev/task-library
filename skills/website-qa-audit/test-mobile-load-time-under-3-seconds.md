---
name: test-mobile-load-time-under-3-seconds
description: Measures real mobile load speed with PageSpeed Insights and Lighthouse to confirm the site loads in under 3 seconds, where most local-service visitors arrive.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Test mobile load time under 3 seconds

**Use this when** running Layer 1 (Digital Plumbing Checks) of the Website QA Audit — most local-service traffic is mobile, and slow pages lose leads before they load.

## Inputs
- Site URL plus the top pages by traffic (homepage, key service pages, top blog posts)
- Google PageSpeed Insights (pagespeed.web.dev) or Lighthouse in Chrome DevTools
- The audit report/spreadsheet for logging results

## Steps
1. Run the homepage through Google PageSpeed Insights and read the **Mobile** tab, not Desktop.
2. Record Largest Contentful Paint (LCP) — the practical "loaded" moment — plus the overall performance score; pass requires LCP under 3.0 seconds on mobile.
3. Repeat for each key service page and the top 2–3 blog posts so the result reflects real templates, not just the homepage.
4. Where a page fails, capture the top Opportunities list (oversized images, render-blocking scripts, missing caching) as the fix punch list.
5. Re-run any failing page once to rule out a one-off test fluke; keep the worse of the two runs as the recorded result.
6. Log LCP, performance score, and the fix list per page in the audit report.

## Definition of done (QA checklist)
- [ ] Every checked page records mobile LCP under 3.0 seconds in PageSpeed Insights/Lighthouse
- [ ] Failing pages have a named fix list pulled from the report's Opportunities section
- [ ] Scores and screenshots logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 / comparable OpenAI or Google models) doesn't stop at the homepage and top posts — it runs every sitemap URL through PageSpeed/Lighthouse mobile, queues the Opportunities fixes, and re-measures after each fix until every page records LCP under 3.0 seconds.
Because scores fluctuate, it self-verifies with multiple runs per page and keeps the worse result; memory stores per-URL LCP history so re-runs target only pages that failed or changed.
Each run logs a before/after example to ## Example(s), so the audit library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /digital-plumbing (speed optimization if this check fails) · /seo-audit · previous: verify-https-with-no-mixed-content · next check: verify-xml-sitemap-exists-and-in-robotstxt
