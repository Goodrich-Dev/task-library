---
name: apply-portability-discipline-to-meta-articles
description: Ensure meta-articles separate the transferable general approach from the platform-specific details of that particular run, so documented agent work stays useful after tools change.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: needs-work
---

# Apply portability discipline to meta-articles

**Use this when** writing or auditing meta-articles — the documented runs of real work created via /meta-article-prompt-template — so each one teaches a reusable method, not just a tour of one tool on one day.

## Inputs
- The meta-article(s) to review, or the run about to be documented
- The two-layer standard from Process 4 (methodology = what/why; implementation = how)
- The Meta-Article Prompt Template (/meta-article-prompt-template)

## Steps
1. Pull the meta-articles in scope: existing ones linked from definitive articles as examples, and any new one being written from a fresh run.
2. For each, check that it distinguishes the two layers: the **general approach** — what was done and why, the decisions and method any reader could transfer; and the **platform-specific execution** — the exact tools, versions, and steps used in this particular run.
3. Where the layers are blended, add explicit framing rather than deleting detail: a short "the approach" passage stating the transferable method, and a clearly marked "how we ran it this time" passage holding the tool specifics. Meta-articles need the specifics — they are the proof — but labeled as that run's implementation.
4. Run the reader test: someone on a different platform (different editor, ad manager, transcription tool) must still be able to extract and apply the method. If the method only makes sense inside the named tool, the methodology framing is missing.
5. For future runs, push the fix upstream: if the Meta-Article Prompt Template does not already ask for approach-vs-execution separation, propose that addition via an SOP Amendment Proposal so every future meta-article is born portable.
6. Record reviewed meta-articles and their fixes in the audit notes; recheck new meta-articles as part of the quarterly audit's example checks.

## Definition of done (QA checklist)
- [ ] Every in-scope meta-article has clearly framed approach (transferable) and execution (this run's tools) layers
- [ ] Reader test passed: the method is extractable by someone on a different platform
- [ ] No proof-level detail deleted — specifics retained but labeled as implementation
- [ ] Template-level fix proposed via SOP Amendment if the Meta-Article Prompt lacks the separation requirement
- [ ] Reviewed articles and fixes recorded for the quarterly audit trail
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /meta-article-prompt-template — the canonical meta-article system this discipline applies to; /knowledge-system-maintenance Process 4 extends portability to these documents explicitly.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first portability pass over a meta-article and link it here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) reviews every in-scope meta-article for the two layers — transferable approach versus this run's tooling — and loops until the Definition of done fully passes: layers explicitly framed, no proof-level detail deleted, reader test passed.
It self-verifies by masking the implementation passages and confirming the method still extracts cleanly for someone on a different platform.
This is the recursion folding back on itself: meta-articles are the agent's own logged runs, so memory across cycles means the agent audits the documentation of its own remembered work — and it pushes the approach-vs-execution requirement upstream into the Meta-Article Prompt Template once, via SOP Amendment Proposal, so every future run is born portable instead of being fixed after the fact.
Each run it logs a new meta-article example, which is itself immediately subject to this discipline — that is how the knowledge base compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related (Process 4 run order): separate-methodology-layer-what-why-from-implementation-layer-how → review-existing-sops-for-portability-compliance → apply-portability-discipline-to-meta-articles. Concepts: /meta-article-prompt-template, /blog-posting-guidelines.
