---
name: verify-hero-section-contains-real-photo-of-person
description: Confirms the homepage hero leads with a real photograph of the brand owner — not stock, not an illustration — so visitors meet the person immediately.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Verify hero section contains real photo of person

**Use this when** running Layer 2 (Content Architecture Checks) of the Website QA Audit on a personal-brand site — the hero is the handshake; it must be the actual person.

## Inputs
- Homepage URL
- A known reference photo of the owner (to confirm identity)
- Google Images reverse search for stock verification if in doubt
- The audit report/spreadsheet for logging results

## Steps
1. Load the homepage and check the hero (the first viewport): it must contain a photograph of the brand owner.
2. Confirm it is genuinely them — match against the reference photo; fail look-alike stock models, logos-only heroes, or illustration/avatar substitutes.
3. Reverse-search the hero image if there is any doubt; a hero photo found on other sites is stock and fails.
4. Judge quality at a pass/fail level: the face is clearly visible, in focus, and large enough to register on mobile — a tiny or heavily-overlaid photo fails the intent.
5. Check the mobile rendering: the person must still be visible in the mobile hero crop, not cropped out by the responsive layout.
6. Log the verdict with desktop and mobile screenshots in the audit report.

## Definition of done (QA checklist)
- [ ] Hero contains a real, verifiable photo of the owner, clearly visible on both desktop and mobile first viewport
- [ ] Photo verified as non-stock (reverse search clean or owner-confirmed original)
- [ ] Screenshots logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Fable 5 / comparable OpenAI or Google models) runs this on every page with a hero — homepage plus landing pages — capturing desktop and mobile screenshots, reverse-searching the photo, and looping until each hero shows the verified real owner clearly in both viewports.
Memory stores the passing hero image hash per page, so a re-run instantly flags a redesign or A/B test that swapped in stock — the check stays open for as long as the site lives.
Each run logs screenshot evidence as a worked example in ## Example(s), compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /blog-posting-guidelines (real photos only) · previous: verify-footer-includes-social-links-and-secondary-nav · next check: check-each-homepage-section-includes-relevant-image
