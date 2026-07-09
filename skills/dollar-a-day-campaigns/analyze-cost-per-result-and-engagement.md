---
name: analyze-cost-per-result-and-engagement
description: Review cost per result, relevance, engagement rate, and conversions per ad set against written targets — the Metrics and Analysis of MAA that turn $7 tests into decisions.
category: Dollar a Day Campaigns
stage: Promote
definitive_article: /dad
status: complete
---

# Analyze cost per result and engagement

**Use this when** a 7-day test window closes — every ad set now owes you a verdict, and the verdict comes from numbers, not impressions of impressions.

## Inputs
- Per-ad-set results for the full window: spend, results, cost per result, engagement, relevance/quality diagnostics, conversions
- The target CPA/ROAS and engagement baseline from Goals (GCT)
- The test log with each cell's hypothesis

## Steps
1. Export results per ad set after the full 7-day window — never judge a partial week.
2. Put every number next to its target. Cost per result without a written target is trivia; Goals defined what winning means before launch.
3. Read engagement quality, not just quantity: shares and substantive comments outrank reactions; on video, watch time and completion rate are the truth serum.
4. Check relevance/quality diagnostics per ad set — content–audience mismatch shows up there before it shows up in cost.
5. Decompose differences: when two ad sets share a creative, the audience explains the gap; when they share an audience, the creative does. (Same logic as apply-metrics-decomposition in Stage 6.)
6. Bucket every ad set: **winners** (beat target), **watch list** (near target with improving trend), **losers** (everything else).
7. Write the Action line for each bucket — scale, hold, or kill. Analysis is not finished until every row carries a verb.
8. Archive results and lessons to the running test log so next week's matrix starts from knowledge, not memory.

## Definition of done (QA checklist)
- [ ] Every ad set scored against a written target for cost per result and engagement
- [ ] Winners / watch list / losers buckets assigned, with decomposition notes explaining why winners won
- [ ] An action verb (scale / hold / kill) recorded per ad set
- [ ] Test log updated with results and one-line lessons
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run (best first candidate: the day-7 readout of a live $1/day matrix showing one audience beating another on the same creative).

## Run on a persistent agent (Fable 5)
Run the day-7 readout on a persistent agent (Claude Fable 5 or comparable OpenAI/Google models) that refuses to finish until every row carries a verb — scored against the written target, bucketed, decomposed, action assigned; a 90% analysis leaves ad sets spending with no verdict, which in Dollar a Day is a missed kill/scale check and therefore a failed run.
It self-verifies that no ad set was judged on a partial window and no target was invented after the fact, and its memory of past readouts turns each week's decomposition into trend instead of anecdote.
Archive each readout as a meta-article example so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /dad
- Related: /social-amplification (Stage 6: Optimization — metrics decomposition, period comparison) · /nine-triangles (MAA cycle)
- Run order (DAD core): run-multiple-simultaneous-tests → **analyze-cost-per-result-and-engagement** → kill-underperforming-ads
