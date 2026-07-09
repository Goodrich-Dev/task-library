---
name: set-correct-business-categories
description: Select the most accurate primary and secondary Google Business Profile categories so the listing ranks for the searches that actually drive revenue.
category: Digital Plumbing
stage: —
definitive_article: /digital-plumbing
status: needs-work
---

# Set Correct Business Categories

**Use this when** a GBP's primary category is generic ("Contractor" instead of "Fence contractor"), missing, or stuffed with aspirational categories the business doesn't serve.

## Inputs
- Verified GBP with edit access
- The business's money service — the one offering that drives most revenue (from GCT: Goals first)
- List of real secondary services the business actually delivers

## Steps
1. Name the money service with the owner. The primary category must match it, not the broadest label — primary category is the strongest ranking lever on the profile.
2. In GBP, search the category picker for the most specific category that matches the money service. Pick specific over general every time (e.g., "Fence contractor," not "Contractor").
3. Add secondary categories only for services the business genuinely sells today. No aspirational categories, no stuffing — irrelevant categories dilute relevance and invite suspensions.
4. Sanity-check against winners: search the money keyword in Google Maps for the service area and note the primary categories the top 3 listings use.
5. Save and re-check after a few days — category edits go through Google review and can be rejected or reverted.
6. Record primary + secondary categories in the client record so future audits can detect drift.

## Definition of done (QA checklist)
- [ ] Primary category is the most specific available match to the money service
- [ ] Every secondary category maps to a service the business actually delivers
- [ ] No generic, aspirational, or unrelated categories remain
- [ ] Edits survived Google's review (re-checked after a few days) and are documented
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
Category edits sit in Google review for days and can be silently rejected — a persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) submits, waits, re-checks, and resubmits until every Definition-of-done item passes, not 90%.
It self-verifies against that checklist, keeps the chosen primary/secondary categories and the top-3 competitor categories in memory so later runs detect drift instantly, and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /digital-plumbing
- Related (run order): verify-google-business-profile → ensure-nap-consistency-across-platforms → upload-real-photos-and-set-business-hours → this
- Cross-links: /nine-triangles (GCT: Goals decide the money service) · /website-qa-audit
