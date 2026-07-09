---
name: add-last-audited-column-to-definitive-article-guide-status-table
description: Add a Last Audited column to the Definitive Article Guide status table, initialized to "Not yet audited" for every article, so audit recency becomes visible and enforceable.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: gap
---

# Add Last Audited column to Definitive Article Guide status table

**Use this when** implementing the maintenance system — this task is a gap from the Implementation Checklist: the status table currently shows what state each article is in, but not when anyone last verified it.

## Inputs
- Edit access to the status table in the Definitive Article Guide
- The Definitive Article Index (the canonical list of articles the table must cover)

## Steps
1. Open the status table in the Definitive Article Guide and add a **Last Audited** column alongside the Green/Yellow/Red status column.
2. Set the initial value for every existing row to **"Not yet audited"** — exactly that, for all articles. No retroactive dates, no "probably checked in spring": the column tells the truth from day one, and the truth is that the quarterly cycle has not run yet.
3. While in the table, reconcile rows against the Definitive Article Index: every article in the index has a row; every row maps to a real article. Add missing rows (also "Not yet audited") and flag orphan rows.
4. Update the table's usage note so the column is load-bearing: each quarterly audit must stamp this column with the audit date when updating status (Process 1's closing step, `update-status-table-in-definitive-article-guide`).
5. Announce the change to the audit team: from now on, "audited" means a date in this column — a status with no date is an unverified claim.
6. Hand off to `schedule-first-quarterly-audit-cycle` so real dates start replacing "Not yet audited" in Q3 2026.

## Definition of done (QA checklist)
- [ ] Last Audited column exists in the status table with every row initialized to "Not yet audited"
- [ ] Table reconciled against the Definitive Article Index — complete rows, no orphans
- [ ] Usage note updated: quarterly audits must stamp date + status here
- [ ] Audit team notified that undated statuses count as unverified
- [ ] First quarterly cycle queued to begin filling real dates
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — the Implementation Checklist specifies this column with initial value "Not yet audited" for all articles. Gap: column not yet added — running this skill closes it.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the column ships and the first real date lands, then link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) adds the Last Audited column, initializes every row to exactly "Not yet audited," reconciles the table against the Definitive Article Index, and loops until the Definition of done fully passes — complete rows, no orphans, the usage note updated, the team notified that an undated status is an unverified claim.
It self-verifies by re-diffing table rows against the index after the edit: zero articles missing a row, zero rows pointing at nothing.
The column is the system's memory made visible, and a memory-bearing agent keeps it honest across every future audit cycle: it remembers the reconciliation state, flags rows added without the convention, and refuses retroactive dates — the table only ever says what was actually verified, and when.
Each run it logs a meta-article example via the Meta-Article Prompt, so the infrastructure change itself enters the knowledge base.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related: update-status-table-in-definitive-article-guide (the step that writes to this column) → schedule-and-assign-quarterly-auditors → schedule-first-quarterly-audit-cycle.
