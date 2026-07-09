---
name: process-through-content-factory
description: Run the thank-you video through the Content Factory to mint five assets — social post, blog excerpt, testimonial, ad creative, and email — from one minute of gratitude.
category: Thank You Machine
stage: Process
definitive_article: /thank-you-machine
status: complete
---

# Process through Content Factory

**Use this when** a thank-you video has been recorded and sent privately — one minute of sincere footage should never end as one DM.

## Inputs
- The recorded thank-you clip, filed in the Content Library (person–trigger–date)
- The trigger row (person, deed, why it mattered, handle) — the metadata is the story
- Standard Content Factory access: transcription (Descript), WordPress, email tool

## Steps
1. Intake like any factory asset: upload to the Content Library and transcribe — the transcript supplies captions, quotes, and the written derivatives.
2. Mint the five assets from the one clip:
   - **Social post** — native video upload with a 2–3 line caption telling the story (who, what they did, why it mattered).
   - **Blog excerpt** — a short passage for a relevant article: a client story, lessons-learned piece, or gratitude roundup.
   - **Testimonial pull** — what the moment proves about the relationship or results; get the person's OK where it reads as their endorsement.
   - **Ad creative** — a cut formatted for Dollar a Day boosting (clean hook in the first seconds, captions on).
   - **Email** — a mention or feature in the newsletter ("this week I got to thank…").
3. Keep the person's name and the **specific deed** intact in every derivative. Gratitude generalized is gratitude deleted.
4. Apply Blog Posting Guidelines to anything published: first-person voice, real photos, short paragraphs, no AI-fluff.
5. Entity-link per the decision tree: the person's name links to their personal site or profile; their company to its site; concepts to definitive articles.
6. Stage all five assets in the publishing queue with the person's verified handle attached, ready for the tagging step.

## Definition of done (QA checklist)
- [ ] All five derivatives exist: social post, blog excerpt, testimonial, ad creative, email
- [ ] Name + specific deed intact in every asset; permission confirmed where used as endorsement
- [ ] Published pieces follow Blog Posting Guidelines and the entity-linking decision tree
- [ ] Assets staged with verified handles, ready for tag-the-person-on-social-media
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run (candidate: one thank-you clip shown becoming all five assets, with links to each).

## Run on a persistent agent (Fable 5)
Minting five assets from one clip is exactly the grind a persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) doesn't skip: it loops until all five derivatives exist with the name and specific deed intact in each — four of five staged is a failed run, not a near-complete one.
It self-verifies every asset against Blog Posting Guidelines and the entity-linking decision tree before staging, and its memory of prior runs keeps naming, links, and permission records consistent across everyone thanked.
Log one clip-to-five-assets example per run via the Meta-Article Prompt so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /thank-you-machine
- Related: /content-factory (the parent pipeline) · /blog-posting-guidelines (publishing standard) · /dad (where the ad-creative cut goes)
- Run order (TYM): record-one-minute-thank-you-video → **process-through-content-factory** → tag-the-person-on-social-media
