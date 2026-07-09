---
name: step-3-identify-money-pages-and-orphan-pages
description: "Mark the revenue-driving pages that need internal-link support and the orphan pages that need connecting, producing the prioritized source-to-target link plan that Step 4 executes."
category: SEO & Content Architecture
stage: —
definitive_article: /internal-linking
status: complete
---

# Step 3: Identify money pages and orphan pages

**Use this when** the inventory (Step 1) and taxonomy (Step 2) are clean, and it is time to decide where links should flow before creating any.

## Inputs
- The Step 1 inventory with GCT, tree roles, and links-in/out per URL
- Knowledge of what actually drives revenue: services, courses, lead capture
- Crawl or LinkWhisper inlink data

## Steps
1. From the inventory, mark the **money pages** — the pages that drive revenue: service pages, course pages, lead-capture pages, key conversion paths.
2. Mark the **orphan pages** — every URL with zero internal links pointing to it.
3. Rank money pages by gap: which carry the most revenue weight with the least internal-link support.
4. For each money page, list the leaves and branches topically qualified to send it a link — use each candidate's GCT as the relevance test; no relevance, no link.
5. Give every orphan a disposition: becomes a linking source for a money page, gets connected to its branch, or goes to the consolidation skills (thin/duplicate).
6. Output two prioritized lists — "money pages needing links" and "orphans needing homes" — as the direct input to Step 4.

## Definition of done (QA checklist)
- [ ] Every money page identified and ranked by link-support gap
- [ ] Every orphan identified with a named disposition
- [ ] Source → target link plan drafted with GCT-based relevance justifications
- [ ] Both lists handed to Step 4 in priority order
- [ ] Linked back to the definitive article (/internal-linking) and relevant siblings

## Example(s)
- The /internal-linking definitive article shows this money-page/orphan analysis as its Step 3 on blitzmetrics.com.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the next link-planning round.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) loops until every money page is ranked by link-support gap and every orphan carries a named disposition — no "unclassified" leftovers — and self-verifies each row of the link plan by re-checking its GCT relevance justification before handing anything to Step 4.
Memory makes each plan smarter: prior runs show which source pages and anchor patterns actually moved targets, so new plans start from evidence, not guesses.
Each planning round logs a meta-article example via /meta-article-prompt-template.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /internal-linking
- Related (run order): step-2-fix-categories-and-tags-in-wordpress (before) → step-4-create-links-with-proper-anchor-text-and-placement (after) · identify-and-eliminate-orphan-standalone-articles (/seo-tree) · remove-duplicate-thin-pages
