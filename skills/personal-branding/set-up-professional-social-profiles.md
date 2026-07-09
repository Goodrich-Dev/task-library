---
name: set-up-professional-social-profiles
description: Create or claim professional profiles on LinkedIn, Facebook, Instagram, YouTube, and Twitter/X that all point back to the entity home.
category: Personal Branding
stage: —
definitive_article: /personal-brand
status: needs-work
---

# Set up professional social profiles

**Use this when** the entity home is live and the person needs the five core profiles that Person schema will bind into one entity — Phase 1 (Digital Plumbing).

## Inputs
- Live entity home at yourname.com
- The canonical name string and professional email on the domain
- Access to (or creation rights for) LinkedIn, Facebook, Instagram, YouTube, and Twitter/X accounts

## Steps
1. Inventory what already exists — claim and clean up old or duplicate accounts before creating new ones; duplicates fragment the entity.
2. Secure handles as close to the canonical name as possible, and use the same handle pattern on every platform.
3. Set up each platform professionally: LinkedIn profile (plus company page if there is a business), Facebook business or Public Figure page, Instagram switched to a professional account and connected to the Facebook page, YouTube channel branded and connected to the website, Twitter/X profile.
4. Put yourname.com in the website/bio field of every single profile — this is half of the entity loop (the schema sameAs array is the other half).
5. Register each account to the person's professional email on their own domain; the person owns every account, with delegated roles for helpers.
6. Save the final URL of every profile into one list — this becomes the sameAs array in implement-person-schema-with-sameas-links.
7. Leave photos and bios for the next skill, which standardizes them across all platforms in one pass.

## Definition of done (QA checklist)
- [ ] All five platforms live: LinkedIn, Facebook, Instagram (professional), YouTube, Twitter/X
- [ ] Every profile's website field links to yourname.com
- [ ] Every account owned by the person under their own email; no orphan or duplicate profiles left
- [ ] Profile URL list saved for the Person schema sameAs array
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) works all five platforms as one campaign: it inventories and de-duplicates existing accounts, claims handles matching the canonical name held in memory from Phase 1, and loops until the Definition-of-done passes in full — five live profiles, every website field on yourname.com — not 90%.
It self-verifies by opening each finished profile logged out and confirming the link back to the entity home.
It saves the final profile-URL list to memory as the exact sameAs array the Person-schema skill consumes next, and logs a meta-article example each run (this file still needs its first) so the brand compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /personal-brand
- Related: /digital-plumbing · previous: verify-google-business-profile · next: add-consistent-headshots-and-bios-across-profiles → implement-person-schema-with-sameas-links
