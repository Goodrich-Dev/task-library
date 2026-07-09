---
name: ensure-proper-dns-records
description: Audit the domain's DNS zone so A/CNAME records point at the live site, MX at the mail provider, and TXT records carry verifications — with no stale leftovers.
category: Digital Plumbing
stage: —
definitive_article: GAP — to be written
status: needs-work
---

# Ensure Proper DNS Records

**Use this when** taking over a domain, after any host or mail migration, or when the site/email misbehaves intermittently and old records are suspect.

## Inputs
- DNS management access (from verify-domain-ownership-and-registrar-access)
- Current truth: live webhost IP/hostname, mail provider, and active third-party services
- Any DNS lookup tool to confirm what actually resolves publicly

## Steps
1. Export or screenshot the current zone before touching anything — your rollback and your before evidence.
2. Web records: confirm the apex domain's A (or ALIAS) record and the www CNAME both point at the current webhost. Both apex and www must load the site (one 301-redirecting to the canonical version).
3. Mail records: confirm MX points only at the current mail provider — stale MX from an old host silently eats mail.
4. TXT records: confirm SPF and DMARC (sibling skill), the Google Search Console verification TXT, and any provider verifications. Add what's missing.
5. Hunt zombies: records pointing at dead hosts, old builders, ex-agency subdomains, or abandoned services. Remove them — dangling records are a security and confusion hazard.
6. Verify public resolution after changes (DNS lookup from outside, not just the DNS panel), allowing for TTL propagation.
7. Document the final zone — every record and why it exists — in the client record, so the next person doesn't have to guess.

## Definition of done (QA checklist)
- [ ] Apex and www both resolve to the live site over HTTPS
- [ ] MX records point only at the current mail provider; mail send/receive tested
- [ ] TXT records present for SPF, DMARC, and GSC verification
- [ ] No stale or dangling records remain; final zone documented with purpose per record
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) snapshots the zone first, fixes web, mail, and TXT records, hunts zombie entries, and re-checks public resolution after TTL propagation — looping until every Definition-of-done box passes, not 90%.
It self-verifies from outside the DNS panel against that checklist, keeps the documented zone — every record and why it exists — in memory so the next run diffs against known-good, and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written (no dedicated hub yet; parent concept: /digital-plumbing)
- Related (run order): verify-domain-ownership-and-registrar-access → this → set-up-professional-email-on-domain → configure-spf-dkim-dmarc-for-deliverability → configure-https-with-no-mixed-content
- Cross-links: verify-google-search-console-and-connect-to-ga4 (DNS TXT verification lives here)
