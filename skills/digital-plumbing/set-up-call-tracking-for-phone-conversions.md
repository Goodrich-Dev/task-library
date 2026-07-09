---
name: set-up-call-tracking-for-phone-conversions
description: Implement call tracking with dynamic number insertion so phone calls — often the real conversion for local businesses — get measured without breaking NAP.
category: Digital Plumbing
stage: —
definitive_article: /digital-plumbing
status: needs-work
---

# Set Up Call Tracking for Phone Conversions

**Use this when** phone calls are a primary way this business wins customers and nobody can say how many calls the website or campaigns generate.

## Inputs
- Confirmation from the owner that calls are a primary conversion (GCT Goals — if calls don't matter, skip this task)
- Canonical NAP phone number and the line calls should forward to
- A call tracking platform with dynamic number insertion (DNI), plus GTM access for events

## Steps
1. Confirm the business case: if calls are a primary conversion method, track them; if not, stop here and rely on form tracking.
2. Provision a tracking number (local area code) in the call tracking platform, forwarding to the real business line. Test the forward with a live call before going further.
3. Use dynamic number insertion on the website: the DNI script swaps the displayed number (and tel: links) per visitor/source while the underlying canonical number stays the business's own. Never paste raw tracking numbers into GBP, citations, or schema — that breaks NAP consistency.
4. Install the DNI script via GTM on all pages and verify the swap happens on desktop and mobile, including the tel: links.
5. Wire measurement: send call events into GA4 (key event) and, if running ads, to the Meta pixel — calls from Dollar a Day traffic must be attributable.
6. Configure sensible call handling: business-hours routing, voicemail fallback, and recording only as permitted by local consent law.
7. Place a test call from the website number end-to-end: phone rings, call logs in the platform, event lands in GA4. Document numbers and routing in the client record.

## Definition of done (QA checklist)
- [ ] Test call via the website's displayed number rings through to the real line and logs in the platform
- [ ] DNI swaps displayed numbers and tel: links; canonical NAP number untouched on GBP, citations, schema
- [ ] Call event appears in GA4 as a key event (and in Meta Events Manager if ads run)
- [ ] Routing, hours, and consent-compliant recording settings documented
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A max-effort agent (Claude Fable 5 or a comparable OpenAI/Google model) tests the whole chain — DNI swap on desktop and mobile, live call forwarding, platform log, GA4 key event — and loops on any broken link until every Definition-of-done item passes, not 90%.
It self-verifies against that checklist that the canonical NAP number stayed untouched on GBP, citations, and schema — pulling that canon from memory of prior runs — and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /digital-plumbing
- Related (run order): add-click-to-call-links-for-mobile → install-meta-pixel-with-standard-events → this
- Cross-links: ensure-nap-consistency-across-platforms (protect NAP while tracking) · /maa (calls are Metrics) · /dad (attribute calls to $1/day ad sets)
