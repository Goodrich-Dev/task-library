---
name: set-up-sop-amendment-proposal-tracking-system
description: Stand up the end-to-end SOP Amendment tracking system — shared location, tracking fields, weekly review slot, and a verified dry run — so Process 2 operates from day one.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: gap
---

# Set up SOP Amendment Proposal tracking system

**Use this when** implementing the maintenance system — this task is the Implementation Checklist milestone that turns the SOP Update Protocol from documentation into a running pipeline. It is a gap: no tracking system exists yet.

## Inputs
- The shared location decision or the skill that creates it (`create-shared-location-for-sop-amendment-proposals`)
- The named senior reviewer and a weekly review slot candidate
- The proposal format standard (≤500 words: problem, affected SOP, proposed language, ≥2 examples)

## Steps
1. Create the shared location first — run `create-shared-location-for-sop-amendment-proposals` (Google Doc, WordPress draft, or project board; exactly one).
2. Define the tracking fields every proposal carries: title, affected-SOP tag, submitter, submission date, priority, status (queued / approved / rejected / returned), resolution note, and the SOP version the approval produced. These fields are what make the 6-month pattern review possible — skimp now, fly blind later.
3. Pin the proposal format at the top of the system so the entry bar is self-explanatory.
4. Lock in the weekly review: a named senior reviewer and a fixed recurring slot on their calendar (see `senior-team-member-reviews-weekly` for the session SOP).
5. Dry-run one test proposal through the complete loop: draft → tag → queue → weekly review → approve with version increment + changelog (or reject with reason) → archive. Fix every snag the dry run exposes before announcing.
6. Announce the system to the team with the one-line rule: SOPs change only through this pipeline — no drive-by edits.
7. Link the system from /knowledge-system-maintenance so the hub points at the live infrastructure.

## Definition of done (QA checklist)
- [ ] One canonical location live with all eight tracking fields and the format pinned
- [ ] Named senior reviewer holding a recurring weekly review slot
- [ ] Dry-run proposal completed the full loop, producing a version increment + changelog entry on a test SOP
- [ ] Team announced and the no-drive-by-edits rule communicated
- [ ] System linked from the hub; pattern-review fields confirmed queryable for the 6-month cycle
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — the Implementation Checklist requires this tracking system as the operational backbone of Process 2. Gap: not yet built — running this skill closes it.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first real proposals flow through, then link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) stands up the full pipeline — canonical location, all eight tracking fields, pinned format, named reviewer with a recurring slot — and loops until the Definition of done fully passes, with the dry run as the gate: one test proposal driven through draft → tag → queue → review → resolve, producing a real version increment and changelog entry on a test SOP.
It self-verifies by querying the tracking fields the way the 6-month pattern review will, confirming proposals-per-SOP, approval rate, and decision time are actually answerable from the data the system records.
The eight fields are memory infrastructure, and the agent treats them that way across audit cycles: it remembers why each field exists, watches that the data keeps accumulating cleanly, and escalates field rot before it blinds the recursive review — "skimp now, fly blind later" is the failure it is built to prevent.
Each run it logs a meta-article example via the Meta-Article Prompt, so the build and its dry run become documented, repeatable knowledge.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related: create-shared-location-for-sop-amendment-proposals (component) → set-up-sop-amendment-proposal-tracking-system (system) → Process 2 run order: create-sop-amendment-proposal-500-words → tag-proposal-with-affected-sop-and-queue-for-review → senior-team-member-reviews-weekly.
