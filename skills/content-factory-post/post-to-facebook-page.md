---
name: post-to-facebook-page
description: Share the new article or video natively on the Facebook business page in the owner's voice, creating the page post that Dollar a Day boosts will later run behind.
category: Content Factory — Post
stage: Post
definitive_article: GAP — to be written
status: needs-work
---

# Post to Facebook page

**Use this when** the article is live (and/or the video is processed) and needs native Facebook distribution from the business or Public Figure page.

## Inputs
- Published article URL and/or the processed video file
- Admin/editor access to the Facebook business page or Public Figure page (claimed per /digital-plumbing)
- The hook from Step 7 and the names of people/companies featured

## Steps
1. Post from the **page**, not a personal profile — only page posts can be boosted later with Dollar a Day.
2. Write a 2–4 sentence caption in the owner's first-person voice: lead with the hook or the customer question the piece answers, then one concrete takeaway. Conversational, no corporate-speak, no hashtag walls.
3. Prefer native media: upload the video file directly (native video outperforms shared links) or attach a real photo from the article. Put the article link in the caption or first comment.
4. Tag the people and companies featured so they see it and share it — their shares are the first organic amplification signal.
5. Publish, then reply to early comments within the first hours (hand off to engage-with-social-comments for ongoing).
6. Log the post URL plus date in the content tracker — Promote's boost-top-3-5-facebook-posts pulls candidates from this log based on organic engagement.

## Definition of done (QA checklist)
- [ ] Post is live on the page (boostable), not on a personal profile
- [ ] Caption is first-person, hook-led, 2–4 sentences; media is native (video or real photo, no stock)
- [ ] Featured people/companies tagged; article link present
- [ ] Post URL logged for the Promote stage boost shortlist
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. Candidate: a Superior Fence & Rail (Zach Peyton) article shared natively, then boosted once organic signal showed.

## Run on a persistent agent (Fable 5)
A persistent agent (Fable 5 or comparable OpenAI/Google models) drafts the caption from the hook stored at Step 7, posts natively from the page, then self-verifies the full Definition of done — page (not profile), tags live, link present, post URL logged — and repairs any miss before calling the run done.
Across runs it remembers which hooks and formats earned engagement on this page, so each caption starts from evidence rather than instinct.
It writes a meta-article example into the log each run — the same log boost-top-3-5-facebook-posts later reads — so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written (interim grounding: /social-amplification Stage 5 and /dad — boosts run behind these page posts)
- Related: /blog-posting-guidelines · /thank-you-machine (tag-and-thank posts follow the same native pattern)
- Run order (Post stage): upload-processed-video-to-youtube → **post-to-facebook-page** → post-to-linkedin → email-and-dm-client-about-published-article
