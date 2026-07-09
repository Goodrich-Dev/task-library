---
name: install-google-tag-manager-container
description: Install one Google Tag Manager container on every page of the site so all future tracking (GA4, Meta pixel, call events) deploys without editing code.
category: Digital Plumbing
stage: —
definitive_article: GAP — to be written
status: gap
---

# Install Google Tag Manager Container

**Use this when** tracking tags are hard-coded into the theme, scattered across plugins, or missing entirely — GTM becomes the single tap point for all measurement.

## Inputs
- Google account owned by the business (GTM container must live in the client's account, with agency added as a user)
- WordPress admin access (theme header editing or a header/footer plugin)
- Google Tag Assistant for verification

## Steps
1. In the business owner's Google account, create a GTM account (company name) and one Web container named for the domain. One site, one container — never share containers across sites.
2. Copy the two install snippets GTM provides: the script for the head and the noscript for the opening of the body.
3. Install both snippets on every page — via the theme's header template or a header/footer plugin, so all templates (pages, posts, archives) carry it.
4. Publish the container. An unpublished container shows installed but fires nothing — this is the most common silent failure.
5. Verify with Tag Assistant: load the homepage, a service page, a blog post, and the contact/thank-you page; the container ID must appear and fire on each.
6. Migrate existing hard-coded tags (GA4, Meta pixel) into GTM as tags, then remove the hard-coded copies to prevent double-firing.
7. Add the agency/operator as a container User (the owner stays Admin). Record the container ID (GTM-XXXXXXX) in the client record.

## Definition of done (QA checklist)
- [ ] GTM container ID present and fires on every page in Tag Assistant (home, service, post, thank-you tested)
- [ ] Container is published — current live version, not just preview
- [ ] No duplicate/hard-coded tags left outside GTM (no double-firing in Tag Assistant)
- [ ] Container lives in the client's Google account; container ID documented
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) catches the classic silent failure — an installed-but-unpublished container — by verifying the container actually fires on every template, and loops through migrating and removing hard-coded tags until the full Definition of done passes with zero double-firing, not 90%.
It self-verifies in Tag Assistant against that checklist, stores the container ID and tag inventory in memory so the GA4, pixel, and call-tracking runs deploy into the same tap point, and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written. "How to Install and Configure GTM" is queued (High Priority) in Gaps & Tasks to Create; until it ships, /digital-plumbing is the parent hub.
- Related (run order): this → set-up-ga4-with-internal-traffic-filtering → install-meta-pixel-with-standard-events → set-up-call-tracking-for-phone-conversions
- Cross-links: /website-qa-audit (Layer 1: "GTM installed and firing on every page") · /dad (working pixels are a prerequisite)
