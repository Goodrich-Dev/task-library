---
name: step-5-qa-links-against-google-guidelines
description: "Audit every link created in Step 4 against Google's quality guidelines — anchors, placement, relevance, volume, and breakage — so nothing manipulative or broken ships to measurement."
category: SEO & Content Architecture
stage: —
definitive_article: /internal-linking
status: complete
---

# Step 5: QA links against Google guidelines

**Use this when** Step 4's links are placed and logged, before any results get measured — QA is the gate between building and trusting.

## Inputs
- The Step 4 link log (source, target, anchor, date)
- A broken-link scanner or full-site crawl
- Google's link quality guidelines as the reference standard

## Steps
1. Pull the Step 4 link log and audit every new link in place on the live page.
2. **Anchor check**: descriptive, 3–6 words, naturally varied — no keyword-stuffed or repeated exact-match anchors across the site.
3. **Placement check**: links live in body content with supporting context — no hidden links, no footer/sidebar link dumps, no link exchanges or schemes.
4. **Relevance check**: source and target GCT actually match — remove any link a reader would not thank you for.
5. **Volume check**: link counts per page stay reasonable; every link must earn its place.
6. Run a broken-link scan across all touched pages; fix anything that 404s or chains through bad redirects.
7. Record every violation found and fixed; pass the clean log to Step 6 for measurement.

## Definition of done (QA checklist)
- [ ] 100% of new links audited against all five checks (anchor, placement, relevance, volume, breakage)
- [ ] Zero open guideline violations; fixes documented
- [ ] Zero broken links on touched pages
- [ ] Clean link log handed to Step 6
- [ ] Linked back to the definitive article (/internal-linking) and relevant siblings

## Example(s)
- The /internal-linking definitive article documents this QA pass as its Step 5; /website-qa-audit Layer 2 carries the matching site-wide checks ("Audit internal links", "Check for broken links", "Verify entity linking follows decision tree").
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the next QA round.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) audits 100% of the Step 4 log against all five checks — sampling is exactly the 90% shortcut this gate exists to block — and loops fix → re-scan until zero violations and zero broken links remain.
Violation patterns persist in memory, so repeat offenders (an anchor habit, a template that link-dumps) get flagged upstream into Step 4 instead of re-caught every round.
Each QA round logs a meta-article example via /meta-article-prompt-template before handing the clean log to Step 6.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /internal-linking
- Related (run order): step-4-create-links-with-proper-anchor-text-and-placement (before) → step-6-measure-and-iterate-with-maa (after) · /website-qa-audit · /blog-posting-guidelines
