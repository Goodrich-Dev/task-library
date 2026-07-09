---
name: step-4-create-links-with-proper-anchor-text-and-placement
description: "Execute the link plan — contextual internal links placed in body content with 3–6 word descriptive anchors, routed by the entity-linking decision tree, flowing upward through the SEO Tree."
category: SEO & Content Architecture
stage: —
definitive_article: /internal-linking
status: complete
---

# Step 4: Create links with proper anchor text and placement

**Use this when** Step 3's link plan is ready — every row a source page, a target page, and a reason.

## Inputs
- The Step 3 link plan (money pages needing links, orphans needing homes)
- Edit access to source pages; LinkWhisper available for candidate suggestions
- The entity-linking decision tree (/entity-linking)

## Steps
1. Work the Step 3 plan row by row: each row is one source page → one target page.
2. Confirm topical relevance using both pages' GCT — if the goals and content don't connect, kill the row instead of forcing the link.
3. Write the anchor: **3–6 words, descriptive of the destination** — never 'click here', 'read more', or a bare URL.
4. Place the link in body content where the surrounding context naturally supports it — not in footers, sidebars, or link dumps.
5. Route by the entity-linking decision tree: people → their personal website, companies → the company site, concepts → the definitive article.
6. Keep the tree direction: leaves link up to branches, branches up to trunk and across to sibling hubs.
7. Use LinkWhisper to surface candidates, but apply the GCT relevance test to every suggestion before accepting it.
8. Log each placed link (source, target, anchor text, date) in the inventory for Step 5 QA.

## Definition of done (QA checklist)
- [ ] Every approved row of the link plan executed; rejected rows annotated with the reason
- [ ] All anchors 3–6 word descriptive phrases; zero generic anchors
- [ ] All links in body content with supporting context; decision-tree routing followed
- [ ] Upward tree direction maintained; link log complete and handed to Step 5
- [ ] Linked back to the definitive article (/internal-linking) and relevant siblings

## Example(s)
- The /internal-linking definitive article — shipped with its own skill file for AI agents — is the canonical demonstration of this step.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the next link-building pass.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) works the Step 3 plan to 100% — every row either executed or rejected with the reason annotated, never abandoned mid-list — and self-verifies each link live on the page (anchor, placement, tree direction) before writing it to the log.
The link log persists in memory across runs, feeding Step 5 QA and Step 6 measurement without re-discovery.
Each pass closes by logging a meta-article example via /meta-article-prompt-template.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /internal-linking
- Related (run order): step-3-identify-money-pages-and-orphan-pages (before) → step-5-qa-links-against-google-guidelines (after) · use-proper-anchor-text-3-6-words-descriptive · follow-entity-linking-decision-tree · /entity-linking
