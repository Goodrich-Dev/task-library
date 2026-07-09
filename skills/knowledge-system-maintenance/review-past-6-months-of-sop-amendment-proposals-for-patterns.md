---
name: review-past-6-months-of-sop-amendment-proposals-for-patterns
description: Mine six months of SOP Amendment Proposals for patterns — repeatedly-patched SOPs, missing processes, proposal friction — and convert each pattern into a system-level fix.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: needs-work
---

# Review past 6 months of SOP Amendment Proposals for patterns

**Use this when** the 6-month recursive review cycle opens — run this analysis first, because its patterns are the evidence the maintenance-article audit needs.

## Inputs
- The complete SOP Amendment Proposal tracker for the past six months: approved, rejected, and returned proposals
- SOP version histories and changelogs for the same period
- The five-process map from /knowledge-system-maintenance

## Steps
1. Export every proposal from the past six months from the shared tracker — including rejected and format-returned ones; failures carry as much signal as approvals.
2. Categorize each proposal three ways: by affected SOP, by problem type (outdated tool step, missing step, wrong sequence, unclear language), and by outcome (approved, rejected, returned).
3. Hunt the known pattern shapes: **same SOP amended repeatedly** — structural weakness; it needs a rewrite or layer separation, not more patches; **clusters around work no process covers** — a candidate new process for the hub; **repeated format rejections** — proposal friction; fix the template, the examples, or the training, not the proposers; **near-zero proposals overall** — pipeline failure, not perfection; SOPs do not stop drifting just because nobody files paperwork.
4. Quantify the basics so trends compare across cycles: proposals per SOP, approval rate, median time from submission to decision.
5. Convert every confirmed pattern into exactly one action: a proposed new/modified process for /knowledge-system-maintenance, a queued SOP rewrite with owner, or a pipeline fix (template, queue, review cadence). A pattern observed but not actioned is trivia, not analysis.
6. Write up findings and actions as the evidence package for `audit-this-maintenance-article-every-6-months`, and file the actions through the SOP Update Protocol where they change documented process.

## Definition of done (QA checklist)
- [ ] 100% of the period's proposals reviewed and categorized — including rejections and returns
- [ ] Metrics computed (proposals per SOP, approval rate, median decision time) and compared to the prior cycle where one exists
- [ ] Every identified pattern paired with exactly one concrete action and owner
- [ ] Zero-proposal or low-flow finding treated as pipeline failure and actioned accordingly
- [ ] Findings handed to the 6-month article audit as its evidence base
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — Process 5 prescribes this pattern review to spot needed new processes and proposal friction across the amendment history.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first 6-month pattern review and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) takes 100% of the period's proposals — approved, rejected, and returned — categorizes each three ways, computes the metrics, and loops until the Definition of done fully passes: every confirmed pattern paired with exactly one concrete action and owner, zero patterns left as trivia.
It self-verifies by reconciling counts (categorized total equals tracker total) and by treating near-zero proposal flow as the pipeline failure the hub says it is, never as good news.
Memory across cycles converts this from archaeology into a query: the agent lived through the weekly reviews and remembers every decision and reason as it happened, so the 6-month pattern hunt runs over held history, and proposals-per-SOP, approval rate, and decision time compare cycle over cycle automatically — the system measuring its own improvement.
Each run it logs a meta-article example via the Meta-Article Prompt, handing the article audit its evidence package and the library a documented run.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related (Process 5 run order): review-past-6-months-of-sop-amendment-proposals-for-patterns → audit-this-maintenance-article-every-6-months; upstream data: senior-team-member-reviews-weekly, set-up-sop-amendment-proposal-tracking-system.
