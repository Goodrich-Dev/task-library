---
name: how-to-process-videos-via-marketscale
description: "Create the missing definitive article — the SOP for processing videos through MarketScale and distributing them across platforms, documented as an alternative lane in the Content Factory's Process stage (Low-priority gap)."
category: Gaps & Tasks to Create
stage: —
definitive_article: "GAP — to be written"
status: gap
---

# How to Process Videos via MarketScale

**Use this when** MarketScale runs live only in operators' heads because no hub documents the workflow — this skill creates the definitive article that closes the gap. **Priority: Low.**

## Inputs
- Real MarketScale runs to document: how raw video goes in, what processing happens, what distribution comes out — the article documents the actual platform workflow, never invented features
- Every existing blitzmetrics.com article that mentions MarketScale or video processing/distribution
- The Content Factory Process-stage context: the existing lane is Google Drive + Descript (upload → transcribe → article, per /blog-posting-guidelines)
- WordPress access (Gutenberg) and the Nine Requirements checklist

## Steps
1. **Identify the concept** and gather every existing page mentioning MarketScale — the hub organizes them, it does not replace them.
2. **Write the definition** (first two paragraphs): what processing videos via MarketScale is — platform-based video processing and multi-platform distribution — what it is not, and when to use it versus the standard Descript lane.
3. **Document the complete process from real runs**: getting raw video into MarketScale; the processing workflow on the platform; the distribution outputs and which platforms they reach; how outputs hand back into the Content Factory (clips, transcripts, posts feeding the /blog-posting-guidelines pipeline); and the decision rule for routing a video to MarketScale versus Descript. Capture from actual operator runs — this is tribal knowledge being written down for the first time.
4. **Link every real example** of a MarketScale-processed video, each with a 1–2 sentence note on the outcome.
5. **Cross-link related definitive articles**: /content-factory (the pipeline this is a lane of) and /blog-posting-guidelines (the downstream steps).
6. **Add the course/service CTA** near the bottom.
7. **Set a short, memorable URL** redirecting to the hub — never to the homepage or a case study.
8. **Add an above-the-fold clickable diagram**: raw video → MarketScale processing → multi-platform distribution → Content Factory handoffs.
9. **Add E-E-A-T**: real distribution results and practitioner testimonials — highest authority first.
10. **Publish** as a Post in the Definitive Articles category (Gutenberg), then **run the Meta-Article Prompt** (/meta-article-prompt-template) for the companion meta-article.
11. Flip the dashboard status from Gap (Red), then update this skill's `definitive_article` field and the Content Factory — Process task "Process videos via MarketScale" (also a gap) to point at the new hub.

## Definition of done (QA checklist)
- [ ] Article meets all Nine Requirements, documented from real runs with no invented platform features
- [ ] The MarketScale-vs-Descript routing decision is stated concretely
- [ ] Published as a Post in the Definitive Articles category via the standard block editor
- [ ] Complies with Blog Posting Guidelines (title <60 chars, meta <160, keyword in first paragraph, no stock images, no AI-fluff)
- [ ] Companion meta-article published; both MarketScale gap tasks updated from GAP to the live short URL
- [ ] Linked back to related hubs: /content-factory, /blog-posting-guidelines

## Example(s)
- Example needed — run the Meta-Article Prompt after first publish; /meta-article-prompt-template (29 linked examples) is the model.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) runs the full 10-step creation process above to completion — publish, companion meta-article, and Gap→live status flip — documenting only from real MarketScale runs, never invented platform features; if no run is on record, capturing one is the loop's first job.
It loops QA until every Definition-of-done box passes, including the MarketScale-vs-Descript routing rule stated concretely.
Memory logs every video processed afterward as a fresh linked example, so the hub stays current with the actual workflow.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written (this skill creates it)
- Related: /content-factory (Process stage) · /blog-posting-guidelines (the downstream pipeline) · how-to-grade-an-article-using-jennifer (the other Process-stage gap)
