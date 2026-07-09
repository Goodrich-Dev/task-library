---
name: update-status-table-in-definitive-article-guide
description: Close out an article's quarterly audit by stamping its Green/Yellow/Red status and audit date into the Definitive Article Guide status table so the dashboard stays true.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: needs-work
---

# Update status table in Definitive Article Guide

**Use this when** the four audit checks (topic coherence, structural completeness, information currency, cross-reference integrity) are finished for an article and the result must be recorded — the final step of each Process 1 audit.

## Inputs
- Completed audit notes for the article (findings from all four checks)
- Edit access to the status table in the Definitive Article Guide
- The status legend: Green = complete, Yellow = needs work, Red = gap/broken

## Steps
1. Confirm all four audit checks actually ran. If any check was skipped, the audit is not done — do not stamp a status you cannot defend.
2. Assign the status from the findings, not from optimism: Green = passes every check and meets all definitive-article requirements; Yellow = page exists but fails at least one check or requirement; Red = missing or fundamentally broken.
3. Open the status table in the Definitive Article Guide and update the article's row: new status plus today's date in the Last Audited column. (If the column is missing, run `add-last-audited-column-to-definitive-article-guide-status-table` first.)
4. Add a one-line note on the row: what changed this quarter, or the single biggest blocker keeping it from Green.
5. For every Yellow or Red, create the follow-up task with a named owner and the specific fixes from the audit notes — a Yellow with no owner is a permanent Yellow.
6. Sanity-check the whole table while you are in it: every definitive article in the index has a row; no row shows an audit date for an audit that never happened; no row is older than one quarter unaudited without being flagged.
7. If the status legend or table structure failed you (statuses that fit nothing, missing columns), file an SOP Amendment Proposal instead of inventing local conventions.

## Definition of done (QA checklist)
- [ ] Status assigned strictly per the legend and backed by recorded findings from all four checks
- [ ] Row updated with status, audit date, and one-line blocker/change note
- [ ] Every Yellow/Red has a follow-up task with a named owner
- [ ] Table-wide sanity check done: complete rows, truthful dates, no silently stale articles
- [ ] Table inconsistencies escalated via SOP Amendment Proposal, not patched ad hoc
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — Process 1 requires updating the status table (Green/Yellow/Red + audit date) after each audit; the Task Library Dashboard mirrors this legend.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first real quarterly run and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) stamps statuses only from recorded findings — refusing to close any audit where one of the four checks is missing — and loops until the Definition of done fully passes: status, date, and blocker note on the row, a named owner on every Yellow/Red, and the whole table sanity-checked.
It self-verifies by cross-checking each stamped row against the audit notes and the article index, so no row claims an audit that never ran.
Memory across audit cycles turns the table into a longitudinal record: the agent remembers every row's history, flags articles stuck Yellow for consecutive quarters, catches statuses that flip Green without an explaining change, and surfaces silently aging rows before they rot — the table is the system's memory made visible, and the agent keeps it truthful.
Each run it logs a meta-article example via the Meta-Article Prompt, so the close-out step itself stays documented and improvable.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related (Process 1 run order): validate-cross-reference-integrity-across-articles → update-status-table-in-definitive-article-guide; setup: add-last-audited-column-to-definitive-article-guide-status-table; scheduling: schedule-and-assign-quarterly-auditors.
