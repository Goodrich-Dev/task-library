---
name: set-1-day-budget-per-ad-set
description: Set the minimum viable spend — $1/day per ad set — so each test buys real performance data with zero meaningful risk, and a 20-cell matrix costs less than one bad boost.
category: Dollar a Day Campaigns
stage: Promote
definitive_article: /dad
status: complete
---

# Set $1/day budget per ad set

**Use this when** content and audience layers are ready and it's time to fund the test matrix — this is the mechanic the whole method is named for.

## Inputs
- Winning-content shortlist and the audience-layer grid
- GCT doc with the Goal per campaign (engagement, traffic, or conversion)
- A funded ad account with budget authority for the full test window

## Steps
1. Accept the premise: $1/day is tuition, not a growth budget. It is the minimum spend that still buys real delivery data — enough to learn, too little to hurt.
2. Structure top-down from GCT: one campaign per Goal, one ad set per audience layer, one proven creative per ad set.
3. Set budgets at the **ad-set level** (not pooled at the campaign level) so the platform cannot starve your tests by funneling spend to one favorite.
4. Set each ad set to exactly **$1/day**. Resist the urge to "give it a real budget" — a winner at $1 is a winner; a loser at $50 is just an expensive loser.
5. Match the objective to the funnel level: video views/engagement for cold layers, conversions for warm layers.
6. Price the matrix before launch: 20 ad sets = $20/day = $140 for the week — less than one bad "big launch." Commit the full 7-day window up front (~$7 per test).
7. Launch and leave: **7 days untouched**. Mid-flight edits reset learning and corrupt the comparison.
8. Calendar the day-7 MAA review before launching, so analysis is scheduled rather than optional.

## Definition of done (QA checklist)
- [ ] Every ad set budgeted at exactly $1/day, set at the ad-set level
- [ ] One audience layer and one proven creative per ad set; objective matches funnel level
- [ ] Total matrix cost computed and approved for a full 7-day window
- [ ] Day-7 review scheduled; no-edit rule communicated to everyone with account access
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Worked example to document: Marko Sipila (HVAC Quote) — one-minute videos funded at $1/day per ad set, with winners later scaled. Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or comparable OpenAI/Google models) runs this launch and loops until the Definition of done passes completely — every ad set at exactly $1/day at the ad-set level, matrix cost approved, day-7 review scheduled; a budget left pooled at the campaign level is a failed run, not a detail.
Long-horizon is the point: the agent holds the 7-day no-edit rule itself, then shows up for the day-7 review on schedule, because in Dollar a Day a missed kill/scale checkpoint equals a failed run.
It keeps each matrix's structure and cost in memory to build on prior launches, and logs a meta-article example per launch so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /dad
- Related: /social-amplification (Stage 2: Goals — target CPA/ROAS and budget) · /nine-triangles (GCT, MAA)
- Run order (DAD core): build-audience-layers → **set-1-day-budget-per-ad-set** → run-multiple-simultaneous-tests
