---
name: repurpose-videos-into-blog-posts-via-content-factory
description: Run the one-minute videos through the Content Factory pipeline to publish structured blog posts on the personal brand site.
category: Personal Branding
stage: Process
definitive_article: /personal-brand
status: needs-work
---

# Repurpose videos into blog posts via Content Factory

**Use this when** raw videos are in the content library and the personal brand site needs written content — Phase 2 (Content Production).

## Inputs
- Raw video files in the designated Google Drive / content library folder
- Access to the transcription tool and the WordPress site at yourname.com
- The Blog Posting Guidelines checklist (/blog-posting-guidelines)

## Steps
1. Feed the video into the Content Factory pipeline (/content-factory): upload to the processing folder and the transcription tool.
2. Transcribe and clean the transcript; correct names, jargon, and mis-heard terms.
3. Identify GCT — the Goals, Content, and Targeting of the piece — before writing a word.
4. Write the article from the transcript per /blog-posting-guidelines: SEO title under 60 characters, meta description under 160, focus keyword in the first paragraph, H2/H3 structure, short paragraphs, active voice, a hook that establishes context.
5. Add real photos (never stock) and a unique featured image; embed the source video in the article.
6. Add internal links using the entity-linking decision tree (/entity-linking) and place the post on the site's SEO Tree (/seo-tree) so it links upward instead of sitting orphaned.
7. Set the WordPress author to the person (never an admin or VA account), proofread, publish, and run final QA.

## Definition of done (QA checklist)
- [ ] Article live on yourname.com with the person as author and the source video embedded
- [ ] Title under 60 chars, meta under 160, focus keyword in first paragraph, H2/H3 structure, real images only
- [ ] Internal links follow the entity-linking decision tree; post placed on the SEO Tree
- [ ] First-person voice throughout
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Harry Gold — harryjgold.com: the site's content was produced from one Zoom recording run through this exact pipeline.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) runs the full pipeline per video — transcribe, clean, GCT, draft, internal-link, publish — and loops QA until the entire Definition-of-done passes: title and meta limits, keyword placement, SEO Tree position, correct author, not 90%.
Self-verification means loading the published URL and re-checking every checklist line against the live page, then fixing and re-checking.
It works the video inventory the recording skill left in memory and records each published URL there for the clip and linking skills downstream, logging a meta-article example each run so the brand compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /personal-brand
- Related: /content-factory · /blog-posting-guidelines · /entity-linking · /seo-tree · previous: record-one-minute-videos-answering-customer-questions · next: create-social-content-from-video-clips
