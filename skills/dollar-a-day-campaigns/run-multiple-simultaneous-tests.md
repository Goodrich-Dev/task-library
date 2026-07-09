---
name: run-multiple-simultaneous-tests
description: Launch many $1/day ad sets at once — different creatives, audiences, and placements, one variable apart — so winners reveal themselves in a week instead of a quarter.
category: Dollar a Day Campaigns
stage: Promote
definitive_article: /dad
status: complete
---

# Run multiple simultaneous tests

**Use this when** the $1/day structure is set and you want maximum learning per week — breadth of parallel tests beats any sequence of one-at-a-time guesses.

## Inputs
- Audience grid and creative shortlist (from the earlier DAD core skills)
- Ad sets structured at $1/day each
- A test log (sheet) ready to record hypothesis and outcome per cell

## Steps
1. Define the matrix from GCT: creatives × audiences × placements. Every cell is a hypothesis — "this video, to this layer, in this placement, will beat target."
2. Enforce one variable per comparison: the same creative across different audiences, or different creatives into the same audience — never both moving at once, or the result reads as noise.
3. Spin up each cell as its own $1/day ad set using the naming scheme (Geo–Age–Interest–Custom + creative ID) so reports self-label.
4. Run 10–30 cells simultaneously. A month of serial testing collapses into one $1/day week — that is the entire economic argument of the method.
5. Launch together and hold discipline: same start time, 7 days untouched, no peeking-and-poking edits.
6. Log every cell before launch — hypothesis, audience, creative, start date. An unrecorded test is wasted spend even when it wins.
7. At day 7, route results to cost-per-result analysis, then issue each cell a verdict: kill, keep, scale, or switch-boost.

## Definition of done (QA checklist)
- [ ] Test matrix documented with a written hypothesis per cell
- [ ] Every comparison isolated to one variable; naming scheme applied throughout
- [ ] All cells launched simultaneously at $1/day and left untouched for 7 days
- [ ] Test log complete; day-7 review held with a verdict recorded per cell
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run (an ideal candidate: a 12–20 cell matrix for a local service brand, e.g., Superior Fence & Rail territories × two winning videos).

## Run on a persistent agent (Fable 5)
This is a long-horizon loop built for a persistent agent (Claude Fable 5 or comparable OpenAI/Google models): write every hypothesis, launch all cells together, hold the 7-day window, then return for verdicts — and the run only counts when the Definition of done fully passes with a kill/keep/scale/switch verdict per cell; a skipped day-7 review is a failed run.
It self-verifies the one-variable rule on every comparison before launch and carries the test log in memory, so each week's matrix builds on every prior week instead of re-testing known losers.
Log one meta-article example per matrix so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /dad
- Related: /social-amplification (Stage 5: Amplification) · /nine-triangles (MAA — the loop these tests feed)
- Run order (DAD core): set-1-day-budget-per-ad-set → **run-multiple-simultaneous-tests** → analyze-cost-per-result-and-engagement
