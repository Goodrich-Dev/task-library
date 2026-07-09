---
name: analyze-why-underperformers-fail
description: Diagnose every underperforming campaign or content piece into one of three root causes — creative, targeting, or offer — so the fix targets the actual failure instead of guessing.
category: Strategy & Measurement
stage: —
definitive_article: GAP — to be written
status: needs-work
---

# Analyze why underperformers fail

**Use this when** the "what isn't working" list exists and you must decide what to fix before deciding what to kill — diagnosis comes between verdict and action.

## Inputs
- The underperformer list with metrics (from show-whats-working-and-what-isnt)
- Funnel-level data per item: impressions, CTR/engagement, watch time, landing page conversion rate
- The item's original GCT brief (goal, content, targeting as stated at launch)

## Steps
1. Take each underperformer one at a time and locate where the funnel breaks — the failure point tells you which of the three causes to suspect.
2. Test **creative** first: weak hook, low watch time (people bail in the first seconds), low CTR despite reaching the right audience. If the right people see it and don't care, the creative failed.
3. Test **targeting** next: decent creative metrics but wrong audience — irrelevant comments, high frequency with falling response, engagement from people who could never buy. If the wrong people see it, targeting failed.
4. Test **offer** last: strong clicks and traffic but no conversions — the landing page promise, price, or proof breaks at the moment of commitment. If the right people care but won't act, the offer failed.
5. Classify every item into exactly one primary bucket — creative, targeting, or offer — with the one metric that justified the call. "All three" is not a diagnosis; pick the binding constraint.
6. Recommend per bucket: creative → swap in a greatest-hit or re-cut the hook; targeting → switch audience (switch boost per /dad); offer → fix the landing page or promise. If the item has been diagnosed and retried once already, recommend kill.
7. Feed the diagnoses into the Friday MAA report and the kill/scale decision.

## Definition of done (QA checklist)
- [ ] Every underperformer assigned exactly one primary cause: creative, targeting, or offer
- [ ] Each diagnosis cites the metric that proves the failure point
- [ ] Each diagnosis carries a concrete fix-or-kill recommendation
- [ ] Repeat offenders (already diagnosed once) marked for kill, not endless iteration
- [ ] Diagnoses delivered into the Friday MAA report
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) walks every underperformer through the creative → targeting → offer test sequence with the funnel data in hand, and loops until the Definition of done fully passes — exactly one primary cause per item, each with its proving metric and a fix-or-kill recommendation, no "all three" cop-outs.
It self-verifies by checking each diagnosis against the item's original GCT brief rather than a remembered version of it.
Memory is what makes the repeat-offender rule enforceable: the agent compares this cycle's list against prior periods' diagnoses — a true MAA memory cycle — marks second-timers for kill, and logs a meta-article example each run.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written (parent methodology: /maa; framework context: /nine-triangles)
- Related, in run order: show-whats-working-and-what-isnt, kill-underperformers-scale-winners, /dad
