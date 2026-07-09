---
name: measure-content-rankings-traffic-revenue
description: Track the full pipeline from content published to rankings to traffic to revenue in one table, so you can see exactly which stage is broken instead of arguing about "marketing."
category: Strategy & Measurement
stage: —
definitive_article: GAP — to be written
status: needs-work
---

# Measure content → rankings → traffic → revenue

**Use this when** content is being produced but nobody can prove it makes money — or when setting up the standing metric set for the weekly MAA report.

## Inputs
- Publishing data: posts/videos shipped per week (the Content Factory output log)
- Google Search Console (impressions, positions, clicks) and analytics (organic sessions)
- Conversion and revenue data: leads, calls, bookings, sales — attributed to pages where possible

## Steps
1. Define the four pipeline stages and one metric each: **Content** (pieces published per week), **Rankings** (keywords ranking / average position in Search Console), **Traffic** (organic sessions to those pages), **Revenue** (leads or sales attributed to them).
2. Build one table — rows are content pieces or topic clusters, columns are the four stages — and update it on the same weekly cadence as the MAA report.
3. Read the table for the break point, stage by stage. Content but no rankings: placement/structure problem — check the piece's position and links on the SEO Tree (/seo-tree).
4. Rankings but no traffic: the snippet problem — titles and meta descriptions aren't earning the click for the positions held.
5. Traffic but no revenue: the conversion problem — the page's offer and conversion path fail visitors who arrived interested (an offer diagnosis, same bucket as in analyze-why-underperformers-fail).
6. Aim the week's actions at the single broken stage instead of "more content" by default — more input doesn't fix a blocked pipe.
7. Report the four stage-metrics as a connected story in every Friday MAA report, with trend arrows week over week.

## Definition of done (QA checklist)
- [ ] All four stages have a named metric, a data source, and a current value
- [ ] One pipeline table exists and is updated weekly (same cadence as the MAA report)
- [ ] The current break point stage is identified in writing
- [ ] This week's actions target the broken stage, not a healthy one
- [ ] Pipeline story included in the Friday MAA report with trends
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) owns the pipeline table: it refreshes all four stages — content, rankings, traffic, revenue — from the live sources each week and loops until the Definition of done fully passes, including the break-point stage named in writing and the week's actions aimed at it.
It self-verifies that every stage has a metric, a data source, and a current value before reporting — no blank cells shipped.
Because prior weeks' tables persist in memory, the trend arrows are real period-over-period comparisons — the MAA loop as a true memory cycle — and a meta-article example is logged each run.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written (parent methodology: /maa; framework context: /nine-triangles)
- Related, in run order: maa-cycle-metrics-analysis-action, submit-weekly-maa-report-every-friday, /seo-tree, /content-factory
