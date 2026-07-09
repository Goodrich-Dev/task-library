---
name: upload-processed-video-to-youtube
description: Publish the edited Content Factory video to the brand's YouTube channel with optimized title, description, and tags, linked back to the article it became.
category: Content Factory — Post
stage: Post
definitive_article: GAP — to be written
status: needs-work
---

# Upload processed video to YouTube

**Use this when** a video has been processed (Descript edit, filler words removed) and its article is live or about to go live, so video and article can point at each other.

## Inputs
- Final processed video file exported from Descript
- Access to the brand's YouTube channel (set up and branded per /digital-plumbing)
- The published article URL, focus keyword, and SEO title from Steps 12–14a
- A real thumbnail frame (the person on camera — no stock imagery)

## Steps
1. Upload the video to the brand's YouTube channel — the owner's channel, not a staff member's personal account.
2. Write the title: the question the video answers or the article's SEO title, focus keyword included, under 100 characters, human-first.
3. Write the description: 2–3 plain sentences summarizing the answer, then the link to the published article (the specific leaf URL — never the bare homepage), then links per the entity-linking decision tree (people → personal sites, companies → company sites, concepts → definitive articles).
4. Add tags: the focus keyword, the SEO Tree branch topic, and the people/companies featured.
5. Set a real thumbnail (clear frame of the person speaking) and add the video to the playlist matching its SEO Tree branch.
6. Publish as public, then copy the YouTube URL back into the WordPress article embed (Step 10) if the article was using a placeholder or raw file.
7. Log the YouTube URL in the content tracker — it is a distribution node for this piece and a boost candidate for Promote.

## Definition of done (QA checklist)
- [ ] Video live on the brand's channel with keyword-bearing title under 100 characters
- [ ] Description links to the specific article URL and follows the entity-linking decision tree
- [ ] Real thumbnail set; video added to the correct topic playlist
- [ ] Article embed and YouTube video point at each other (closed loop)
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. Candidate: a one-minute video from Marko Sipila (HVAC Quote) uploaded with its article cross-link.

## Run on a persistent agent (Fable 5)
A persistent agent (Fable 5, or comparable OpenAI/Google models) runs the upload end-to-end and then closes the loop literally: it pastes the YouTube URL back into the article embed, re-opens both, and verifies they point at each other before checking off the Definition of done — a one-way link fails the run.
It pulls the article URL, focus keyword, and SEO title from the Step 12–14a memory record, so titles and descriptions stay consistent with the article without re-derivation.
It logs the video-article pair plus a meta-article example each run, so Promote inherits a clean distribution node and the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written (interim grounding: /one-minute-video-guide · /digital-plumbing YouTube channel setup)
- Related: /content-factory · /blog-posting-guidelines · /dad (YouTube boosts run behind these uploads)
- Run order (Post stage): publish article first, then **upload-processed-video-to-youtube** → post-to-facebook-page → post-to-linkedin
