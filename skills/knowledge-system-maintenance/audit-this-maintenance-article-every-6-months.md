---
name: audit-this-maintenance-article-every-6-months
description: Run the 6-month recursive audit of /knowledge-system-maintenance itself — test its five processes against six months of reality and amend, add, or retire them through their own protocol.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: needs-work
---

# Audit this maintenance article every 6 months

**Use this when** the scheduled 6-month recursive review arrives (see `schedule-first-6-month-recursive-review`) — the maintenance system must pass the same tests it imposes on everything else, or it has no authority to impose them.

## Inputs
- /knowledge-system-maintenance (the article under audit) and its version/changelog history
- Six months of operating evidence: status table audit dates, the SOP Amendment Proposal tracker, Knowledge Capture Note volume, portability review grades
- The pattern review output (`review-past-6-months-of-sop-amendment-proposals-for-patterns`)

## Steps
1. Run the full Process 1 audit on /knowledge-system-maintenance itself: topic coherence (SEO Tree test), structural completeness, information currency, and cross-reference integrity. The maintenance article gets no exemption from its own checks.
2. Test each of the five processes against six months of reality, not theory: Did quarterly audits actually run and stamp the status table? Did amendment proposals flow and get weekly review? Were Knowledge Capture Notes generated within 24 hours? Did portability reviews happen? Is this recursive cycle itself running on schedule?
3. Disposition every process explicitly: **keep** (working as written), **modify** (works but the article describes it wrong — or it needs adjustment), or **remove** (cost exceeds value). Silence is not a disposition.
4. Identify missing processes: recurring problems from the past six months that none of the five processes addresses are candidates for a new sixth process.
5. Ship every change to the article through its own Process 2: SOP Amendment Proposal(s), weekly senior review, version increment, changelog entry. The system editing itself outside its own protocol is the first sign of rot.
6. Update the article's row in the status table with this audit's date and status, and update the corresponding Task Library skills if any process changed — the skills must mirror the hub.
7. Before closing, schedule the next 6-month review with named reviewers. A recursive cycle that does not schedule its own next iteration has terminated.

## Definition of done (QA checklist)
- [ ] All four Process 1 checks run against /knowledge-system-maintenance with findings recorded
- [ ] Each of the five processes explicitly dispositioned keep/modify/remove with six months of evidence cited
- [ ] All article changes shipped via approved SOP Amendment Proposals with version increment and changelog
- [ ] Status table stamped; affected Task Library skills updated to mirror the revised hub
- [ ] Next 6-month review scheduled with named reviewers before this one closes
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — Process 5 defines this self-audit; the article is both the subject and the standard, which is the point of the recursive layer.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first 6-month review and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) is the natural owner of this skill, because the 6-month recursive audit is exactly what a long-horizon agent with memory is for: it runs all four Process 1 checks on /knowledge-system-maintenance itself, tests each of the five processes against six months of remembered evidence, and loops until the Definition of done fully passes — every process explicitly dispositioned keep / modify / remove, no silence.
It self-verifies by shipping every change through the article's own Process 2 and then confirming the version incremented, the changelog recorded it, and the affected Task Library skills were updated to mirror the revised hub — the system editing itself outside its own protocol is the exact failure this audit exists to prevent.
Memory across audit cycles is the entire point: the agent arrives with the status-table dates, amendment flow, capture volume, and portability grades already held from living through them, compares this cycle against the last one, and schedules the next review before closing — a recursive loop that cannot forget is a recursive loop that cannot quietly terminate.
Each run it logs a meta-article example via the Meta-Article Prompt, so the system's self-audits become part of the knowledge base they audit.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related (Process 5 run order): review-past-6-months-of-sop-amendment-proposals-for-patterns → audit-this-maintenance-article-every-6-months → schedule the next cycle (schedule-first-6-month-recursive-review for the inaugural one). Concept: /seo-tree.
