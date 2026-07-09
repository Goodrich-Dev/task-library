---
name: route-notes-to-sop-update-protocol-or-directly-to-articles
description: Move every Knowledge Capture Note to its correct destination — into the SOP Update Protocol when it changes how work is done, or directly into a definitive article when it adds facts.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: needs-work
---

# Route notes to SOP Update Protocol or directly to articles

**Use this when** Knowledge Capture Notes are sitting in the shared capture location — routing runs on a fixed cadence so notes become changes instead of a graveyard of good intentions.

## Inputs
- The shared capture location with unrouted Knowledge Capture Notes
- The SOP Amendment Proposal queue (Process 2) and edit access to definitive articles
- The entity map of which definitive article owns which concept

## Steps
1. Review all new notes at a fixed cadence (daily or each working session); high-priority notes jump the queue immediately.
2. Apply the routing test per note: **does this insight change how we do work?** Yes → it is an SOP/process change → route into the SOP Update Protocol. No, it adds a fact, example, number, or proof → route directly into the destination definitive article.
3. **SOP path:** draft (or request from the note's author) the ≤500-word SOP Amendment Proposal, citing the note's source as one real example — remember the protocol requires at least two, so pair it with a second occurrence or hold it tagged until one appears.
4. **Article path:** update the destination article directly — place the addition where it supports the declared topic (SEO Tree test), keep Blog Posting Guidelines compliance, and respect methodology/implementation separation (Process 4).
5. Verify the note's stated destination is actually correct before acting; the capturer guessed under a 24-hour clock. Re-route to the true owning hub if needed.
6. Mark each note routed: destination, action taken, date. No note remains unrouted past the next cycle — "parked" is a status with a reason, not a default.
7. If many notes pile up against one SOP or article, that is a pattern — feed it to the 6-month pattern review rather than processing them one by one forever.

## Definition of done (QA checklist)
- [ ] Every note in the location is routed, actioned, or parked-with-reason — none silently pending past one cycle
- [ ] SOP-path notes became (or joined) a four-part amendment proposal in the queue
- [ ] Article-path notes landed in the correct hub, passing the SEO Tree test and Blog Posting Guidelines
- [ ] Each note marked with destination, action, and date — auditable later
- [ ] Pile-up patterns flagged for the 6-month recursive review
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — Process 3 defines the two routes (SOP Update Protocol vs direct article update) as the only exits from the capture pipeline.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first routing cycle and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) runs the routing cadence without slipping — every cycle it takes all unrouted notes, applies the routing test (changes how we work → SOP path; adds a fact → article path), and loops until the Definition of done fully passes: zero notes silently pending, every one routed, actioned, or parked with a reason.
It self-verifies by re-checking each routed note's destination — the amendment proposal exists in the queue, or the article edit landed and passes the SEO Tree test.
Memory across cycles makes routing smarter every pass: the agent holds the entity map of which hub owns which concept plus every past routing decision and correction, so destinations guessed under the capturer's 24-hour clock get corrected consistently, and notes piling up against one SOP are counted as a remembered pattern for the 6-month review.
Each run it logs a meta-article example via the Meta-Article Prompt, so the routing discipline itself stays documented.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related (Process 3 run order): generate-knowledge-capture-note-within-24-hours → route-notes-to-sop-update-protocol-or-directly-to-articles → create-sop-amendment-proposal-500-words (SOP path). Concepts: /seo-tree, /blog-posting-guidelines.
