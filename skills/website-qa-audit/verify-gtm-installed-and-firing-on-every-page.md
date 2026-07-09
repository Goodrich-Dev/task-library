---
name: verify-gtm-installed-and-firing-on-every-page
description: Confirms Google Tag Manager is present and firing site-wide so every downstream tracking tag works, for any personal-brand or local-service site under audit.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Verify GTM installed and firing on every page

**Use this when** starting Layer 1 (Digital Plumbing Checks) of the Website QA Audit — tracking is worthless if the container isn't on every page.

## Inputs
- Site URL plus a full page list (XML sitemap or crawl export)
- The expected GTM container ID (GTM-XXXXXXX) from the owner's Tag Manager account
- Google Tag Assistant (tagassistant.google.com or the Chrome extension)
- The audit report/spreadsheet for logging results

## Steps
1. Open the owner's Tag Manager account (Admin → Container Settings) and note the expected container ID.
2. Connect the homepage in Google Tag Assistant and confirm the GTM container loads and the ID matches — no typo'd or duplicate containers.
3. View page source and confirm the GTM script is in the `<head>` and the noscript iframe sits after the opening `<body>` tag.
4. Repeat the Tag Assistant check on one page of every template type: homepage, service page, blog post, about, contact, and any landing pages.
5. Spot-check at least one URL from each sitemap section; flag every page where the container does not fire.
6. Log pass/fail per page in the audit report with the container ID found and a Tag Assistant screenshot for any failure.

## Definition of done (QA checklist)
- [ ] The correct GTM container fires on 100% of checked pages — zero pages missing the snippet
- [ ] Exactly one container fires — no duplicate or orphaned containers detected by Tag Assistant
- [ ] Pass/fail logged per template type in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google frontier model) doesn't spot-check template types — it walks the full sitemap, fetches every URL's source, and confirms the container ID in the `<head>` plus the noscript iframe on each page, looping until 100% of pages fire exactly one correct container.
It self-verifies by re-fetching every page it marked fixed, and keeps a memory ledger of passed URLs so each re-run only retests failures and newly published pages.
Every run appends one worked example to ## Example(s) via the Meta-Article Prompt, so the audit library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /digital-plumbing (how to install GTM if this check fails) · next check: verify-ga4-configured-with-internal-traffic-filtered
