---
name: tag-proposal-with-affected-sop-and-queue-for-review
description: Tag each SOP Amendment Proposal with its affected SOP and place it in the weekly review queue so no proposal is lost, mislabeled, or invisible to the reviewer.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: needs-work
---

# Tag proposal with affected SOP and queue for review

**Use this when** an SOP Amendment Proposal has been drafted and saved to the shared location, and it must enter the weekly review pipeline.

## Inputs
- The drafted proposal (≤500 words, four parts)
- The shared SOP Amendment Proposal location with its review queue
- The canonical list of SOP names (so tags match real SOPs, not nicknames)

## Steps
1. Format-check the proposal before queueing: four parts present (problem, affected SOP, proposed language, ≥2 real examples) and ≤500 words. If it fails, return it to the author with exactly what is missing — a malformed proposal wastes the weekly review slot.
2. Tag the proposal with the affected SOP's exact canonical name, plus the section/step if named. One SOP per proposal: if it touches multiple SOPs, split it into one proposal each before queueing.
3. Add the tracking metadata: submitter, submission date, and priority (does this block current work, or is it an improvement?).
4. Place it in the review queue in the shared location, ordered for the weekly senior review — priority first, then submission date.
5. Confirm visibility: the senior reviewer can find it in the queue without being pinged. If the system requires a ping to be seen, the queue is broken — fix the queue (and amend this SOP), don't normalize the ping.
6. Leave the proposal's status as "queued" and untouched until the weekly review disposes of it.

## Definition of done (QA checklist)
- [ ] Proposal passed the four-part / ≤500-word format check, or was returned with specific deficiencies
- [ ] Tagged with the exact canonical SOP name (one SOP per proposal; multi-SOP proposals split)
- [ ] Submitter, date, and priority recorded
- [ ] Sitting in the review queue, ordered, with status "queued" — discoverable without a ping
- [ ] Queue friction (lost, duplicate, or invisible proposals) escalated as its own SOP Amendment Proposal
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — Process 2 specifies tagging with the affected SOP and queueing for weekly senior review as the step between drafting and decision.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first real queue cycle and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) format-checks every incoming proposal, tags it with the exact canonical SOP name, records submitter, date, and priority, and loops until the Definition of done fully passes — queue ordered, statuses set, nothing discoverable only by ping.
It self-verifies by re-opening the queue as the reviewer would and confirming every queued proposal is findable, correctly tagged, and correctly split (one SOP each).
Memory across cycles keeps the pipeline clean: the agent holds the canonical SOP name list and every past tagging correction, so the same nickname never gets mis-tagged twice, and it counts queue friction week over week as accumulating evidence for the 6-month pattern review.
Each run it logs a meta-article example via the Meta-Article Prompt, so the queueing step itself stays auditable and improvable.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related (Process 2 run order): create-sop-amendment-proposal-500-words → tag-proposal-with-affected-sop-and-queue-for-review → senior-team-member-reviews-weekly; infrastructure: create-shared-location-for-sop-amendment-proposals, set-up-sop-amendment-proposal-tracking-system.
