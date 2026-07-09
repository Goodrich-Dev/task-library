---
name: generate-knowledge-capture-note-within-24-hours
description: Capture any reusable insight as a four-field Knowledge Capture Note (source, insight, destination, priority) within 24 hours, before context decays and the lesson is lost.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: needs-work
---

# Generate Knowledge Capture Note within 24 hours

**Use this when** a reusable insight surfaces anywhere in real work — a client Zoom call, campaign results, an audit finding, a support thread — anything that should eventually change a definitive article or an SOP.

## Inputs
- The triggering moment (call recording/notes, campaign data, audit finding)
- The Knowledge Capture Note template (see `provide-knowledge-capture-note-template`)
- The team's shared capture location

## Steps
1. Recognize the trigger: you just learned something that is true beyond this one client, campaign, or run. If a teammate would repeat your mistake or miss your shortcut without it, it qualifies.
2. Start the 24-hour clock from the moment of insight. The deadline exists because fidelity decays — a note written next week records what you think you learned, not what you learned.
3. Write the note using the template's four fields, nothing more: **Source** — where/when/who (call, campaign, audit, with date); **Insight** — 1 to 3 sentences stating what is newly known; **Destination** — the definitive article or SOP this belongs in; **Priority** — how urgently it should land.
4. Keep the insight tight: 1–3 sentences of what changed in your understanding, not a meeting summary or a transcript excerpt.
5. If the destination is unclear, name the closest definitive article hub and flag it for the router — an imperfect destination beats an unrouted orphan.
6. File the note in the shared capture location and hand off to routing (`route-notes-to-sop-update-protocol-or-directly-to-articles`).
7. If you blow the 24-hour window, still write the note — and log the miss, because repeated misses mean the capture step is missing from a workflow (`add-knowledge-capture-to-existing-workflows`).

## Definition of done (QA checklist)
- [ ] Note created within 24 hours of the insight (or the miss explicitly logged)
- [ ] All four fields present: source with date, 1–3 sentence insight, named destination article/SOP, priority
- [ ] Insight is a claim about what is newly known — not a summary, not raw notes
- [ ] Filed in the shared capture location and visible to the router
- [ ] Repeated capture misses escalated as workflow-integration fixes, not guilt
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — Process 3 defines the 24-hour Knowledge Capture Note with exactly these fields as the entry point of the capture pipeline.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first batch of real notes and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) never blows the 24-hour window, because holding the clock is what persistent means: it drafts the four-field note the moment a reusable insight surfaces in a call transcript, campaign data, or audit finding, and loops until the Definition of done fully passes — source dated, insight stated in 1–3 sentences as a claim, destination named, priority set, note filed.
It self-verifies by checking the insight is genuinely a claim about what is newly known (not a summary) and that the named destination article or SOP actually exists.
Memory across cycles is this pipeline's whole reason to run on an agent: every prior note is retained, so duplicate insights merge instead of piling up, and the second occurrence of the same failure automatically arms the SOP Amendment path — the system literally remembering what it has learned.
Each run it logs a meta-article example via the Meta-Article Prompt, so captured insights compound into documented practice.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related (Process 3 run order): generate-knowledge-capture-note-within-24-hours → route-notes-to-sop-update-protocol-or-directly-to-articles; infrastructure: provide-knowledge-capture-note-template, add-knowledge-capture-to-existing-workflows. Sources flow from /content-factory work, audits, and campaigns.
