---
name: convert-instagram-to-professional-account
description: Switch Instagram to a professional account connected to the Facebook page, with handle, bio, and photo matching the brand canon.
category: Digital Plumbing
stage: —
definitive_article: /digital-plumbing
status: needs-work
---

# Convert Instagram to Professional Account

**Use this when** the business's Instagram is still a personal account, isn't connected to the Facebook page, or carries an off-canon handle, bio, or photo.

## Inputs
- Login to the Instagram account (owner-held credentials)
- Claimed, branded Facebook page (run claim-and-brand-facebook-page first)
- Canonical headshot/logo and bio copy, plus the canonical NAP contact details

## Steps
1. In Instagram settings, switch the account type to Professional (Business for a company; Creator fits some personal brands). This unlocks insights, contact buttons, and ad eligibility.
2. Connect the account to the business's Facebook page during the professional setup (via the client's Business Manager / Meta Business Suite). Without this link, Dollar a Day can't run placements or use the account properly.
3. Set the username and display name to match the business entity as closely as the platform allows — same spelling as the canon.
4. Apply the canonical profile photo (same headshot or logo used everywhere) and write the bio in first person: who you help, where, with what proof. Add the website link.
5. Add contact options — the canonical email and phone from the NAP record.
6. Confirm in Business Manager/Business Suite that the IG account appears alongside the page, and verify the public profile from a logged-out view.
7. Add the Instagram URL to the schema sameAs list (sibling skill).

## Definition of done (QA checklist)
- [ ] Account shows as Professional with insights available
- [ ] Connected to the correct Facebook page under the client's Business Manager
- [ ] Handle, display name, photo, and bio match the brand canon; website link works
- [ ] Contact options show canonical email/phone
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) runs the conversion, the Business Manager connection, and the canon pass — handle, photo, bio, contacts — as one loop, re-checking the public profile logged-out until every Definition-of-done box passes, not 90%.
It pulls the canonical headshot and bio from memory of prior runs, records the IG URL for the schema sameAs step that follows, self-verifies against that checklist, and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /digital-plumbing
- Related (run order): claim-and-brand-facebook-page → this → set-up-youtube-channel-with-proper-branding → set-up-consistent-headshots-and-bios-across-profiles
- Cross-links: /dad (IG placements) · /personal-brand (Phase 1 social profiles)
