---
name: replace-ai-looking-content-with-real-eeat
description: "Rewrite generic AI-generated pages with real experience, named examples, and third-party proof so every page demonstrates E-E-A-T instead of merely claiming expertise."
category: SEO & Content Architecture
stage: —
definitive_article: /seo-tree
status: needs-work
---

# Replace AI-looking content with real EEAT

**Use this when** pages read like they could be about anyone — generic claims, no named people or results, stock imagery, no first-person experience.

## Inputs
- List of suspect pages (from a content audit or the /website-qa-audit Layer 2–3 checks)
- The proof file: real client results, screenshots of actual work, named testimonials with headshots, podcast/conference/media appearances
- Edit access and /blog-posting-guidelines open

## Steps
1. Audit page by page for AI tells: generic claims with no named people or numbers, AI-fluff phrases, stock images, third-person corporate voice on a personal brand site, full-viewport walls of text.
2. Build the proof file for each flagged page: actual results with numbers, real screenshots, testimonials with full attribution, talks, podcasts, and press.
3. Rewrite in first person with specific experience — what you did, for whom, what happened — in plain language and active voice.
4. Replace every stock image with a real photo or real screenshot, each with descriptive alt text.
5. Add third-party endorsements, highest authority first — this is Requirement 9, the E-E-A-T layer of a definitive article.
6. Re-run the page against /blog-posting-guidelines (no AI-fluff phrases, no stock images) and the /website-qa-audit Layer 2–3 checks (first-person voice, evidenced achievements, attributed testimonials).
7. Log before/after in the MAA loop (/maa) so the rewrite's ranking and traffic impact is measurable.

## Definition of done (QA checklist)
- [ ] Zero stock images and zero AI-fluff phrasing on the rewritten pages
- [ ] Every claim of expertise or results is evidenced, not just asserted
- [ ] First-person voice throughout (personal brand sites)
- [ ] Endorsements present, ordered highest-authority first
- [ ] Complies with Blog Posting Guidelines; linked back to /seo-tree and relevant siblings

## Example(s)
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first before/after rewrite.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) works the flagged list page by page, looping audit → proof file → rewrite → re-check against /blog-posting-guidelines and the /website-qa-audit Layer 2–3 checks until zero stock images, zero AI-fluff, and zero unevidenced claims remain on every page — not most pages.
The proof file lives in memory and compounds: every testimonial, screenshot, and result gathered for one page is already on hand for the next run.
Each rewrite logs its before/after as a meta-article example (/meta-article-prompt-template) and feeds the /maa loop.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /seo-tree
- Related: enhance-existing-articles-before-creating-new-ones (run first) · /website-qa-audit (Layers 2–3 are the test) · /blog-posting-guidelines · /personal-brand
