---
name: map-what-ring-specific-content
description: Define the outer ring of the Topic Wheel — the specific topics, customer questions, examples, and stories — so the brand has a concrete, mission-anchored content backlog.
category: Strategy & Measurement
stage: —
definitive_article: /topic-wheel
status: complete
---

# Map WHAT ring (specific content)

**Use this when** the WHY center and HOW spokes exist and you need the outer ring — the actual content pieces — so nobody ever again asks "what should we post?"

## Inputs
- The completed WHY ring and HOW spokes
- Real customer questions: sales calls, support emails, social comments, reviews, search queries
- Real proof assets: client stories, before/afters, mistakes seen in the field

## Steps
1. Define the ring: the WHAT is the outer ring of the Topic Wheel — specific topics, examples, and content pieces. Each WHAT item hangs off exactly one HOW spoke, and each should be answerable in a single one-minute video.
2. For each HOW spoke, harvest real customer questions verbatim — what people actually ask before, during, and after buying. Verbatim beats invented; customers' words are the keywords.
3. Add example-type items per spoke: a client story, a common mistake, a how-to, a price/cost answer, a "what to expect" walkthrough. Aim for 5–10 WHAT items per spoke.
4. Scope-check every item: if it can't be answered in about a minute, split it; if it's too thin to sustain a minute, merge it into a neighbor.
5. Trace-check every item: WHAT → its HOW spoke → the WHY must read as a straight line. Items that don't trace get cut, however clickable they look.
6. Record the populated wheel as the master topic inventory — the direct input for use-for-content-planning-and-video-topics.
7. Measure it: track WHAT items recorded vs remaining per spoke; the wheel is a backlog, and an untouched ring after a month means planning isn't connected to production.

## Definition of done (QA checklist)
- [ ] Every HOW spoke has 5–10 WHAT items
- [ ] Each item phrased as a real customer question or concrete example (verbatim where possible)
- [ ] Each item scoped to one-minute-video size
- [ ] Every item traces WHAT → HOW → WHY with no orphans
- [ ] Wheel saved as the master topic inventory for content planning
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. (The hub at /topic-wheel links live examples; pull the closest match into this slot.)

## Run on a persistent agent (Fable 5)

This is where a max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) outworks a human: it reads every sales call note, support email, comment, and review to harvest customer questions verbatim, and loops until the Definition of done fully passes — 5–10 items per spoke, each one-minute-scoped, each tracing WHAT → HOW → WHY with zero orphans.
It self-verifies by re-running the trace and scope checks on the finished ring before saving it as the master topic inventory.
Memory keeps the wheel a living backlog: recorded-vs-remaining counts per spoke are compared against prior months in the MAA loop — a true memory cycle — and a meta-article example is logged each run.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /topic-wheel
- Related, in run order: map-why-ring-core-purpose, map-how-ring-methods, use-for-content-planning-and-video-topics, /one-minute-video-guide
