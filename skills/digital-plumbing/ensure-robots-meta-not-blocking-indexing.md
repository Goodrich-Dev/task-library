---
name: ensure-robots-meta-not-blocking-indexing
description: Verify no robots meta tag, header, or WordPress setting is silently telling Google not to index the site.
category: Digital Plumbing
stage: —
definitive_article: GAP — to be written
status: needs-work
---

# Ensure Robots Meta Not Blocking Indexing

**Use this when** a site or page won't appear in Google, after any migration/redesign (staging noindex settings love to ship to production), or as a standard takeover check.

## Inputs
- WordPress admin access (Settings and SEO plugin)
- Google Search Console access for the verified property
- List of money pages to spot-check: homepage, top service page, a recent post

## Steps
1. Check the kill switch first: WordPress Settings → Reading → "Discourage search engines from indexing this site" must be unchecked. This single box has buried entire businesses post-launch.
2. View source on the homepage and each money page: search for meta name="robots". Any noindex or nofollow there must be deliberate — on money pages it never is.
3. Check the SEO plugin (Rank Math) per-page robots settings and sitewide defaults for accidental noindex on pages, posts, or key archives.
4. Check HTTP responses for an X-Robots-Tag: noindex header (host- or plugin-injected) on the same pages.
5. Confirm robots.txt isn't disallowing the whole site or key directories (see the sitemap skill for the full robots.txt pass).
6. Run GSC URL Inspection on the homepage, a service page, and a post: each should report indexing allowed. Fix anything that doesn't, then Request Indexing.
7. Document what you found and fixed — a reverted noindex is worth a Knowledge Capture Note so it never recurs.

## Definition of done (QA checklist)
- [ ] "Discourage search engines" is unchecked in WordPress Reading settings
- [ ] No unintended noindex/nofollow in meta robots or X-Robots-Tag on homepage, service pages, or posts
- [ ] GSC URL Inspection reports "Indexing allowed" on all spot-checked pages
- [ ] Any deliberate noindex (thank-you pages, internal search) documented as intentional
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) checks all four layers — Reading setting, meta robots, X-Robots-Tag, robots.txt — then proves each page in GSC URL Inspection, looping on every fix until the full Definition of done reads "indexing allowed," not 90%.
It self-verifies against that checklist instead of trusting any single setting, keeps prior reverted-noindex incidents in memory (the Knowledge Capture Note) so recurrences are caught on the next run, and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written (no dedicated hub yet; parent concept: /digital-plumbing)
- Related (run order): write-proper-title-tags-and-meta-descriptions → this → create-xml-sitemap-and-reference-in-robots-txt → verify-google-search-console-and-connect-to-ga4
- Cross-links: /website-qa-audit (Layer 1 robots check) · /knowledge-system-maintenance (Knowledge Capture Note)
