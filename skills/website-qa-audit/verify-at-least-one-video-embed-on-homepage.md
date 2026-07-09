---
name: verify-at-least-one-video-embed-on-homepage
description: Confirms the homepage carries at least one working embedded video of the owner, adding motion, face, and voice to the first impression.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Verify at least one video embed on homepage

**Use this when** running Layer 2 (Content Architecture Checks) of the Website QA Audit — video is the fastest way for a visitor to know, like, and trust the person.

## Inputs
- Homepage URL on desktop and mobile
- The owner's video inventory (YouTube channel, one-minute videos) to confirm the embed is theirs
- The audit report/spreadsheet for logging results

## Steps
1. Scroll the full homepage and locate every video element — true embeds (YouTube/hosted player) count; a thumbnail image merely linking away does not.
2. Confirm at least one embed exists; zero embeds is an immediate fail.
3. Press play and watch the first seconds: the video must load and play in place, and it must feature the brand owner (a WHY video or one-minute video is the standard fill).
4. Check mobile: the embed must render and play on a phone, not overflow the viewport or disappear responsively.
5. Open DevTools Console while the player loads to confirm the embed isn't throwing mixed-content or blocked-script errors.
6. Log the embed location, source URL, and playback results in the audit report.

## Definition of done (QA checklist)
- [ ] At least one true video embed on the homepage, playing successfully on desktop and mobile
- [ ] The video features the brand owner and loads without console errors
- [ ] Embed details and playback evidence logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent Fable 5 agent (or comparable OpenAI/Google model) verifies playback, not just presence: each run it loads the homepage on desktop and mobile, confirms the embed renders, plays, and features the owner, and checks the console for blocked-script errors — looping until all conditions pass, and re-checking every run because embeds die when videos get moved or set private.
Memory stores the embed source URL and last-verified playback, so any swap or takedown is caught on the next pass.
Each run logs playback evidence as a worked example in ## Example(s), compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /blog-posting-guidelines (Step 10 covers embedding source video in posts) · previous: check-lead-magnet-section-has-visual-mockup · next check: ensure-no-text-only-sections-spanning-full-viewport
