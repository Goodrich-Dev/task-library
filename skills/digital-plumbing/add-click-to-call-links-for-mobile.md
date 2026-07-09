---
name: add-click-to-call-links-for-mobile
description: Make every displayed phone number a tap-to-dial tel: link on mobile, tracked as a conversion event.
category: Digital Plumbing
stage: —
definitive_article: /digital-plumbing
status: needs-work
---

# Add Click-to-Call Links for Mobile

**Use this when** phone numbers on the site are plain text, when mobile visitors must copy-paste to call, or when call clicks aren't being measured.

## Inputs
- Canonical NAP phone number (one number, one format)
- Website edit access (header, footer, contact page, service pages)
- GTM container installed (for click tracking)

## Steps
1. Find every place a phone number renders: header, hero, footer, contact page, service pages, and any sticky bars.
2. Wrap each one in a tel: link using the canonical number (tel:+1XXXXXXXXXX format works everywhere). The visible text keeps the human-readable format from the NAP record.
3. Make the header number an easy thumb target on mobile — large enough to tap, visible without scrolling.
4. Test on a real phone: tap each instance; the dialer must open pre-filled with the correct number. Also confirm desktop behavior isn't broken.
5. Track it: in GTM, add a click trigger on tel: links firing an event into GA4 (and Contact to the Meta pixel if installed). Phone taps are conversions — measure them.
6. If call tracking with dynamic number insertion is in play, confirm the DNI script swaps the tel: link too, not just the visible text.

## Definition of done (QA checklist)
- [ ] Every displayed phone number on tested templates is a working tel: link
- [ ] Tap on a real phone opens the dialer with the correct canonical number
- [ ] Click-to-call event fires in GA4 on tap (verified in DebugView/Realtime)
- [ ] Number format on screen still matches the NAP record
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A max-effort agent (Claude Fable 5 or a comparable OpenAI/Google model) finds every rendered number — not just the obvious ones — wraps each in a tel: link, and verifies on a real device and in GA4 DebugView, looping until the entire Definition of done passes, not 90% of instances.
It self-verifies each item against that checklist, keeps the canonical number and the inventory of tel: locations in memory so new templates get caught on later runs, and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /digital-plumbing
- Related (run order): ensure-nap-consistency-across-platforms → this → set-up-call-tracking-for-phone-conversions → create-clear-conversion-path
- Cross-links: /website-qa-audit (CTA destination checks) · /dad
