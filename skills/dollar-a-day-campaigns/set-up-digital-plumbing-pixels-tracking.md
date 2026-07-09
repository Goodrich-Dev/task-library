---
name: set-up-digital-plumbing-pixels-tracking
description: Stand up the tracking layer — verified profiles, working pixels, end-to-end conversion tracking — before the first dollar is spent, so every $1/day test produces readable data.
category: Dollar a Day Campaigns
stage: Promote
definitive_article: /dad
status: complete
---

# Set up digital plumbing (pixels, tracking)

**Use this when** prerequisites have passed and campaigns are next — no plumbing, no launch; Dollar a Day without tracking is gambling, not testing.

## Inputs
- Admin access to the website, domain, and all social/ad accounts (owned by the business owner, not an agency)
- The conversion actions that matter (form fill, call, booking, purchase)
- The customer email list and any existing engagement sources for seed audiences

## Steps
1. Audit ownership first: who controls the ad account, page, pixel, and domain? Recover anything held by a past agency or VA before building — see /digital-plumbing for the full standard.
2. Verify the profiles ads will run from: Facebook page claimed, Instagram converted to professional and connected, YouTube channel branded, Google Business Profile verified — one consistent entity everywhere.
3. Install the Meta pixel on every page, then add standard events (Lead, Contact, Purchase) on the actions that matter. PageView-only is plumbing theater.
4. Wire the Google side: Tag Manager container, GA4 property, Search Console connected — paid and organic must read from the same dashboard.
5. Make conversions trackable end-to-end: form notifications delivering, call tracking if the phone is the conversion, purchase events firing with values.
6. Build seed custom audiences now — site visitors, video viewers, page engagers, customer email upload — so warm layers exist on day one, not week six.
7. QA with a live test: submit a test lead and watch it register in the pixel, GA4, and the inbox/CRM before any ad set spends.

## Definition of done (QA checklist)
- [ ] Pixel fires on every page with standard events on key actions (verified with a test event)
- [ ] One test conversion traced end-to-end: pixel → analytics → notification/CRM
- [ ] All ad-bearing profiles verified and owned by the business owner
- [ ] Seed custom audiences created and populating
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run (a local-service plumbing rescue, e.g., recovering pixel ownership before relaunching $1/day, is the ideal first candidate).

## Run on a persistent agent (Fable 5)
Run this on a persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) that loops until the whole Definition of done passes — pixel events verified, one test conversion traced pixel → analytics → CRM, ownership confirmed — not "pixel installed, probably fine."
It self-verifies with the live test lead rather than trusting setup screens, and records the ownership/access map in memory so the next run detects drift (a pixel quietly reassigned to an agency is a failed run, caught before launch).
Each run, log the setup or rescue as a meta-article example so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /dad
- Related: /digital-plumbing (full infrastructure standard) · /social-amplification (Stage 1: Plumbing) · /website-qa-audit (Layer 1 verification checks)
- Run order (DAD core): verify-prerequisites-product-customers-content → **set-up-digital-plumbing-pixels-tracking** → identify-signals-worth-amplifying
