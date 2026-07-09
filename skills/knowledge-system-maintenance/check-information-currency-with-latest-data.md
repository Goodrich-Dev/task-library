---
name: check-information-currency-with-latest-data
description: Refresh a definitive article's facts, numbers, and tool steps against the latest GBP, Ahrefs, client Zoom, and campaign data so the page never teaches stale reality.
category: Knowledge System Maintenance
stage: —
definitive_article: /knowledge-system-maintenance
status: needs-work
---

# Check information currency with latest data

**Use this when** running the quarterly audit's third check — the article is coherent and structurally complete, but its facts may have drifted since the last audit.

## Inputs
- The definitive article under audit, plus its last audit date
- Access to the four named data sources: Google Business Profile, Ahrefs, client Zoom call recordings/notes, and campaign results
- The audit notes for this article and quarter

## Steps
1. Inventory every claim in the article that can drift: metrics, dates, prices, screenshots, tool names, UI steps, rankings, and "currently" statements. List them with their location.
2. Pull the freshest data from each named source: GBP (listings, reviews, profile facts), Ahrefs (rankings, traffic, backlinks the article cites), client Zoom calls (what clients are actually experiencing now), and campaign results (what the method currently produces).
3. Compare each inventoried claim against current data and mark it current, stale, or wrong.
4. Update stale and wrong items in the article: refresh numbers, replace outdated screenshots, correct tool steps. Touch only the implementation facts — keep the methodology layer (what/why) intact per Platform Portability Discipline (Process 4).
5. If a Zoom call or campaign surfaced a reusable insight that belongs in the article but is not yet there, generate a Knowledge Capture Note within 24 hours and route it (Process 3) rather than improvising new content mid-audit.
6. If the *process the article teaches* has materially changed — not just its data — do not silently rewrite it: file an SOP Amendment Proposal (Process 2) so the change gets reviewed, versioned, and changelogged.
7. Record the data-refresh date and what changed in the audit notes; pass the result to the status-table update.

## Definition of done (QA checklist)
- [ ] Drift inventory built and every item dispositioned current / stale / wrong — none left unmarked
- [ ] All four data sources actually consulted (GBP, Ahrefs, client Zooms, campaign results), not just the convenient ones
- [ ] Every stale/wrong item updated in the article or ticketed with owner; methodology layer left intact
- [ ] New insights routed as Knowledge Capture Notes; process changes routed as SOP Amendment Proposals — no silent process edits
- [ ] Refresh date recorded for the status table
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- /knowledge-system-maintenance — Process 1 names GBP, Ahrefs, client Zoom calls, and campaign results as the currency sources for this exact check.
- Example needed — run the Meta-Article Prompt (/meta-article-prompt-template) after the first real quarterly run and link the meta-article here.

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) builds the full drift inventory, pulls fresh data from all four named sources (GBP, Ahrefs, client Zooms, campaign results) — not just the convenient ones — and loops until the Definition of done fully passes: every claim dispositioned current, stale, or wrong, and every stale item updated or ticketed.
It self-verifies by diffing the article before and after the refresh to confirm only implementation facts changed and the methodology layer survived untouched.
Memory across audit cycles is what makes this check compound: the agent carries last quarter's claim inventory and refresh dates forward, starts each audit from remembered state instead of re-discovering the page, and flags claims that go stale every single cycle as candidates to restructure rather than re-refresh.
Each run it logs a meta-article example via the Meta-Article Prompt, so the knowledge base records how the refresh was actually done.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /knowledge-system-maintenance
- Related (Process 1 run order): verify-structural-completeness-against-8-step-framework → check-information-currency-with-latest-data → validate-cross-reference-integrity-across-articles → update-status-table-in-definitive-article-guide; feeds: generate-knowledge-capture-note-within-24-hours, create-sop-amendment-proposal-500-words.
