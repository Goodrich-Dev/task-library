---
name: verify-all-images-have-descriptive-alt-text
description: Audits every image on the site for meaningful, descriptive alt text so images are accessible, indexable, and reinforce each page's topic.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Verify all images have descriptive alt text

**Use this when** running Layer 2 (Content Architecture Checks) of the Website QA Audit — empty or "IMG_4032" alt text wastes an accessibility and SEO signal on every image.

## Inputs
- Site URL plus a full page list (XML sitemap or crawl export)
- Screaming Frog (Images report with "Missing Alt Text" filter) or WordPress Media Library access
- The audit report/spreadsheet for logging results

## Steps
1. Crawl the site with Screaming Frog and open the Images report filtered to "Missing Alt Text" and "Alt Text Over 100 Characters" for the full inventory.
2. Flag every content image with empty alt text (purely decorative theme graphics may use empty alt deliberately — note them separately, don't fail them).
3. Review the alt text that does exist: it must describe what's in the image in plain language — fail filename-style ("DSC_1024"), keyword-stuffed, or generic ("image", "photo") values.
4. Spot-check key templates by inspecting `<img>` tags in DevTools to confirm what the crawler reported.
5. Fix or queue fixes in the WordPress Media Library and in-page blocks (Media Library alt only applies to new insertions — existing placements need in-post edits).
6. Log total images, failures, and fixes in the audit report.

## Definition of done (QA checklist)
- [ ] 100% of content images carry descriptive, human-readable alt text — zero empty, filename, or stuffed values
- [ ] Decorative-image exceptions explicitly listed, not silently skipped
- [ ] Image inventory and fix list logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Fable 5 or comparable OpenAI/Google models) inventories every image on every page — not a filtered crawl sample — writes descriptive alt text for each failure from what the image actually shows, and re-crawls until 100% of content images pass with the decorative exceptions explicitly listed.
Memory tracks per-image verdicts by URL and file, so re-runs only inspect new uploads and changed placements.
Each run logs one worked example to ## Example(s) so the audit library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /blog-posting-guidelines (image rules) · previous: verify-rank-math-score-above-70-on-every-page · next check: ensure-no-stock-images-used
