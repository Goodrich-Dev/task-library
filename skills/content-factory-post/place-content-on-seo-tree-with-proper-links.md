---
name: place-content-on-seo-tree-with-proper-links
description: Position the new piece at its correct spot in the SEO Tree hierarchy and wire the upward internal links (leaf → branch → trunk → root) before it goes live.
category: Content Factory — Post
stage: Post
definitive_article: /seo-tree
status: complete
---

# Place content on SEO Tree with proper links

**Use this when** any new piece is about to publish and must be located in the site's content hierarchy — or when an existing post is found floating with no parent.

## Inputs
- The site's SEO Tree map: homepage root → topic trunks → subtopic branches → detail leaves
- The draft post with category set (Step 13) and LinkWhisper pass done (Step 14b)
- The site's content inventory with GCT per major page (/internal-linking Step 1)

## Steps
1. Classify the piece: is it a **leaf** (one specific question/detail), a **branch** (subtopic hub), or trunk-level? Most Content Factory articles are leaves.
2. Identify its parent: which branch does this leaf hang from, which trunk does that branch support? Confirm against the category assigned in Step 13 — category and tree position must agree.
3. Add the **upward links**: the leaf links to its branch page, and (where context allows) to the trunk. Upward links are mandatory; they tell Google what supports what.
4. Add a link **from** the parent branch or a strong sibling down/across to the new leaf, so the piece is reachable and not an orphan.
5. Check you are not committing content vandalism: if a definitive article already owns this concept, this piece must link up to that hub — never compete with it. New thin pages lose to enhancing existing ones (/seo-tree: enhance before creating).
6. If no logical parent exists, halt and flag it: either the tree is missing a branch (propose it) or the piece doesn't belong on this site.
7. Record the placement in the content inventory so future audits can find orphans by diff.

## Definition of done (QA checklist)
- [ ] Piece classified (leaf/branch) with an explicit parent on the SEO Tree
- [ ] Upward link(s) to branch/trunk live in body copy with descriptive anchors
- [ ] At least one inbound link from parent or sibling — zero orphan risk
- [ ] No competing page created against an existing definitive article hub
- [ ] Placement recorded in the content inventory
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. Candidate: placing a Marko Sipila (HVAC Quote) customer-question leaf under its service branch with upward links.

## Run on a persistent agent (Fable 5)
A persistent agent (Fable 5 or a comparable OpenAI/Google model) holds the whole SEO Tree and content inventory in memory, so classifying the new leaf and finding its parent is a lookup, not a re-derivation — and it verifies every Definition-of-done box (upward links live, inbound link added, no hub competition) before declaring placement done, halting and flagging when no parent exists rather than guessing.
Each placement updates the in-memory inventory, which is what makes the next run's orphan check trivial.
It logs a meta-article example per run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /seo-tree
- Related: /internal-linking · /entity-linking · /blog-posting-guidelines
- Run order (Post stage): set-wordpress-author-to-correct-person → **place-content-on-seo-tree-with-proper-links** → verify-all-items-on-blog-posting-checklist
