---
name: senior-team-member-reviews-weekly
description: Run the weekly senior review of queued SOP Amendment Proposals — approve with version increment and changelog, or reject with a written reason — so SOPs evolve under control.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: needs-work
---

# Senior team member reviews weekly

**Use this when** the fixed weekly review slot arrives and there are queued SOP Amendment Proposals — and run it even when the queue looks empty, to confirm the queue is truly empty and not silently broken.

## Inputs
- The review queue in the shared SOP Amendment Proposal location
- Edit access to the live SOPs, their version numbers, and changelogs
- The proposal format standard (≤500 words, four parts) as the acceptance bar

## Steps
1. At the fixed weekly time, open the queue and take every pending proposal. The standing rule: nothing remains queued for more than one week — a stale queue teaches the team to stop proposing.
2. For each proposal, verify format compliance first: four parts, ≤500 words, exactly one SOP. Non-compliant proposals go back to the submitter with the specific gaps, without consuming a full review.
3. Evaluate substance: Are the ≥2 examples real and do they actually demonstrate the problem? Does the proposed language fix it? Would dropping the text in break surrounding steps or violate methodology/implementation separation (Process 4)?
4. **Approve path:** integrate the proposed language into the SOP (verbatim or with reviewer edits), increment the SOP's version number, and add a changelog entry — date, what changed, proposer, reviewer. An approval without a version bump and changelog entry is not done.
5. **Reject path:** record the reason on the proposal itself and notify the submitter. Rejection without explanation kills the pipeline — the reason is the teaching moment (Learn, Do, Teach).
6. Mark every proposal resolved (approved/rejected) in the tracker with the decision date. The queue ends the session empty.
7. Note any cross-proposal patterns (same SOP repeatedly, recurring rejection causes) for the 6-month pattern review (`review-past-6-months-of-sop-amendment-proposals-for-patterns`).

## Definition of done (QA checklist)
- [ ] Queue emptied: every proposal approved, rejected, or returned for format — none older than one week
- [ ] Every approval shipped as live SOP text + version increment + changelog entry (date, change, proposer, reviewer)
- [ ] Every rejection carries a written reason and the submitter was notified
- [ ] Tracker statuses updated; decisions auditable later without asking anyone
- [ ] Patterns logged for the 6-month recursive review
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — Process 2 assigns weekly review to a senior team member with exactly these two outcomes: approve (version increment + changelog) or reject with reason.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first weekly review cycle and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) never misses the weekly slot: it opens the queue on schedule, pre-screens every proposal for format compliance, drafts an approve/reject recommendation with evidence for the senior reviewer's decision, and loops until the Definition of done fully passes — queue emptied, every approval shipped with version increment and changelog, every rejection carrying a written reason.
It self-verifies by confirming each approved text actually landed in the live SOP with its version bumped — an approval recorded but not shipped is caught the same session.
Memory across cycles is the review remembering itself: the agent retains every decision, reason, and returned proposal, so recurring rejection causes and repeatedly-amended SOPs surface automatically as patterns for the 6-month recursive review instead of being rediscovered by archaeology.
Each run it logs a meta-article example via the Meta-Article Prompt, so the review cadence produces compounding documentation, not just dispositions.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related (Process 2 run order): tag-proposal-with-affected-sop-and-queue-for-review → senior-team-member-reviews-weekly → review-past-6-months-of-sop-amendment-proposals-for-patterns; infrastructure: set-up-sop-amendment-proposal-tracking-system.
