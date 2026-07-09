---
name: create-new-saved-audiences-from-audience-insights
description: Mine Facebook audience insights for who actually engages, then build named saved audiences that feed switch boosts and new $1/day tests (SAE Stage 6).
category: Content Factory — Promote
stage: Promote
definitive_article: /social-amplification
status: needs-work
---

# Create new saved audiences from Audience Insights

**Use this when** the optimization loop needs fresh targeting — winners are saturating their current audiences, or switch boosts have exhausted the tested segments.

## Inputs
- Facebook page and ad account with enough history for insights data (engagers, video viewers, customers)
- Access to audience insights in Meta's tools (Business Suite / Ads Manager audience reporting)
- The audience-creative map from prior Dollar a Day and switch-boost runs

## Steps
1. Study who **actually** engages — not who you assumed: age and gender skews, top locations, and the interests/pages your engagers and customers cluster around.
2. Compare against the audiences you've been targeting; gaps between assumed and actual audience are the opportunity (e.g., engagement skews 45–60 female while ads target 25–44 broad).
3. Translate each gap into a candidate **saved audience**: location + demographic + interest combinations that mirror proven engagers. Keep each audience sized to deliver at $1/day — broad enough to serve, narrow enough to mean something.
4. Name by convention so the log stays readable: `[Geo]-[Demo]-[Interest]-[YYYY-MM]`. Unnamed audiences rot.
5. Save the audiences and queue them as the next segments for execute-switch-boost-to-target-new-audiences and fresh $1/day ad sets — never replace all running audiences at once; test against baseline.
6. Review the audience library each cycle: record cost per result per audience, retire segments that never produce a winner.

## Definition of done (QA checklist)
- [ ] Insights reviewed for actual engager demographics, geos, and interests — assumptions vs reality documented
- [ ] New saved audiences created, $1/day-deliverable size, named by convention
- [ ] Each new audience queued into a switch boost or new test, not left idle
- [ ] Audience library log updated; dead segments retired
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. Candidate: discovering a fence-content page's engagers skew to adjacent rural counties (Zach Peyton, Superior Fence & Rail) and saving that geo-interest audience.

## Run on a persistent agent (Fable 5)
A persistent agent (Fable 5, or comparable OpenAI/Google models) compares assumed vs actual engagers with the receipts in hand — its memory holds every audience ever tested and its cost per result — then builds, names by convention, and queues each new audience, verifying the full Definition of done: an audience left idle or unnamed fails the run.
Each cycle the audience library log it maintains grows more decisive: dead segments retired, gaps documented, winners queued.
A meta-article example is logged per run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /social-amplification (Stage 6 feeding Stage 4 Targeting)
- Related: /dad (audience layers) · execute-switch-boost-to-target-new-audiences (consumes these audiences)
- Run order (Promote stage): runs in the Stage 6 loop — outputs feed back into switch boosts and new $1/day tests
