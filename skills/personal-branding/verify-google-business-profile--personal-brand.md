---
name: verify-google-business-profile--personal-brand
description: Complete Google's verification of the Business Profile attached to the personal brand, where a qualifying business exists.
category: Personal Branding
stage: —
definitive_article: /personal-brand
status: needs-work
---

# Verify Google Business Profile

**Use this when** the personal brand sits on a real business with a storefront or service area — Phase 1 (Digital Plumbing). Skip if no qualifying business exists.

## Inputs
- Confirmation the business qualifies for GBP (physical location or service area)
- A Google account owned by the person (not an agency)
- Exact NAP — name, address, phone — matching the website
- Real photos of the person, team, and work

## Steps
1. Check applicability first: GBP requires a real storefront or service-area business. A pure personal brand with no qualifying business skips this skill — document the skip decision and move on.
2. Search Google Maps for an existing unclaimed listing before creating a new one; claim it if it exists (duplicates fragment the entity).
3. Enter the business name, address, and phone exactly as they appear on the entity-home website — NAP consistency is an entity signal.
4. Complete Google's verification flow (postcard, phone, email, or video — whichever Google offers).
5. Confirm the person's own Google account holds the Owner role; agencies and VAs get Manager access at most.
6. Fill the profile completely: accurate primary and secondary categories, real hours, real photos (no stock), and the website field pointing to yourname.com.
7. Record the verification date and account details in the credentials vault.

## Definition of done (QA checklist)
- [ ] Profile shows as verified by Google, or a documented "not applicable" decision exists
- [ ] Owner role held by the person's own Google account
- [ ] NAP matches the website exactly; website field points to yourname.com
- [ ] Real photos uploaded; categories and hours accurate
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Marko Sipila (HVAC Quote) and Zach Peyton (Superior Fence & Rail) — service-business personal-brand builds where a verified GBP is part of the entity's plumbing, tied to the owner's name and site.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) first resolves applicability from memory — if no qualifying business exists it documents the skip and exits clean; otherwise it drives the claim-and-verify flow across days or weeks (postcard waits included), looping until every Definition-of-done box passes, not 90%.
It self-verifies against the live listing: verified badge showing, Owner role on the person's account, NAP matching the entity home character for character.
It logs the verification record and NAP to memory for the Phase 4 identity audit, and a meta-article example each run so the brand compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /personal-brand
- Related: /digital-plumbing · previous: build-personal-brand-website · next: set-up-professional-social-profiles
