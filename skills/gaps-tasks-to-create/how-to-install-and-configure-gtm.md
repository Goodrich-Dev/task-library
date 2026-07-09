---
name: how-to-install-and-configure-gtm
description: "Create the missing definitive article — a step-by-step guide to installing and configuring a Google Tag Manager container on any website (High-priority gap; also closes the open Digital Plumbing GTM task)."
category: Gaps & Tasks to Create
stage: —
definitive_article: "GAP — to be written"
status: gap
---

# How to Install and Configure GTM

**Use this when** an agent or operator needs the GTM install SOP and finds no hub — this skill creates the definitive article that closes the gap. **Priority: High.**

## Inputs
- At least one real GTM container installation to document: screenshots, decisions, gotchas
- Every existing blitzmetrics.com article that mentions GTM — the hub organizes them, it does not replace them
- WordPress access (Gutenberg block editor) and /blog-posting-guidelines open
- The Nine Requirements checklist from the Task Library Standard

## Steps
1. **Identify the concept** and collect every existing page mentioning GTM — these become organized spokes, never competitors.
2. **Write the definition** (first two paragraphs): what GTM is — a container that lets you add tracking without editing code — what it is not, and who needs it.
3. **Document the complete process**, detailed enough to follow without further instruction: create the GTM account and container; install the container snippet site-wide so it loads on every page; publish the container; verify it fires on every page (mirroring the /website-qa-audit Layer 1 check); hand off so future tags ship without code edits.
4. **Link every real example** of an install — each with a 1–2 sentence note on why it is relevant.
5. **Cross-link related definitive articles**: /digital-plumbing (GTM is core plumbing) and /website-qa-audit (the verification layer).
6. **Add the course/service CTA** near the bottom — never as the core content.
7. **Set a short, memorable URL** redirecting to the hub — never to the homepage or a case study.
8. **Add an above-the-fold clickable diagram** of the install flow (multi-step concept, so the diagram is required and must be visible without scrolling).
9. **Add E-E-A-T**: real install results, practitioner testimonials, talks or media — highest authority first.
10. **Publish** as a Post in the Definitive Articles category (Gutenberg, not a page builder), then **run the Meta-Article Prompt** (/meta-article-prompt-template) to document how the article was built.
11. Flip the dashboard status from Gap (Red), then update this skill's `definitive_article` field and the Digital Plumbing task "Install Google Tag Manager container" to point at the new hub.

## Definition of done (QA checklist)
- [ ] Article meets all Nine Requirements (definition, complete process, every example, cross-links, CTA, guidelines compliance, short URL, above-the-fold diagram, E-E-A-T)
- [ ] Published as a Post in the Definitive Articles category via the standard block editor
- [ ] Complies with Blog Posting Guidelines (title <60 chars, meta <160, keyword in first paragraph, no stock images, no AI-fluff)
- [ ] Companion meta-article published and linking up to the new hub
- [ ] This skill.md and the related Digital Plumbing gap task updated from GAP to the live short URL
- [ ] Linked back to related hubs: /digital-plumbing, /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first publish; /meta-article-prompt-template (29 linked examples) sets the bar for example volume.
- /internal-linking is the model hub that ships with its own skill file for AI agents — copy its pattern.

## Run on a persistent agent (Fable 5)
Give this gap to a persistent, max-effort agent (Claude Fable 5 or a comparable OpenAI/Google frontier model) and have it run the full 10-step creation process above to completion — definition through publish, companion meta-article, and the Gap→live status flip — not a draft handed back for someone else to finish.
It loops QA against the Definition of done until every box passes (all Nine Requirements, not seven of nine), self-verifying on the live post: short-URL redirect, category, title/meta lengths, diagram above the fold.
Memory carries the documented install's screenshots and gotchas forward, so the GA4 article — which installs through GTM — builds on this run instead of starting cold.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written (this skill creates it)
- Related: /digital-plumbing · /website-qa-audit · /blog-posting-guidelines · how-to-configure-ga4-with-internal-traffic-filtering (run next — GA4 installs through GTM)
