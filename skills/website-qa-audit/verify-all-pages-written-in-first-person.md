---
name: verify-all-pages-written-in-first-person
description: Confirms every page of a personal-brand site speaks as the owner ("I" and "my"), not about them in third person, so the site reads as the person and not a brochure.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Verify all pages written in first person

**Use this when** starting Layer 2 (Content Architecture Checks) of the Website QA Audit on a personal-brand site.

## Inputs
- Site URL plus a full page list (XML sitemap or crawl export)
- The owner's name (to search for third-person constructions)
- The audit report/spreadsheet for logging results

## Steps
1. Read the homepage hero and first section aloud — it must say "I help…" / "my clients…", not "[Name] helps…" or agency-style "we" on a solo personal brand.
2. Use the browser find function (Ctrl/Cmd+F) on every page to search for the owner's name followed by "is", "has", or "helps" — the telltale third-person patterns.
3. Run a `site:domain.com "Name is"` Google search to surface third-person copy on pages you might have skipped.
4. Check the about page especially — it is the most common third-person offender (bio copy pasted from a speaker kit).
5. List every page and the specific sentences that break first-person voice, so the rewrite is a punch list rather than a vague note.
6. Log pass/fail per page in the audit report.

## Definition of done (QA checklist)
- [ ] 100% of audited pages use first-person voice — zero third-person references to the owner outside testimonials and press quotes
- [ ] Every violation documented with page URL and exact sentence
- [ ] Results logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 / comparable OpenAI or Google models) reads every page's full copy — not just hero sections — pattern-matching third-person constructions around the owner's name, and loops rewrite-recheck until 100% of pages pass with zero violations outside testimonials and press quotes.
Memory holds the per-page verdict and the exact sentences flagged, so re-runs only re-read changed or new pages instead of the whole site.
Each run logs a real before/after example to ## Example(s), compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /blog-posting-guidelines (voice and style rules) · next check: verify-wordpress-author-set-to-site-owner-name
