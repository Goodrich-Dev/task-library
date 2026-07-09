---
name: stage-2-goals-mission-90-day-goals-cpa-roas-budget
description: Complete Stage 2 of the Social Amplification Engine — define the mission (start with WHY), 90-day goals, target CPA/ROAS, and budget — so amplification has numbers to optimize toward.
category: Strategy & Measurement
stage: —
definitive_article: /social-amplification
status: complete
---

# Stage 2: Goals (mission, 90-day goals, CPA/ROAS, budget)

**Use this when** Stage 1 plumbing is verified and the brand needs its targets set before any content is assembled or money is spent — this stage is the "G" of GCT for the whole engine.

## Inputs
- The brand's WHY (from the Topic Wheel WHY ring, or an owner interview to extract it)
- Business economics: average customer value, margin, close rate from lead to sale
- Available monthly marketing budget and the revenue the owner needs in 90 days

## Steps
1. Write the **mission** first — start with WHY: the one-to-two-sentence purpose statement that all campaigns must express. If the Topic Wheel WHY ring exists, reuse it verbatim; one WHY per brand, everywhere.
2. Set **90-day goals**: a small set of numeric targets (e.g., leads per month, booked jobs, revenue) that are believable from current baseline — 90 days is long enough to compound, short enough to stay honest.
3. Derive **target CPA** from the economics: what a customer is worth times close rate tells you the most you can pay per lead while staying profitable. For e-commerce or direct sale, set target **ROAS** instead.
4. Set the **budget**: monthly amount the owner can sustain for the full 90 days without panic-pausing — consistent $1/day-scale spend beats sporadic bursts (see /dad).
5. Sanity-check the math: budget ÷ target CPA must be able to produce the 90-day goal. If it can't, lower the goal or raise the budget now — not in week 10.
6. Document mission, goals, CPA/ROAS, and budget on one page; Stages 3–6 and every weekly MAA report judge themselves against this page.

## Definition of done (QA checklist)
- [ ] Mission/WHY written and consistent with the Topic Wheel WHY ring
- [ ] 90-day goals are numeric, dated, and agreed with the owner
- [ ] Target CPA (or ROAS) derived from real economics, not picked from air
- [ ] Budget sustainable for the full 90 days, and budget ÷ CPA covers the goal
- [ ] One-page goals doc stored where Stage 6 and the MAA report reference it
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. (The hub at /social-amplification links live examples; pull the closest match into this slot.)

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) derives target CPA from the real economics and loops until the Definition of done fully passes — including the budget ÷ CPA sanity check actually covering the 90-day goal, forcing the goal or budget to be revised in week 0, not week 10.
It self-verifies by recomputing the math from source numbers (customer value × close rate) instead of accepting a stated CPA.
The one-page goals doc lives in its memory for the full 90 days, so every weekly MAA report is judged against the original targets — a true memory cycle with no quiet goal-shifting — and a meta-article example is logged each run.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /social-amplification
- Related, in run order: stage-1-plumbing-fb-ads-google-ads-analytics, stage-3-content-endorsements-why-video-3x3-grid-library, map-why-ring-core-purpose, gct-goals-content-targeting
