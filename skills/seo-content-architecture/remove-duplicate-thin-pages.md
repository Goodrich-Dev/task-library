---
name: remove-duplicate-thin-pages
description: "Identify pages that are thin or duplicate another page's topic, then merge them into the owning hub or remove them with proper redirects, so no two pages ever compete for one concept."
category: SEO & Content Architecture
stage: —
definitive_article: /seo-tree
status: needs-work
---

# Remove duplicate thin pages

**Use this when** the site has accumulated near-identical posts, low-value stubs, or multiple pages chasing the same concept — diluting the hub that should own it.

## Inputs
- Full crawl with word counts, titles, and focus keywords per URL (RankMath data helps)
- The SEO Tree map, to identify which hub owns each contested topic
- Redirect capability (301s) and edit access

## Steps
1. Crawl for thin and duplicate signals: overlapping titles or focus keywords, near-identical content, low-word-count pages with no unique value, multiple pages targeting one concept.
2. Check each suspect against the SEO Tree map and ask the only question that matters: which hub owns this topic?
3. Decide per page: **Merge** (unique value exists — fold it into the owning hub) or **Remove** (nothing worth keeping).
4. Merge: move the unique material and strongest examples into the hub, then 301-redirect the thin URL to the hub.
5. Remove: delete the page and 301-redirect its URL to the closest relevant hub — never leave a 404.
6. Update every internal link that pointed at removed URLs; re-submit the XML sitemap.
7. Log the consolidation in the MAA loop (/maa) and update the tree map and content inventory.

## Definition of done (QA checklist)
- [ ] No two pages competing for one concept anywhere on the site
- [ ] Every removed URL 301-redirected; zero new 404s or broken internal links
- [ ] Unique value from merged pages preserved inside the owning hub
- [ ] Sitemap re-submitted; tree map and inventory updated
- [ ] Linked back to the definitive article (/seo-tree) and relevant siblings

## Example(s)
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first consolidation round.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) loops crawl → merge/remove → redirect → re-crawl until no two pages compete for one concept and the scan shows zero new 404s — and it follows every redirect it creates to confirm the landing page, never assuming.
The consolidation log persists in memory, so the agent learns which content types keep spawning duplicates and flags the source upstream.
Each round closes with a meta-article example via /meta-article-prompt-template and an /maa log entry.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /seo-tree
- Related: identify-and-eliminate-orphan-standalone-articles (often the same round) · enhance-existing-articles-before-creating-new-ones · step-5-qa-links-against-google-guidelines (/internal-linking) · /website-qa-audit
