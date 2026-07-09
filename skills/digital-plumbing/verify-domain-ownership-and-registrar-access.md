---
name: verify-domain-ownership-and-registrar-access
description: Confirm the business actually owns its domain and can log into the registrar — the single point of failure under everything else in digital plumbing.
category: Digital Plumbing
stage: —
definitive_article: /digital-plumbing
status: needs-work
---

# Verify Domain Ownership and Registrar Access

**Use this when** onboarding any client, when nobody remembers where the domain is registered, or when a past webmaster "handled all that."

## Inputs
- The domain name(s) in use
- The business owner present (recovery may require their identity/email/payment history)
- WHOIS lookup access (any public WHOIS tool)

## Steps
1. Run a WHOIS lookup: identify the registrar, creation/expiry dates, and registrant (often privacy-masked — the registrar is the key fact).
2. Ask the owner to log into that registrar while you watch. If they can't, find who can: old webmaster, ex-agency, a defunct email. This is the moment to recover control, not during an outage.
3. If a third party holds the domain, transfer it: initiate a registrar account change or domain transfer into an account owned by the business, with the owner's email on file.
4. Harden the account: owner's current email as primary contact, two-factor authentication on, domain transfer lock on, auto-renew on with a valid payment method.
5. Check expiry: renew now if less than 6 months out. An expired domain takes the website, email, and every profile link down with it.
6. Confirm DNS management access from this account (or document where DNS is delegated) — sibling skills depend on it.
7. Record registrar, account holder, expiry date, and nameservers in the client record.

## Definition of done (QA checklist)
- [ ] Owner can personally log into the registrar account holding the domain
- [ ] Registrant/account belongs to the business, not a vendor or ex-employee
- [ ] 2FA on, transfer lock on, auto-renew on with valid payment; expiry >6 months out
- [ ] DNS management location confirmed and documented with nameservers
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) treats this as the single point of failure it is: it works recovery or transfer to the end — not "emailed the old webmaster, waiting" — and loops until every Definition-of-done item passes, not 90%.
It self-verifies 2FA, transfer lock, auto-renew, and expiry against that checklist, writes registrar, nameservers, and expiry date to memory so every later DNS, email, and GSC run builds on confirmed access, and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /digital-plumbing
- Related (run order): this → ensure-proper-dns-records → set-up-professional-email-on-domain → configure-spf-dkim-dmarc-for-deliverability
- Cross-links: /personal-brand (Phase 1: register the name domain) · verify-google-search-console-and-connect-to-ga4 (DNS TXT verification needs this access)
