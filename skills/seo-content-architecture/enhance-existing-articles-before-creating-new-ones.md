---
name: enhance-existing-articles-before-creating-new-ones
description: "Force a search-first discipline on all content proposals — improve the page that already owns a concept instead of publishing thin new competitors, keeping effort on Greatest Hits rather than net-new bets."
category: SEO & Content Architecture
stage: —
definitive_article: /seo-tree
status: complete
---

# Enhance existing articles before creating new ones

**Use this when** anyone — human or agent — proposes a new article, and before any new draft is approved.

## Inputs
- The proposed topic/concept, named in one line
- The SEO Tree map and WordPress search access
- The Nine Requirements checklist from the Task Library Standard

## Steps
1. Search first: check the tree map, WordPress search, and a site: query for the concept — find every page that already touches it.
2. If a hub already owns the concept, **enhance it instead of publishing a competitor**: sharpen the definition, add new linked examples with notes, refresh data, strengthen the E-E-A-T section, improve the above-the-fold diagram.
3. If coverage exists but is scattered with no clear owner, pick (or build) one hub and fold the fragments into it — consolidate and 301-redirect the rest.
4. Only create a new page when nothing on the site owns the concept — and then build it as a definitive article to the Nine Requirements, not as another thin post.
5. Apply the content-strategy ratio: roughly 90% of effort on proven existing content (Greatest Hits), 10% on new experiments.
6. Re-verify the enhanced page against the Nine Requirements and republish in compliance with /blog-posting-guidelines.
7. Record the decision (enhance / consolidate / create new) in the content inventory so the tree map stays true.

## Definition of done (QA checklist)
- [ ] Documented search performed before any new page was approved
- [ ] No new page published on a concept an existing hub already owned
- [ ] Enhanced page re-checked against the Nine Requirements (definition, process, examples, cross-links, CTA, guidelines, short URL, diagram, E-E-A-T)
- [ ] Decision logged in the inventory; tree map current
- [ ] Linked back to the definitive article (/seo-tree) and relevant siblings

## Example(s)
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first enhance-vs-create decision is executed.

## Run on a persistent agent (Fable 5)
Run the search-first gate as a standing rule: a persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) intercepts every content proposal, performs the documented search, and — when enhancing — loops the rewrite against the Nine Requirements until all nine pass, not until it looks better.
Its memory holds the enhance/consolidate/create-new decision log, so no concept is ever re-litigated and the 90/10 Greatest Hits ratio is enforced across runs, not per session.
Each executed decision gets logged as a meta-article example via /meta-article-prompt-template.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /seo-tree
- Related: fit-every-new-piece-into-the-tree-structure (the publish-time gate) · remove-duplicate-thin-pages · replace-ai-looking-content-with-real-eeat · /blog-posting-guidelines
