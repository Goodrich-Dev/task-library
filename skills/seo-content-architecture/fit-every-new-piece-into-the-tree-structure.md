---
name: fit-every-new-piece-into-the-tree-structure
description: "Classify every new piece of content as a leaf, a branch, or an enhancement to an existing hub before it publishes, so nothing ships outside the SEO Tree and no page ever competes with its own hub."
category: SEO & Content Architecture
stage: —
definitive_article: /seo-tree
status: complete
---

# Fit every new piece into the tree structure

**Use this when** anything new is about to be published — article, case study, landing page — and its place in the hierarchy has not been decided yet.

## Inputs
- The site's current SEO Tree map (output of the hierarchy-mapping skill)
- The draft or content brief, with its concept named
- WordPress category list (categories = SEO Tree branches)

## Steps
1. Before drafting or publishing, open the SEO Tree map and name the single concept this piece serves.
2. Find the branch that owns that concept on the map.
3. If a hub already owns it and the new piece would restate or compete with it: **do not publish a second page** — that is content vandalism. Enhance the existing hub instead (see enhance-existing-articles-before-creating-new-ones).
4. If the piece is new evidence — a case study, example, or meta-article — it is a **leaf**: assign exactly one parent branch.
5. If it is a genuinely new core concept with no owner anywhere on the site, it earns a new **branch**: a definitive article built to the Nine Requirements, not a quick post.
6. Set the WordPress category to the parent branch and apply the correct stage/topic tags.
7. Add the upward link(s) in body copy — 3–6 word descriptive anchor text pointing to the parent branch — before hitting publish.
8. Update the tree map so the inventory stays current.

## Definition of done (QA checklist)
- [ ] Piece classified (leaf / new branch / enhancement) before publication, with the decision recorded
- [ ] Exactly one parent branch assigned; WordPress category matches it
- [ ] At least one upward in-body link to the parent with descriptive anchor text
- [ ] No second page published on a concept an existing hub already owns
- [ ] Tree map updated; complies with Blog Posting Guidelines (/blog-posting-guidelines)

## Example(s)
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first real placement decision.
- The /seo-tree hub defines the leaf/branch logic this skill applies piece by piece.

## Run on a persistent agent (Fable 5)
This is a publish-time gate, so run it as a standing job: a persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) classifies every new draft — leaf, new branch, or enhancement — and refuses to ship anything until all five Definition-of-done boxes pass, not four.
It keeps the SEO Tree map in memory across runs, so each placement decision builds on the last and the map never goes stale.
Every run logs the placement decision as a meta-article example (/meta-article-prompt-template) before closing.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /seo-tree
- Related: map-content-hierarchically-root-trunk-branches-leaves (run first) · link-leaves-to-branches-branches-to-trunk · enhance-existing-articles-before-creating-new-ones · step-2-fix-categories-and-tags-in-wordpress (/internal-linking)
