---
name: map-content-hierarchically-root-trunk-branches-leaves
description: "Organize every page on a site into the SEO Tree — root (homepage/entity), trunk (brand), branches (definitive articles), leaves (case studies and meta-articles) — so one coherent hierarchy replaces a pile of disconnected posts."
category: SEO & Content Architecture
stage: —
definitive_article: /seo-tree
status: complete
---

# Map content hierarchically (root → trunk → branches → leaves)

**Use this when** a site has published content but no deliberate hierarchy — nothing tells Google (or an AI agent) which page owns which topic.

## Inputs
- Complete URL inventory: WordPress posts + pages export, sitemap.xml, or a full crawl
- The brand's entity definition: who this person/company is, core concepts, money pages
- The /seo-tree definitive article open as the reference model

## Steps
1. Pull every published URL into a single inventory — posts, pages, landing pages, nothing skipped.
2. Set the **root**: the homepage as the entity hub — who this is, what they do, why trust them.
3. Set the **trunk**: the brand layer — core offer and positioning pages everything else grows from.
4. Assign **branches**: one definitive article per core concept. Each branch is the single hub that owns its topic — never allow two pages to compete for one concept (that is content vandalism).
5. Assign **leaves**: case studies, examples, and meta-articles, each parented to exactly one branch.
6. Flag everything that does not fit — orphans (no parent), duplicates (two pages, one topic), thin pages — and route them to the orphan-elimination and thin-page-removal skills.
7. Draw the tree (root → trunk → branches → leaves) as a clickable diagram and save it as the site's content map; every future publish decision starts from this map.

## Definition of done (QA checklist)
- [ ] Every published URL appears exactly once on the tree map
- [ ] Each core concept has exactly one branch page — zero competing hubs
- [ ] Every leaf has a named parent branch; every misfit flagged with a disposition (connect / consolidate / cut)
- [ ] Tree diagram exists and a stranger can read the site's structure from it in under a minute
- [ ] Linked back to the definitive article (/seo-tree) and relevant siblings

## Example(s)
- The /seo-tree definitive article is the canonical model this skill mirrors — read it before the first run.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first real site mapping.

## Run on a persistent agent (Fable 5)
Hand the full URL inventory to a persistent, max-effort agent (Claude Fable 5 or a comparable OpenAI/Google frontier model) and let it loop classify → flag → redraw until every box in the Definition of done passes — every URL on the tree exactly once, zero competing hubs — not 90% mapped.
It self-verifies by diffing the finished map against a fresh sitemap crawl, and persists the tree map in memory so the next run diffs new URLs instead of remapping from scratch.
Each run ends by logging a meta-article example via /meta-article-prompt-template, clearing this file's "Example needed."
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /seo-tree
- Related: fit-every-new-piece-into-the-tree-structure · link-leaves-to-branches-branches-to-trunk · identify-and-eliminate-orphan-standalone-articles · /internal-linking (6-step process) · /website-qa-audit (Layer 2 checks)
