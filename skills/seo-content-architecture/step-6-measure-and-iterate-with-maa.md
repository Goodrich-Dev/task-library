---
name: step-6-measure-and-iterate-with-maa
description: "Close the internal linking loop with the MAA cycle — baseline, measure rankings and traffic per page, analyze which links worked, act on the findings, and re-run the 6-step process on schedule."
category: SEO & Content Architecture
stage: —
definitive_article: /internal-linking
status: complete
---

# Step 6: Measure and iterate with MAA

**Use this when** Step 5's clean link log is in hand and the links are live — internal linking is a loop, not a project, and this step keeps it spinning.

## Inputs
- Pre-change baseline window defined; Google Search Console and GA4 access
- The Step 5 clean link log (which pages were touched, when)
- The MAA cycle (/maa): Metrics, Analysis, Action

## Steps
1. Baseline first: capture pre-change impressions, average position, and clicks for the money and orphan pages (Search Console), plus sessions (GA4).
2. **Metrics**: after links go live, track the same numbers weekly per page — rankings, impressions, click-through, internal traffic flow, and indexation of former orphans.
3. **Analysis**: determine which links moved which pages — which anchors and source pages did the work, and which links did nothing.
4. **Action**: add links where the pattern works, rewrite anchors that underperform, and remove links that fail the relevance test in hindsight.
5. Fold the findings into the weekly MAA report: what's working, what isn't, and the next 3–5 linking moves.
6. Re-run the full 6-step process (/internal-linking) on a recurring schedule — new content keeps arriving, so the loop never finishes.

## Definition of done (QA checklist)
- [ ] Baseline captured before any links went live
- [ ] Weekly per-page metrics flowing for all touched money and orphan pages
- [ ] At least one analysis-driven action taken per cycle, with the reasoning logged
- [ ] Linking section included in the weekly MAA report; next 6-step cycle scheduled
- [ ] Linked back to the definitive articles (/internal-linking, /maa) and relevant siblings

## Example(s)
- The /internal-linking definitive article closes with this measurement loop as its Step 6 on blitzmetrics.com.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first full measurement cycle.

## Run on a persistent agent (Fable 5)
This step is where a persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) beats any chat session: it captures the baseline, returns weekly for Metrics → Analysis → Action, and never marks the task done — the Definition of done demands at least one analysis-driven action per cycle, every cycle.
Per-page metric history accumulates in memory across cycles; that longitudinal record is the analysis, and it is what schedules the next full 6-step run.
Each cycle logs its findings to the weekly /maa report and a meta-article example via /meta-article-prompt-template.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /internal-linking
- Related (run order): step-5-qa-links-against-google-guidelines (before) → step-1-inventory-content-and-establish-gct-per-page (the loop restarts) · /maa · /seo-tree
