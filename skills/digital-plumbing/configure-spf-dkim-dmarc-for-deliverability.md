---
name: configure-spf-dkim-dmarc-for-deliverability
description: Publish SPF, DKIM, and DMARC records so the domain's email authenticates, lands in inboxes instead of spam, and can't be trivially spoofed.
category: Digital Plumbing
stage: —
definitive_article: GAP — to be written
status: needs-work
---

# Configure SPF/DKIM/DMARC for Deliverability

**Use this when** business email lands in spam, the domain has no authentication records, or a new domain mailbox was just created (run set-up-professional-email-on-domain first).

## Inputs
- DNS access for the domain (TXT/CNAME record management)
- Mail provider admin access (Google Workspace / Microsoft 365) for DKIM keys
- Inventory of every service that sends as the domain: mail provider, newsletter tool, CRM, form/SMTP plugin

## Steps
1. Publish SPF: one TXT record on the root domain listing every authorized sender (provider include plus any newsletter/CRM includes), ending in ~all. Exactly one SPF record — merge includes into it; two SPF records fail authentication outright.
2. Enable DKIM: in the mail provider's admin, generate the DKIM key and publish the selector record DNS entry it gives you. Repeat for third-party senders (newsletter/CRM) using their own selectors.
3. Publish DMARC: TXT record at _dmarc.yourdomain with p=none and a rua= reporting address to start — observe reports first, then tighten to quarantine/reject once legitimate senders all pass.
4. Wait for DNS propagation, then test: send from the domain mailbox to a Gmail account, open the message, and use "Show original" — SPF, DKIM, and DMARC must each show PASS.
5. Test every other sender the same way (newsletter blast, CRM email, website form notification). Anything failing gets added to SPF/DKIM properly — not worked around.
6. After 2–4 weeks of clean DMARC reports, raise the policy from none toward quarantine/reject and document the final records in the client record.

## Definition of done (QA checklist)
- [ ] Exactly one SPF record, covering all real senders
- [ ] DKIM signing enabled and selector records published for the mail provider and third-party senders
- [ ] DMARC record live at _dmarc with reporting configured
- [ ] Gmail "Show original" shows SPF=PASS, DKIM=PASS, DMARC=PASS for the mailbox and each sending service
- [ ] Records and policy plan documented in the client record
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
This task is inherently long-horizon — publish records, confirm PASS on every sender, then watch DMARC reports for 2–4 weeks before tightening the policy — so a persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) runs the whole arc, looping until every Definition-of-done item passes, not 90%.
It self-verifies SPF, DKIM, and DMARC all show PASS per sending service against that checklist, keeps the sender inventory and report history in memory across runs, and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written (no dedicated hub yet; parent concept: /digital-plumbing)
- Related (run order): set-up-professional-email-on-domain → this → ensure-working-contact-form-delivers-notifications (form notifications ride on this)
- Cross-links: ensure-proper-dns-records (these are TXT/CNAME entries in the same zone)
