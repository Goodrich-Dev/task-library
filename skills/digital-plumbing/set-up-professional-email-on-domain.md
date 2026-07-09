---
name: set-up-professional-email-on-domain
description: Move the business off @gmail.com onto name@itsowndomain.com with a real mail provider, so every email reinforces the brand and deliverability can be authenticated.
category: Digital Plumbing
stage: —
definitive_article: GAP — to be written
status: needs-work
---

# Set Up Professional Email on Domain

**Use this when** the business still runs on a free @gmail/@yahoo address, or team members each use random personal addresses for business mail.

## Inputs
- Domain with registrar/DNS access verified (run verify-domain-ownership-and-registrar-access first)
- Chosen mail provider — Google Workspace or Microsoft 365 are the standard choices
- List of needed addresses: owner (firstname@domain) plus role addresses (info@, support@) as required

## Steps
1. Sign the business up for the mail provider under the owner's control (owner is the admin of the Workspace/365 tenant — same ownership rule as every other platform).
2. Create the owner's mailbox and any role addresses. Keep it simple: one real mailbox per human; role addresses can alias or forward.
3. Add the provider's MX records at the DNS host (and remove old/conflicting MX). Mail flow follows MX — this is the cutover moment, so do it deliberately.
4. Verify send and receive both directions: from the new address to an external account and back.
5. Bridge the old address: set the legacy @gmail to forward to the new mailbox and reply from the domain address, so nothing is missed during migration.
6. Update the public touchpoints to the domain address: website contact form recipient and displayed email, GBP, social profile contact fields, and email signatures (with the canonical NAP).
7. Proceed immediately to configure-spf-dkim-dmarc-for-deliverability — an unauthenticated new domain address lands in spam.

## Definition of done (QA checklist)
- [ ] name@businessdomain.com sends and receives successfully both directions
- [ ] MX records resolve to the chosen provider; no stale MX entries remain
- [ ] Owner holds admin of the mail tenant; mailboxes/aliases documented
- [ ] Website, GBP, and social contact points show the domain address; legacy address forwards
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) stages the MX cutover deliberately, tests send and receive in both directions, and updates every public touchpoint — looping until the entire Definition of done passes, not 90%, because one stale MX record fails the run.
It self-verifies against that checklist, builds on the registrar and DNS access already confirmed in memory from prior runs, records the mailbox map for the SPF/DKIM/DMARC step that follows, and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written (no dedicated hub yet; parent concept: /digital-plumbing)
- Related (run order): verify-domain-ownership-and-registrar-access → ensure-proper-dns-records → this → configure-spf-dkim-dmarc-for-deliverability
- Cross-links: ensure-working-contact-form-delivers-notifications (form mail should come from this domain)
