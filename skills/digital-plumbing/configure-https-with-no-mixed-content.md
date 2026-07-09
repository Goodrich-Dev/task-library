---
name: configure-https-with-no-mixed-content
description: Serve the entire site over HTTPS with zero mixed-content warnings so browsers, Google, and visitors trust every page.
category: Digital Plumbing
stage: —
definitive_article: /digital-plumbing
status: needs-work
---

# Configure HTTPS With No Mixed Content

**Use this when** any page shows "Not secure," a broken padlock, or console mixed-content warnings — or when HTTPS has never been verified end-to-end.

## Inputs
- Hosting control panel access (SSL certificate management)
- WordPress admin access
- List of key templates to test: homepage, contact page, a service page, a blog post

## Steps
1. Confirm a valid SSL certificate covers both the apex domain and www, and that it auto-renews at the host.
2. Force HTTPS site-wide: 301-redirect every http:// URL to https:// (host setting or server config). Test by loading the plain http:// version — it must redirect.
3. In WordPress, set both the WordPress Address and Site Address to https://.
4. Hunt mixed content: open each key template, check the browser console for mixed-content warnings, and search page source for hard-coded http:// references in images, scripts, stylesheets, and embeds.
5. Fix offenders at the source — update URLs in content and theme settings (a search-replace on http://yourdomain works for legacy content). Re-check third-party embeds.
6. Re-test all key templates: full padlock, no warnings, no console errors. Then confirm Google Search Console tracks the https property.

## Definition of done (QA checklist)
- [ ] Valid certificate on apex and www, auto-renewing
- [ ] http:// URLs 301-redirect to https:// (tested)
- [ ] Homepage, contact, service page, and a blog post all show the padlock with zero mixed-content console warnings
- [ ] No hard-coded http:// asset references remain in source on tested templates
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) sweeps template after template — load, read the console, fix the http:// reference, reload — and refuses to stop at "mostly green": it loops until every Definition-of-done item passes, not 90%.
It self-verifies against that checklist on all key templates, keeps the list of fixed offenders and tested templates in memory so later runs diff new content instead of re-auditing blind, and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /digital-plumbing
- Related (run order): ensure-proper-dns-records → this → ensure-site-loads-under-3-seconds-on-mobile
- Cross-links: /website-qa-audit (Layer 1 HTTPS check)
