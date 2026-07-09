---
name: upload-real-photos-and-set-business-hours
description: Load the Google Business Profile with recent real photos (no stock) and make the posted hours match reality, including holidays.
category: Digital Plumbing
stage: —
definitive_article: /digital-plumbing
status: needs-work
---

# Upload Real Photos and Set Business Hours

**Use this when** a verified Google Business Profile has stock images, stale photos, an empty gallery, or hours that don't match when the business actually answers.

## Inputs
- Verified GBP with Manager or Owner access
- 10+ recent real photos from the owner's phone: owner headshot, team, storefront/vehicles, real jobs in progress, before/after shots
- The true operating hours, confirmed by the owner (including when phones are actually answered)

## Steps
1. Collect real photos only — phone-shot, recent, recognizably this business. Reject stock photography and AI-generated images on sight; they destroy trust and violate the no-stock rule.
2. Upload to the right GBP slots: logo, cover photo, then gallery photos across exterior, interior, team, and at-work categories.
3. Delete or flag outdated photos (old branding, ex-employees, previous location).
4. Set regular hours to match reality. If calls are answered beyond door hours, use the "more hours" options where applicable.
5. Add special hours for every upcoming holiday this quarter — wrong holiday hours generate the angriest reviews.
6. View the live listing on Google Maps from a phone: confirm photos render, the cover photo is the one you chose, and hours read correctly.
7. Set a recurring reminder to add fresh photos monthly — recency is a ranking and trust signal.

## Definition of done (QA checklist)
- [ ] 10 or more real photos live on the profile; zero stock or AI images
- [ ] Logo and cover photo set and rendering on the Maps listing
- [ ] Regular hours match confirmed reality; special hours set for upcoming holidays
- [ ] Outdated photos removed or flagged
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
This task never really ends — fresh photos monthly, special hours every holiday — which is exactly what a persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) is for: it uploads, confirms the live Maps rendering, and loops until every Definition-of-done box passes, not 90%.
It self-verifies against that checklist (photo count, zero stock, hours match reality), remembers in memory which photos and hours shipped on prior runs so each pass only adds what is new, and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /digital-plumbing
- Related (run order): verify-google-business-profile → ensure-nap-consistency-across-platforms → this → set-correct-business-categories
- Cross-links: /website-qa-audit (no-stock-images check) · /one-minute-video-guide (same phone-real-content principle)
