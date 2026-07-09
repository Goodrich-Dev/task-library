---
name: verify-social-proof-photos-present
description: Confirms social proof sections show real photographic evidence — client photos, job results, event shots — not text-only claims that anyone could type.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Verify social proof photos present

**Use this when** running Layer 2 (Content Architecture Checks) of the Website QA Audit — text-only proof is just a claim; photos make it evidence.

## Inputs
- Site URL with the social proof sections identified (testimonials, results, logos, press, reviews)
- The no-stock verification method (reverse image search) from earlier checks
- The audit report/spreadsheet for logging results

## Steps
1. Locate every social proof element on the site: testimonial blocks, results/case-study sections, client logo strips, press mentions, review embeds.
2. For each, record whether it includes a real photo or visual artifact — client headshot, before/after job photo, screenshot of an actual review or analytics result, event photo.
3. Fail any social proof section that is text-only (quotes with no faces, claims with no captures).
4. Verify the photos are real: reverse-search suspect headshots; a "client" who appears on stock sites fails the section.
5. Confirm visuals match the claim — a review screenshot must show the named platform and reviewer, a results image must show the metric claimed.
6. Log each social proof element, its visual evidence, and verdict in the audit report.

## Definition of done (QA checklist)
- [ ] Every social proof section includes at least one real photo or screenshot artifact — zero text-only proof blocks
- [ ] All proof photos verified non-stock and consistent with the claims they support
- [ ] Element-by-element verdicts logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent Fable 5 agent (or comparable OpenAI/Google model) sweeps every social proof element across the entire site — every testimonial block, results section, logo strip, and review embed — verifying each carries real photographic evidence, and loops until zero text-only proof blocks remain anywhere.
Memory tracks each proof element's verdict, so re-runs only inspect new or edited blocks, and any new testimonial added without a photo re-opens the check automatically.
Each run logs one worked example to ## Example(s), compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /blog-posting-guidelines (real images only) · previous: check-each-homepage-section-includes-relevant-image · next check: verify-testimonials-include-headshots-with-attribution
