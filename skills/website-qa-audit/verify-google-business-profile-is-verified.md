---
name: verify-google-business-profile-is-verified
description: Confirms the Google Business Profile tied to the site is actually verified by Google and under the owner's control, anchoring local trust signals.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Verify Google Business Profile is verified

**Use this when** running Layer 3 (Authority & Trust Checks) of the Website QA Audit — an unverified GBP can't rank in the map pack and signals an unclaimed entity.

## Inputs
- Owner access to the Google Business Profile (via google.com/business or managing directly from Google Search)
- The site URL and business NAP (name, address, phone) for cross-checking
- The audit report/spreadsheet for logging results

## Steps
1. Log into the Google Business Profile manager as the owner and confirm the profile status shows verified — no pending "Verify now" banner or suspension notice.
2. Confirm the OWNER holds primary ownership of the listing — not an old agency, a former employee, or an unknown manager account (check the Managers list).
3. Search the business name on Google and confirm the profile actually appears in Search/Maps with the knowledge-style panel showing.
4. Cross-check the profile's website field links to this site, and the NAP matches the site's footer and contact page exactly.
5. Confirm the profile is not flagged "Temporarily closed" or carrying a wrong category that contradicts the site.
6. Log verification status, ownership, and the NAP cross-check in the audit report with a screenshot.

## Definition of done (QA checklist)
- [ ] GBP status is verified, with the business owner holding primary ownership
- [ ] Profile is live in Google Search/Maps, links to this site, and its NAP exactly matches the site
- [ ] Status screenshot and cross-check logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
Run on a persistent agent (Claude Fable 5 or comparable OpenAI/Google models), this check never closes: each run re-confirms verified status, primary ownership, live panel presence, and exact NAP match against the site — looping on any mismatch until all four hold, because suspensions and ownership changes arrive without warning.
Memory stores the last-confirmed status, manager list, and NAP strings, so a re-run flags any drift — a new manager account, a changed phone number — the day it appears.
Each run logs status evidence as a worked example in ## Example(s), compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /digital-plumbing (GBP verification and NAP consistency) · previous: verify-achievements-are-evidenced-not-just-claimed · next check: check-schema-connects-to-all-verified-profiles
