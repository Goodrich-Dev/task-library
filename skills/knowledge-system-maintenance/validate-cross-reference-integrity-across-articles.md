---
name: validate-cross-reference-integrity-across-articles
description: Verify that every other article linking to the audited definitive article still describes it accurately — and that its own outbound cross-links do the same.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: needs-work
---

# Validate cross-reference integrity across articles

**Use this when** running the quarterly audit's fourth check — the article itself is sound, and now the entity graph around it must be verified so no link promises content that is not there.

## Inputs
- The definitive article under audit (its short URL and full URL)
- Site search or an export of internal links (to find every page referencing this article)
- The entity-linking decision tree from /blog-posting-guidelines
- Audit notes for this article and quarter

## Steps
1. Find every other article that links to the audited article: search the site for its short URL, full URL, and title mentions. List each inbound cross-reference with its source page.
2. For each inbound reference, read the anchor text and the surrounding sentence: does it accurately describe what the audited article *currently* contains? An accurate link last quarter can be a lie this quarter.
3. Flag stale references: links pointing at sections that were renamed or removed, descriptions claiming the article covers something it no longer does, or anchors framing it as a different concept than it now owns.
4. Check each anchor against the entity-linking decision tree and anchor standards (descriptive 3–6 word anchors, no "click here"), since you are already touching every link.
5. Fix inaccurate references in the source articles directly where you have access; otherwise ticket the owning article's auditor/owner with the exact sentence and the corrected language. Never leave a cross-reference promising content that is not there.
6. Reverse the check: audit the article's own outbound cross-links to sibling definitive articles and confirm each still describes its target accurately.
7. Record all fixes and tickets in the audit notes. If the same drift pattern keeps appearing (e.g., renames never propagate), file an SOP Amendment Proposal against the renaming/update SOP.

## Definition of done (QA checklist)
- [ ] Complete inbound-reference list built; every reference read in context and marked accurate or stale
- [ ] Every stale reference fixed in the source article or ticketed with exact corrected language
- [ ] Outbound cross-links reverse-checked against their targets
- [ ] Anchors comply with the entity-linking decision tree and 3–6 word descriptive standard
- [ ] Recurring drift patterns escalated as an SOP Amendment Proposal, not just patched
- [ ] Results recorded for the status-table update with audit date
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — Process 1 defines this integrity check: other articles' links must describe this one accurately for the entity graph to hold.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first real quarterly run and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) builds the complete inbound-reference list, reads every anchor in context against what the audited article contains today, reverse-checks the outbound links, and loops until the Definition of done fully passes — every reference marked accurate or stale, every stale one fixed or ticketed with exact corrected language.
It self-verifies by re-crawling the fixed references to confirm no link still promises content that is not there.
Memory across audit cycles is the entity graph remembering itself: the agent retains which references it verified last quarter and which articles renamed or removed sections since, so each audit checks the delta plus a sample — and when rename-propagation failures recur, it files one SOP Amendment Proposal against the update SOP instead of patching the same drift quarterly.
Each run it logs a meta-article example via the Meta-Article Prompt, so the cross-reference audit itself becomes documented, reusable knowledge.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related (Process 1 run order): check-information-currency-with-latest-data → validate-cross-reference-integrity-across-articles → update-status-table-in-definitive-article-guide. Concepts: /blog-posting-guidelines (entity-linking decision tree), /seo-tree.
