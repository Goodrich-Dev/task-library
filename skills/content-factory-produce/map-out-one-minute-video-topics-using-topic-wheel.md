---
name: map-out-one-minute-video-topics-using-topic-wheel
description: Use the Topic Wheel's WHY/HOW/WHAT rings to turn a brand's purpose and real customer questions into a systematic one-minute video recording queue.
category: Content Factory — Produce
stage: Produce
definitive_article: /topic-wheel
status: complete
---

# Map out one-minute video topics using Topic Wheel

**Use this when** recording sessions keep stalling on "what should I talk about?" — the Topic Wheel replaces improvised topic-picking with a system.

## Inputs
- The brand's mission/WHY (from SAE Stage 2 Goals or the WHY video work)
- Sources of real customer questions: sales calls, support emails, social comments, conference Q&A, FAQ pages
- A way to diagram three concentric rings (whiteboard, doc, or sheet)
- The Content Library tracker, where the output queue lives

## Steps
1. Draw three concentric rings. Center/WHY ring: the core purpose and mission — one or two statements, taken from the brand's WHY, not invented.
2. Middle/HOW ring: the methods, frameworks, and approaches the brand actually uses (e.g., for Local Service Spotlight: Dollar a Day, Content Factory, Digital Plumbing). 3–6 spokes.
3. Outer/WHAT ring: specific topics and real customer questions. Harvest them verbatim from the input sources — the customer's wording becomes the video prompt and, later, the SEO keyword.
4. Connect every WHAT spoke upward to a HOW spoke, and every HOW to the WHY. A question that connects to no method is off-topic; park it.
5. Sanity-check against the SEO Tree: HOW spokes should correspond to trunks/branches on the website so every video has a home when it becomes an article.
6. Convert the WHAT ring into the recording queue: one row per question in the Content Library tracker, prioritized by how often customers actually ask it.
7. Hand the queue to recording (`record-one-minute-videos` or `batch-record-50-raw-clips-in-one-session`).
8. Refresh the wheel monthly: add new questions from comments, calls, and conference Q&A; retire answered ones.

## Definition of done (QA checklist)
- [ ] All three rings populated: WHY (purpose), HOW (methods), WHAT (specific questions)
- [ ] Every WHAT item is a real customer question with a traceable source, not a brainstormed guess
- [ ] Every WHAT connects to a HOW, and every HOW to the WHY — no orphan topics
- [ ] WHAT ring exported as a prioritized recording queue in the Content Library tracker
- [ ] Wheel aligns with the site's SEO Tree trunks
- [ ] Linked back to the definitive article and relevant siblings

## Example(s)
- The WHY/HOW/WHAT ring construction is documented with examples at /topic-wheel, which also drives the Strategy & Measurement topic-wheel tasks.
- Example needed for a fresh client wheel — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)

A persistent agent (Claude Fable 5, or comparable OpenAI/Google models that loop and hold memory) harvests questions verbatim from every input source, wires each WHAT to a HOW to the WHY, and loops until no orphan topics remain and the prioritized queue is exported — a wheel with unconnected spokes fails its own Definition of done. Memory holds the living wheel, so the monthly refresh adds and retires questions instead of redrawing the rings. Log a meta-article example per refresh so the wheel's evolution stays documented.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /topic-wheel
- Related: /one-minute-video-guide (what the queue feeds), /seo-tree (where the articles land), /social-amplification (Stage 3 content planning)
- Sibling skills, in run order: this → `record-one-minute-videos` → `batch-record-50-raw-clips-in-one-session` → `create-a-3-minute-why-video`
