---
name: how-to-grade-an-article-using-jennifer
description: "Create the missing definitive article — the guide to scoring article quality with the Jennifer grading system, the quality gate in the Content Factory's Process stage (Low-priority gap)."
category: Gaps & Tasks to Create
stage: —
definitive_article: "GAP — to be written"
status: gap
---

# How to Grade an Article Using Jennifer

**Use this when** articles ship ungraded because no hub documents the Jennifer grading system — this skill creates the definitive article that closes the gap. **Priority: Low.**

## Inputs
- Real Jennifer grading runs to document: actual inputs, actual scores, actual rework decisions — the article documents the real system, never invented criteria
- Every existing blitzmetrics.com article that mentions Jennifer or article grading
- The Content Factory Process-stage context: grading sits alongside proofreading (Step 11 of /blog-posting-guidelines)
- WordPress access (Gutenberg) and the Nine Requirements checklist

## Steps
1. **Identify the concept** and gather every existing page mentioning Jennifer grading — the hub organizes them, it does not replace them.
2. **Write the definition** (first two paragraphs): what grading with Jennifer is — a quality score on a draft before it posts — what it is not (a replacement for editorial judgment), and who runs it.
3. **Document the complete process from real runs**: what Jennifer takes as input (the draft article); how to submit it; what the score covers and the pass threshold; what to do with a failing grade — fix and re-grade before posting; where the gate sits in the pipeline (after proofreading, before WordPress posting per /blog-posting-guidelines). Capture this from actual operator runs — the gap exists because tribal knowledge was never written down.
4. **Link every real example** of a graded article, each with a 1–2 sentence note (score, what changed, outcome).
5. **Cross-link related definitive articles**: /content-factory (the pipeline it gates) and /blog-posting-guidelines (the steps it sits between).
6. **Add the course/service CTA** near the bottom.
7. **Set a short, memorable URL** redirecting to the hub — never to the homepage or a case study.
8. **Add an above-the-fold visual**: the grade-rework-pass loop as a clickable diagram.
9. **Add E-E-A-T**: real grade reports and before/after article improvements — highest authority first.
10. **Publish** as a Post in the Definitive Articles category (Gutenberg), then **run the Meta-Article Prompt** (/meta-article-prompt-template) for the companion meta-article.
11. Flip the dashboard status from Gap (Red), then update this skill's `definitive_article` field and the Content Factory — Process task "Grade article using Jennifer" (also a gap) to point at the new hub.

## Definition of done (QA checklist)
- [ ] Article meets all Nine Requirements, documented from real runs with no invented criteria
- [ ] Pass threshold and rework loop stated concretely enough to follow without asking anyone
- [ ] Published as a Post in the Definitive Articles category via the standard block editor
- [ ] Complies with Blog Posting Guidelines (title <60 chars, meta <160, keyword in first paragraph, no stock images, no AI-fluff)
- [ ] Companion meta-article published; both Jennifer gap tasks updated from GAP to the live short URL
- [ ] Linked back to related hubs: /content-factory, /blog-posting-guidelines

## Example(s)
- Example needed — run the Meta-Article Prompt after first publish; /meta-article-prompt-template (29 linked examples) is the model.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) runs the full 10-step creation process above to completion — publish, companion meta-article, and Gap→live status flip — but its first loop is evidence-gathering: collect real Jennifer grading runs (inputs, scores, rework decisions) and refuse to draft from invented criteria.
It loops QA until every Definition-of-done box passes, including the pass threshold and rework loop stated concretely enough to follow without asking anyone.
Graded-article records accumulate in memory across runs, growing the hub's example base with every gate the system runs.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written (this skill creates it)
- Related: /content-factory (Process stage) · /blog-posting-guidelines (sits after Step 11 proofreading) · how-to-process-videos-via-marketscale (the other Process-stage gap)
