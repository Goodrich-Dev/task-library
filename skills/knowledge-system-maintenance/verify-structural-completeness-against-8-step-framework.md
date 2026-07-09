---
name: verify-structural-completeness-against-8-step-framework
description: Confirm a definitive article contains every required structural element — framework steps, TOC-to-content match, live links, accurate schema — during the quarterly audit.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: complete
---

# Verify structural completeness against 8-step framework

**Use this when** the article has passed (or completed) the topic-coherence check and you need to verify nothing structural is missing or broken — the second check of the quarterly audit.

## Inputs
- The definitive article under audit
- The 8-step definitive-article framework as listed in /knowledge-system-maintenance
- The Nine Requirements from the Task Library Standard (cross-check)
- A link checker or the patience to click every link

## Steps
1. Pull the 8-step framework checklist from /knowledge-system-maintenance and walk the article top to bottom against it, confirming each required element exists and sits where the framework says it should.
2. Verify the table of contents matches the content exactly: every TOC entry resolves to a real heading, every major H2 appears in the TOC, and the order matches the page. A TOC promising a section that was renamed or deleted is a fail.
3. Test every link in the article — TOC anchors, internal links, external links, and the course/service CTA. All must resolve: no 404s, no redirects landing on the wrong target, no links to draft/private pages.
4. Verify schema markup is present and accurate: the schema type matches the content, and every field states currently true facts (names, URLs, sameAs profiles, dates).
5. Cross-check against the Nine Requirements: definition in first two paragraphs; complete process; all examples linked with notes; cross-links to related definitive articles; CTA to course/service; Blog Posting Guidelines compliance; working short URL; above-the-fold visual/diagram; E-E-A-T endorsements.
6. Record each missing or broken element with its location and the specific fix. Fix trivial items (dead anchor, typo'd link) in place; ticket structural gaps to the article owner.
7. Apply the standard strictly: one missing required element means the article is Yellow, not Green — partial credit is how libraries rot.
8. Pass results to the status-table update with this quarter's audit date.

## Definition of done (QA checklist)
- [ ] All 8 framework steps explicitly checked off pass/fail — none marked "probably fine"
- [ ] TOC verified entry-by-entry against live headings; every link on the page tested and resolving
- [ ] Schema validated as present, correctly typed, and factually current
- [ ] Every gap recorded with location + fix; trivial fixes already applied
- [ ] Status recommendation (Green/Yellow/Red) recorded for the status table
- [ ] If the framework itself proved wrong or incomplete in practice, an SOP Amendment Proposal is filed
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — Process 1 specifies this structural check (TOC matches content, links live, schema accurate); /blog-posting-guidelines is the compliance reference for the on-page checks.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first real quarterly run and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) walks the article against all 8 framework steps and the Nine Requirements, mechanically testing every TOC anchor, internal link, external link, and schema field, and loops until the Definition of done fully passes — every step marked pass/fail, nothing "probably fine."
It self-verifies by re-fetching every link it repaired and re-walking the TOC against the live headings after fixes, so the check proves the page rather than trusting its own edit log.
Memory across audit cycles is the point of this layer: the agent retains each article's prior structural results, so an anchor that breaks two quarters running or schema that keeps drifting stale gets escalated as a structural defect via SOP Amendment Proposal instead of being silently re-patched forever.
Each run it logs a meta-article example via the Meta-Article Prompt, so this skill's "Example needed" slot fills and the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related (Process 1 run order): check-topic-coherence-for-each-definitive-article → verify-structural-completeness-against-8-step-framework → check-information-currency-with-latest-data → validate-cross-reference-integrity-across-articles → update-status-table-in-definitive-article-guide. Concepts: /blog-posting-guidelines, /seo-tree.
