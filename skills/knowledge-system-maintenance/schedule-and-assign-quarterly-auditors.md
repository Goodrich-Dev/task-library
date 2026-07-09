---
name: schedule-and-assign-quarterly-auditors
description: Assign a named auditor and deadline to every definitive article each quarter so the Process 1 audit actually happens instead of remaining a good intention.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: gap
---

# Schedule and assign quarterly auditors

**Use this when** a new quarter approaches and audit assignments must be set — or now, because no assignment system exists yet (this task is a gap: the first run creates the rotation).

## Inputs
- The full list of definitive articles from the Definitive Article Guide status table
- The team roster with availability
- The quarterly calendar (first cycle deadline: Q3 2026, per the Implementation Checklist)

## Steps
1. Pull the complete article list from the status table — every definitive article gets audited every quarter; no article is exempt because it "was fine last time."
2. Divide the articles across team members so each article has exactly one named auditor. Balance load by article size, and avoid assigning authors to audit only their own articles — fresh eyes catch drift the author has normalized.
3. Set the quarter's audit deadline. For the first cycle, use Q3 2026 (see `schedule-first-quarterly-audit-cycle`); thereafter, keep a fixed cadence each quarter.
4. Record the assignments where the team already looks: an auditor column or section alongside the status table, with auditor name and due date per article.
5. Put the audit window on the calendar with a midpoint reminder, so misses surface with time to recover rather than on deadline day.
6. Point each auditor at the Process 1 skills in run order: topic coherence → structural completeness → information currency → cross-reference integrity → status-table update.
7. At quarter close, verify every assigned article shows a fresh audit date in the table. Carry any miss visibly into next quarter with a reassigned (not quietly dropped) auditor.
8. After the first full rotation, capture what broke (load imbalance, unclear ownership) as Knowledge Capture Notes and amend this SOP accordingly.

## Definition of done (QA checklist)
- [ ] Every definitive article has exactly one named auditor and a due date this quarter
- [ ] No auditor is solely auditing their own articles; load is roughly balanced
- [ ] Assignments recorded next to the status table and calendared with a midpoint reminder
- [ ] Quarter-close verification done: 100% of articles show a current audit date, or misses are visibly carried forward
- [ ] Rotation friction captured as Knowledge Capture Notes / SOP Amendment Proposals
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — Process 1 calls for scheduling and assigning quarterly auditors; this skill operationalizes it. Gap: no rotation exists yet — the first run is the example.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first real assignment cycle and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) pulls the full article list, balances assignments so every article has exactly one named auditor with a due date, calendars the window with its midpoint reminder, and loops until the Definition of done fully passes — including the quarter-close verification that every assigned article shows a fresh audit date.
It self-verifies by re-counting assignments against the article list and confirming no auditor is grading only their own work.
Memory across cycles is what makes the rotation improve itself: the agent remembers who audited what, who missed deadlines, and where load was unbalanced, then designs the next quarter's rotation from that history — misses are carried forward visibly because the agent does not forget them.
Each run it logs a meta-article example via the Meta-Article Prompt, so the assignment cycle's friction becomes documented knowledge instead of folklore.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related: schedule-first-quarterly-audit-cycle (first cycle, Q3 2026), then the Process 1 audit skills in run order beginning with check-topic-coherence-for-each-definitive-article; update-status-table-in-definitive-article-guide closes each audit.
