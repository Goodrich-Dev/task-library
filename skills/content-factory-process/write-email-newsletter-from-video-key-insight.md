---
name: write-email-newsletter-from-video-key-insight
description: Draft an email newsletter built on the video's single key insight, driving the list back to the full article on the brand's site.
category: Content Factory — Process
stage: Process
definitive_article: GAP — to be written
status: needs-work
---

# Write email newsletter from video key insight

**Use this when** a video has been processed into an article (or is about to publish) and the email list should hear the insight and visit the post.

## Inputs
- The GCT statement from Step 3 — the Content line IS the key insight
- The article draft or published URL, and the source video
- The brand's email platform and list
- The sender identity (the real person, not a noreply)

## Steps
1. Take the single key insight from the GCT Content line. One email = one insight; if you are tempted to include three, that is three newsletters.
2. Write the subject line: short, specific, curiosity with substance — the insight's tension, not clickbait ("Why the cheapest HVAC quote cost Sarah $3,000"). Draft 3, pick 1.
3. Open with the hook in the sender's first-person voice — same voice as the video, often the same opening moment the article's Step 7 hook uses.
4. Deliver the insight in scannable form: 3–6 short paragraphs or a tight list, concrete numbers and the story beat included. The email must be valuable even if nobody clicks.
5. Add ONE call to action: read the full article (the canonical post on the brand's site — traffic flows to the SEO Tree, not to a social platform). Link with descriptive anchor text.
6. Close as the real person (name, role) — no corporate sign-offs, no noreply sender.
7. Proofread per Step 11 standards (names, numbers, no AI-fluff), send a test to yourself, check rendering on mobile.
8. Schedule/send, then log in the Content Library tracker against the source video; record opens/clicks for the weekly MAA review.

## Definition of done (QA checklist)
- [ ] Exactly one insight, traceable to the video's GCT Content line
- [ ] Subject line specific and honest; no clickbait
- [ ] Email valuable standalone, in the sender's first-person voice
- [ ] Single CTA linking to the article on the brand's own site
- [ ] Test send reviewed on mobile; logged in tracker with metrics slot for MAA
- [ ] Linked back to the definitive article and relevant siblings

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. Candidate: a newsletter from a Marko Sipila (HVAC Quote) video insight driving readers to the published article.

## Run on a persistent agent (Fable 5)

A persistent agent (Claude Fable 5, or a comparable OpenAI/Google model that loops and holds memory) builds the email from the GCT Content line, drafts three subject lines and picks one, proofs to Step 11 standards, and loops the checklist — one insight, one CTA, mobile render verified — until every box passes. Memory holds what the list has already received, so insights never repeat and each send builds on past open and click data. Log a meta-article example per send.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — no definitive article yet; this skill flags the missing hub. Until written, ground runs in /blog-posting-guidelines (voice, hook, and proofing standards).
- Related: /content-factory, /maa (measuring the send), /seo-tree (where the click lands)
- Sibling skills, in run order: `step-11-proofread-with-grammarly-or-chatgpt` → this (parallel with `create-social-media-posts-per-platform`)
