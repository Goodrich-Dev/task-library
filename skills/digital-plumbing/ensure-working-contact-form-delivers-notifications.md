---
name: ensure-working-contact-form-delivers-notifications
description: Prove the contact form actually submits and that notifications land in an inbox the owner reads — because a silent form is a lead funeral.
category: Digital Plumbing
stage: —
definitive_article: /digital-plumbing
status: needs-work
---

# Ensure Working Contact Form Delivers Notifications

**Use this when** taking over any site, after any form/plugin/email change, or whenever the owner says "we don't get many leads from the website."

## Inputs
- The live form URL(s) and access to the form plugin settings
- The correct destination inbox — confirmed with the owner as one they actually monitor
- Email deliverability basics in place (see configure-spf-dkim-dmarc-for-deliverability)

## Steps
1. Submit a real test through the live form on desktop and on a phone, using an obvious test marker in the message.
2. Confirm the notification arrives in the owner's monitored inbox within minutes. Check spam/junk. Check it didn't go to a dead VA, ex-employee, or agency address.
3. Fix the recipient list in the form settings if wrong. If notifications don't send at all, route form mail through authenticated SMTP (and verify SPF/DKIM cover the sender).
4. Confirm the visitor-facing success state: a thank-you message or thank-you page must appear — this is also the conversion-tracking hook.
5. Wire the submission into measurement: fire a form-submit event via GTM into GA4 (and Meta pixel Lead, if installed).
6. Re-test end-to-end after every fix: submit → notification received → thank-you shown → event recorded.
7. Put a quarterly form re-test on the maintenance calendar — forms break silently when plugins update.

## Definition of done (QA checklist)
- [ ] Test submission from mobile and desktop arrives in the owner's monitored inbox, not spam
- [ ] Thank-you message/page displays after submission
- [ ] Form-submit event visible in GA4 (and Lead in Meta Events Manager if pixel installed)
- [ ] No dead or wrong recipients left in form settings
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) re-runs the full chain — submit, notification received, thank-you shown, GA4 event — after every change, looping until all Definition-of-done boxes pass, not 90%; since forms break silently, it also owns the quarterly re-test.
It self-verifies with real test submissions against that checklist, keeps recipient/SMTP settings and past failure causes in memory so regressions are caught on sight, and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /digital-plumbing
- Related (run order): configure-spf-dkim-dmarc-for-deliverability → this → create-clear-conversion-path → set-up-ga4-with-internal-traffic-filtering
- Cross-links: /website-qa-audit (email opt-in / CTA checks) · /dad (conversion tracking prerequisite)
