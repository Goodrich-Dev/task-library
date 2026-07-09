---
name: schedule-first-quarterly-audit-cycle
description: Launch the first quarterly definitive-article audit cycle — every article assigned to a named auditor with Q3 2026 as the deadline — turning Process 1 from spec into schedule.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: gap
---

# Schedule first quarterly audit cycle

**Use this when** implementing the maintenance system — this Implementation Checklist task is a gap: no quarterly audit has ever run, every status-table row still reads "Not yet audited," and Q3 2026 is the committed first deadline.

## Inputs
- The Definitive Article Guide status table with the Last Audited column in place (`add-last-audited-column-to-definitive-article-guide-status-table`)
- The team roster and the assignment method (`schedule-and-assign-quarterly-auditors`)
- The four Process 1 audit skills, ready to hand to auditors

## Steps
1. Verify the prerequisite: the status table has its Last Audited column, initialized to "Not yet audited." If not, run that skill first — the cycle needs somewhere to write its results.
2. Pull the complete definitive article list from the table and assign every article to a named team auditor using the assignment SOP: one auditor per article, balanced load, fresh eyes preferred over authors auditing their own work.
3. Set **Q3 2026** as the first cycle's deadline, per the Implementation Checklist, and calendar the audit window with a midpoint reminder so misses surface early.
4. Equip each auditor with the Process 1 run order: `check-topic-coherence-for-each-definitive-article` → `verify-structural-completeness-against-8-step-framework` → `check-information-currency-with-latest-data` → `validate-cross-reference-integrity-across-articles` → `update-status-table-in-definitive-article-guide`.
5. Set the completion bar explicitly: an article counts as audited only when all four checks ran and the status table row shows this cycle's date and a defensible Green/Yellow/Red.
6. At the Q3 2026 deadline, verify coverage: every article stamped, every Yellow/Red carrying a follow-up owner. Carry misses visibly into Q4 with reassigned auditors — quietly dropping them resets the system to zero.
7. Close the first cycle by capturing what broke (load, unclear checks, tooling) as Knowledge Capture Notes and amendments, so the second cycle runs smoother — the recursive loop applies to the cycle itself.

## Definition of done (QA checklist)
- [ ] Every definitive article assigned to a named auditor with the Q3 2026 deadline calendared (window + midpoint reminder)
- [ ] All auditors equipped with the four-check run order and the completion bar
- [ ] At deadline: 100% of articles stamped with date + status, or misses visibly carried into Q4 with new owners
- [ ] First-cycle friction captured as Knowledge Capture Notes / SOP Amendment Proposals
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — the Implementation Checklist sets Q3 2026 as the first audit deadline with articles assigned to team members. Gap: cycle not yet scheduled — running this skill closes it.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the Q3 2026 cycle completes and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) verifies the Last Audited column exists, assigns every definitive article to a named auditor, calendars the Q3 2026 window with its midpoint reminder, equips each auditor with the four-check run order, and loops until the Definition of done fully passes — 100% assignment coverage and the completion bar stated explicitly.
It self-verifies by counting assignments against the article list, then again at the midpoint and the deadline: every article stamped with date and a defensible status, or the miss carried visibly into Q4 with a reassigned owner.
Memory across the cycle is what makes a first launch survivable: the agent holds the assignment state for the whole quarter, never loses a miss, and remembers the first cycle's friction — load imbalance, unclear checks, tooling gaps — so the second cycle is designed from evidence, which is the recursive loop applied to the cycle itself.
Each run it logs a meta-article example via the Meta-Article Prompt, replacing this skill's "Example needed" with the documented Q3 2026 run.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related: add-last-audited-column-to-definitive-article-guide-status-table (prerequisite) → schedule-and-assign-quarterly-auditors (assignment method) → schedule-first-quarterly-audit-cycle (first launch) → Process 1 audit skills in run order.
