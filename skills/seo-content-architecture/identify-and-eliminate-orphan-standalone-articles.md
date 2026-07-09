---
name: identify-and-eliminate-orphan-standalone-articles
description: "Find every page with zero internal links pointing to it and give each one a disposition — connect it to its branch, consolidate it into the owning hub, or cut it — until the site has no orphans."
category: SEO & Content Architecture
stage: —
definitive_article: /seo-tree
status: needs-work
---

# Identify and eliminate orphan/standalone articles

**Use this when** a crawl, audit, or the tree-mapping skill surfaces pages no other page links to — content invisible to both readers and crawlers.

## Inputs
- Inlink counts for every URL (site crawl or LinkWhisper report)
- The SEO Tree map, to test where each orphan belongs
- Redirect capability (301s) on the site

## Steps
1. Export internal-links-in counts for every URL and flag every page with zero inbound internal links.
2. Cross-check flagged pages against the SEO Tree map — an orphan has no parent branch and no inbound links.
3. Classify each orphan: **Connect** (real value, fits an existing branch), **Consolidate** (thin or duplicate — its topic already has a hub), or **Cut** (no value, no fit).
4. Connect: assign the branch's WordPress category, add upward in-body links from the orphan to its branch, and add the orphan to the hub's linked examples with a 1–2 sentence note.
5. Consolidate: move any unique material into the owning hub, then 301-redirect the orphan URL to that hub; update any links that pointed at the old URL.
6. Cut: remove the page and 301-redirect its URL to the closest relevant hub — never leave a 404 behind.
7. Re-crawl to confirm zero orphans, update the tree map, and log the round in the weekly MAA report (/maa).

## Definition of done (QA checklist)
- [ ] Zero pages with no inbound internal links on the re-crawl
- [ ] Every former orphan has a logged disposition: connect / consolidate / cut
- [ ] All redirects live and tested; no broken internal links created
- [ ] Tree map and link inventory updated
- [ ] Linked back to the definitive article (/seo-tree) and relevant siblings

## Example(s)
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first orphan-elimination round.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) loops export → disposition → fix → re-crawl until the re-crawl shows zero orphans — "down to a few" is the 90% trap this skill exists to kill — and it tests every 301 it creates rather than assuming redirects landed.
It keeps the disposition log in memory across rounds, so recurring orphan patterns get fixed upstream instead of re-triaged forever.
Every round ends with a meta-article example logged via /meta-article-prompt-template and the result recorded in the weekly /maa report.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /seo-tree
- Related: map-content-hierarchically-root-trunk-branches-leaves (run first) · step-3-identify-money-pages-and-orphan-pages (/internal-linking) · remove-duplicate-thin-pages · step-6-measure-and-iterate-with-maa (/maa)
