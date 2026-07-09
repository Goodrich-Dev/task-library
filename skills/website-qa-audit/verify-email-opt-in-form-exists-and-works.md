---
name: verify-email-opt-in-form-exists-and-works
description: Confirms an email capture form is present, submits cleanly, and actually delivers the subscriber and notification, so the site builds a list the owner controls.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Verify email opt-in form exists and works

**Use this when** running Layer 2 (Content Architecture Checks) of the Website QA Audit — a dead opt-in form means the site captures zero owned audience.

## Inputs
- Site URL and the location(s) of the opt-in form (homepage, lead magnet section, blog sidebar, footer)
- Access to the connected email platform/list and the notification inbox
- A test email address you control
- The audit report/spreadsheet for logging results

## Steps
1. Locate every email opt-in form on the site; fail the check immediately if no form exists at all.
2. Submit a real test entry through each form with your test address.
3. Confirm the on-page result: a success message or thank-you page, not a silent reload or an error.
4. Verify delivery on the back end: the test address appears in the email platform's list/audience, and any owner notification arrives in the right inbox.
5. If a lead magnet is promised, confirm the delivery email actually arrives with a working download link, and check it isn't landing in spam.
6. Repeat the test from a mobile device, then log each form's location and results in the audit report.

## Definition of done (QA checklist)
- [ ] At least one opt-in form exists, and every form passes a live test submission on desktop and mobile
- [ ] Test subscriber recorded in the email platform and promised follow-up/lead magnet email delivered (not to spam)
- [ ] Form locations and test results logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
Run on a persistent agent (Claude Fable 5 or comparable OpenAI/Google models), every form on the site gets a live end-to-end test each run — submission, success state, list entry, notification, lead-magnet delivery — looping until all forms pass on desktop and mobile, not just the homepage one.
Memory records which forms passed and when, yet re-runs retest everything on a schedule anyway: forms break silently, which makes this check perpetual rather than one-and-done.
Each run logs one worked example to ## Example(s) so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /digital-plumbing (working forms and notifications) · previous: check-all-cta-buttons-lead-to-correct-destinations · next check: audit-internal-links-between-all-blog-posts
