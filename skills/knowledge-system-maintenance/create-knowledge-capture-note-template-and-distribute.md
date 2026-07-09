---
name: create-knowledge-capture-note-template-and-distribute
description: Build the Knowledge Capture Note template and distribute it into the team's actual workflows, then confirm real notes start flowing — the implementation milestone for Process 3.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: gap
---

# Create Knowledge Capture Note template and distribute

**Use this when** implementing the maintenance system — this Implementation Checklist task is a gap: until the template exists *and* lives where work happens, the Knowledge Capture Pipeline is theory.

## Inputs
- The four-field template spec from Process 3 (see `provide-knowledge-capture-note-template`): source, insight in 1–3 sentences, destination, priority
- The shared capture location, plus the Zoom / campaign-review / audit workflow checklists
- The team roster (everyone who touches client calls, campaigns, or audits)

## Steps
1. Build the template per the spec — Source, Insight (1–3 sentences), Destination, Priority — with one line of guidance per field and one filled real example, all under one page (`provide-knowledge-capture-note-template` is the authoring SOP).
2. Place the template in the shared capture location as the canonical copy; every other reference links here, so updates propagate from one place.
3. Distribute it into the three named workflows: embed the template (or a direct link) at the capture step in Zoom post-call checklists, campaign data reviews, and audit wrap-ups (`add-knowledge-capture-to-existing-workflows` is the integration SOP).
4. Teach it once, live: walk the team through capturing one real insight end to end — Learn, Do, Teach — so the first note everyone sees is a correct one.
5. Confirm adoption within the first two weeks: real notes are arriving, they follow the template, and the 24-hour rule is holding. Adoption is the deliverable; an undistributed template is a gap with extra steps.
6. Collect friction (fields misused, info repeatedly added outside fields) and revise the template via SOP Amendment Proposal — not a silent edit — so the change is versioned and announced.

## Definition of done (QA checklist)
- [ ] Template live in the shared capture location: four fields, guidance lines, filled example, ≤1 page
- [ ] Embedded at the capture step of all three workflows (Zoom, campaign reviews, audits)
- [ ] Live walkthrough delivered; team knows where the template lives and when the 24-hour clock starts
- [ ] Two-week adoption check passed: real, on-template notes flowing — or the blockers identified and actioned
- [ ] Revisions routed through the SOP Update Protocol with version + changelog
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — the Implementation Checklist pairs template creation with distribution into team workflows. Gap: neither exists yet — running this skill closes both.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first weeks of real notes and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) builds the four-field template, places the canonical copy in the shared capture location, embeds it at the capture step of all three workflows, and loops until the Definition of done fully passes — where the deliverable is adoption: real, on-template notes flowing within two weeks, or the blockers identified and actioned.
It self-verifies by checking the notes themselves, not the distribution checklist — template compliance and the 24-hour rule measured on actual captures.
Memory across cycles makes the adoption check real: a long-horizon agent returns at the two-week mark without being reminded, compares note volume against the remembered baseline, tracks recurring field misuse, and ships exactly one versioned revision through the SOP Update Protocol when the evidence warrants it.
Each run it logs a meta-article example via the Meta-Article Prompt, so distribution lessons compound into the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related: provide-knowledge-capture-note-template (authoring spec) → create-knowledge-capture-note-template-and-distribute (milestone) → add-knowledge-capture-to-existing-workflows → generate-knowledge-capture-note-within-24-hours → route-notes-to-sop-update-protocol-or-directly-to-articles.
