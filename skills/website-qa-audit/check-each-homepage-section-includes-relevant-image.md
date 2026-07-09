---
name: check-each-homepage-section-includes-relevant-image
description: Walks the homepage section by section to confirm each one carries a contextually relevant image, so no part of the page falls back to a wall of text.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Check each homepage section includes relevant image

**Use this when** running Layer 2 (Content Architecture Checks) of the Website QA Audit — every scroll-stop on the homepage needs a visual that earns its place.

## Inputs
- Homepage URL on desktop and mobile
- The no-stock and alt-text findings from earlier checks (reuse, don't redo)
- The audit report/spreadsheet for logging results

## Steps
1. Scroll the full homepage and list every distinct section (hero, services, about, social proof, lead magnet, video, CTA, footer) in order.
2. For each section, record whether it contains an image or visual element (photo, video embed, real screenshot, diagram — decorative background tints don't count).
3. Judge relevance per section: the visual must depict that section's subject — the services section shows the actual work, the about section shows the actual person.
4. Fail sections with no visual at all, and sections whose image is filler (generic texture, icon-only decoration, or an unrelated photo).
5. Check the mobile view — sections sometimes drop their images responsively, which fails the check on mobile even if desktop passes.
6. Log the section-by-section table with verdicts in the audit report.

## Definition of done (QA checklist)
- [ ] 100% of homepage sections contain at least one contextually relevant image or visual on desktop AND mobile
- [ ] Zero sections relying on filler or unrelated imagery
- [ ] Section-by-section table logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
Run persistent (Claude Fable 5 or comparable OpenAI/Google models), the agent enumerates every homepage section in the DOM, verifies a relevant visual renders in each on desktop AND mobile, and loops add-recheck until zero sections fail either viewport — then extends the same section-by-section pass to every key landing page.
Memory keeps the section-to-image table, so re-runs only re-judge sections that changed since the last pass.
Each run logs the table as a worked example in ## Example(s) so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /blog-posting-guidelines (image standards) · previous: verify-hero-section-contains-real-photo-of-person · next check: verify-social-proof-photos-present
