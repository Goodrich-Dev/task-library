---
name: list-top-3-5-recommendations-for-next-7-days
description: Distill the week's analysis into 3–5 force-ranked, owner-assigned actions for the next 7 days — the deliverable that closes the SAE Stage 6 optimization loop.
category: Content Factory — Promote
stage: Promote
definitive_article: /social-amplification
status: complete
---

# List top 3–5 recommendations for next 7 days

**Use this when** the weekly optimization pass is done (decomposition, period comparison, budget review) and the findings must become a short list someone will actually execute.

## Inputs
- Outputs of apply-metrics-decomposition, compare-current-vs-last-period-performance, and review-budget-allocation-by-channel
- The 90-day goals and target CPA/ROAS (SAE Stage 2) to rank against
- Last week's recommendation list with completion status

## Steps
1. Start with accountability: score last week's recommendations — done or not, and did the metric move as predicted? Unexecuted recommendations repeat or escalate; wrong predictions get a cause note.
2. Draft candidate actions from this week's findings. Every candidate must trace to a specific finding, not a hunch.
3. Force-rank by expected impact on the 90-day goal, and **cut to 3–5**. Ten recommendations means nothing happens; the cut is the discipline.
4. Write each as an executable order: verb + specific object + owner + deadline + expected metric move. "Kill ad sets FB-07/FB-09, shift $14/week to the remarketing set — expect blended CPA down ~20% by Friday. Owner: media VA."
5. Classify each as **kill / scale / test** so the mix is visible at a glance (all-test weeks and all-kill weeks both signal something wrong upstream).
6. Deliver the list in the Friday MAA report alongside the period table, and queue each item into the task tracker with its owner.

## Definition of done (QA checklist)
- [ ] Last week's list scored (execution + prediction accuracy) before the new list exists
- [ ] Exactly 3–5 recommendations, each traceable to a named finding
- [ ] Each item has verb, owner, deadline, and predicted metric move; each tagged kill/scale/test
- [ ] Delivered in the Friday MAA report and queued in the tracker
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. Candidate: a Friday top-5 for a local-service account (Marko Sipila, HVAC Quote) showing one kill, two scales, and a test, with next week's scoring.

## Run on a persistent agent (Fable 5)
This skill assumes exactly what a persistent agent (Fable 5, or a comparable OpenAI/Google model) provides: last week's list, predictions, and outcomes held in memory, so the run opens by scoring its own prior calls before drafting new ones — then it cuts to 3–5, writes each as verb + owner + deadline + predicted move, and verifies every Definition-of-done box before the Friday report ships.
Weeks of scored predictions compound into better-calibrated recommendations — the loop literally learns its own accuracy.
Each cycle logs a meta-article example so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /social-amplification (Stage 6: Optimization)
- Related: /maa · /nine-triangles (MAA cycle; Communicate–Iterate–Delegate)
- Run order (Promote stage): apply-metrics-decomposition → compare-current-vs-last-period-performance → review-budget-allocation-by-channel → **list-top-3-5-recommendations-for-next-7-days** → next week's cycle
