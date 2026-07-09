---
name: verify-ga4-configured-with-internal-traffic-filtered
description: Confirms the GA4 property is correctly installed and excludes the owner's and team's own visits, so audit and campaign data reflect real visitors only.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Verify GA4 configured with internal traffic filtered

**Use this when** running Layer 1 (Digital Plumbing Checks) of the Website QA Audit — owner and VA visits inflate every metric if they aren't filtered out.

## Inputs
- GA4 admin access for the property tied to the site
- The site URL and the office/home IP addresses of the owner and team (whatismyip lookup)
- Google Tag Assistant to confirm the GA4 tag fires
- The audit report/spreadsheet for logging results

## Steps
1. In GA4 Admin → Data Streams, confirm exactly one web stream exists for the live domain and the Measurement ID matches what fires on the site (check with Tag Assistant).
2. In Admin → Data Settings → Data Filters, open the Internal Traffic filter and confirm its state is **Active** — not Testing or inactive.
3. In Admin → Data Streams → Configure Tag Settings → Define Internal Traffic, confirm the rule lists the owner's and team's current IP addresses.
4. Test it: browse the site from an internal IP, then check GA4 Realtime — the visit must NOT appear (or appears only with the internal traffic_type while the filter is in Testing).
5. Browse from an external connection (phone on cellular) and confirm that visit DOES appear in Realtime.
6. Log filter state, IPs covered, and both test outcomes in the audit report.

## Definition of done (QA checklist)
- [ ] GA4 tag fires site-wide with the correct Measurement ID for one (and only one) web stream
- [ ] Internal Traffic data filter is Active and covers all known internal IPs
- [ ] Internal test visit excluded and external test visit recorded in Realtime, evidence logged and linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
Run on Claude Fable 5 (or a comparable OpenAI/Google long-horizon model), this check covers every sitemap URL rather than one page per template: the agent confirms the Measurement ID fires on each page, then re-runs the internal/external Realtime test after any filter or IP change, looping until all three Definition-of-done boxes hold at once.
Memory keeps the verified page list and the last-confirmed IP set, so subsequent runs only retest new pages and changed IPs — and the check re-opens automatically whenever the team's IPs change.
Each run ends by logging a real example under ## Example(s), compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /digital-plumbing (GA4 setup if this check fails) · previous: verify-gtm-installed-and-firing-on-every-page · next check: verify-meta-pixel-installed-with-lead-events
