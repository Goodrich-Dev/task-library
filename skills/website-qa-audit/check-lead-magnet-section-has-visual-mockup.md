---
name: check-lead-magnet-section-has-visual-mockup
description: Confirms the lead magnet offer is shown with a visual mockup or preview image, because an offer people can see converts better than a text link.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Check lead magnet section has visual mockup

**Use this when** running Layer 2 (Content Architecture Checks) of the Website QA Audit — a lead magnet with no visual looks like nothing is actually being given away.

## Inputs
- Site URL and the location of the lead magnet offer(s) (homepage section, popup, blog sidebar)
- The actual lead magnet file (to confirm the mockup honestly represents it)
- The audit report/spreadsheet for logging results

## Steps
1. Locate every place the lead magnet is offered on the site.
2. Confirm each placement includes a visual representation: a cover mockup, device-screen preview, or first-page screenshot — not just a headline and button.
3. Open the actual lead magnet and verify the mockup matches it — same title, same content; a mockup of a different or hypothetical asset fails.
4. Check the mockup's rendering quality: sharp at the displayed size on desktop and mobile, not stretched or pixelated.
5. Confirm the visual sits adjacent to the opt-in form/CTA so the offer and the action are one unit.
6. Log each placement, its visual, and verdict in the audit report.

## Definition of done (QA checklist)
- [ ] Every lead magnet placement includes a visual mockup or preview that accurately represents the real asset
- [ ] Mockup renders cleanly on desktop and mobile next to its opt-in CTA
- [ ] Placement verdicts logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
Run on a persistent agent (Claude Fable 5 or comparable OpenAI/Google models), every lead magnet placement on the site gets checked each run — homepage section, popups, sidebars — confirming a sharp, accurate mockup sits beside the opt-in on desktop and mobile, looping until all placements pass.
Memory pairs each placement with the asset version it represents, so a re-run flags drift the moment the lead magnet is updated but the mockup isn't.
Each run logs one worked example to ## Example(s), compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: sibling check: verify-email-opt-in-form-exists-and-works (the form behind this visual) · next check: verify-at-least-one-video-embed-on-homepage
