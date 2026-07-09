---
name: link-all-content-back-to-personal-brand-site
description: Make sure every published piece — posts, articles, profiles, guest features — links back to yourname.com through proper entity linking.
category: Personal Branding
stage: Post
definitive_article: /personal-brand
status: needs-work
---

# Link all content back to personal brand site

**Use this when** content is flowing across platforms and authority needs to consolidate on the entity home — runs continuously through Phase 2 (Content Production).

## Inputs
- Inventory of every live asset: blog posts, social posts and clips, profiles, podcast and guest pages
- The entity-linking decision tree (/entity-linking)
- Edit access to the brand site and social properties

## Steps
1. Inventory everything published to date and where it lives — site articles, each platform's posts, profile pages, third-party features.
2. Apply the entity-linking decision tree to every link decision: mentions of the person link to yourname.com, mentions of the company link to the company site, concepts link to their definitive articles (/entity-linking).
3. Use descriptive 3–6 word anchor text — the person's name or what the target page is about — never "click here."
4. On the brand site, link every post up the SEO Tree (leaf → branch → trunk → homepage) so no article is orphaned (/seo-tree).
5. On social platforms, confirm each profile's website field carries yourname.com and post copy links to the relevant article wherever the platform allows.
6. For guest content and podcast features, ask the host to link the person's name to yourname.com in the show notes or byline.
7. Audit monthly: list any asset with no path back to the entity home and fix it.

## Definition of done (QA checklist)
- [ ] Zero orphan assets — every published piece has a working path back to yourname.com
- [ ] All internal links follow the decision tree with descriptive 3–6 word anchors
- [ ] Profiles carry the site link; guest features link the person's name
- [ ] Monthly link audit scheduled
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Cam Hazzard — camhazzard.com: the entity-home pattern this skill protects — one hub that every profile and piece of content points back to.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) is built for this standing audit: it walks the full asset inventory held in memory, applies the decision tree to every link, and loops until the Definition-of-done fully passes — zero orphan assets — not 90%.
It self-verifies by following each fixed path from asset to yourname.com and re-listing anything still orphaned until the list is empty.
Because it persists, the monthly audit actually recurs; each pass updates the inventory in memory that the Authority and Knowledge Panel phases extend, and a meta-article example is logged each run so the brand compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /personal-brand
- Related: /entity-linking · /seo-tree · previous: create-dollar-a-day-ad-creatives-from-best-content · next phase: get-featured-on-podcasts
