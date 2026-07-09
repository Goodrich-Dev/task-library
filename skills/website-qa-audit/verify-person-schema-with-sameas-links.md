---
name: verify-person-schema-with-sameas-links
description: Validates that Person schema markup exists, parses cleanly, and carries sameAs links to the owner's social profiles, tying the personal brand together as one entity for Google.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: needs-work
---

# Verify Person schema with sameAs links

**Use this when** running Layer 1 (Digital Plumbing Checks) of the Website QA Audit — schema is how Google connects the person, the site, and the social profiles into one entity.

## Inputs
- Site URL (homepage and about page are the usual schema homes)
- Google Rich Results Test (search.google.com/test/rich-results) and validator.schema.org
- The owner's list of social profile URLs (LinkedIn, Facebook, Instagram, YouTube, Twitter/X)
- The audit report/spreadsheet for logging results

## Steps
1. Run the homepage URL through the Google Rich Results Test and confirm the page's structured data parses with zero errors.
2. Inspect the detected markup for a `Person` type (or Person nested in LocalBusiness/Organization) naming the site owner — exact name match with the site and GBP.
3. Confirm the Person markup includes a `sameAs` array, and that each entry is a full URL to one of the owner's real social profiles.
4. Click every sameAs URL — each must resolve to the owner's live profile, not a 404, a placeholder, or someone else's account.
5. Re-validate at validator.schema.org to catch warnings the Rich Results Test skips (missing image, url, or jobTitle properties).
6. Log schema type found, sameAs URLs verified, and validator results in the audit report.

## Definition of done (QA checklist)
- [ ] Person schema present and parsing with zero errors in the Rich Results Test
- [ ] sameAs array present and every listed URL resolves to the owner's live profile
- [ ] Validation results and verified URL list logged, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
Run persistent (Fable 5 / comparable OpenAI or Google models), this check extends beyond the homepage: the agent validates structured data on every page that emits Person markup, resolves every sameAs URL with a live fetch, and loops fix-revalidate until both validators return zero errors and every profile link lands on the owner's real account.
Memory keeps the verified sameAs set, so a re-run flags any added, removed, or newly dead profile instantly rather than re-auditing blind.
Each run appends a worked example to ## Example(s), compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /digital-plumbing (schema implementation if this check fails) · Layer 3 sibling: check-schema-connects-to-all-verified-profiles · next check: check-favicon-is-set
