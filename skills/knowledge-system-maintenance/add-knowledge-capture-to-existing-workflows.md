---
name: add-knowledge-capture-to-existing-workflows
description: Embed an explicit Knowledge Capture step inside the Zoom call, campaign review, and audit workflows so insights are captured by process, not by memory.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: gap
---

# Add Knowledge Capture to existing workflows

**Use this when** standing up the Knowledge Capture Pipeline — this task is a gap: the capture step is not yet built into any workflow, which is why insights currently survive only when someone remembers.

## Inputs
- The three insight-producing workflows named by the hub: client Zoom calls, campaign data reviews, and audits (quarterly article audits, website QA audits)
- The Knowledge Capture Note template (see `provide-knowledge-capture-note-template`)
- Edit access to those workflows' checklists/SOPs, plus the SOP Amendment Proposal process

## Steps
1. Map where each workflow ends: the post-Zoom wrap-up, the campaign review's MAA action step, the audit close-out. The capture step belongs at the natural end, while context is hot and before the team disperses.
2. Add the explicit step to each: **Zoom calls** — "Any reusable insight from this call? Generate a Knowledge Capture Note within 24 hours" in the post-call checklist; **campaign reviews** — capture step right after metrics analysis, where surprises surface; **audits** — capture step in the audit wrap-up, feeding findings beyond the audited article itself.
3. Embed the note template (or a one-click link to it) at each capture point — if the capturer has to hunt for the template, the 24-hour window loses an hour to friction.
4. Make the changes legitimately: editing these workflows is itself an SOP change, so file the SOP Amendment Proposal(s) and let weekly review approve with version increment and changelog. The pipeline obeys its own protocol.
5. Verify with one live run of each workflow: confirm the capture step fires, a note gets written within 24 hours, and it lands in the shared capture location.
6. Monitor for 2–4 weeks: if a workflow produces zero notes, the step is in the wrong place or phrased as optional — move it or sharpen it, and amend again.

## Definition of done (QA checklist)
- [ ] All three named workflows (Zoom, campaign reviews, audits) contain an explicit capture step with the template linked at the point of use
- [ ] Workflow edits shipped via approved SOP Amendment Proposals with version increments and changelog entries
- [ ] One live run per workflow produced a real, on-template note within 24 hours
- [ ] 2–4 week adoption check scheduled; silent workflows get the step repositioned
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — Process 3 requires integrating note generation into Zoom, campaign data, and audit workflows. Gap: not yet integrated — the first run is the example.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the integration ships and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) embeds the capture step at the natural end of all three named workflows, ships the edits through the SOP Update Protocol, and loops until the Definition of done fully passes — including one verified live run per workflow producing a real, on-template note within 24 hours.
It self-verifies by watching the live runs rather than trusting the checklist edit: the step either fired and produced a note, or it goes back for repositioning.
Memory across cycles is what makes the 2–4 week adoption check real instead of aspirational: a long-horizon agent actually returns on schedule, remembers which workflows produced zero notes, and keeps repositioning the step until insights flow by process — the integration is monitored into existence, not declared.
Each run it logs a meta-article example via the Meta-Article Prompt, so the integration pattern transfers to every future workflow.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related: provide-knowledge-capture-note-template and create-knowledge-capture-note-template-and-distribute (template first), then generate-knowledge-capture-note-within-24-hours → route-notes-to-sop-update-protocol-or-directly-to-articles; changes ship via create-sop-amendment-proposal-500-words.
