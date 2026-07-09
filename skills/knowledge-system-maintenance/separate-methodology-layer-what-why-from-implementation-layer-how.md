---
name: separate-methodology-layer-what-why-from-implementation-layer-how
description: Split a process document into a tool-agnostic methodology layer (what/why) and a platform-specific implementation layer (how) so platform churn never invalidates the method.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: needs-work
---

# Separate methodology layer (what/why) from implementation layer (how)

**Use this when** writing or restructuring any process document — and whenever a tool change (new editor, dead plugin, renamed platform feature) threatens to invalidate a whole SOP instead of one section.

## Inputs
- The process document to restructure
- Knowledge of which parts are principle and which are this year's tooling
- The portability standard from /knowledge-system-maintenance (Process 4)

## Steps
1. Read the document and classify every step, sentence, and screenshot into one of two layers: **methodology** — what we do and why, true regardless of tool; **implementation** — how we currently do it, naming specific tools, menus, buttons, prices, and UI paths.
2. Restructure into clearly labeled layers: methodology first as the spine of the document, implementation second (or as marked tool-specific sub-blocks under each methodology step).
3. Rewrite mixed sentences so the principle survives a tool swap. "Transcribe the video and correct every error" is methodology; "open Descript and click each blue-underlined word" is implementation. Both belong in the doc — in different layers.
4. Sweep all tool names, screenshots, UI paths, keyboard shortcuts, and pricing into the implementation layer only. A tool name inside the methodology layer is a defect.
5. Run the portability test: mentally delete the implementation layer. The methodology that remains must still be executable by a competent operator using any equivalent tool. If it is not, the methodology layer is incomplete — fix the method description, don't lean on the screenshots.
6. Add a maintenance note to the document: when platforms change, only the implementation layer should need editing. If a platform change forces methodology edits, the separation was done wrong — redo steps 1–5.
7. Ship the restructure through the SOP Update Protocol (amendment proposal, weekly review, version increment, changelog) — restructuring an SOP is an SOP change.

## Definition of done (QA checklist)
- [ ] Every element of the document classified and placed; layers explicitly labeled
- [ ] Zero tool names, UI paths, or screenshots remaining in the methodology layer
- [ ] Portability test passed: methodology alone is executable with any equivalent tool
- [ ] Maintenance note added; restructure shipped via approved SOP Amendment Proposal with version + changelog
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — Process 4 defines the two-layer discipline; /blog-posting-guidelines is the designated pilot document (see conduct-first-portability-review-of-blog-posting-guidelines).
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first full restructure and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) classifies every sentence, step, and screenshot into methodology or implementation and loops until the Definition of done fully passes — zero tool names left in the methodology layer and the restructure shipped through the SOP Update Protocol with version and changelog.
It self-verifies by running the portability test mechanically: strip the implementation layer and confirm the remaining method is still executable by a competent operator on any equivalent tool.
Memory across cycles is where the separation pays off: the agent remembers exactly which tools, UI paths, and prices it swept into each document's implementation layer, so when a platform changes it knows precisely which blocks to refresh — and a platform change that forces methodology edits is remembered as proof the separation failed and must be redone.
Each run it logs a meta-article example via the Meta-Article Prompt, so each restructure teaches the next one.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related (Process 4 run order): separate-methodology-layer-what-why-from-implementation-layer-how → review-existing-sops-for-portability-compliance → apply-portability-discipline-to-meta-articles; pilot: conduct-first-portability-review-of-blog-posting-guidelines.
