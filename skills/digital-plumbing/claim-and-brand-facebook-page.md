---
name: claim-and-brand-facebook-page
description: Put the Facebook business page under the owner's control with correct admin structure, real branding, and NAP that matches the canon.
category: Digital Plumbing
stage: —
definitive_article: /digital-plumbing
status: needs-work
---

# Claim and Brand Facebook Page

**Use this when** the Facebook page is unclaimed, controlled by an ex-employee or old agency, duplicated, unbranded, or showing stale business info.

## Inputs
- Business owner's personal Facebook profile (pages are controlled through real profiles/Business Manager)
- Canonical NAP record, real cover photo, and logo or owner headshot
- Client's Meta Business Manager (create one if none exists — it also owns the pixel and ad account)

## Steps
1. Search Facebook for the business name. Identify the real page plus any duplicates or auto-generated unofficial pages; claim or merge/report duplicates so one page remains.
2. Fix control first: the owner's profile gets Full control of the page. Agencies and VAs get task-level access through Business Manager — never sole admin. Remove ex-employees.
3. Connect the page to the client's Business Manager (prerequisite for the pixel and Dollar a Day).
4. Set the page name and username/handle to match the business entity exactly, per the canonical NAP.
5. Brand it real: profile photo (logo, or headshot for personal brands), real cover photo from the business — no stock.
6. Complete the About section: canonical NAP, hours matching GBP, website link, and a first-person description of who the business serves.
7. Verify from a logged-out browser: correct name, photos, phone, address, and site link all render publicly.

## Definition of done (QA checklist)
- [ ] Exactly one page exists for the business; duplicates merged or reported
- [ ] Owner holds Full control; no ex-employee or unknown admins; agency on task access via Business Manager
- [ ] Page name and handle match the business entity; About shows canonical NAP + working site link
- [ ] Profile and cover photos are real brand assets, no stock
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) hunts duplicates until exactly one page remains, fixes control before cosmetics, and verifies everything from a logged-out browser — looping until the full Definition of done passes, not 90%.
It self-checks every line — admin roles, canonical NAP, real photos — against that checklist, stores the page URL and admin structure in memory for the sameAs and Business Manager runs that follow, and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /digital-plumbing
- Related (run order): ensure-nap-consistency-across-platforms → this → convert-instagram-to-professional-account → set-up-consistent-headshots-and-bios-across-profiles → add-schema-markup-person-localbusiness (add page URL to sameAs)
- Cross-links: /dad (Business Manager + page setup feeds campaigns) · /social-amplification (Stage 1)
