---
name: verify-meta-pixel-installed-with-lead-events
description: Confirms the Meta pixel loads on every page and fires standard Lead events on key actions, so Dollar a Day campaigns can optimize and retarget correctly.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Verify Meta pixel installed with lead events

**Use this when** running Layer 1 (Digital Plumbing Checks) of the Website QA Audit — without pixel events, ad spend can't be attributed or optimized.

## Inputs
- The expected Pixel ID from the owner's Meta Events Manager
- Meta Pixel Helper (Chrome extension) and access to Events Manager → Test Events
- List of key conversion actions (contact form, opt-in form, booking, click-to-call)
- The audit report/spreadsheet for logging results

## Steps
1. Get the Pixel ID from Meta Events Manager and confirm the owner's Business Manager controls it.
2. Load the homepage with Meta Pixel Helper open; confirm one pixel with the correct ID fires a PageView — flag duplicates or wrong IDs.
3. Repeat on every template type (service page, blog post, contact, landing pages) to confirm the base pixel is site-wide.
4. Complete each key action with a test submission (contact form, email opt-in, booking) and confirm Pixel Helper shows a standard **Lead** event — not just PageView.
5. Cross-check in Events Manager → Test Events that the events arrive server-side with the right page URLs.
6. Log pixel ID, pages checked, and each event result in the audit report with Pixel Helper screenshots for failures.

## Definition of done (QA checklist)
- [ ] One pixel with the correct ID fires PageView on 100% of checked pages — no duplicates
- [ ] Every key conversion action fires a standard Lead event confirmed in both Pixel Helper and Test Events
- [ ] Results and evidence logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A max-effort persistent agent (Fable 5 or comparable OpenAI/Google models) loads every URL in the sitemap — not one per template — confirming exactly one correct pixel fires PageView, then drives a test submission through every conversion action and watches Test Events until each fires a Lead, looping until both thresholds hit 100%.
It self-verifies by retesting after every fix, and its memory ledger of passed pages and passed events means re-runs only touch what is new or previously broken.
Every run appends one worked example to ## Example(s) so the audit library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /digital-plumbing (pixel installation if this check fails) · previous: verify-ga4-configured-with-internal-traffic-filtered · next check: verify-https-with-no-mixed-content
