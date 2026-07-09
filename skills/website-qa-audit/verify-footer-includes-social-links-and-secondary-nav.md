---
name: verify-footer-includes-social-links-and-secondary-nav
description: Confirms the site footer carries working social media links and a secondary navigation so every page ends with somewhere useful to go.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Verify footer includes social links and secondary nav

**Use this when** running Layer 2 (Content Architecture Checks) of the Website QA Audit — the footer is the site-wide safety net for navigation and profile discovery.

## Inputs
- Site URL and the owner's canonical list of social profile URLs
- Desktop and mobile browsers
- The audit report/spreadsheet for logging results

## Steps
1. Scroll to the footer on the homepage and confirm social icons/links are present.
2. Click every social icon: each must open the owner's correct, live profile (the same URLs used in the schema sameAs list) — not a platform homepage, a dead account, or someone else's page.
3. Confirm a secondary navigation exists in the footer covering at least the key pages: services, about, blog, contact, and privacy/terms.
4. Click each secondary nav link and confirm it resolves to the right live page.
5. Verify the footer renders consistently on every template (post, page, landing) and on mobile — not just the homepage.
6. Log each link's destination and pass/fail in the audit report.

## Definition of done (QA checklist)
- [ ] Footer shows social links on every template, and 100% open the owner's correct live profiles
- [ ] Footer secondary nav present with all key pages linked and resolving correctly on desktop and mobile
- [ ] Link-by-link results logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent Fable 5 agent (or comparable OpenAI/Google model) renders the footer on every template and page type — not just the homepage — clicks through each social and nav link at desktop and mobile widths, and loops until every link resolves correctly everywhere the footer appears.
Memory keeps the footer link map and per-template verdicts, so re-runs only retest after theme or menu changes — and the check re-opens whenever a profile URL changes elsewhere in the audit.
Each run logs one worked example to ## Example(s), compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /digital-plumbing (social profiles setup) · Layer 3 sibling: check-social-profiles-linked-and-prominent · next check: verify-hero-section-contains-real-photo-of-person
