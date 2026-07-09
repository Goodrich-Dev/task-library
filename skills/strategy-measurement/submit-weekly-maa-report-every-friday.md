---
name: submit-weekly-maa-report-every-friday
description: Deliver the weekly MAA report every Friday — same metrics, what's working vs not, why, and the actions taken — so clients and the team see decisions, not just numbers.
category: Strategy & Measurement
stage: —
definitive_article: GAP — to be written
status: needs-work
---

# Submit weekly MAA report every Friday

**Use this when** it's Friday — the report ships every week, on the same day, whether the news is good or bad. No-skip is the rule that makes it work.

## Inputs
- Access to the measurement stack: analytics, search console, ad platforms, CRM/revenue
- The standing metric set and targets (CPA/ROAS, leads, traffic) agreed with the client/team
- Last Friday's report, so this week compares like-for-like

## Steps
1. Pull the same standing metric set as every prior week, covering the full pipeline — content published → rankings → traffic → leads/revenue — plus active campaign performance.
2. Compare against last week and against target; flag anything materially up or down.
3. Split the page into two sections: **What's working** (with the metric evidence) and **What isn't** (same standard of evidence) — see show-whats-working-and-what-isnt.
4. For each underperformer, add a one-line diagnosis — creative, targeting, or offer — per analyze-why-underperformers-fail.
5. List the actions taken or proposed this week: what was killed, what was scaled, what gets iterated (kill-underperformers-scale-winners), each with an owner and date.
6. Close with the top 3–5 recommendations for the next 7 days, in priority order.
7. Send it Friday, same channel, same format every week; archive the report so the trail of decisions is auditable.

## Definition of done (QA checklist)
- [ ] Report sent on Friday — not Monday — in the standing format
- [ ] Same metric definitions as last week (no metric-shopping)
- [ ] Both sections present: what's working AND what isn't, each with evidence
- [ ] Every underperformer has a creative/targeting/offer diagnosis
- [ ] Every action has an owner and a date; top 3–5 next-7-day recommendations included
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)

The no-skip rule is exactly what a persistent agent (Claude Fable 5 or comparable OpenAI/Google models) guarantees: it runs every Friday on schedule, pulls the same standing metric set, and loops until the Definition of done fully passes — both sections present, every underperformer diagnosed, every action owned and dated — before the report sends.
It self-verifies against the QA checklist and refuses to ship a numbers-only report.
Because last Friday's archived report lives in its memory, the comparison is genuinely like-for-like — the MAA loop runs as a true memory cycle against prior weeks — and a meta-article example is logged from each run.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written (parent methodology: /maa; framework context: /nine-triangles)
- Related, in run order: show-whats-working-and-what-isnt, analyze-why-underperformers-fail, kill-underperformers-scale-winners, measure-content-rankings-traffic-revenue
