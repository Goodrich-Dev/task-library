---
name: step-2-fix-categories-and-tags-in-wordpress
description: "Rebuild WordPress taxonomy so categories mirror the SEO Tree branches and tags carry cross-cutting attributes, making the site's structure legible to readers, Google, and agents querying the REST API."
category: SEO & Content Architecture
stage: —
definitive_article: /internal-linking
status: complete
---

# Step 2: Fix categories and tags in WordPress

**Use this when** Step 1's inventory is complete and the taxonomy is a mess — overlapping categories, one-off tags, posts filed nowhere meaningful.

## Inputs
- The Step 1 content inventory with each page's SEO Tree role
- WordPress admin access (Posts → Categories / Tags)
- The site's SEO Tree map (branches list)

## Steps
1. Export the current category and tag lists with post counts.
2. Rebuild categories to mirror the SEO Tree: **one category per branch — categories ARE the branches.** Definitive articles belong in the Definitive Articles category.
3. Reassign every post to the category matching its tree role from the Step 1 inventory.
4. Use tags only for cross-cutting attributes, never hierarchy: Content Factory stage tags (`Stage: Produce | Process | Post | Promote`) and `Topic:` tags — so agents can pull, e.g., `category=definitive-articles&tag=stage-process` from the REST API.
5. Delete or merge empty, duplicate, and one-off taxonomy terms.
6. Spot-check the category archive pages — each should read like a coherent branch of the tree, not a junk drawer.

## Definition of done (QA checklist)
- [ ] Categories map 1:1 to SEO Tree branches; definitive articles in the Definitive Articles category
- [ ] Every post assigned to its correct branch category
- [ ] Stage and Topic tags applied; tags carry attributes, not hierarchy
- [ ] Zero empty, duplicate, or one-off taxonomy terms remain
- [ ] A REST API query by category + tag returns the expected post set; linked back to /internal-linking

## Example(s)
- The /internal-linking definitive article documents this taxonomy pass as run on blitzmetrics.com — categories as branches is its Step 2.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the next taxonomy rebuild.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) reassigns posts and prunes terms in a loop until categories map 1:1 to SEO Tree branches and zero empty, duplicate, or one-off terms remain — then self-verifies with the Definition of done's own test: a REST API query by category + tag must return exactly the expected post set.
Taxonomy decisions persist in memory, so every future post gets filed by precedent instead of re-inventing categories.
Each rebuild logs a meta-article example via /meta-article-prompt-template.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /internal-linking
- Related (run order): step-1-inventory-content-and-establish-gct-per-page (before) → step-3-identify-money-pages-and-orphan-pages (after) · fit-every-new-piece-into-the-tree-structure (/seo-tree) · /blog-posting-guidelines (Step 13: categorize and tag)
