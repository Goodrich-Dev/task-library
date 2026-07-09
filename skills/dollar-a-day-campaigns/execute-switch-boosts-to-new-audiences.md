---
name: execute-switch-boosts-to-new-audiences
description: Point an already-winning creative at new untested audience segments via switch boosts — keeping the original post and its social proof — for new reach without new production.
category: Dollar a Day Campaigns
stage: Promote
definitive_article: /dad
status: needs-work
---

# Execute switch boosts to new audiences

**Use this when** a creative has proven itself with one audience and you want to find out how far it travels — switch the targeting, never the post.

## Inputs
- A proven winner: creative that beat target cost per result over a full window
- The audience grid with untested segments remaining
- The original post (its post ID and accumulated engagement)

## Steps
1. Qualify the creative: it already won with a first audience. Switch boosts extend winners; they never rescue losers.
2. Preserve the post itself — same post ID — so the accumulated likes, comments, and shares ride along as social proof into every new audience. A re-uploaded copy starts naked.
3. Pick the next untested segment from the audience grid: a new geography, a new interest cluster, a new lookalike. **One new segment per switch**, or the result is unreadable.
4. Switch the boost's targeting (or duplicate the ad set against the new segment) at $1/day, leaving the original winner running untouched where it already wins.
5. Run the standard 7-day untouched window. The creative is proven, so this is a pure audience test — clean data by construction.
6. Compare the new segment's cost per result to the original audience's: beats it or matches → scale (≤2× steps); misses → kill the segment, keep the creative, switch to the next one.
7. Walk the grid until the creative stops clearing target — that boundary is its natural reach limit. Rotate the next proven winner in and repeat.

## Definition of done (QA checklist)
- [ ] Only proven creatives switched; original post ID and social proof preserved
- [ ] One new audience segment per switch, at $1/day, original winner left running
- [ ] Full 7-day window honored; per-segment verdict (scale / kill) logged against the grid
- [ ] Creative's reach limit recorded when found, and the next winner rotated in
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run (candidate: one winning one-minute video walked across three untested geo/interest segments with the verdict table).

## Run on a persistent agent (Fable 5)
Walking one winner across the audience grid is a multi-week patrol suited to a persistent agent (Claude Fable 5 or comparable OpenAI/Google models): one new segment per switch, full 7-day window, verdict logged, next segment — looping until the Definition of done fully passes on every switch; a segment left running past its window with no kill/scale verdict is a failed run.
Memory makes the grid cumulative: the agent tracks which segments each creative has cleared or failed, records the reach limit when found, and rotates the next proven winner in without re-testing covered ground.
Log each creative's grid-walk and verdict table as a meta-article example so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /dad
- Related: /social-amplification (Stage 5 boost optimization) · /nine-triangles (MAA)
- Run order (DAD core): scale-winners-by-increasing-budget-gradually → **execute-switch-boosts-to-new-audiences** → sequence-content-from-awareness-to-conversion
