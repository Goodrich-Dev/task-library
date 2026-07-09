---
name: post-to-linkedin
description: Publish the new piece to LinkedIn with professional first-person framing from the owner's profile, turning the article into a lesson the owner's network will share.
category: Content Factory — Post
stage: Post
definitive_article: GAP — to be written
status: needs-work
---

# Post to LinkedIn

**Use this when** the article is live and needs professional distribution to the owner's LinkedIn network and company page.

## Inputs
- Published article URL and/or the processed video file
- Access to the owner's LinkedIn profile (and the company page matching the business entity, per /digital-plumbing)
- The article's key insight and the people/companies featured

## Steps
1. Post from the **owner's personal profile** — people follow people; the company page reshare is secondary.
2. Reframe the hook professionally: open with the problem or lesson, not "New blog post!" Write in first person, 1–3 short paragraphs with line breaks, the way the owner actually talks.
3. State one concrete insight from the article so the post stands alone, then point to the article for the full process.
4. Use native media: upload the video directly or attach a real photo. Put the article link in the post or first comment.
5. Tag featured people and companies; add at most 3 relevant hashtags (topic-level, not spam).
6. Reshare from the company page with a one-line frame.
7. Reply to every comment in the owner's voice within 24 hours, and log the post URL in the content tracker for the Promote stage.

## Definition of done (QA checklist)
- [ ] Live on the owner's personal profile, first-person professional framing, standalone insight included
- [ ] Native media attached (no stock); article link present; ≤3 hashtags
- [ ] Featured people/companies tagged; company page reshare done
- [ ] Post URL logged for Promote; comments answered within 24 hours
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. Candidate: a Harry Gold insight post pointing to its definitive article.

## Run on a persistent agent (Fable 5)
A persistent agent (Fable 5, or a comparable OpenAI/Google model) writes the post in the owner's stored voice profile, publishes from the personal profile, reshares from the company page, then audits itself against every Definition-of-done box — a missing tag, a fourth hashtag, or an unlogged URL each trigger another pass.
Because it is long-horizon, it returns within 24 hours to answer comments and record what resonated, feeding that back into memory for the next post.
Each run logs a meta-article example so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written (interim grounding: /personal-brand Phase 2 distribution and /blog-posting-guidelines)
- Related: /content-factory · /thank-you-machine
- Run order (Post stage): post-to-facebook-page → **post-to-linkedin** → email-and-dm-client-about-published-article
