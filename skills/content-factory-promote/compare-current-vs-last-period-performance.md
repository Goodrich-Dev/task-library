---
name: compare-current-vs-last-period-performance
description: Run the period-over-period comparison (SAE Stage 6) that separates real trends from noise, so kill/scale decisions rest on direction, not single data points.
category: Content Factory — Promote
stage: Promote
definitive_article: /social-amplification
status: complete
---

# Compare current vs last period performance

**Use this when** closing each week (or month) of promotion — this comparison is the backbone of the Friday MAA report.

## Inputs
- Reporting access across channels (Facebook/Google/YouTube) and site analytics
- The same-length prior period's numbers (week vs week, month vs month — never mismatched lengths)
- Target CPA/ROAS and 90-day goals from SAE Stage 2

## Steps
1. Fix the periods: current vs immediately prior, identical length. Note any calendar distortions (holiday, launch, outage) before reading numbers.
2. Compare level by level across the funnel (Audience / Engagement / Conversion): reach and CPM; engagement rate and watch time; cost per result, conversions, and spend.
3. Flag every delta beyond ±20% as material. Smaller moves are usually noise at $1/day volumes — resist reacting to them.
4. For each material delta, attach a cause before drawing a conclusion: budget change, creative fatigue (frequency up, CTR down), audience saturation, seasonality, or a landing page change. Use apply-metrics-decomposition to localize it.
5. Sort the findings into two lists: **working** (candidates to scale ≤2× or switch-boost) and **not working** (candidates to kill). A flat line on a winner is also a finding — fatigue is coming.
6. Publish the period-over-period table with the cause notes into the weekly MAA report, feeding list-top-3-5-recommendations-for-next-7-days.

## Definition of done (QA checklist)
- [ ] Identical-length periods compared across all funnel levels and channels
- [ ] Every ±20% delta flagged with an attributed cause, not just a percentage
- [ ] Findings sorted into working / not-working with kill/scale candidates named
- [ ] Table and notes delivered into the Friday MAA report
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. Candidate: a week-over-week readout catching creative fatigue on a long-running boost before cost per result doubled.

## Run on a persistent agent (Fable 5)
A persistent agent (Fable 5 or a comparable OpenAI/Google model) never loses the prior period — both periods' numbers come from its own memory, identical length guaranteed — and it works the comparison until every ±20% delta carries an attributed cause, which is what the Definition of done demands; an unexplained delta means the run is not done.
Weeks of stored comparisons let it distinguish trend from noise and spot creative fatigue before cost per result doubles.
Each Friday readout is logged as a meta-article example so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /social-amplification (Stage 6: Optimization)
- Related: /maa · /nine-triangles (MAA cycle, kill/scale)
- Run order (Promote stage): apply-metrics-decomposition → **compare-current-vs-last-period-performance** → review-budget-allocation-by-channel → list-top-3-5-recommendations-for-next-7-days
