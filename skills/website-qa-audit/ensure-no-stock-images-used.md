---
name: ensure-no-stock-images-used
description: Audits all site imagery to confirm photos are real — the owner, their team, their work — because stock photography destroys the authenticity a personal brand runs on.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Ensure no stock images used

**Use this when** running Layer 2 (Content Architecture Checks) of the Website QA Audit — visitors and Google both recognize stock photos, and both discount them.

## Inputs
- Site URL plus a full page list (XML sitemap or crawl export)
- Google Images reverse search (or TinEye) for verifying suspect photos
- The owner's confirmation of which photos are genuinely theirs
- The audit report/spreadsheet for logging results

## Steps
1. Scroll every page and inventory the imagery; flag the stock tells — generic handshakes, polished models in headsets, watermark remnants, perfect-but-placeless offices.
2. Reverse-search each suspect image with Google Images or TinEye; a photo appearing on dozens of unrelated sites is stock.
3. Confirm the remaining photos are genuinely the owner's: their face, team, jobsite, clients, or screenshots of their actual work.
4. Check the blog separately — featured images are where stock sneaks in post by post (see /blog-posting-guidelines Step 8: real photos only).
5. For every confirmed stock image, specify the real replacement to capture (for example, a phone photo of the owner on an actual job).
6. Log each image's verdict and the replacement list in the audit report.

## Definition of done (QA checklist)
- [ ] Zero stock images remain on any audited page — every photo verified as real via reverse search or owner confirmation
- [ ] Each removed stock image has a named real replacement queued
- [ ] Image verdicts logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
Run persistent (Claude Fable 5 / comparable OpenAI or Google models), this check reverse-searches every image on the site — not just the obvious suspects — and loops through flag-replace-reverify until zero stock images remain and every replacement is confirmed real.
Memory keeps the verified-real image list with file hashes, so each re-run only checks new or changed images instead of re-searching the whole library.
Each run logs one worked example to ## Example(s), compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /blog-posting-guidelines (no-stock rule) · previous: verify-all-images-have-descriptive-alt-text · next check: verify-featured-images-unique-per-blog-post
