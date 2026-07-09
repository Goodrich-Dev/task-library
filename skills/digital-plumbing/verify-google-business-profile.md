---
name: verify-google-business-profile
description: Complete Google's verification of the Google Business Profile and put admin control in the business owner's own hands, so the profile can rank in Maps and anchor the entity.
category: Digital Plumbing
stage: —
definitive_article: /digital-plumbing
status: complete
---

# Verify Google Business Profile

**Use this when** a business (or personal brand with a physical/service presence) has no verified Google Business Profile, or nobody knows which account controls it.

## Inputs
- Business owner's own Google account (never verify under an agency or VA account)
- Canonical NAP record: exact business Name, Address, Phone
- Ability to receive Google's verification (video walkthrough, postcard, phone, or email — whatever Google offers this listing)

## Steps
1. Search the exact business name on Google and Google Maps. Find the existing profile, including any unclaimed or duplicate listings.
2. If a profile exists, start "Claim this business" / "Own this business?" from the listing. If none exists, create one in the Google Business Profile manager with the canonical NAP.
3. Sign in as the business owner — the owner's Google account must end up as Primary owner. Agencies and VAs get added later as Managers, never as Primary owner.
4. Complete whichever verification method Google offers (video verification is most common now: film the storefront/vehicle/equipment and proof of business as prompted). Follow it to the end — a half-verified profile is invisible.
5. Once verified, audit Profile access: remove ex-employees and unknown accounts, demote agencies to Manager.
6. Confirm the profile data matches the canonical NAP character-for-character (this feeds the NAP consistency task).
7. Record the managing Google account and verification date in the client record.

## Definition of done (QA checklist)
- [ ] Profile shows as Verified in the Google Business Profile dashboard (no pending banner)
- [ ] Business owner's own Google account is Primary owner; access list contains no strangers
- [ ] Listing appears on Google Maps when searching the exact business name
- [ ] NAP on the profile matches the canonical NAP record exactly
- [ ] Managing account + verification date documented in the client record
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- The /digital-plumbing hub links the library's real GBP verification examples (Requirement 3). Example needed here — run the Meta-Article Prompt after the next real run.

## Run on a persistent agent (Fable 5)
Google's verification can stretch across days and methods, and a half-verified profile is invisible — a persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) follows it to the end, re-checking status and access until every Definition-of-done item passes, not 90%.
It self-verifies owner, access list, and NAP against that checklist, writes the managing account and verification date to memory so every downstream GBP run builds on confirmed control, and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /digital-plumbing
- Related (run order): ensure-nap-consistency-across-platforms → upload-real-photos-and-set-business-hours → set-correct-business-categories
- Cross-links: /website-qa-audit (Layer 3 re-checks GBP verification) · /personal-brand (Phase 1) · /dad (verified plumbing is a prerequisite)
