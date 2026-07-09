---
name: verify-minimum-5-distinct-images-on-homepage
description: Counts the unique, relevant images on the homepage and confirms there are at least five, the minimum visual density for a credible personal-brand site.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Verify minimum 5 distinct images on homepage

**Use this when** closing Layer 2 (Content Architecture Checks) of the Website QA Audit — five distinct real images is the floor, not the goal.

## Inputs
- Homepage URL
- Chrome DevTools (Network tab filtered to Img) or a Screaming Frog crawl of the homepage for the exact image inventory
- Verdicts from the no-stock and relevant-image checks (reuse them)
- The audit report/spreadsheet for logging results

## Steps
1. Load the homepage with DevTools Network → Img (or crawl the URL in Screaming Frog) to list every image file the page actually renders.
2. Strip non-qualifying entries from the count: logos, icons, background textures, spacer graphics, and favicons don't count as content images.
3. De-duplicate — the same photo used twice counts once. The count needs DISTINCT images.
4. Confirm each counted image is relevant and real (cross-reference the ensure-no-stock-images-used verdicts; stock images don't count toward the five).
5. Confirm all qualifying images actually render on mobile — responsively hidden images don't count for mobile visitors.
6. Log the final count with the image list in the audit report; 5 or more passes, 4 or fewer fails.

## Definition of done (QA checklist)
- [ ] Homepage renders at least 5 distinct, relevant, non-stock content images on desktop and mobile
- [ ] Count excludes logos, icons, backgrounds, and duplicates — image list itemized
- [ ] Count and inventory logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
Run persistent (Claude Fable 5 or comparable OpenAI/Google models), the agent pulls the homepage's exact rendered image inventory each run, strips logos, icons, duplicates, and known stock, and confirms the distinct-real count holds at 5+ on desktop and mobile — looping with the image-sourcing fixes until it does, and rechecking after every redesign.
Memory stores the qualifying image list and count history, so a re-run catches the count silently dropping when a section is removed.
Each run logs the itemized count as a worked example in ## Example(s), compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /blog-posting-guidelines (image standards) · previous: ensure-no-text-only-sections-spanning-full-viewport · next: Layer 3 begins with verify-testimonials-with-full-attribution
