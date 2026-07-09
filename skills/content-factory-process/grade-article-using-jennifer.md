---
name: grade-article-using-jennifer
description: Run a finished article through the Jennifer grading system for a quality score and fix what it flags before the piece moves to the Post stage.
category: Content Factory — Process
stage: Process
definitive_article: GAP — to be written
status: gap
---

# Grade article using Jennifer

**Use this when** an article has cleared proofreading (Step 11) and you want an objective quality score before WordPress posting.

> **Gap notice:** this task has no definitive article and the Jennifer rubric/threshold is not yet documented in the library. The steps below are the provisional process from the task definition; the FIRST real run must be documented with the Meta-Article Prompt so the rubric, scoring scale, and pass threshold get written down.

## Inputs
- The finished article draft (post-Step 11, pre-posting)
- Access to the Jennifer grading system
- The article's GCT statement and transcript (so fixes never drift from the source material)
- The Content Library tracker

## Steps
1. Submit the complete article — title, meta, body, image alt text — to Jennifer for grading.
2. Record the returned score and the full rubric feedback verbatim in the tracker row; the score is a Metric in the MAA loop, not a verdict to skim.
3. Triage every flagged issue: fix it, or document explicitly why it stands (e.g., the "issue" is the speaker's authentic phrasing, which the guidelines protect).
4. Make fixes against the source of truth — adjustments must stay faithful to the transcript and the GCT statement; never "fix" an article by inventing content the video does not support.
5. Re-run the grade after fixes and record the new score. Iterate until flagged issues are resolved or consciously accepted with reasons.
6. Cross-check that Jennifer-driven edits did not break the hard specs: title <60, meta <160, keyword in first paragraph, links intact (these remain governed by /blog-posting-guidelines regardless of grade).
7. Attach the final score to the post record so RankMath score (70+), Jennifer score, and audit results travel together as the article's quality file.
8. Document the run via `write-meta-article-documenting-agent-work` — the first documented run defines the pass threshold and seeds the definitive article.

## Definition of done (QA checklist)
- [ ] Article graded; score and full feedback recorded verbatim in the tracker
- [ ] Every flagged issue fixed or explicitly accepted with a written reason
- [ ] Fixes verified against transcript and GCT (no invented content)
- [ ] Hard Blog Posting Guidelines specs still pass after edits
- [ ] Final score attached to the post record; first-run meta-article created
- [ ] Linked back to the definitive article and relevant siblings (hub pending)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. No documented Jennifer grading run exists in the library yet; the first one defines the rubric.

## Run on a persistent agent (Fable 5)

The grade-fix-regrade cycle is a loop by design, and a persistent agent (Claude Fable 5, or comparable OpenAI/Google models that loop and hold memory) runs it without fatigue: every flag fixed or explicitly accepted with a written reason, hard specs re-verified after each edit, iterating until the checklist closes — never stopping at a "good enough" score. Memory accumulates Jennifer's recurring findings across articles, so future drafts pre-empt the flags before submission. Log each run's meta-article — the first one defines the rubric for everyone after.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — to be written ("How to Grade an Article Using Jennifer" is on the Gaps & Tasks to Create list, low priority).
- Related: /blog-posting-guidelines (the standards Jennifer scores against), /website-qa-audit, /maa
- Sibling skills, in run order: `step-11-proofread-with-grammarly-or-chatgpt` → this → `step-12-post-article-on-wordpress` (Post stage)
