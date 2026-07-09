---
name: review-existing-sops-for-portability-compliance
description: Audit the existing SOP library for methodology/implementation separation, grade each document, and queue the entangled ones for restructuring.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: needs-work
---

# Review existing SOPs for portability compliance

**Use this when** rolling Platform Portability Discipline across the existing SOP library — after the separation method is proven on the pilot (/blog-posting-guidelines) and before the next platform change forces emergency rewrites.

## Inputs
- An inventory of all current SOPs and process documents
- The two-layer standard from Process 4 and the separation skill (`separate-methodology-layer-what-why-from-implementation-layer-how`)
- Results of the pilot review of Blog Posting Guidelines (the worked pattern)

## Steps
1. Build the SOP inventory: every process document the team actually runs — content factory steps, audit checklists, campaign SOPs, this maintenance system's own processes. An SOP not on the list is an SOP that never gets reviewed.
2. For each SOP, run the tool-dependence scan: strike out every named tool, menu path, and screenshot, and ask whether the remaining document still teaches the method. Note where logic collapses without the tool references.
3. Grade each SOP: **compliant** — layers already separated and labeled; **mixed** — separable with moderate edits; **entangled** — methodology and tooling so interwoven a rewrite is needed.
4. For mixed SOPs, apply the separation skill directly and ship the edits through the SOP Update Protocol.
5. For entangled SOPs, queue a full restructure as an SOP Amendment Proposal with priority based on how exposed the SOP is to platform churn (ad platforms and editors churn fastest).
6. Record the grade and review date per SOP alongside the inventory, and recheck grades during quarterly audits — compliance is a state that decays, not a one-time stamp.
7. Close the loop for new documents: add a portability check to the SOP authoring checklist so nothing newly published starts life entangled (file the amendment to that checklist).

## Definition of done (QA checklist)
- [ ] Complete SOP inventory built — no actively-used process document missing
- [ ] Every SOP graded compliant / mixed / entangled with the failing sections noted
- [ ] All mixed SOPs restructured or in the amendment queue; all entangled SOPs queued with churn-based priority
- [ ] Grades and review dates recorded; recheck wired into the quarterly audit
- [ ] Authoring checklist updated so new SOPs must pass portability before publishing
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — Process 4 mandates reviewing existing SOPs for compliance, naming Blog Posting Guidelines as the worked starting point.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first library-wide review and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) builds the complete SOP inventory, runs the tool-dependence scan on every document, grades each compliant / mixed / entangled, and loops until the Definition of done fully passes — every mixed SOP restructured or queued, every entangled one queued with churn-based priority, the authoring checklist updated.
It self-verifies by re-running the strike-out test on its own grades: delete the tool references and confirm the document still teaches (or provably fails to teach) the method as graded.
Memory across audit cycles treats compliance as the decaying state it is: the agent retains every SOP's grade and review date, rechecks them each quarter, and catches regressions the cycle they happen — an SOP sliding from compliant to mixed is a remembered trend, not a surprise at the next platform change.
Each run it logs a meta-article example via the Meta-Article Prompt, so the library-wide review compounds on the pilot's worked pattern.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related (Process 4 run order): conduct-first-portability-review-of-blog-posting-guidelines (pilot) → review-existing-sops-for-portability-compliance → apply-portability-discipline-to-meta-articles; method: separate-methodology-layer-what-why-from-implementation-layer-how. Concept: /blog-posting-guidelines.
