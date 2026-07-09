---
name: capture-client-stories-on-phone
description: Film real client testimonials and success stories on a smartphone so the brand has authentic third-party proof to process, post, and promote.
category: Content Factory — Produce
stage: Produce
definitive_article: GAP — to be written
status: needs-work
---

# Capture client stories on phone

**Use this when** a client has a result worth telling — a finished project, a milestone, a referral-worthy outcome — and you are physically or virtually with them.

## Inputs
- A phone with camera and microphone
- A client with a real, specific result (numbers, before/after, a story — not generic praise)
- Verbal or written permission to record and publish (name, face, company)
- Access to the Content Library Google Drive folder

## Steps
1. Ask permission first: confirm the client is comfortable being named, shown, and published. No anonymous testimonials — attribution is what makes proof credible (see the Website QA Audit trust checks).
2. Set the phone at eye level in the client's real environment (their shop, their yard, the finished job).
3. Do not hand them a script. Ask real questions and let them answer: "What problem did you have? What did we do? What changed — be specific? Would you recommend this, and to whom?"
4. Get them to say their full name, title, and company on camera — this becomes the attribution line.
5. Capture 30–60 seconds of b-roll: the finished work, the location, the handshake. Process will need visuals that are not stock.
6. Shoot a still photo (headshot or with the work) for use as the testimonial photo and article imagery.
7. Name files `YYYY-MM-DD-clientname-story` and upload video + photos to the Content Library Drive folder.
8. Log in the Content Library tracker with status "Raw — ready for Process" and note the permission status.

## Definition of done (QA checklist)
- [ ] Client states a specific, concrete result (not "they were great")
- [ ] Full name, title, and company captured on camera for attribution
- [ ] Publication permission confirmed and noted in the tracker
- [ ] At least one still photo and 30s of b-roll captured alongside the testimonial
- [ ] Files uploaded to the Content Library and logged for the Process stage
- [ ] Linked back to the definitive article and relevant siblings

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. Candidate: a Superior Fence & Rail (Zach Peyton) customer story or a Thank You Machine follow-up captured on site.

## Run on a persistent agent (Fable 5)

A human films the client; a persistent agent (Claude Fable 5, or a comparable long-horizon OpenAI/Google model) owns the rest — it preps the question list and permission checklist, then loops post-capture until every Definition-of-done item passes: attribution on camera, permission noted, b-roll and photo filed, tracker logged. Memory tracks which clients are captured and each one's permission status, so follow-ups extend prior runs instead of starting cold. Log a meta-article example per story so the proof bank compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — no definitive article yet; this skill flags the missing hub. Until written, ground runs in /one-minute-video-guide and /thank-you-machine.
- Related: /thank-you-machine (gratitude content from the same moments), /website-qa-audit (testimonial attribution standards), /one-minute-video-guide
- Sibling skills, in run order: `record-one-minute-videos` → this → `step-1-upload-video-to-google-drive-and-descript`
