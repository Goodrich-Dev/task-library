---
name: create-facebook-instagram-campaigns-with-location-targeting
description: Build Facebook/Instagram campaigns layered by location, demographics, and interests at $1/day per ad set — the local-service workhorse of the Dollar a Day method.
category: Dollar a Day Campaigns
stage: Promote
definitive_article: /dad
status: needs-work
---

# Create Facebook/Instagram campaigns with location targeting

**Use this when** a business serves a defined geography — every dollar shown outside the service area is reach you can't sell to.

## Inputs
- GCT written: Goal (leads/booked jobs vs awareness), Content (proven winners), Targeting (the service area)
- Meta Business Manager set up with pixel and pages connected
- The audience grid for this market (geo, demo, interest, custom layers)

## Steps
1. Confirm GCT before structure: which Goal, which proven Content (from identify-signals-worth-amplifying), which Targeting boundary.
2. Draw the **location layer first**: radius around the shop or an explicit city/ZIP list matching the real service area — and exclude where you don't serve. Cheap reach you can't service is expensive.
3. Stack demographics on the geo: age range and attributes matching the actual buyer (for home services, homeowners roughly 30–65+), not platform defaults.
4. Add interest clusters as **separate ad sets**, never merged: each geo + interest combination is its own $1/day test cell, readable on its own.
5. Run placements across Facebook and Instagram feeds/reels with the creative that earned it — one-minute videos and real job photos beat polished agency ads for local service.
6. Launch the matrix at $1/day per ad set, 7 days untouched, then the standard loop: analyze cost per result → kill losers → scale winners ≤2× → switch boosts to the next territory.
7. Harvest locally: leads and engagers feed custom audiences; build the local lookalike for the next round and sequence warm engagers toward the quote/booking offer.

## Definition of done (QA checklist)
- [ ] Location layer matches the true service area, with exclusions applied
- [ ] Demographic and interest layers split one-per-ad-set on top of geo
- [ ] All cells at $1/day across FB + IG; 7-day window held; verdicts logged
- [ ] Local custom audiences and lookalike building from results
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Worked example to document: Zach Peyton (Superior Fence & Rail) — location-targeted FB/IG campaigns by territory for fence installation demand. Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
Run the local matrix on a persistent agent (Claude Fable 5 or comparable OpenAI/Google models) that owns the whole loop — geo layers with exclusions, $1/day cells, the untouched week, then verdicts — and loops until the Definition of done fully passes; a missed day-7 kill/scale check on any territory equals a failed run, the core Dollar a Day rule.
It self-verifies the location layer against the real service area before any spend, and keeps per-territory results in memory so each new territory launch starts from what the last one proved.
Log one territory's full cycle per run as a meta-article example so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /dad
- Related: /digital-plumbing (GBP + NAP for the same geography) · /social-amplification (Stages 4–5)
- Run order (platform setup): set-up-meta-business-manager-and-public-figure-pages → **create-facebook-instagram-campaigns-with-location-targeting** → create-youtube-campaigns-using-aducate-model
