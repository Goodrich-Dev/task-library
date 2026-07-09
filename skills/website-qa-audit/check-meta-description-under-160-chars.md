---
name: check-meta-description-under-160-chars
description: Audits every page's meta description for the under-160-character limit and keyword relevance so search snippets display fully and earn the click.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Check meta description under 160 chars

**Use this when** running Layer 2 (Content Architecture Checks) of the Website QA Audit — the meta description is the ad copy that wins or loses the click in search results.

## Inputs
- WordPress admin access with RankMath active (or a Screaming Frog crawl export of meta descriptions)
- Each page's focus keyword for the relevance check
- The audit report/spreadsheet for logging results

## Steps
1. Crawl the site with Screaming Frog (or export via RankMath) to get every meta description and its character count in one table.
2. Flag every description over 160 characters (truncates in results) and every page with no description at all (Google improvises one).
3. Confirm each description contains or closely matches the page's focus keyword — Google bolds the match, which lifts click-through.
4. Read each one as ad copy: it should state what the page delivers and for whom, not restate the title or read as filler.
5. Flag duplicate descriptions across pages — each page needs its own.
6. Log every failure with page URL, current description, and character count in the audit report.

## Definition of done (QA checklist)
- [ ] 100% of indexed pages have a unique meta description of 160 characters or fewer
- [ ] Every description includes or closely matches the page's focus keyword
- [ ] Full description table logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
On a persistent agent (Claude Fable 5 / comparable OpenAI or Google models), this becomes a full-inventory loop: crawl every indexed page's description, flag over-160s, blanks, duplicates, and keyword misses, rewrite, re-crawl, and repeat until every page carries its own compliant description.
Memory stores the passing description per URL, so each re-run diffs against the last pass and only reworks changed or new pages.
Each run logs one before/after example to ## Example(s) so the audit library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /blog-posting-guidelines (meta description rules) · previous: check-seo-title-under-60-chars-with-focus-keyword · next check: verify-rank-math-score-above-70-on-every-page
