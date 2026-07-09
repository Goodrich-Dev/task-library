---
name: write-proper-title-tags-and-meta-descriptions
description: Give every indexable page a unique title tag under 60 characters and meta description under 160 characters, each carrying its focus keyword.
category: Digital Plumbing
stage: —
definitive_article: /digital-plumbing
status: needs-work
---

# Write Proper Title Tags and Meta Descriptions

**Use this when** pages have missing, duplicate, truncated, or keyword-less titles and meta descriptions — or after launching any new page.

## Inputs
- Crawl or page list of all indexable pages (Rank Math's list or a site crawl)
- Focus keyword per page (from the page's GCT: what searcher is this page for?)
- Access to the SEO plugin (Rank Math) to edit titles and metas

## Steps
1. Inventory every indexable page and its current title and meta description. Flag missing, duplicate, over-length, and keyword-less entries.
2. For each page, confirm the focus keyword — the real phrase its target searcher uses. One page, one keyword family (no two pages competing for the same term; that's content vandalism).
3. Write the title: under 60 characters, focus keyword near the front, brand at the end if it fits. Describe what the page actually delivers — no clickbait, no AI-fluff phrasing.
4. Write the meta description: under 160 characters, focus keyword included naturally, plus a concrete reason to click (outcome, proof, or offer). Active voice.
5. Enter both in Rank Math per page and confirm no template is overriding them.
6. QA pass: every title and meta unique site-wide; spot-check a Google result (site:yourdomain) to see how they render in the SERP.

## Definition of done (QA checklist)
- [ ] Every indexable page has a title under 60 characters containing its focus keyword
- [ ] Every indexable page has a meta description under 160 characters containing its focus keyword
- [ ] Zero duplicate titles or metas site-wide
- [ ] No truncation on spot-checked SERP renderings
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A long-horizon agent (Claude Fable 5 or a comparable OpenAI/Google model) works the full page inventory, not a sample: write, check length and keyword, re-crawl for duplicates, and loop until every indexable page passes the entire Definition of done, not 90% of pages.
It self-verifies the 60/160 limits and site-wide uniqueness against that checklist programmatically, stores the page-to-keyword map in memory so new pages slot into the same canon on later runs, and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /digital-plumbing
- Related (run order): this → ensure-robots-meta-not-blocking-indexing → create-xml-sitemap-and-reference-in-robots-txt
- Cross-links: /blog-posting-guidelines (title/meta rules live here) · /website-qa-audit (Layer 2 title/meta checks) · /seo-tree (one page per concept)
