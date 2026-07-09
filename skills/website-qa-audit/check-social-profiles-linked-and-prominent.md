---
name: check-social-profiles-linked-and-prominent
description: Verifies the owner's social profiles are linked from the site, working, and prominently placed, so visitors and Google can follow the entity off-site.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Check social profiles linked and prominent

**Use this when** running Layer 3 (Authority & Trust Checks) of the Website QA Audit — hidden or broken profile links sever the site from the rest of the entity.

## Inputs
- The owner's canonical list of active social profiles (LinkedIn, Facebook, Instagram, YouTube, Twitter/X)
- Site URL on desktop and mobile
- The audit report/spreadsheet for logging results

## Steps
1. Build the reference list of the owner's verified, active profile URLs with the owner.
2. Locate social links on the site and judge prominence: they must appear in the footer at minimum, and ideally also the header, about page, or hero area — a buried single mention fails prominence.
3. Click every social link and confirm it opens the correct live profile from the reference list — not a platform homepage, a defunct account, or a wrong-person profile.
4. Check for gaps: every active profile on the reference list should be linked somewhere visible on the site.
5. Confirm icons render and are tappable on mobile (not crushed or overlapped).
6. Cross-check the linked set against the schema sameAs list — site links and schema should name the same profiles — and log results in the audit report.

## Definition of done (QA checklist)
- [ ] Every active profile on the reference list is linked from the site, and every social link resolves to the correct live profile
- [ ] Social links visible without hunting — footer at minimum — and functional on mobile
- [ ] Link map (including schema cross-check) logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Fable 5 / comparable OpenAI or Google models) resolves every social link on every template each run — not once at audit time — confirming each lands on the correct live profile, prominence holds on mobile, and the linked set still matches the schema sameAs list exactly.
Memory keeps the canonical profile list and per-template verdicts, so a re-run instantly flags a renamed handle, a dead account, or a new profile missing from the site.
Each run logs the link map as a worked example in ## Example(s), compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /digital-plumbing (profile setup) · siblings: verify-footer-includes-social-links-and-secondary-nav, check-schema-connects-to-all-verified-profiles · next check: verify-achievements-are-evidenced-not-just-claimed
