---
name: show-whats-working-and-what-isnt
description: Present performance data as an explicit two-column verdict — winners with evidence, underperformers with evidence — so the weekly report drives kill/scale decisions instead of hiding them.
category: Strategy & Measurement
stage: —
definitive_article: GAP — to be written
status: needs-work
---

# Show what's working and what isn't

**Use this when** assembling the weekly MAA report, or any time a stakeholder asks "how's it going?" and deserves a straight answer instead of a wall of screenshots.

## Inputs
- Current-period metrics for every active item: campaigns, boosted posts, articles, pages
- The thresholds that define "working" — target CPA/ROAS, engagement benchmarks, ranking/traffic goals (from GCT and SAE Stage 2)
- Last period's numbers for trend context

## Steps
1. Fix the verdict thresholds first: an item is "working" only if it meets its stated target (e.g., at-or-under target CPA, at-or-above engagement benchmark). Write the threshold at the top of the report so the verdicts are checkable.
2. Score every active item against its threshold — no item gets to be "too new to judge" for more than one cycle.
3. Build two lists. **Working:** each item with the one metric that proves it, plus trend vs last period. **Not working:** same evidence standard — no euphemisms, no burying.
4. Lead with winners (they get scaled), follow with losers (they get diagnosed and killed) — but never omit the losers; hiding them is how budgets die.
5. Keep each line to one sentence: item, verdict metric, trend. Detail lives in the linked dashboards, not the verdict page.
6. Hand both lists downstream: losers go to analyze-why-underperformers-fail; the combined picture feeds kill-underperformers-scale-winners and the Friday report.

## Definition of done (QA checklist)
- [ ] Verdict thresholds stated explicitly at the top
- [ ] Every active item appears in exactly one list — working or not working
- [ ] Each line carries its proof metric and period-over-period trend
- [ ] Underperformers are as visible as winners (equal evidence, equal prominence)
- [ ] Both lists handed into the Friday MAA report unedited
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) has no favorites: it scores every active item against the stated thresholds and loops until the Definition of done fully passes — every item in exactly one list with its proof metric and trend, underperformers as visible as winners.
It self-verifies by reconciling both lists against the full active inventory so nothing gets quietly omitted.
Memory supplies the period-over-period trend column and tracks each item's launch date, so nothing hides behind "too new to judge" past one cycle — the MAA loop runs as a true memory cycle — and a meta-article example is logged each run.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written (parent methodology: /maa; framework context: /nine-triangles)
- Related, in run order: submit-weekly-maa-report-every-friday, analyze-why-underperformers-fail, kill-underperformers-scale-winners
