---
name: verify-https-with-no-mixed-content
description: Confirms the entire site serves over HTTPS with zero mixed-content warnings, protecting visitor trust and preventing browser security flags.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Verify HTTPS with no mixed content

**Use this when** running Layer 1 (Digital Plumbing Checks) of the Website QA Audit — a broken padlock kills trust before a visitor reads a word.

## Inputs
- Site URL plus a full page list (XML sitemap or crawl export)
- Chrome with DevTools (Console and Security panels)
- The audit report/spreadsheet for logging results

## Steps
1. Load the homepage over `https://` and confirm the browser padlock shows with no warning state.
2. Request the `http://` version and the non-www/www variants; confirm each 301-redirects to the single canonical HTTPS URL (check the redirect chain in DevTools Network).
3. Open DevTools → Console and Security panel on the homepage; record any "mixed content" warnings (insecure images, scripts, stylesheets, or iframes loaded over http).
4. Repeat the DevTools check on one page of every template type plus any page embedding video, forms, or third-party widgets — the usual mixed-content offenders.
5. For each warning, note the exact insecure resource URL so the fix is a find-and-replace, not a hunt.
6. Log pass/fail per page with the list of insecure resources in the audit report.

## Definition of done (QA checklist)
- [ ] Every checked page loads over HTTPS with a clean padlock — zero mixed-content warnings in DevTools
- [ ] http, www, and non-www variants all 301-redirect to one canonical HTTPS version
- [ ] Findings logged with exact offending resource URLs, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
Instead of one page per template, a persistent Fable 5 agent (or comparable OpenAI/Google model) fetches every sitemap URL and scans each response for insecure `http://` resource references, looping through fix-and-recheck cycles until zero mixed-content warnings remain site-wide and every variant 301s to canonical HTTPS in one hop.
It self-verifies by re-fetching every previously flagged page, and memory tracks which URLs already pass so each re-run only covers failures and new pages.
One worked example gets logged to ## Example(s) per run, compounding the library.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /digital-plumbing (HTTPS configuration if this check fails) · previous: verify-meta-pixel-installed-with-lead-events · next check: test-mobile-load-time-under-3-seconds
