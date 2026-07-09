---
name: stage-6-optimization-metrics-budget-review-recommendations
description: Complete Stage 6 of the Social Amplification Engine — decompose metrics, compare periods, audit budget allocation, and deliver the top 3–5 actions for the next 7 days — closing the loop back into the engine.
category: Strategy & Measurement
stage: —
definitive_article: /social-amplification
status: complete
---

# Stage 6: Optimization (metrics, budget review, recommendations)

**Use this when** amplification (Stage 5) has been running long enough to produce data — then weekly, forever. Stage 6 isn't the end of the engine; it's what makes it an engine.

## Inputs
- Campaign data from Stage 5 (spend, delivery, cost per result by ad set and audience)
- The Stage 2 goals page (mission, 90-day goals, target CPA/ROAS, budget)
- Last period's Stage 6 report for comparison

## Steps
1. Apply **Metrics Decomposition**: break each headline result into its component drivers (e.g., cost per lead decomposes through reach, CTR, and conversion rate) so you can see *which* component moved the number instead of staring at the total.
2. **Compare current vs last period**: same metrics, like-for-like windows; flag material changes and attribute each to a cause — creative fatigue, audience saturation, seasonality, or a change you made.
3. **Audit budget allocation**: map spend by channel and ad set against cost per result; find money sitting on losers or starving winners, and check total pace against the Stage 2 budget.
4. Draft the **top 3–5 recommendations for the next 7 days** — each one a concrete action (kill X, scale Y by no more than 2×, switch-boost Z to a new audience, refresh a creative), with the expected effect and owner.
5. Deliver as the weekly report (this is the SAE's instance of the Friday MAA report) and execute the approved actions — recommendations that nobody executes are decoration.
6. Loop back: actions route to the stage they touch — new audiences to Stage 4, new content needs to Stage 3, budget changes to Stage 5 — and next week's Stage 6 first checks whether this week's actions worked.

## Definition of done (QA checklist)
- [ ] Metrics decomposed to component drivers, not just headline totals reported
- [ ] Period-over-period comparison done with causes attributed
- [ ] Budget audit complete: misallocations identified channel-by-channel
- [ ] Top 3–5 next-7-day recommendations written, each with action, owner, and expected effect
- [ ] Report delivered on the weekly cadence and prior week's actions reviewed for impact
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. (The hub at /social-amplification links live examples; pull the closest match into this slot.)

## Run on a persistent agent (Fable 5)

Stage 6 is home turf for a persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models): it decomposes every headline metric to its component drivers and loops until the Definition of done fully passes — causes attributed, budget audit complete, top 3–5 recommendations each carrying action, owner, and expected effect.
It self-verifies that last week's actions were reviewed for impact before any new recommendation ships.
The "compare current vs last period" step is literal memory: prior Stage 6 reports persist across runs, making the MAA loop a true memory cycle with like-for-like windows — and a meta-article example is logged each run.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /social-amplification
- Related, in run order: stage-5-amplification-boost-posts-remarketing-ads, maa-cycle-metrics-analysis-action, submit-weekly-maa-report-every-friday, kill-underperformers-scale-winners
