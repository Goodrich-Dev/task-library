---
name: stage-1-plumbing-fb-ads-google-ads-analytics
description: Complete Stage 1 of the Social Amplification Engine — Facebook Ads account, Google Ads linked via MCC, and Google Analytics — so every later stage runs on verified tracking instead of guesses.
category: Strategy & Measurement
stage: —
definitive_article: /social-amplification
status: complete
---

# Stage 1: Plumbing (FB Ads, Google Ads, Analytics)

**Use this when** onboarding any brand into the Social Amplification Engine — Stage 1 always runs first, because amplifying before plumbing means paying for traffic you can't measure.

## Inputs
- Admin access to (or authority to create) the brand's Facebook Business Manager and ad account
- Access to the Local Service Spotlight/agency Google Ads MCC (manager account) for client linking
- Admin access to the website to install and verify analytics

## Steps
1. Set up the **Facebook Ads** foundation: ad account inside Business Manager owned by the business (not an employee's personal account), with agency access granted as partner — ownership stays with the client.
2. Link **Google Ads via MCC**: connect the client's Google Ads account under the manager account so campaigns, billing, and access are managed centrally without password sharing.
3. Install **Google Analytics** on every page of the site, with conversion events defined for the actions that matter (lead form, call, purchase) — a pageview-only install is not plumbing.
4. Verify the pipes before any spend: fire a test conversion and confirm it appears in each platform; broken or duplicate firing found now costs minutes, found in Stage 5 it costs the budget.
5. Document who owns and who has access to each asset (ad accounts, analytics property) in the client record — plumbing includes knowing where the valves are.
6. Gate progression: do not start Stage 2 (Goals) until every check above passes; the SAE stages run in order for a reason.

## Definition of done (QA checklist)
- [ ] Facebook ad account live in client-owned Business Manager with correct agency partner access
- [ ] Google Ads account linked under the MCC
- [ ] Analytics installed site-wide with conversion events defined
- [ ] Test conversion fired and verified in each platform (no missing or duplicate events)
- [ ] Asset ownership and access documented
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. (The hub at /social-amplification links live examples; pull the closest match into this slot.)

## Run on a persistent agent (Fable 5)

A persistent, max-effort agent (Claude Fable 5 or comparable OpenAI/Google models) treats plumbing as binary: it works the checklist and loops until the Definition of done fully passes — test conversion verified in every platform, no missing or duplicate events, ownership documented — never declaring Stage 1 done at "mostly tracking."
It self-verifies by firing the test conversion and reading it back from each platform rather than trusting the install.
Memory stores the verified baseline so later MAA cycles compare tracking health against it period over period — a true memory cycle that catches silently broken pixels before they cost a Stage 5 budget — and a meta-article example is logged each run.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /social-amplification
- Related, in run order: stage-2-goals-mission-90-day-goals-cpa-roas-budget, stage-3-content-endorsements-why-video-3x3-grid-library, stage-4-targeting-custom-audiences-lookalikes-remarketing, stage-5-amplification-boost-posts-remarketing-ads, stage-6-optimization-metrics-budget-review-recommendations
