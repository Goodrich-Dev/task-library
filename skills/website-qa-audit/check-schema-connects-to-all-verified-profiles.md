---
name: check-schema-connects-to-all-verified-profiles
description: Confirms the schema sameAs array covers every active, verified profile the owner has — the completeness pass that closes the entity loop for Google.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Check schema connects to all verified profiles

**Use this when** closing Layer 3 (Authority & Trust Checks) of the Website QA Audit — Layer 1 proved schema exists; this check proves it's complete.

## Inputs
- The verified-profile inventory built during this audit (social links check + GBP check)
- Google Rich Results Test and validator.schema.org
- WordPress admin access to RankMath (where sameAs URLs are managed on standard builds)
- The audit report/spreadsheet for logging results

## Steps
1. Assemble the master list of the owner's verified, active profiles confirmed earlier in this audit: LinkedIn, Facebook, Instagram, YouTube, Twitter/X, plus the Google Business Profile listing.
2. Run the homepage through the Rich Results Test and extract the current sameAs array from the Person/Organization markup.
3. Diff the two lists: every verified active profile must appear in sameAs — record each missing profile.
4. Check the reverse direction: flag sameAs entries pointing to dead, abandoned, or wrong-person profiles for removal.
5. Apply fixes in RankMath's schema/sameAs settings and re-run the Rich Results Test to confirm the updated array parses with zero errors.
6. Log the final sameAs list against the profile inventory in the audit report, then compile the full three-layer audit findings for delivery.

## Definition of done (QA checklist)
- [ ] sameAs array matches the verified-profile inventory one-to-one — no missing profiles, no dead or wrong entries
- [ ] Updated markup re-validates with zero errors in the Rich Results Test
- [ ] Final diff logged and the complete 36-check audit report delivered, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent Fable 5 agent (or comparable OpenAI/Google model) re-diffs the sameAs array against the full verified-profile inventory every run — every entry fetched live, every profile accounted for — and loops update-revalidate until the two lists match one-to-one with zero validator errors.
Memory carries the profile inventory forward from the sibling checks, so any profile added, renamed, or abandoned anywhere in the audit re-opens this completeness pass automatically.
Each run logs the final diff as a worked example in ## Example(s) so the audit library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /digital-plumbing (schema implementation) · Layer 1 sibling: verify-person-schema-with-sameas-links · siblings: check-social-profiles-linked-and-prominent, verify-google-business-profile-is-verified
