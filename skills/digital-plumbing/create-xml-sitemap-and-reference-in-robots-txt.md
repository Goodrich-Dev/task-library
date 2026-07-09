---
name: create-xml-sitemap-and-reference-in-robots-txt
description: Generate a clean XML sitemap, reference it in robots.txt, and submit it to Search Console so Google can find every page worth indexing.
category: Digital Plumbing
stage: —
definitive_article: GAP — to be written
status: needs-work
---

# Create XML Sitemap and Reference in robots.txt

**Use this when** the site has no sitemap.xml, the sitemap is missing from robots.txt, or Search Console shows the sitemap as unfetched or erroring.

## Inputs
- WordPress admin with Rank Math (or equivalent SEO plugin that generates sitemaps)
- Ability to edit robots.txt (plugin or file access)
- Google Search Console access for the verified property

## Steps
1. Enable the XML sitemap in Rank Math (Sitemap Settings). Include posts, pages, and real taxonomies; exclude thin archives, media attachments, and anything noindexed.
2. Load /sitemap_index.xml (or /sitemap.xml) in a browser: it must return without error and list the live, canonical, HTTPS URLs — no 404s, no noindexed or redirected URLs.
3. Edit robots.txt at the domain root and add the absolute sitemap line: Sitemap: https://yourdomain.com/sitemap_index.xml
4. While in robots.txt, confirm nothing vital is disallowed (no Disallow: / and no blocking of CSS/JS or key directories).
5. In Search Console, submit the sitemap (Indexing → Sitemaps) and confirm status reads Success with a plausible discovered-URL count.
6. Re-check after content restructures — a sitemap full of redirects or deleted URLs tells Google the site is unmaintained.

## Definition of done (QA checklist)
- [ ] Sitemap URL loads without error and contains only live, canonical, indexable URLs
- [ ] robots.txt contains the absolute Sitemap: line and blocks nothing essential
- [ ] Sitemap submitted in GSC with status "Success" and a sane URL count
- [ ] Excluded content (noindexed pages, attachments) absent from the sitemap
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) generates the sitemap, validates every listed URL as live, canonical, and indexable, submits to GSC, and waits to confirm "Success" — looping on errors until the full Definition of done passes, not 90%.
It self-verifies against that checklist, keeps the expected URL count and exclusion rules in memory so a restructure that fills the sitemap with redirects gets flagged on the next run, and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written (no dedicated hub yet; parent concept: /digital-plumbing)
- Related (run order): ensure-robots-meta-not-blocking-indexing → this → verify-google-search-console-and-connect-to-ga4
- Cross-links: /website-qa-audit (Layer 1: "sitemap exists and in robots.txt") · /seo-tree (the sitemap should mirror a clean tree)
