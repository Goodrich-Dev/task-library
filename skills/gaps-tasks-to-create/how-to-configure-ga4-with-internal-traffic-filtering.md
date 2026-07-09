---
name: how-to-configure-ga4-with-internal-traffic-filtering
description: "Create the missing definitive article — the complete GA4 setup guide covering property creation and internal traffic filtering, so analytics reflect customers instead of the team (High-priority gap)."
category: Gaps & Tasks to Create
stage: —
definitive_article: "GAP — to be written"
status: gap
---

# How to Configure GA4 with Internal Traffic Filtering

**Use this when** GA4 setup keeps being done from memory because no hub documents it — this skill creates the definitive article that closes the gap. **Priority: High.**

## Inputs
- At least one real GA4 configuration to document end to end, including the internal-traffic filter
- Every existing blitzmetrics.com article that mentions GA4 or analytics setup
- WordPress access (Gutenberg) and /blog-posting-guidelines open
- The Nine Requirements checklist from the Task Library Standard

## Steps
1. **Identify the concept** and gather every existing page touching GA4 setup — the hub organizes them, it does not replace them.
2. **Write the definition** (first two paragraphs): what a correctly configured GA4 property is, what it is not (a default install polluted by your own visits), and who needs it.
3. **Document the complete process**: create the GA4 property; install it on the site — via the GTM container, which is why the GTM article runs first; define internal traffic (team, office, home IPs) and activate the internal-traffic filter; verify clean data is flowing; connect Google Search Console to GA4 so search performance data lands in one place (mirroring the Digital Plumbing task and the /website-qa-audit Layer 1 check "GA4 configured with internal traffic filtered").
4. **Link every real example** of a configured property, each with a 1–2 sentence relevance note.
5. **Cross-link related definitive articles**: /digital-plumbing and /website-qa-audit; reference the GTM hub once it exists.
6. **Add the course/service CTA** near the bottom.
7. **Set a short, memorable URL** redirecting to the hub — never to the homepage or a case study.
8. **Add an above-the-fold clickable diagram** of the setup flow (property → install → filter → verify → connect GSC).
9. **Add E-E-A-T**: real before/after data showing internal traffic removed, practitioner testimonials — highest authority first.
10. **Publish** as a Post in the Definitive Articles category (Gutenberg), then **run the Meta-Article Prompt** (/meta-article-prompt-template) for the companion meta-article.
11. Flip the dashboard status from Gap (Red), then update this skill's `definitive_article` field and the Digital Plumbing task "Set up GA4 with internal traffic filtering" to point at the new hub.

## Definition of done (QA checklist)
- [ ] Article meets all Nine Requirements, including the above-the-fold diagram and E-E-A-T section
- [ ] Published as a Post in the Definitive Articles category via the standard block editor
- [ ] Complies with Blog Posting Guidelines (title <60 chars, meta <160, keyword in first paragraph, no stock images, no AI-fluff)
- [ ] Companion meta-article published and linking up to the new hub
- [ ] This skill.md and the related Digital Plumbing gap task updated from GAP to the live short URL
- [ ] Linked back to related hubs: /digital-plumbing, /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first publish; /meta-article-prompt-template (29 linked examples) is the model for example volume.
- /internal-linking shows the finished pattern: a hub plus a downloadable skill file for AI agents.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) runs the full 10-step creation process above to completion — through publish, the companion meta-article, and the Gap→live status flip — sequencing itself after the GTM hub exists, since GA4 installs through the container.
It loops QA against the Definition of done until all Nine Requirements pass, and self-verifies the proof: before/after data showing internal traffic actually filtered is in the article, not just claimed.
Memory carries the GTM run's container details into this build, and the published configuration becomes the worked example the next run extends.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written (this skill creates it)
- Related: how-to-install-and-configure-gtm (run first — GA4 installs through GTM) · /digital-plumbing · /website-qa-audit · /maa (clean data feeds the measurement loop)
