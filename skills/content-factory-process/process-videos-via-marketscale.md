---
name: process-videos-via-marketscale
description: Use the MarketScale platform to process and distribute raw video as an alternate Process-stage path, returning finished assets to the Content Library.
category: Content Factory — Process
stage: Process
definitive_article: GAP — to be written
status: gap
---

# Process videos via MarketScale

**Use this when** a raw video is designated for the MarketScale processing/distribution path instead of (or alongside) the in-house Descript pipeline.

> **Gap notice:** this task has no definitive article and no documented house SOP yet. The steps below are the provisional process from the task definition; the FIRST real run must be documented with the Meta-Article Prompt to seed the definitive article and harden this skill.

## Inputs
- The raw video file from the Content Library `01-Raw` folder (already archived in Google Drive per Step 1 — Drive remains the system of record)
- MarketScale platform access (account credentials held by the brand, not an individual VA)
- The video's GCT statement, title, and description copy (so distribution carries correct framing)
- The Content Library tracker

## Steps
1. Confirm why this video routes through MarketScale rather than the standard Descript path (e.g., client mandate or distribution reach) and note the reason in the tracker — routing decisions are knowledge to capture.
2. Upload the raw video from Drive to MarketScale; never let MarketScale hold the only copy.
3. Submit it for MarketScale's processing (editing/captioning per the platform's workflow), supplying the GCT-derived title, description, and the brand/speaker attribution.
4. Review the processed cut before any distribution: names spelled correctly, captions accurate, nothing cut that changes the speaker's meaning. Apply the same authenticity bar as the Descript path.
5. Approve distribution targets in line with the video's Targeting — and record exactly where MarketScale publishes it.
6. Download the processed master and captions back into the Content Library (`02-In-Process` → `03-Published`), so the article pipeline (Steps 2–11) can still run off the same asset.
7. Update the tracker: processed-asset links, distribution URLs, and status. Embed/link distribution URLs from the eventual article where appropriate.
8. Document this run via `write-meta-article-documenting-agent-work` — the gap closes only when a real run is published and the definitive article gets written.

## Definition of done (QA checklist)
- [ ] Routing reason recorded; Drive still holds the master copy
- [ ] Processed cut reviewed and approved against transcript-accuracy and authenticity standards
- [ ] Distribution destinations recorded with URLs in the tracker
- [ ] Processed assets returned to the Content Library for the article pipeline
- [ ] First-run meta-article created (Meta-Article Prompt) to seed the missing definitive article
- [ ] Linked back to the definitive article and relevant siblings (hub pending)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. No documented MarketScale run exists in the library yet; the first one defines the standard.

## Run on a persistent agent (Fable 5)

A gap task is the ideal persistent-agent assignment: the agent (Claude Fable 5, or a comparable OpenAI/Google model that loops and holds memory) documents the run while executing it — routing reason, processing notes, distribution URLs — so the first pass produces both the deliverable and the meta-article that seeds the missing definitive article. It loops until assets are back in the Content Library and every tracker field is filled, never "distributed, details later." Memory carries each run's routing decisions forward into the SOP this task still lacks.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written ("How to Process Videos via MarketScale" is on the Gaps & Tasks to Create list, low priority).
- Related: /content-factory, /blog-posting-guidelines (the parallel in-house path), /meta-article-prompt-template
- Sibling skills, in run order: `step-1-upload-video-to-google-drive-and-descript` → this (alternate path) → `step-12-post-article-on-wordpress` (Post stage)
