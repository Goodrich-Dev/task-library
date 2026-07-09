---
name: kill-underperforming-ads
description: Cut every ad set that misses its target cost per result — on schedule, without sentiment — so budget concentrates on winners and losers cost $7 instead of $700.
category: Dollar a Day Campaigns
stage: Promote
definitive_article: /dad
status: complete
---

# Kill underperforming ads

**Use this when** the day-7 analysis has bucketed losers — the kill is the discipline that makes cheap testing cheap; skipping it quietly converts tests into waste.

## Inputs
- Bucketed day-7 analysis (winners / watch list / losers)
- The kill criteria written before launch (target cost per result, minimum engagement)
- The test log, open for lessons

## Steps
1. Pre-commit kill criteria **before** launch, from Goals: cost per result above target at day 7, near-zero engagement, or falling relevance/quality. Criteria decided after the fact get negotiated.
2. Kill on schedule (the day-7 review), not on mood. The calendar, not your patience, decides when judgment happens.
3. Pause every loser without sentiment — typically the large majority of cells. Cheap tests exist so you can afford cheap funerals.
4. Harvest the lesson before moving on: did the audience, the creative, or the offer fail? One line per kill in the test log — a paid lesson left unwritten is paid twice.
5. Never "fix" a loser mid-flight. Edits reset learning, and a failed combination is information, not a repair project. Build a new test next week instead.
6. Reallocate the freed dollars: winners get gradual increases (≤2× per adjustment), and ~10% keeps funding next week's fresh $1/day tests.
7. Keep killing after the test phase: survivors are reviewed weekly, and rising cost per result or frequency fatigue revokes immunity — yesterday's winner earns no pension.

## Definition of done (QA checklist)
- [ ] Kill criteria documented before launch and applied unmodified at review
- [ ] All below-target ad sets paused at the scheduled review date
- [ ] One-line lesson logged per kill (audience vs creative vs offer)
- [ ] Freed budget reallocated to winners and new tests, with the change logged
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run (document one kill cycle: the before/after budget table and the lessons column).

## Run on a persistent agent (Fable 5)
This is the discipline a persistent agent (Claude Fable 5 or comparable OpenAI/Google models) exists to enforce: it shows up at the scheduled review, applies the pre-committed criteria unmodified, and pauses every loser without negotiation — in Dollar a Day a missed kill check equals a failed run, full stop.
It loops until the Definition of done fully passes — every below-target set paused, one lesson logged per kill, freed budget reallocated and recorded — and keeps the kill log in memory so the same audience–creative–offer failure is never paid for twice.
Each cycle, log the before/after budget table as a meta-article example so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /dad
- Related: /nine-triangles (kill underperformers, scale winners — the MAA action) · /social-amplification (Stage 6)
- Run order (DAD core): analyze-cost-per-result-and-engagement → **kill-underperforming-ads** → scale-winners-by-increasing-budget-gradually
