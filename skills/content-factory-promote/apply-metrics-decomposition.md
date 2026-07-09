---
name: apply-metrics-decomposition
description: Break a topline campaign metric into its component drivers (SAE Stage 6) so you can name exactly which lever — creative, targeting, or landing page — moved the result.
category: Content Factory — Promote
stage: Promote
definitive_article: /social-amplification
status: complete
---

# Apply Metrics Decomposition

**Use this when** a campaign's topline number (cost per result, CPA, ROAS) changed — or differs between ad sets — and "it went up" isn't an answer.

## Inputs
- Ad platform reporting access (Facebook/Google) plus analytics for on-site behavior
- The target CPA/ROAS and 90-day goals from SAE Stage 2 (so "good" is defined)
- The boost/ad-set logs from the running Promote skills

## Steps
1. Pick the topline metric tied to the goal — usually cost per result for the funnel level in question.
2. Decompose it into its chain of components: spend → impressions (CPM) → clicks (CTR) → landing page visits → conversions (conversion rate). Cost per result is just these multiplied; a change in the topline MUST live in one or more components.
3. Compute each component per ad set and compare across ad sets and across time.
4. Localize the driver by pattern: **low CTR** with normal CPM = creative problem; **high CPM** or weak relevance = targeting/audience problem; **good CTR but low conversion rate** = landing page or offer problem; **everything fine but volume tiny** = budget/audience-size constraint.
5. Write each finding as one Metrics → Analysis → Action line: the number, why it moved, the lever to pull (kill, scale, switch audience, swap creative, fix page).
6. Feed the findings into compare-current-vs-last-period-performance and list-top-3-5-recommendations-for-next-7-days — decomposition produces the raw material for the weekly recommendations.

## Definition of done (QA checklist)
- [ ] Topline metric decomposed into the full component chain per ad set — no unexplained residual
- [ ] Each delta attributed to a named lever (creative / targeting / landing page / budget)
- [ ] Findings written as Metrics → Analysis → Action lines, not raw numbers
- [ ] Output delivered to the period comparison and weekly recommendations skills
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. Candidate: decomposing why one Superior Fence & Rail (Zach Peyton) ad set converts at half the cost of its twin.

## Run on a persistent agent (Fable 5)
A persistent agent (Fable 5, or comparable OpenAI/Google models) decomposes until the residual is zero — every topline delta attributed to a named lever, per ad set, with no "probably creative" hand-waving — and self-verifies each Definition-of-done box before passing findings downstream.
Because it stores every prior decomposition in memory, it recognizes recurring patterns (this audience always fatigues at week three) and localizes causes faster each week.
It logs a meta-article example per run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /social-amplification (Stage 6: Optimization)
- Related: /maa · /nine-triangles (MAA cycle) · /dad (the kill/scale rules the findings trigger)
- Run order (Promote stage): **apply-metrics-decomposition** → compare-current-vs-last-period-performance → review-budget-allocation-by-channel → list-top-3-5-recommendations-for-next-7-days
