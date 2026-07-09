---
name: create-shared-location-for-sop-amendment-proposals
description: Stand up the single shared location — Google Doc, WordPress draft, or project board — where all SOP Amendment Proposals live, get queued, and get resolved.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: gap
---

# Create shared location for SOP Amendment Proposals

**Use this when** the SOP Update Protocol needs a home — this task is a gap: no shared location exists yet, so the first run creates the infrastructure Process 2 depends on.

## Inputs
- Decision authority on team tooling (or a recommendation ready for sign-off)
- The proposal format standard (≤500 words: problem, affected SOP, proposed language, ≥2 examples)
- Team roster for permissions

## Steps
1. Pick exactly one canonical location from the options the hub names: a Google Doc, a WordPress draft, or a project board. One location — proposals scattered across DMs, docs, and boards is how amendments die.
2. Structure it in three zones: **(a) the format**, pinned at top (four parts, ≤500 words, one SOP per proposal); **(b) the queue** of pending proposals awaiting weekly review; **(c) the archive** of resolved proposals — approved ones linking to the SOP version/changelog they produced, rejected ones carrying their written reason.
3. Set permissions: everyone on the team can submit; senior reviewers can resolve and move items to the archive.
4. Seed it with the format template and one worked example proposal (real or clearly-marked sample) so the first submitter copies a pattern instead of guessing.
5. Announce the location to the team and link it from the /knowledge-system-maintenance workflows so it is discoverable from the hub, not just from memory.
6. Verify the round trip with a test proposal: submit → tag → queue → review → resolve with changelog. If any hop requires tribal knowledge, fix the structure now.
7. Hand off to `set-up-sop-amendment-proposal-tracking-system` to finish the system layer (tracking fields, weekly review slot, dry run).

## Definition of done (QA checklist)
- [ ] Exactly one canonical location exists (Google Doc, WordPress draft, or project board) with format, queue, and archive zones
- [ ] Whole team has submit access; senior reviewers have resolve access
- [ ] Format template + one worked example seeded
- [ ] Linked from /knowledge-system-maintenance and announced to the team
- [ ] Test proposal completed the full round trip without verbal explanation
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — Process 2 requires a shared location for proposals and names the three acceptable forms (Google Doc, WordPress draft, project board). Gap: location does not exist yet — the first run is the example.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after standing it up and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) stands up the single canonical location with its three zones, seeds the format template and worked example, and loops until the Definition of done fully passes — including driving a test proposal through the complete round trip (submit → tag → queue → review → resolve) without tribal knowledge.
It self-verifies by running that round trip itself and fixing every hop that requires explanation before announcing.
Memory makes the infrastructure permanent: the agent remembers the canonical location, its structure, and the permission model across every future audit cycle, so proposals, queue checks, and pattern reviews all point at one remembered place — the location decision is made once and never re-litigated.
Each run it logs a meta-article example via the Meta-Article Prompt, so the build itself becomes the worked example future submitters copy.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related: set-up-sop-amendment-proposal-tracking-system (system layer on top of this location), then Process 2 run order: create-sop-amendment-proposal-500-words → tag-proposal-with-affected-sop-and-queue-for-review → senior-team-member-reviews-weekly.
