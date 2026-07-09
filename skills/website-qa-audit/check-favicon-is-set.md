---
name: check-favicon-is-set
description: Confirms a proper branded favicon is uploaded and rendering in browser tabs, bookmarks, and search results instead of a blank or default icon.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: needs-work
---

# Check favicon is set

**Use this when** running Layer 1 (Digital Plumbing Checks) of the Website QA Audit — a missing favicon is the small detail that signals an unfinished site.

## Inputs
- Site URL
- A desktop browser and a mobile browser for visual confirmation
- WordPress admin access (Appearance → Customize → Site Identity → Site Icon) if a fix is needed
- The audit report/spreadsheet for logging results

## Steps
1. Load the site in a desktop browser tab and confirm a branded icon appears — not the browser's default blank-page glyph.
2. Fetch `/favicon.ico` directly and view page source for the icon link tags; confirm at least one icon resource returns 200, not 404.
3. Confirm the icon is actually the brand (logo mark or the person's recognizable mark), not the WordPress default, the theme developer's logo, or the hosting company's icon.
4. Check on mobile by saving the site to the home screen or viewing the tab switcher — the icon must render legibly at small sizes.
5. Google the brand name and check whether the favicon shows next to the site in mobile search results (Google pulls it from the same icon).
6. Log pass/fail with a screenshot of the tab icon in the audit report.

## Definition of done (QA checklist)
- [ ] A branded favicon renders in desktop tabs and mobile, with the icon resource returning 200
- [ ] The icon is the owner's brand — not a default, theme, or host placeholder
- [ ] Screenshot evidence logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
Even a small check runs to exhaustion on a persistent agent (Fable 5 or comparable OpenAI/Google models): it fetches every declared icon resource — favicon.ico, apple-touch-icon, manifest icons — until each returns 200, confirms the rendered icon is the brand at every size, and loops on any 404 or default glyph until the fix sticks.
Memory records the passing icon set and file hashes, so a re-run instantly detects a theme update silently swapping the icon back to a default.
Each run logs a worked example to ## Example(s) so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /digital-plumbing · previous: verify-person-schema-with-sameas-links · next check: ensure-robots-meta-not-blocking-indexing
