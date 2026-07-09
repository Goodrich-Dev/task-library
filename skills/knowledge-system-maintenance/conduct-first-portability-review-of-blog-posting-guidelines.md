---
name: conduct-first-portability-review-of-blog-posting-guidelines
description: Run the pilot portability review on the Blog Posting Guidelines — separate its methodology from its tool-specific steps and document the worked pattern for every other SOP.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: gap
---

# Conduct first portability review of Blog Posting Guidelines

**Use this when** implementing Platform Portability Discipline — this Implementation Checklist task is a gap: /blog-posting-guidelines is the designated pilot, and no SOP has yet been through the separation.

## Inputs
- /blog-posting-guidelines — the full numbered process (Steps 1–17, from video upload through final QA)
- The two-layer method (`separate-methodology-layer-what-why-from-implementation-layer-how`)
- The SOP Amendment Proposal pipeline (the restructure ships through it)

## Steps
1. Open /blog-posting-guidelines and walk every numbered step (1–17), classifying each instruction as **methodology** (what/why: "transcribe the video and correct every error," "add internal links following the entity-linking decision tree") or **implementation** (how: Descript and its blue-underlined words, Grammarly/ChatGPT proofing, RankMath scores, LinkWhisper suggestions, WordPress block editor specifics).
2. Note why this article is the pilot: it is dense with named tools, so it stress-tests the discipline — if separation works here, it works anywhere.
3. Restructure each step so the methodology line leads and the tool-specific execution sits beneath it as a clearly labeled implementation block. Delete nothing — the tool detail is what makes the SOP runnable today; it just must be swappable tomorrow.
4. Run the portability test: with all implementation blocks removed, Steps 1–17 must still describe a complete, executable content process on any equivalent toolchain. Patch methodology gaps the test exposes.
5. Ship the restructure through the SOP Update Protocol: amendment proposal(s) within the 500-word format (split by section if needed), weekly senior review, version increment, changelog entry.
6. Document the worked pattern — classification calls that were hard, formatting choices, time taken — as the pilot playbook for `review-existing-sops-for-portability-compliance` to apply across the rest of the library.
7. Capture lessons as Knowledge Capture Notes within 24 hours of finishing; the pilot's purpose is to teach the system, not just fix one article.

## Definition of done (QA checklist)
- [ ] All numbered steps of /blog-posting-guidelines classified with zero unlabeled mixed instructions remaining
- [ ] Portability test passed: methodology layer alone still teaches the full process; no tool detail deleted, only layered
- [ ] Restructure approved via SOP Amendment Proposal(s) with version increment and changelog
- [ ] Pilot playbook documented and handed to the library-wide compliance review
- [ ] Lessons filed as Knowledge Capture Notes within 24 hours
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — the Implementation Checklist names Blog Posting Guidelines as the portability pilot; /blog-posting-guidelines is the document under review.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the pilot ships and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) walks all numbered steps of /blog-posting-guidelines, classifies every instruction as methodology or implementation, restructures so the method leads and the tool detail sits beneath it clearly labeled, and loops until the Definition of done fully passes — zero unlabeled mixed instructions, nothing deleted, the restructure shipped through the SOP Update Protocol.
It self-verifies by running the portability test: with every implementation block removed, Steps 1–17 must still describe a complete, executable content process on any equivalent toolchain, and the agent patches the methodology gaps the test exposes.
Memory is how the pilot teaches the system: the agent retains the worked pattern — the hard classification calls, the formatting choices, the time taken — and carries it directly into the library-wide compliance review, so every subsequent SOP inherits the pilot's lessons instead of rediscovering them.
Each run it logs a meta-article example via the Meta-Article Prompt and files the lessons as Knowledge Capture Notes within 24 hours, exactly as the skill demands of humans.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related (Process 4): separate-methodology-layer-what-why-from-implementation-layer-how (method) → conduct-first-portability-review-of-blog-posting-guidelines (pilot) → review-existing-sops-for-portability-compliance → apply-portability-discipline-to-meta-articles. Concept: /blog-posting-guidelines.
