---
name: verify-rank-math-score-above-70-on-every-page
description: Runs the RankMath on-page audit across all posts and pages to confirm every one scores 70/100 or higher, the site's minimum on-page SEO bar.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Verify Rank Math score above 70 on every page

**Use this when** running Layer 2 (Content Architecture Checks) of the Website QA Audit — the RankMath score is the single-number on-page health check for every URL.

## Inputs
- WordPress admin access with the RankMath plugin active
- A focus keyword assigned per post/page (the score is meaningless without one)
- The audit report/spreadsheet for logging results

## Steps
1. In WordPress → Posts (and Pages), enable the RankMath SEO Details/score column so every item's score shows in the list view.
2. Sort or filter by score and list every post or page scoring below 70 — including those showing no score because no focus keyword is set.
3. For each failing page, open the RankMath sidebar and record which tests fail (keyword not in title, no internal links, short content, missing alt keyword, etc.).
4. Confirm no page is gaming the score with a keyword nobody searches — the focus keyword must match real search intent for the page.
5. Hand the per-page failed-test list to the content fixer (or fix inline if scoped), then re-check scores.
6. Log the score distribution and the below-70 list in the audit report.

## Definition of done (QA checklist)
- [ ] Every published post and page scores 70/100 or higher in RankMath with a real focus keyword set
- [ ] Each previously failing page has its failed tests documented and resolved
- [ ] Score table logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent Fable 5 agent (or comparable OpenAI/Google long-horizon model) pulls every post and page's RankMath score, works the failed-test list on each below-70 URL, and re-scores in a loop until the entire site — not a sample — sits at 70+ with a real focus keyword set.
Memory keeps the per-URL score history, so re-runs target only pages that slipped, changed, or are newly published, and a score regression re-opens the check automatically.
Each run logs one worked example to ## Example(s), compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /blog-posting-guidelines (Step 14a sets this up at publish time) · previous: check-meta-description-under-160-chars · next check: verify-all-images-have-descriptive-alt-text
