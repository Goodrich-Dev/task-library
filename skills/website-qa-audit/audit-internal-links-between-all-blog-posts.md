---
name: audit-internal-links-between-all-blog-posts
description: Checks that every blog post links to at least one other post and a service page, so no content is orphaned and link equity flows toward money pages.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Audit internal links between all blog posts

**Use this when** running Layer 2 (Content Architecture Checks) of the Website QA Audit — orphaned posts earn no rankings and pass no authority.

## Inputs
- WordPress admin access, ideally with LinkWhisper installed (its internal links report does the counting)
- Alternatively a Screaming Frog crawl with inlink/outlink counts per URL
- The site's list of money/service pages
- The audit report/spreadsheet for logging results

## Steps
1. Pull the internal links report from LinkWhisper (or Screaming Frog's inlinks/outlinks columns) covering every published post.
2. Flag every post with zero outbound internal links to other posts — each post must link to at least one related post.
3. Flag every post that links to no service/money page — content exists to route readers toward the offer.
4. Flag orphans from the other direction: posts that no other page links TO (zero internal inlinks).
5. Check link placement: links belong in body copy with descriptive 3–6 word anchors, not dumped in a "related posts" widget alone.
6. Log the per-post link counts and the orphan/fix list in the audit report.

## Definition of done (QA checklist)
- [ ] Every published post links to at least one other post AND at least one service page in body content
- [ ] Zero orphan posts — every post has at least one internal inlink
- [ ] Per-post link table logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent Fable 5 agent (or comparable OpenAI/Google long-horizon model) computes inlink/outlink counts for every published post each run, inserts the missing post-to-post and post-to-service links in body copy with descriptive anchors, and re-crawls until zero orphans remain and every post meets both link minimums.
Memory keeps the per-post link graph, so re-runs only rework new posts and posts whose links changed — and every newly published post automatically re-opens the orphan check.
Each run logs one worked example to ## Example(s), compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /seo-tree (leaves → branches → trunk structure) · /blog-posting-guidelines · previous: verify-email-opt-in-form-exists-and-works · next check: verify-entity-linking-follows-decision-tree
