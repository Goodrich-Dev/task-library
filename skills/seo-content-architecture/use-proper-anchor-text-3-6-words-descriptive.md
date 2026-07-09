---
name: use-proper-anchor-text-3-6-words-descriptive
description: "Enforce the house anchor-text rule on every link — 3–6 descriptive words that predict the destination — and purge generic anchors like 'click here' from the entire site."
category: SEO & Content Architecture
stage: —
definitive_article: /internal-linking
status: complete
---

# Use proper anchor text (3–6 words, descriptive)

**Use this when** writing any link — internal or external — and when auditing the site for the generic anchors that always creep back in.

## Inputs
- The page(s) being written or audited
- Site-wide anchor report (crawl or LinkWhisper)
- Each destination page's GCT, so the anchor can promise what the page delivers

## Steps
1. Apply the rule to every link: the anchor is **3–6 words and describes the destination** — a reader should predict where the link goes before clicking.
2. Ban the generics outright: 'click here', 'read more', 'learn more', 'this article', and bare URLs.
3. Keep anchors keyword-relevant but natural — no exact-match stuffing; vary the phrasing across multiple links to the same target.
4. Match each anchor to the destination's GCT: the anchor's promise is the target page's content.
5. Audit site-wide: pull the anchor report and flag every violation, oldest content included.
6. Fix flagged anchors in body copy, then re-run the report to confirm zero generic anchors remain; archive the report for the MAA loop.

## Definition of done (QA checklist)
- [ ] Zero generic anchors site-wide on the re-run report
- [ ] All anchors 3–6 words and descriptive of their destinations
- [ ] No exact-match stuffing patterns across repeated links to one target
- [ ] Anchor report archived for trend tracking in MAA (/maa)
- [ ] Linked back to the definitive article (/internal-linking) and relevant siblings

## Example(s)
- The /internal-linking definitive article sets this anchor standard as part of its Step 4 (create links with proper anchor text and placement).
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first site-wide anchor cleanup.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) loops fix → re-run the anchor report until it reads zero generic anchors site-wide, oldest content included — "most of them fixed" fails the Definition of done.
Because generics always creep back, the agent re-runs on a schedule and diffs each archived report against memory, so regressions surface as a short list instead of a fresh audit.
Each cleanup logs a meta-article example via /meta-article-prompt-template.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /internal-linking
- Related: step-4-create-links-with-proper-anchor-text-and-placement · step-5-qa-links-against-google-guidelines · follow-entity-linking-decision-tree (/blog-posting-guidelines) · /entity-linking
