---
name: link-leaves-to-branches-branches-to-trunk
description: "Wire the SEO Tree together with upward internal links — every leaf links to its branch, every branch to the trunk and root — so authority flows from examples up to hubs and money pages."
category: SEO & Content Architecture
stage: —
definitive_article: /seo-tree
status: complete
---

# Link leaves to branches, branches to trunk

**Use this when** the tree has been mapped but pages still sit unconnected — or after every new publish, to wire the new piece in.

## Inputs
- The SEO Tree map with every page's role assigned (root / trunk / branch / leaf)
- Edit access to the pages being linked
- Anchor-text rule in hand: 3–6 words, descriptive, never generic

## Steps
1. From the tree map, list every leaf grouped under its parent branch.
2. In each leaf's body copy, add at least one upward link to its parent branch using a 3–6 word descriptive anchor — never 'click here'.
3. In each branch (definitive article), link upward to the trunk/root and **across** to the sibling definitive articles it references.
4. Keep the relationship direction one way up: examples and meta-articles → definitive article → course/service.
5. The hub's examples section links down to its leaves (Requirement 3 — every example, each with a 1–2 sentence note); what never happens is a leaf restating the hub's content.
6. QA every new link against Google guidelines (Step 5 of /internal-linking) and record it in the link inventory.

## Definition of done (QA checklist)
- [ ] Every leaf carries at least one upward in-body link to its parent branch
- [ ] Every branch links up to trunk/root and across to related definitive articles
- [ ] All anchors are 3–6 word descriptive phrases; zero generic anchors
- [ ] Zero orphans remain in the mapped section; links logged in the inventory
- [ ] Linked back to the definitive article (/seo-tree) and relevant siblings

## Example(s)
- The /internal-linking definitive article — which ships with its own skill file for AI agents — demonstrates the link-creation mechanics this skill applies tree-wide.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first full wiring pass.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) wires the tree leaf by leaf and loops until the Definition of done fully passes — every leaf linked upward, every branch linked up and across, zero generic anchors — verifying by re-crawling touched pages and re-running the anchor report, not by trusting its own edits.
The link inventory persists in memory between runs, so each pass wires only the new publishes instead of re-auditing the whole tree.
Each wiring pass closes by logging a meta-article example via /meta-article-prompt-template.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /seo-tree
- Related: map-content-hierarchically-root-trunk-branches-leaves (run first) · step-4-create-links-with-proper-anchor-text-and-placement (/internal-linking) · step-5-qa-links-against-google-guidelines · use-proper-anchor-text-3-6-words-descriptive
