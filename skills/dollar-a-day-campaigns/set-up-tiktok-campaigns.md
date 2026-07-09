---
name: set-up-tiktok-campaigns
description: Configure TikTok ads through the six-part Dollar a Day sequence — plumbing, goals, content, targeting, amplification, optimization — using native vertical video that already won.
category: Dollar a Day Campaigns
stage: Promote
definitive_article: /dad
status: needs-work
---

# Set up TikTok campaigns

**Use this when** the brand's buyers are on TikTok and you have raw, native-feeling vertical video with proven signal — the platform punishes anything that smells like an ad.

## Inputs
- TikTok Business account with admin owned by the business owner
- Proven native vertical videos (organic TikTok winners, or one-minute videos that won elsewhere)
- Target cost per result and budget envelope from GCT

## Steps
1. **Plumbing** — set up the TikTok Business account and install the TikTok pixel with events on the actions that matter; fire a test event before any spend.
2. **Goals** — write the GCT: goal level (views/engagement cold, leads warm), target cost per result, and the weekly budget envelope.
3. **Content** — use native vertical one-minute videos that already earned signal. Raw and unscripted outperforms produced; never upload content carrying another platform's watermark.
4. **Targeting** — layer location, age, interests/behaviors, and custom audiences (engagers, site traffic) into discrete ad groups, one variable apart, mirroring the standard audience grid.
5. **Amplification** — run minimum viable spend per ad group. TikTok enforces higher daily minimums than Meta's $1, so treat the platform minimum as your "dollar": smallest spend, many simultaneous tests, 7 days untouched.
6. **Optimization** — weekly MAA: cost per result, watch time, engagement per ad group; kill losers, scale winners ≤2× per adjustment, switch winning creative to new audience segments.
7. Feed TikTok winners back into the cross-platform library — a TikTok winner is a candidate for FB/IG and YouTube boosts, and vice versa.

## Definition of done (QA checklist)
- [ ] Pixel installed and verified with a test event; account owned by the business owner
- [ ] GCT documented; only proven, native, watermark-free vertical video promoted
- [ ] Ad groups layered one variable apart at the platform-minimum budget, 7 days untouched
- [ ] Weekly MAA running with kill/scale/switch verdicts logged; winners shared to the cross-platform library
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run (candidate: a local-service brand testing two native videos across three ad groups at platform-minimum spend).

## Run on a persistent agent (Fable 5)
Hand the six-part sequence to a persistent agent (Claude Fable 5 or comparable OpenAI/Google models) that loops until the Definition of done fully passes — pixel test event fired, GCT written, creative verified native and watermark-free, ad groups one variable apart, weekly MAA running; skipping the weekly kill/scale/switch verdicts is a failed run even when everything launched cleanly.
Memory carries the cross-platform library: the agent logs which TikTok winners traveled to Meta or YouTube and which did not, so each platform test builds on the last instead of starting cold.
Log every cycle as a meta-article example so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /dad
- Related: /one-minute-video-guide (native-format production) · /social-amplification (the six-stage engine this sequence mirrors)
- Run order (platform setup): create-youtube-campaigns-using-aducate-model → **set-up-tiktok-campaigns** → run-twitter-x-promotion-for-thought-leader-threads
