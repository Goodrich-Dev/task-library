---
name: scale-winners-by-increasing-budget-gradually
description: Grow budget on proven winners gradually — never more than 2× per adjustment — so results scale without resetting delivery learning or breaking the economics that made them winners.
category: Dollar a Day Campaigns
stage: Promote
definitive_article: /dad
status: complete
---

# Scale winners by increasing budget gradually

**Use this when** an ad set has beaten its target over a full 7-day window — the temptation is to 10× it; the method is to compound it.

## Inputs
- Qualified winners: full-window performance at or better than target, stable or improving engagement
- The target cost per result (the line scaling must not cross)
- The adjustment log (date, budget, cost per result per change)

## Steps
1. Qualify before scaling: a winner beat its target across the whole 7-day window — not one lucky day — with engagement holding.
2. Increase the budget **no more than 2× per adjustment**: $1 → $2 → $4 → $8. Bigger jumps reset the platform's delivery learning and routinely destroy the cost per result that made it a winner.
3. After each increase, wait several days (a fresh learning window) and re-check cost per result before the next step. Scaling is a staircase, not a ramp.
4. If cost per result climbs past target after a bump, step back to the last good budget. The audience just told you its depth — believe it.
5. Scale horizontally in parallel: the same winning creative into new audience layers via switch boosts. New audiences are often cheaper than higher bids on the old one.
6. Watch frequency as spend grows. Rising frequency plus sagging engagement = fatigue → refresh the creative or rotate audiences before costs decay.
7. Preserve the 90/10 split at every size: ~90% of spend behind greatest hits, ~10% funding new $1/day tests so the winner pipeline never runs dry.
8. Log every adjustment — MAA applies to scaling exactly as it does to testing.

## Definition of done (QA checklist)
- [ ] Every budget increase ≤2×, with a re-check window between steps
- [ ] Rollback executed (and logged) wherever cost per result crossed target
- [ ] Horizontal scaling via switch boosts running alongside vertical increases
- [ ] Frequency monitored; 90/10 test budget preserved; adjustment log current
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Worked example to document: Marko Sipila (HVAC Quote) — scaled via $1/day by compounding winning one-minute videos instead of betting big on day one. Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
Scaling is a staircase a persistent agent (Claude Fable 5 or comparable OpenAI/Google models) climbs over weeks: qualify the winner, bump ≤2×, wait out the learning window, re-check cost per result, repeat — and a missed re-check or skipped rollback is a missed kill/scale check, which in Dollar a Day means a failed run.
It loops until the Definition of done fully passes (every increase ≤2×, rollbacks logged, frequency watched, 90/10 preserved) and holds the adjustment log in memory, so each step starts from the audience's proven depth rather than hope.
Log every scaling arc as a meta-article example so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /dad
- Related: /nine-triangles (90/10 Content Strategy, MAA) · /social-amplification (Stage 5 boost optimization)
- Run order (DAD core): kill-underperforming-ads → **scale-winners-by-increasing-budget-gradually** → execute-switch-boosts-to-new-audiences
