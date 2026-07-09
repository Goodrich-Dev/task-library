---
name: how-to-set-up-schema-markup-for-personal-brand-site
description: "Create the missing definitive article — a guide to implementing Person schema with sameAs links that bind a personal brand's site and social profiles into one entity Google can recognize (High-priority gap)."
category: Gaps & Tasks to Create
stage: —
definitive_article: "GAP — to be written"
status: gap
---

# How to Set Up Schema Markup for Personal Brand Site

**Use this when** Person schema keeps being implemented ad hoc because no hub documents it — this skill creates the definitive article that closes the gap. **Priority: High.**

## Inputs
- At least one real personal-brand schema implementation to document (a worked example with validation results)
- Every existing blitzmetrics.com article that mentions schema, sameAs, or entity markup
- The brand's verified profile list (the sameAs targets) and consistent NAP details
- WordPress access (Gutenberg), /blog-posting-guidelines, and the Nine Requirements checklist

## Steps
1. **Identify the concept** and gather every existing page touching schema markup — the hub organizes them, it does not replace them.
2. **Write the definition** (first two paragraphs): what Person schema with sameAs links is — structured data binding every verified profile into one entity — what it is not, and why personal brands need it.
3. **Document the complete process**: choose Person schema (LocalBusiness where the brand is also a local business, per /digital-plumbing); fill identity fields consistent with the site and NAP; add sameAs links to every verified social profile; place the markup site-wide; validate it; confirm it passes the /website-qa-audit checks ("Verify Person schema with sameAs links", "Check schema connects to all verified profiles"). Note where it sits in /personal-brand Phase 1 and how it feeds the later Knowledge Panel work.
4. **Link every real example** of an implemented schema, each with a 1–2 sentence relevance note.
5. **Cross-link related definitive articles**: /personal-brand, /digital-plumbing, /website-qa-audit.
6. **Add the course/service CTA** near the bottom.
7. **Set a short, memorable URL** redirecting to the hub — never to the homepage or a case study.
8. **Add an above-the-fold clickable diagram**: the entity graph — site at the center, sameAs spokes to each verified profile.
9. **Add E-E-A-T**: real validation screenshots and outcomes (entity recognition, panel progress), practitioner testimonials — highest authority first.
10. **Publish** as a Post in the Definitive Articles category (Gutenberg), then **run the Meta-Article Prompt** (/meta-article-prompt-template) for the companion meta-article.
11. Flip the dashboard status from Gap (Red), then update this skill's `definitive_article` field and the related Digital Plumbing and Personal Branding schema tasks to point at the new hub.

## Definition of done (QA checklist)
- [ ] Article meets all Nine Requirements, including the above-the-fold entity diagram and E-E-A-T section
- [ ] Published as a Post in the Definitive Articles category via the standard block editor
- [ ] Complies with Blog Posting Guidelines (title <60 chars, meta <160, keyword in first paragraph, no stock images, no AI-fluff)
- [ ] Companion meta-article published and linking up to the new hub
- [ ] This skill.md and the sibling schema tasks updated from GAP to the live short URL
- [ ] Linked back to related hubs: /personal-brand, /digital-plumbing, /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first publish; /meta-article-prompt-template (29 linked examples) sets the example-volume bar.
- /internal-linking is the model hub that ships with its own skill file for AI agents.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) runs the full 10-step creation process above to completion — publish, companion meta-article, and Gap→live status flip included — never stopping at a draft.
Self-verification is concrete here: validate the documented markup, re-run the /website-qa-audit schema checks against the worked example, and loop until validation and every Definition-of-done box pass.
The verified sameAs profile list persists in memory — the later Knowledge Panel work reuses it, so this run's accuracy compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written (this skill creates it)
- Related: /personal-brand (Phase 1) · /digital-plumbing · /website-qa-audit (Layer 1 + Layer 3 schema checks) · how-to-install-and-configure-gtm (the plumbing gap that runs alongside)
