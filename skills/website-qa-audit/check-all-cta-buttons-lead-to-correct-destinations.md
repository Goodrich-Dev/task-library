---
name: check-all-cta-buttons-lead-to-correct-destinations
description: Click-tests every call-to-action button on the site to confirm each routes to the destination its copy promises, keeping the conversion path unbroken.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: needs-work
---

# Check all CTA buttons lead to correct destinations

**Use this when** running Layer 2 (Content Architecture Checks) of the Website QA Audit — a CTA that 404s or routes to the wrong page is a lead silently lost.

## Inputs
- Site URL plus a full page list (XML sitemap or crawl export)
- The intended destination map (which CTA should go where — booking page, contact form, lead magnet, phone)
- Desktop and mobile browsers for click-testing
- The audit report/spreadsheet for logging results

## Steps
1. Inventory every CTA button across the site: hero, section CTAs, header button, footer, in-post CTAs, and popups.
2. Click each one and record the actual destination URL; fail anything returning 404, the homepage, a stale landing page, or a placeholder anchor (`#`).
3. Match destination to promise: "Get a Quote" must land on the quote/contact form, "Book a Call" on the live scheduler, "Download" on the actual opt-in — not a generic page.
4. Test click-to-call CTAs on a real phone — the `tel:` link must dial the current business number.
5. Repeat the clicks on mobile, where overlays and sticky bars often break or cover buttons.
6. Log every CTA with its label, location, expected vs actual destination, and pass/fail in the audit report.

## Definition of done (QA checklist)
- [ ] 100% of CTAs route to their promised, working destination on desktop and mobile — zero 404s, placeholders, or mismatches
- [ ] Click-to-call links dial the correct current number
- [ ] CTA inventory with expected-vs-actual logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Fable 5 / comparable OpenAI or Google models) inventories every CTA on every page — including popups and sticky bars — resolves each destination at desktop and mobile widths, and loops fix-retest until 100% match their promised destination with zero 404s or placeholder anchors.
Memory keeps the CTA inventory with expected-vs-actual per page, so re-runs only retest changed pages, new CTAs, and previously failing buttons.
Each run logs one worked example to ## Example(s), compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /digital-plumbing (clear conversion path) · previous: verify-featured-images-unique-per-blog-post · next check: verify-email-opt-in-form-exists-and-works
