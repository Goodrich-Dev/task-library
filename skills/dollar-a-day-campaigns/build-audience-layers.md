---
name: build-audience-layers
description: Layer location, age, demographics, interests, and custom audiences into discrete, one-variable-apart ad-set targets so every $1/day test result is readable.
category: Dollar a Day Campaigns
stage: Promote
definitive_article: /dad
status: complete
---

# Build audience layers

**Use this when** the content shortlist is set and you need targets to test it against — audiences are the T in GCT, and layers are how you learn who actually responds.

## Inputs
- The winning-content shortlist with its GCT notes
- Seed custom audiences from plumbing (site visitors, video viewers, engagers, email list)
- Knowledge of the real buyer: service area, age range, traits, interests

## Steps
1. Start from Targeting in GCT: who is this content for, and at which funnel level (audience / engagement / conversion)?
2. Layer 1 — **location**: the service area for local businesses (radius or city/ZIP list), market geography for everyone else. Exclude where you don't serve.
3. Layer 2 — **age + demographics**: match the actual buyer (e.g., homeowners 30–65), never default "everyone 18–65."
4. Layer 3 — **interests**: 3–5 interest clusters that proxy the customer — competitors, trade publications, adjacent behaviors. Keep clusters separate, not merged.
5. Layer 4 — **custom audiences**: customer email upload, site visitors, video viewers, page engagers — then lookalikes of the best-performing of these.
6. Keep every layer discrete: one variable difference per ad set, so when results diverge you know why. Name them with a consistent scheme (Geo–Age–Interest–Custom).
7. Size-check each layer: large enough to absorb $1/day without instant frequency fatigue, small enough to stay meaningfully targeted.
8. Map content to layers: cold layers get one-minute videos and proven organic winners; warm custom audiences get deeper proof and offers.

## Definition of done (QA checklist)
- [ ] Audience grid documented — location, age/demo, interest, and custom rows with naming convention applied
- [ ] Each planned ad-set audience differs from its neighbor by exactly one variable
- [ ] Custom audiences and lookalikes created and populating
- [ ] Every audience layer mapped to a content piece and funnel level
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Worked example to document: Zach Peyton (Superior Fence & Rail) — territory-by-territory location layers stacked with homeowner demographics for local fence campaigns. Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
Give this to a persistent agent (Claude Fable 5 or comparable OpenAI/Google models) and require the full Definition of done — grid documented, customs populating, every layer mapped to content — before it stops; one merged interest cluster makes the whole matrix unreadable, so 90% here is 0%.
It self-verifies by diffing each neighboring ad-set pair for exactly one changed variable, and stores the grid in memory so next quarter's layers extend the tested map instead of rebuilding it blind.
Each run, log the grid and its naming scheme as a meta-article example so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /dad
- Related: /social-amplification (Stage 4: Targeting — custom audiences, lookalikes, remarketing) · /nine-triangles (funnel levels)
- Run order (DAD core): identify-signals-worth-amplifying → **build-audience-layers** → set-1-day-budget-per-ad-set
