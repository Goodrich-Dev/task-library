---
name: create-quote-cards-from-strongest-statements
description: Turn the video's best verbatim soundbites into attributed visual quote cards for social posting and article imagery.
category: Content Factory — Process
stage: Process
definitive_article: GAP — to be written
status: needs-work
---

# Create quote cards from strongest statements

**Use this when** a transcript contains short, punchy statements that work as standalone text — typically right after clip extraction has surfaced the best moments.

## Inputs
- The verified transcript (and clip log, if `extract-15-60-second-clips-from-long-form-video` already ran)
- A real photo of the speaker from the Content Library (no stock imagery)
- The brand's visual conventions (colors, logo, typography)
- A design tool the team already uses for social graphics

## Steps
1. Sweep the transcript for one-to-two sentence statements that stand alone: contrarian claims, hard numbers, blunt advice ("the lowest quote is usually the most expensive one").
2. Keep quotes VERBATIM — what the person actually said, from the verified transcript. No tightening that changes their words; credibility is the asset.
3. Shortlist 3–5 quotes per source video; reject anything that needs context to land.
4. Design each card: the quote large and readable at thumbnail size, attribution line with full name and company (e.g., "Marko Sipila, HVAC Quote"), the speaker's real photo, brand colors/logo. No stock backgrounds.
5. Export per-destination sizes (square for feed, vertical for stories) with descriptive filenames.
6. Verify each card against the transcript one last time — a misquoted card published is worse than none.
7. Log cards in the Content Library tracker, linked to the source video row, routed to `create-social-media-posts-per-platform` and available as article imagery for Step 8.

## Definition of done (QA checklist)
- [ ] Every quote is verbatim from the verified transcript
- [ ] Full attribution on every card: name + company/title
- [ ] Real photo of the speaker used — zero stock imagery
- [ ] Readable at thumbnail size; brand-consistent design
- [ ] Cards logged, linked to source, and routed in the tracker
- [ ] Linked back to the definitive article and relevant siblings

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. Candidate: quote cards from a Zach Peyton (Superior Fence & Rail) interview's strongest lines.

## Run on a persistent agent (Fable 5)

Verbatim is verifiable: a persistent agent (Claude Fable 5, or comparable long-horizon OpenAI/Google models) shortlists the strongest lines, then loops a word-for-word check of every card against the verified transcript before anything gets logged — one misquote fails the whole run. Memory tracks which quotes have already shipped, so the same line never publishes twice. Close each run with a logged meta-article example.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — no definitive article yet; this skill flags the missing hub. Until written, ground runs in /blog-posting-guidelines (real-image and attribution standards).
- Related: /social-amplification (Stage 3 content assets), /website-qa-audit (attribution standards)
- Sibling skills, in run order: `extract-15-60-second-clips-from-long-form-video` → this → `create-social-media-posts-per-platform`
