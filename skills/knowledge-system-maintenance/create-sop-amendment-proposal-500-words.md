---
name: create-sop-amendment-proposal-500-words
description: Turn a real-world SOP failure into a ≤500-word amendment proposal — problem, affected SOP, exact proposed language, and at least two real examples — ready for weekly senior review.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: complete
---

# Create SOP Amendment Proposal (≤500 words)

**Use this when** you hit a point in real work where an SOP is wrong, outdated, or missing a step — and you can point to at least two real occurrences, not one bad day.

## Inputs
- The affected SOP's name and the exact section that failed
- At least two real examples of the failure (dates, clients, runs, or links)
- The shared SOP Amendment Proposal location (see `create-shared-location-for-sop-amendment-proposals`)

## Steps
1. Confirm the trigger is real: the SOP failed, drifted from reality, or lacked a needed step in at least two actual runs. One occurrence may be noise — log it as a Knowledge Capture Note and wait for a second before proposing.
2. Draft the proposal with exactly four parts: **(a) the problem** — what failed or drifted, stated plainly; **(b) the affected SOP** — name plus the specific section/step; **(c) proposed language** — the exact replacement or added text, ready to paste in; **(d) examples** — at least two real cases with dates/links where the current SOP failed.
3. Write the proposed language in the SOP's own voice: imperative, concrete steps. Respect Platform Portability Discipline (Process 4) — keep methodology (what/why) separate from tool-specific implementation (how).
4. Enforce the budget: 500 words maximum across all four parts. Cut backstory and justification prose; keep the problem, the text, and the proof. If it cannot fit, you are proposing more than one amendment — split it.
5. Self-check against the reviewer's criteria: Would the proposed text drop into the SOP without breaking surrounding steps? Do the examples actually demonstrate the problem?
6. Save the proposal to the shared location, then hand off to tagging and queueing (`tag-proposal-with-affected-sop-and-queue-for-review`). Do not edit the live SOP yourself — that is the reviewer's call.

## Definition of done (QA checklist)
- [ ] All four parts present: problem, affected SOP + section, paste-ready proposed language, ≥2 real examples with dates/links
- [ ] Total length ≤500 words (counted, not eyeballed)
- [ ] Proposed language is imperative, concrete, and preserves methodology/implementation separation
- [ ] Exactly one SOP and one coherent change per proposal
- [ ] Filed in the shared location; live SOP left untouched pending review
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — Process 2 defines this exact format (≤500 words: problem, SOP, proposed language, ≥2 real examples) as the only entry path for SOP changes.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first approved amendment and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) drafts the four-part proposal and loops until the Definition of done fully passes — counting the 500-word budget literally, verifying both examples carry dates or links, and splitting anything that covers more than one coherent change.
It self-verifies by paste-testing the proposed language against the live SOP's surrounding steps to confirm it drops in without breaking them.
Memory across cycles is what powers the two-example threshold: the agent remembers every failure it has logged, so the moment a second real occurrence appears it pairs the two into a proposal automatically — single incidents wait as remembered Knowledge Capture Notes instead of being lost or prematurely escalated.
Each run it logs a meta-article example via the Meta-Article Prompt, so approved amendments arrive with their own documented origin story.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related (Process 2 run order): create-sop-amendment-proposal-500-words → tag-proposal-with-affected-sop-and-queue-for-review → senior-team-member-reviews-weekly; infrastructure: create-shared-location-for-sop-amendment-proposals; upstream feeder: route-notes-to-sop-update-protocol-or-directly-to-articles.
