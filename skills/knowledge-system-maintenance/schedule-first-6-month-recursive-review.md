---
name: schedule-first-6-month-recursive-review
description: Put the first 6-month recursive review of the knowledge maintenance system on the calendar with named reviewers and a prep package, arming the self-improvement loop.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: gap
---

# Schedule first 6-month recursive review

**Use this when** the knowledge maintenance system goes live — this task is a gap: the first recursive review is not yet on any calendar, and an unscheduled recursive loop is a loop that never starts.

## Inputs
- The adoption date of the maintenance system (sets the 6-month mark)
- Team calendar and roster (a review lead plus a senior reviewer)
- Locations of the evidence sources: status table, SOP Amendment tracker, Knowledge Capture location

## Steps
1. Set the date six months out from the system's adoption. Pick a real date now and defend it — "in about six months" is how recursive reviews become annual, then never.
2. Name the reviewers: a review lead to run the cycle and a senior reviewer with authority to approve resulting amendments (the weekly SOP reviewer is the natural fit). Named people, not roles-to-be-determined.
3. Create the calendar event with the agenda baked in: run `review-past-6-months-of-sop-amendment-proposals-for-patterns` first, then `audit-this-maintenance-article-every-6-months`, then schedule the next cycle.
4. Attach the prep list to the invite so evidence is pulled before the session: current status table with audit dates, full amendment-tracker export, Knowledge Capture Note volume and routing stats, portability review grades.
5. Confirm both reviewers accepted and the date does not collide with a quarterly audit crunch — the recursive review needs attention, not leftovers.
6. Record in the hub's audit record that the cycle is armed: date, reviewers, agenda link. From here on, each review schedules its successor before closing — this skill only fires the first shot.

## Definition of done (QA checklist)
- [ ] A specific date ~6 months from adoption is on the team calendar, accepted by a named lead and a named senior reviewer
- [ ] Agenda embeds the two Process 5 skills in run order plus "schedule the next cycle"
- [ ] Prep list attached covering status table, amendment tracker, capture stats, and portability grades
- [ ] The armed cycle recorded in the hub's audit record (date, reviewers, agenda)
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — Process 5 requires putting the first recursive review on the calendar with assigned reviewers. Gap: not yet scheduled — running this skill closes the gap.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first review actually convenes and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) is the guarantee that "in about six months" never decays into never: it sets the real date, names the lead and senior reviewer, builds the agenda from the two Process 5 skills in run order, and loops until the Definition of done fully passes — invite accepted, prep list attached, the armed cycle recorded in the hub's audit record.
It self-verifies by confirming both reviewers actually accepted and the date avoids the quarterly audit crunch.
Memory across the six-month gap is the job itself: the agent holds the date, assembles the prep package continuously as evidence accrues (status-table dates, tracker exports, capture stats, portability grades), and fires the review on time — then enforces the standing rule that each review schedules its successor before closing, so the loop self-perpetuates.
Each run it logs a meta-article example via the Meta-Article Prompt, so even the scheduling step leaves compounding documentation.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related (Process 5 run order): schedule-first-6-month-recursive-review (arms the loop) → review-past-6-months-of-sop-amendment-proposals-for-patterns → audit-this-maintenance-article-every-6-months → next cycle self-schedules.
