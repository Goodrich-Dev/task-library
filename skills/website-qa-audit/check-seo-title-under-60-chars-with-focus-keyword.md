---
name: check-seo-title-under-60-chars-with-focus-keyword
description: Audits every page's SEO title for the under-60-character limit and focus keyword inclusion so titles display fully in search and rank for the right terms.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Check SEO title under 60 chars with focus keyword

**Use this when** running Layer 2 (Content Architecture Checks) of the Website QA Audit — truncated or keyword-less titles waste the strongest on-page ranking signal.

## Inputs
- WordPress admin access with RankMath active (or a Screaming Frog crawl export of title tags)
- The focus keyword assigned to each page (from RankMath's per-post setting)
- The audit report/spreadsheet for logging results

## Steps
1. Crawl the site with Screaming Frog (or export titles via RankMath) to get every page title and its character count in one table.
2. Flag every title over 60 characters — these truncate with "…" in Google results.
3. For each page, open the RankMath snippet editor and confirm the focus keyword is set AND appears in the SEO title, preferably near the front.
4. Flag duplicate titles — two pages with the same title compete with each other.
5. Flag empty or auto-generated titles (raw "Page Title – Site Name" defaults with no keyword intent).
6. Log every failure with page URL, current title, character count, and assigned keyword in the audit report.

## Definition of done (QA checklist)
- [ ] 100% of indexed pages have an SEO title of 60 characters or fewer containing the page's focus keyword
- [ ] Zero duplicate or default titles across the site
- [ ] Full title table with character counts logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent Fable 5 agent (or comparable OpenAI/Google model) audits the full title table — every indexed page, every run — flagging over-60 lengths, missing keywords, and duplicates, then loops rewrite-recrawl until 100% of pages pass all three conditions at once.
It self-verifies by re-fetching each rewritten title from the live page, and memory keeps the passing title per URL so re-runs only retest pages whose titles changed or are new.
Each run appends one worked example to ## Example(s), compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /blog-posting-guidelines (title rules) · /seo-audit · previous: verify-wordpress-author-set-to-site-owner-name · next check: check-meta-description-under-160-chars
