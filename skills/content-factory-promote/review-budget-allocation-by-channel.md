---
name: review-budget-allocation-by-channel
description: Audit how spend is distributed across channels, ad sets, and funnel levels against performance, then reallocate by Dollar a Day rules — starve losers, feed winners ≤2× per step.
category: Content Factory — Promote
stage: Promote
definitive_article: /social-amplification
status: needs-work
---

# Review budget allocation by channel

**Use this when** closing each optimization cycle (SAE Stage 6), or whenever spend has drifted from where results are actually coming from.

## Inputs
- Spend and results by channel (Facebook/Instagram, Google, YouTube) and by ad set for the period
- Target CPA/ROAS and budget from SAE Stage 2 goals
- Funnel-level mapping of every ad set (cold / warm / conversion) from the sequencing skill

## Steps
1. Build the allocation table: spend, results, and cost per result for every channel and ad set, subtotaled by funnel level.
2. Compare each line against target CPA/ROAS. Mark every line **above target** (overpriced) and every line **at or below target running at its budget cap** (starved winner).
3. Check the funnel-level balance: all budget on cold = filling a bucket you never harvest; all on conversion = exhausting a warm pool nothing refills. The three levels must each be funded.
4. Reallocate by Dollar a Day rules: kill the worst performers outright (bottom of the table), shift their dollars to starved winners — increasing any single ad set by **no more than 2× per adjustment**.
5. Keep a small test reserve: roughly 10% of budget on new content/audiences (the 90/10 content strategy applied to spend).
6. Document before/after allocation with the reasoning per change in the weekly MAA report — next period's comparison must be able to judge these moves.

## Definition of done (QA checklist)
- [ ] Full spend table built by channel, ad set, and funnel level with cost per result vs target
- [ ] Losers killed; winners scaled ≤2× per step; no funnel level left unfunded
- [ ] ~10% test reserve maintained for new content and audiences
- [ ] Before/after allocation and reasoning documented in the MAA report
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. Candidate: a monthly reallocation moving dead cold-audience spend into a starved remarketing ad set and logging the CPA drop.

## Run on a persistent agent (Fable 5)
A persistent agent (Fable 5 or comparable OpenAI/Google models) rebuilds the full allocation table each cycle from the spend and results data it has been logging all period, then executes the reallocation by rule — kill losers, feed starved winners ≤2×, keep the ~10% test reserve, fund all three funnel levels — and self-verifies every Definition-of-done box, including the documented before/after reasoning.
Because last cycle's moves and their predicted outcomes live in memory, each review opens by judging its own previous calls.
Each cycle logs a meta-article example so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /social-amplification (Stage 6: Optimization)
- Related: /dad (kill/scale mechanics) · /nine-triangles (MAA, funnel levels, 90/10 content strategy)
- Run order (Promote stage): compare-current-vs-last-period-performance → **review-budget-allocation-by-channel** → list-top-3-5-recommendations-for-next-7-days
