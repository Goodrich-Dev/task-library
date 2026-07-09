---
name: provide-knowledge-capture-note-template
description: Author the canonical Knowledge Capture Note template — source, insight in 1–3 sentences, destination, priority — so capturing an insight takes two minutes, not a decision.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: gap
---

# Provide Knowledge Capture Note template

**Use this when** building the Knowledge Capture Pipeline — this task is a gap: no template exists yet, so every note currently invents its own format and the router pays the price.

## Inputs
- The four required fields specified by /knowledge-system-maintenance: source, insight (1–3 sentences), destination, priority
- One real captured insight to use as the filled example
- The shared capture location where the template will live

## Steps
1. Create the template with exactly the four fields the hub specifies — no more: **Source** (where the insight came from: call/campaign/audit, with date and who); **Insight** (1–3 sentences stating what is newly known); **Destination** (which definitive article or SOP it belongs in); **Priority** (how urgently it should be routed).
2. Add one line of guidance under each field — e.g., under Insight: "State the lesson, not the story. If it takes more than 3 sentences, it is two notes."
3. Include one filled example using a real captured insight, so users copy a pattern instead of interpreting instructions.
4. Keep the whole template under one page. Every added field is friction, and friction is why knowledge dies in people's heads instead of reaching the library.
5. Store the template at the shared capture location and link it from /knowledge-system-maintenance so it is findable from the hub.
6. Hand distribution to `create-knowledge-capture-note-template-and-distribute` (the implementation milestone) and embedding to `add-knowledge-capture-to-existing-workflows`.
7. After the first weeks of real notes, check fit: if capturers keep abusing a field or adding the same extra info, the template is wrong — revise it through an SOP Amendment Proposal, not a quiet edit.

## Definition of done (QA checklist)
- [ ] Template contains exactly the four specified fields with one-line guidance each
- [ ] One filled, realistic example included; total length under one page
- [ ] Stored in the shared capture location and linked from the hub
- [ ] First real notes audited for fit; revisions routed through the SOP Update Protocol
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — Process 3 specifies this template (source, insight in 1–3 sentences, destination, priority level). Gap: template not yet created — the first run produces the artifact.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the template's first real use and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) authors the template with exactly the four specified fields, one line of guidance each, and a filled real example, and loops until the Definition of done fully passes — under one page, stored in the shared capture location, linked from the hub.
It self-verifies by filling the template itself with a genuine captured insight as the acceptance test: if the agent cannot complete a correct note in two minutes, neither can the team.
Memory across cycles closes the fit loop: the agent watches the real notes that follow, remembers which fields get abused or what extra information capturers keep adding, and converts recurring misuse into one versioned revision via SOP Amendment Proposal — the template improves from remembered evidence, never from quiet edits.
Each run it logs a meta-article example via the Meta-Article Prompt, so the template's evolution is itself documented.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related: provide-knowledge-capture-note-template → create-knowledge-capture-note-template-and-distribute → add-knowledge-capture-to-existing-workflows → generate-knowledge-capture-note-within-24-hours → route-notes-to-sop-update-protocol-or-directly-to-articles.
