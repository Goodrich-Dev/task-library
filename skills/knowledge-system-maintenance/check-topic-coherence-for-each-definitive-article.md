---
name: check-topic-coherence-for-each-definitive-article
description: Run the SEO Tree test on a definitive article so every element provably supports its declared topic — the first check of the quarterly audit.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: complete
---

# Check topic coherence for each definitive article

**Use this when** a quarterly audit cycle opens and you are the assigned auditor for a definitive article — run this check first, before structure, currency, or cross-references.

## Inputs
- The definitive article's URL, short URL, and declared topic (the one concept it owns)
- The Definitive Article Guide status table (to record findings)
- The article's position in the SEO Tree (/seo-tree) — root, trunk, branch, or leaf
- Audit notes doc or row for this article and quarter

## Steps
1. Write the article's declared topic as one sentence at the top of your audit notes, taken from its title, first-two-paragraph definition, and short URL. If you cannot state it in one sentence, that is itself a Red finding.
2. Apply the SEO Tree test to every element: for each H2/H3 section, paragraph block, image, embedded video, example, and link, ask "does this directly support the declared topic?" Every element either supports the topic or does not belong on this page.
3. Walk the heading outline specifically. Flag any H2/H3 that actually serves a *different* concept — it likely belongs in that concept's own definitive article. Moving it prevents two pages competing for one topic (content vandalism).
4. Check every linked example: each must demonstrate *this* topic, and its 1–2 sentence relevance note must say why in terms of this topic, not a neighboring one.
5. Check outbound links: cross-links to related definitive articles are correct; links that drag the reader into an unrelated topic mid-article are coherence failures. Confirm the article links upward/across consistent with its SEO Tree position.
6. Record every failing element in the audit notes as: element → why it fails the test → recommended fix (cut, rewrite to serve the topic, or relocate to the correct hub).
7. Fix trivial failures in place. For structural moves (relocating a section to another hub), ticket the article owner or file an SOP Amendment Proposal if the creation process itself allowed the drift.
8. Pass the findings to the status-table update step (Green/Yellow/Red plus audit date) — see `update-status-table-in-definitive-article-guide`.

## Definition of done (QA checklist)
- [ ] Declared topic stated in one sentence in the audit notes
- [ ] Every heading, image, example, and link checked; pass/fail recorded — no element skipped
- [ ] Zero unresolved off-topic elements: each is fixed, relocated, or ticketed with owner and recommended fix
- [ ] Findings recorded for the status table with this quarter's audit date
- [ ] Any reusable insight from the audit captured as a Knowledge Capture Note within 24 hours
- [ ] If this skill's steps no longer match how audits actually run, an SOP Amendment Proposal is filed
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — Process 1 defines this check and applies it to Local Service Spotlight' own article library; use its audit criteria verbatim.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first real quarterly run and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) walks every heading, paragraph, image, example, and link of the assigned article against its declared topic and loops until the Definition of done fully passes — no element skipped, zero unresolved off-topic elements, findings stamped for the status table.
It self-verifies by re-running the SEO Tree test on every element it fixed or relocated, confirming the repaired page now reads as one topic end to end.
Because this is the recursive maintenance layer, memory across audit cycles is the mechanism, not a convenience: the agent retains each article's declared-topic sentence and every prior quarter's findings, so this quarter's audit is a diff against remembered state — drift in the same section two cycles running becomes an SOP Amendment Proposal, not another patch.
Each run it logs a meta-article example via the Meta-Article Prompt, filling this skill's "Example needed" slot so the knowledge base compounds with every cycle.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related (Process 1 run order): check-topic-coherence-for-each-definitive-article → verify-structural-completeness-against-8-step-framework → check-information-currency-with-latest-data → validate-cross-reference-integrity-across-articles → update-status-table-in-definitive-article-guide; scheduling: schedule-and-assign-quarterly-auditors. Concept: /seo-tree.
