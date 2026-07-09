---
name: set-favicon
description: Upload a proper branded favicon so the site stops showing a default icon in browser tabs, bookmarks, and search results.
category: Digital Plumbing
stage: —
definitive_article: GAP — to be written
status: needs-work
---

# Set Favicon

**Use this when** the browser tab shows the default WordPress, host, or theme icon instead of the brand — a small but visible "nobody finished this site" signal.

## Inputs
- Brand mark, logo, or (for personal brands) the canonical headshot — a real asset, not stock
- Square source image at 512×512 px or larger
- WordPress admin access

## Steps
1. Prepare a square 512×512 image of the brand mark. Crop tight — favicons render at 16–32 px, so a wordmark or busy logo becomes noise; use the simplest distinctive element.
2. In WordPress, set it under Appearance → Customize → Site Identity → Site Icon (or the theme/SEO plugin's site icon setting). WordPress generates the required sizes.
3. Hard-refresh and confirm the icon shows in the browser tab on desktop. Favicons cache aggressively — test in a private window if the old icon lingers.
4. Check a phone browser tab and the bookmark/home-screen rendering.
5. Confirm no plugin or hard-coded link rel="icon" in the theme header is overriding the new icon with an old file.
6. Note: Google can show the favicon next to mobile search results — one more reason it must be the brand, not the host's default.

## Definition of done (QA checklist)
- [ ] Favicon displays in the browser tab on desktop and mobile (fresh/private session tested)
- [ ] Icon is the brand's own mark — not a WordPress, theme, or hosting default, not stock
- [ ] Legible at tab size (16–32 px)
- [ ] No conflicting icon declarations left in the theme header
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
Small task, same standard: a persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) sets the icon, then verifies in fresh private sessions on desktop and mobile — favicons cache aggressively — and hunts conflicting declarations, looping until every Definition-of-done item passes, not 90%.
It self-verifies against that checklist, records the source asset and where it is set in memory so future theme changes do not silently regress it, and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written (no dedicated hub yet; parent concept: /digital-plumbing)
- Related (run order): configure-https-with-no-mixed-content → this → ensure-robots-meta-not-blocking-indexing
- Cross-links: /website-qa-audit (Layer 1: "Check favicon is set")
