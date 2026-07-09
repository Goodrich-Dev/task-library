---
name: create-social-media-posts-per-platform
description: Write platform-native social posts (Facebook, LinkedIn, Instagram, Twitter/X) from one piece of processed content — reframed per platform, never copy-pasted across.
category: Content Factory — Process
stage: Process
definitive_article: GAP — to be written
status: needs-work
---

# Create social media posts per platform

**Use this when** an article, clip set, or quote card batch is ready and each platform needs its own native version of the content.

## Inputs
- The processed assets: article URL (or draft), clips from `extract-15-60-second-clips-from-long-form-video`, quote cards
- The GCT statement (Targeting tells you which platforms matter most)
- The brand's accounts: Facebook page, LinkedIn, Instagram, Twitter/X
- Names/handles of any people or companies mentioned (for tagging)

## Steps
1. Start from the GCT statement, not the article: each post re-delivers the one insight natively, it does not announce "new blog post."
2. Facebook: conversational, story-first, written like talking to the 44K-group audience; pair with the clip or a real photo; invite comment with a genuine question.
3. LinkedIn: professional framing of the same insight — the lesson, the numbers, what practitioners should do; first-person from the real person's profile voice; short paragraphs with white space.
4. Instagram: visual-first — the clip or quote card carries it; caption opens with the hook line; hashtags relevant and few, not a tag wall.
5. Twitter/X: the sharpest single line or a short thread walking the insight's logic; the quote-card line often is the tweet.
6. Tag every person and company mentioned (entity mentions build the graph — tag Zach Peyton and Superior Fence & Rail, not just "a client"). Link back to the article where the platform allows links to perform.
7. Proofread each post per Step 11 standards; verify names, handles, and the article URL.
8. Schedule or queue per platform, then log all posts in the Content Library tracker against the source — engagement on these posts is the signal Promote reads for boosting.

## Definition of done (QA checklist)
- [ ] One distinct, platform-native post per platform — no identical cross-posts
- [ ] Each post delivers the insight standalone and attaches a real visual (clip, card, or photo)
- [ ] All mentioned people/companies tagged with correct handles
- [ ] Article link present where appropriate, pointing to the brand's own site
- [ ] Posts logged in tracker so Promote can read engagement signals
- [ ] Linked back to the definitive article and relevant siblings

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. Candidate: the four-platform rollout of one processed one-minute video for a local service brand.

## Run on a persistent agent (Fable 5)

A persistent agent (Claude Fable 5, or comparable OpenAI/Google models that loop and hold memory) writes four genuinely native versions and loops the checklist until each post delivers the insight standalone with a real visual and correct tags — identical copy across platforms fails the run. Memory maintains the handle map for every person and company tagged before, so attribution is instant and never wrong. Document each rollout with a meta-article example.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — no definitive article yet; this skill flags the missing hub. Until written, ground runs in /social-amplification (what gets amplified) and /blog-posting-guidelines (voice/QA standards).
- Related: /social-amplification, /dad (winners become ads), /content-factory
- Sibling skills, in run order: `extract-15-60-second-clips-from-long-form-video` / `create-quote-cards-from-strongest-statements` → this → `create-dollar-a-day-ad-creatives`
