---
name: verify-achievements-are-evidenced-not-just-claimed
description: Audits every expertise and results claim on the site for attached proof — links, photos, screenshots, named sources — converting assertions into E-E-A-T evidence.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Verify achievements are evidenced, not just claimed

**Use this when** running Layer 3 (Authority & Trust Checks) of the Website QA Audit — "award-winning" and "trusted by hundreds" mean nothing without something a visitor can check.

## Inputs
- Site URL (about page, homepage, and bio sections are the claim hotspots)
- The owner's actual proof inventory: press links, podcast/talk recordings, certifications, review platform profiles, real metrics
- The audit report/spreadsheet for logging results

## Steps
1. Sweep the site and list every achievement claim: years in business, jobs completed, awards, certifications, media features, "as seen on" logos, revenue/results numbers.
2. For each claim, check for attached evidence on the page: a link to the source, a photo of the award or jobsite, a screenshot of the metric or review, a named publication with a working link.
3. Fail unevidenced claims — especially logo walls that don't link to the actual feature, and round-number boasts with no source.
4. Verify the evidence itself: click press links (the article must actually mention the owner), and confirm certificates and review counts are current.
5. For every failed claim, pair it with the proof to add from the owner's inventory — or flag it for removal if no proof exists.
6. Log the claim-to-evidence table in the audit report.

## Definition of done (QA checklist)
- [ ] 100% of achievement claims on the site carry attached, working evidence — zero naked claims, zero logos without linked features
- [ ] Claims with no obtainable proof removed rather than left unsupported
- [ ] Claim-to-evidence table logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent Fable 5 agent (or comparable OpenAI/Google long-horizon model) sweeps every page for claims — not just the about page — pairs each with working evidence from the owner's proof inventory, and loops until 100% of claims carry checkable proof or are removed, re-clicking every evidence link each run because press links rot.
Memory holds the claim-to-evidence table, so re-runs only evaluate new claims and re-verify previously passing links.
Each run logs one worked example to ## Example(s) so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /seo-audit (E-E-A-T signals) · previous: check-social-profiles-linked-and-prominent · next check: verify-google-business-profile-is-verified
