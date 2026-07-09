---
name: verify-featured-images-unique-per-blog-post
description: Confirms every blog post carries its own unique featured image so archives, social shares, and search results don't show a wall of identical thumbnails.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Verify featured images unique per blog post

**Use this when** running Layer 2 (Content Architecture Checks) of the Website QA Audit — duplicate featured images make the blog look templated and machine-generated.

## Inputs
- WordPress admin access (Posts list with featured-image visibility)
- The live blog archive page for visual confirmation
- The audit report/spreadsheet for logging results

## Steps
1. Open the live blog archive and scan the grid — duplicate thumbnails jump out immediately at this view.
2. In WordPress → Posts, review every post's featured image (use a list view or theme admin column showing thumbnails) and record the image file used per post.
3. Flag every post with no featured image set — the theme will fall back to a default, creating accidental duplicates.
4. Flag every image file attached as the featured image on more than one post.
5. Confirm featured images are real photos relevant to each post's topic, consistent with the no-stock rule.
6. Log the post-to-image table with duplicates and gaps highlighted in the audit report.

## Definition of done (QA checklist)
- [ ] Every published post has a featured image, and no image file is reused across two or more posts
- [ ] All featured images are real (non-stock) and topically relevant to their post
- [ ] Post-to-image table logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent Fable 5 agent (or comparable OpenAI/Google model) pulls the full post-to-featured-image table via the WordPress API every run, flags gaps and duplicates across all posts at once, and loops assign-recheck until every published post has its own unique, real image — no archive-page eyeballing.
Memory holds the post-to-image map, so re-runs only examine new posts and any image swaps since the last pass.
Each run appends one worked example to ## Example(s) so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /blog-posting-guidelines (Step 8: photos and featured image) · previous: ensure-no-stock-images-used · next check: check-all-cta-buttons-lead-to-correct-destinations
