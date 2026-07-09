---
name: ensure-site-loads-under-3-seconds-on-mobile
description: Get the website loading in under 3 seconds on a mobile device, because slow plumbing wastes every ad dollar and ranking the site earns.
category: Digital Plumbing
stage: —
definitive_article: /digital-plumbing
status: needs-work
---

# Ensure Site Loads Under 3 Seconds on Mobile

**Use this when** the site feels slow on a phone, PageSpeed Insights mobile scores are poor, or before sending any Dollar a Day traffic to the site.

## Inputs
- Admin access to WordPress (plugins, theme, media) and hosting/CDN
- Baseline measurement: PageSpeed Insights mobile run for the homepage and the top landing page
- List of the highest-traffic pages (from GA4 if installed)

## Steps
1. Baseline first (MAA: Metrics before Action): run PageSpeed Insights on mobile for the homepage and top landing pages. Save scores and load times — this is your before evidence.
2. Fix images, the usual offender: compress, serve modern formats, size to display dimensions, lazy-load below-the-fold images. Hero images shot on a phone are often uploaded at full resolution — scale them.
3. Cut render-blocking weight: remove unused plugins and scripts, defer non-critical JavaScript, drop heavy page-builder modules that load site-wide.
4. Enable caching at the host and a CDN if available; verify caching is actually serving (check response headers).
5. Re-test on PageSpeed Insights and on a real phone over cellular — the lived experience is the test that matters.
6. Repeat steps 2–4 until mobile load is under 3 seconds, then record before/after numbers in the client record (Analysis → Action complete).

## Definition of done (QA checklist)
- [ ] Homepage and top landing page load in under 3 seconds on mobile (PageSpeed Insights + real-device check)
- [ ] No unused plugins or render-blocking scripts left from the audit
- [ ] Caching/CDN confirmed serving
- [ ] Before/after measurements recorded in the client record
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
This is a literal optimization loop, so run it on a max-effort agent (Claude Fable 5 or a comparable OpenAI/Google model): re-measure PageSpeed after every fix — images, scripts, caching — and keep cutting weight until mobile load is under 3 seconds and every Definition-of-done box passes, not 90%.
It self-verifies against that checklist with fresh measurements rather than assuming a fix worked, carries the before/after baselines in memory across runs so regressions stand out, and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /digital-plumbing
- Related (run order): configure-https-with-no-mixed-content → this → write-proper-title-tags-and-meta-descriptions
- Cross-links: /website-qa-audit (Layer 1 speed check) · /maa (measure → analyze → act) · /dad (never pay to send traffic to a slow page)
