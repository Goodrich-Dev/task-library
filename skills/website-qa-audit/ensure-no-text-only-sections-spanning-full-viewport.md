---
name: ensure-no-text-only-sections-spanning-full-viewport
description: Scans every page for sections that fill an entire screen with nothing but text, the wall-of-words pattern that makes visitors bounce.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Ensure no text-only sections spanning full viewport

**Use this when** running Layer 2 (Content Architecture Checks) of the Website QA Audit — if a full screen scrolls by with no visual, you've lost the skimmer.

## Inputs
- Site URL plus the key pages (homepage, services, about, top posts)
- Desktop browser and a real phone (the mobile viewport is where text walls happen first)
- The audit report/spreadsheet for logging results

## Steps
1. Scroll each key page slowly on DESKTOP and note any point where the entire visible viewport contains only text — no photo, video, diagram, screenshot, or meaningful visual element.
2. Repeat on MOBILE: text stacks taller on phones, so sections that pass desktop often fail mobile — judge each viewport-height of scroll.
3. Record each violation with the page, the section heading, and which viewport(s) it fails in.
4. For each violation, name the fix: insert a relevant real image, embed the source video, break copy with a diagram or screenshot, or tighten the copy.
5. Re-check long blog posts specifically — body copy between images must not exceed one full viewport on mobile (matches the visual-rhythm intent of /blog-posting-guidelines).
6. Log violations and fixes in the audit report.

## Definition of done (QA checklist)
- [ ] Zero sections on audited pages span a full viewport with text only, on both desktop and mobile
- [ ] Every violation has a named visual fix queued or applied
- [ ] Scroll-audit results logged per page in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Fable 5 / comparable OpenAI or Google models) scroll-audits every page on the site — not just the key ones — measuring rendered viewport-heights of unbroken text at both desktop and mobile widths, and loops insert-visual-recheck until zero full-viewport text walls remain anywhere.
Memory keeps per-page verdicts, so re-runs only re-measure pages with edited or new content — and every new long post triggers the mobile pass automatically.
Each run logs one worked example to ## Example(s) so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /blog-posting-guidelines (short paragraphs, images throughout) · previous: verify-at-least-one-video-embed-on-homepage · next check: verify-minimum-5-distinct-images-on-homepage
