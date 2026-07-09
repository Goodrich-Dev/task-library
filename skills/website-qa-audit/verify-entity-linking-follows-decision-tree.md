---
name: verify-entity-linking-follows-decision-tree
description: Audits all internal and outbound links against the entity linking decision tree — people to personal sites, companies to company sites, concepts to definitive articles.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Verify entity linking follows decision tree

**Use this when** running Layer 2 (Content Architecture Checks) of the Website QA Audit — links that point entities to the wrong destinations scramble the site's entity graph.

## Inputs
- A crawl export of all links with anchor text (Screaming Frog) or post-by-post review access
- The entity linking decision tree (see /entity-linking)
- The site's map of concept hubs/definitive articles
- The audit report/spreadsheet for logging results

## Steps
1. Export every in-content link with its anchor text and destination from a Screaming Frog crawl (or review post by post on smaller sites).
2. For each anchor naming a PERSON, confirm it links to that person's own site or primary profile — not to a generic page.
3. For each anchor naming a COMPANY, confirm it links to the company's website.
4. For each anchor naming a CONCEPT, confirm it links to the one definitive article/hub that owns the concept — never to a competing duplicate page (content vandalism).
5. Check anchor quality alongside destination: descriptive 3–6 word anchors, no "click here."
6. Log every violation with page, anchor, current destination, and correct destination per the tree in the audit report.

## Definition of done (QA checklist)
- [ ] 100% of entity-naming anchors route per the decision tree — people → personal sites, companies → company sites, concepts → definitive articles
- [ ] Zero generic anchors ("click here") and zero concept links pointing at duplicate/competing pages
- [ ] Violation list with corrections logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Fable 5 / comparable OpenAI or Google models) classifies every in-content anchor on the site as person, company, or concept, checks each against the decision tree, and loops correct-recrawl until 100% of entity anchors route to the right destination with zero "click here" anchors left.
Memory stores each anchor's classification and verdict, so re-runs only evaluate links added or edited since the last pass instead of reclassifying the whole site.
Each run logs one worked example to ## Example(s) so the audit library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /entity-linking (the decision tree itself) · /blog-posting-guidelines · /seo-tree · previous: audit-internal-links-between-all-blog-posts · next check: check-for-broken-links
