---
name: record-one-minute-videos
description: Record short, unscripted one-minute videos on a phone answering real customer questions — the raw fuel every Content Factory pipeline run starts from.
category: Content Factory — Produce
stage: Produce
definitive_article: /one-minute-video-guide
status: complete
---

# Record one-minute videos

**Use this when** you (or a client) need raw video content for the Content Factory and have real customer questions waiting to be answered.

## Inputs
- A phone with a working camera and microphone (no studio gear — authenticity beats production value)
- A list of real customer questions, pulled from the Topic Wheel WHAT ring, sales calls, comments, or support emails
- The person who actually answers these questions in real life (owner, practitioner — not an actor)
- Access to the Content Library Google Drive folder for upload

## Steps
1. Pick ONE real customer question from the topic queue (see `map-out-one-minute-video-topics-using-topic-wheel`). One question per video — never bundle.
2. Set up the phone at eye level in a real setting (truck, job site, office). Natural light, quiet enough to hear clearly.
3. Do not script. Glance at the question, then talk to the camera like the customer is standing in front of you.
4. Structure the take: say the question → answer it with a specific story or example → give the "so what" for the customer.
5. Keep it to roughly 60 seconds. If it runs 90, fine — do not restart chasing perfection. One take, move on.
6. Record the next question. Momentum matters more than polish; batch where possible (see `batch-record-50-raw-clips-in-one-session`).
7. Name each file `YYYY-MM-DD-topic-person` and upload to the designated Google Drive folder in the Content Library.
8. Log each clip in the Content Library tracker with status "Raw — ready for Process" so Step 1 of the Process stage can pick it up.

## Definition of done (QA checklist)
- [ ] Each video answers exactly one real customer question (not an invented topic)
- [ ] Unscripted, first person, shot on a phone — no teleprompter read, no stock-feel staging
- [ ] Audio is clearly audible on phone speakers
- [ ] Runtime is ~60 seconds (45–90s acceptable)
- [ ] Files named to convention and uploaded to the Content Library Drive folder
- [ ] Logged in the Content Library tracker and queued for the Process stage
- [ ] Linked back to the definitive article and relevant siblings

## Example(s)
- Marko Sipila (HVAC Quote) and Zach Peyton (Superior Fence & Rail) built their pipelines on exactly these phone-shot answer videos — their published articles trace back to clips recorded this way.
- Example needed — run the Meta-Article Prompt after first real run to document a fresh batch.

## Run on a persistent agent (Fable 5)

A persistent agent (Claude Fable 5, or a comparable OpenAI/Google model that loops and holds memory) can't hold the camera, but it runs everything around it: queue the next real customer question, then verify every clip against the Definition of done — naming, Drive upload, tracker row — and keep chasing until all boxes check, not most. Memory holds the topic queue and which questions are already answered, so sessions build forward instead of re-recording. Every run closes by logging a meta-article example, which is how the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /one-minute-video-guide
- Related: /topic-wheel (topic planning), /content-factory (the full pipeline), /blog-posting-guidelines (what Process does with the clip)
- Sibling skills, in run order: `map-out-one-minute-video-topics-using-topic-wheel` → this → `step-1-upload-video-to-google-drive-and-descript`
