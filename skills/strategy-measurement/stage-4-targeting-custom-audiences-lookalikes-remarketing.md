---
name: stage-4-targeting-custom-audiences-lookalikes-remarketing
description: Complete Stage 4 of the Social Amplification Engine — import custom audiences, build interest targets, create lookalikes, and set remarketing pools — so Stage 5 boosts reach people who can actually buy.
category: Strategy & Measurement
stage: —
definitive_article: /social-amplification
status: complete
---

# Stage 4: Targeting (custom audiences, lookalikes, remarketing)

**Use this when** the Content Library is stocked (Stage 3) and the engine needs its audience layer built before any boosting begins — content without targeting is shouting into the void.

## Inputs
- Customer email/phone lists, exportable from the CRM or invoicing system (with permission to use for ads)
- Working pixel/analytics from Stage 1 (remarketing pools depend on it)
- The customer profile from Stage 2 goals: who buys, where, and why

## Steps
1. Import **custom audiences**: upload the customer email list (and past-lead lists) into the ad platform as custom audiences — existing customers are the seed of all good targeting.
2. Build **remarketing audiences** from the Stage 1 plumbing: website visitors, video viewers, and page engagers, in recency windows (e.g., short-window site visitors for hot remarketing, longer windows for warm pools).
3. Create **lookalikes** from the highest-quality seeds — start at 1% similarity from the customer custom audience, because lookalikes inherit the quality of their seed (a lookalike of all visitors is weaker than a lookalike of buyers).
4. Layer **saved interest audiences** for cold reach: location, age, demographics, and interests that match the Stage 2 customer profile — these are the engine's prospecting layer.
5. Map every audience to its funnel level — cold (interests, lookalikes), warm (engagers, video viewers), hot (site visitors, customer lists) — so Stage 5 can sequence cold → warm → conversion (see /dad).
6. Name audiences descriptively (source + definition + window) and document the audience map; Stage 6 optimization needs to know exactly what each audience was.

## Definition of done (QA checklist)
- [ ] Customer list imported as a custom audience (match rate checked)
- [ ] Remarketing pools created for site visitors and video viewers with sensible windows
- [ ] 1% lookalike(s) built from the best seed audiences
- [ ] Saved interest audiences created matching the Stage 2 customer profile
- [ ] Audience map documented: every audience named, defined, and assigned a funnel level
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. (The hub at /social-amplification links live examples; pull the closest match into this slot.)

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) builds the full audience layer and loops until the Definition of done fully passes — custom audience match rate checked, remarketing windows set, 1% lookalikes seeded from buyers, and every audience named, defined, and mapped to a funnel level, with none left undocumented.
It self-verifies by reconciling the documented audience map against what actually exists in the ad platform.
Memory keeps the map versioned across periods, so the MAA loop compares audience performance run over run — a true memory cycle that flags saturated or stale pools for refresh — and a meta-article example is logged each run.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /social-amplification
- Related, in run order: stage-3-content-endorsements-why-video-3x3-grid-library, stage-5-amplification-boost-posts-remarketing-ads, funnel-levels-audience-engagement-conversion, /dad
