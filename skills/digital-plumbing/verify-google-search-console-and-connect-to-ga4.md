---
name: verify-google-search-console-and-connect-to-ga4
description: Verify Search Console ownership of the domain and link it to GA4 so search queries, impressions, and clicks flow into one measurement view.
category: Digital Plumbing
stage: —
definitive_article: /digital-plumbing
status: needs-work
---

# Verify Google Search Console and Connect to GA4

**Use this when** nobody can see what the site ranks for, GSC is unverified or stuck in an old webmaster's account, or GA4 shows no Search Console data.

## Inputs
- Business owner's Google account (property ownership stays with the client)
- DNS access at the registrar/DNS host (for domain verification — see verify-domain-ownership-and-registrar-access)
- GA4 property with Editor access (run set-up-ga4-with-internal-traffic-filtering first)

## Steps
1. In Search Console under the owner's Google account, add a Domain property for the root domain (covers http/https, www/non-www, and subdomains in one property).
2. Verify via the DNS TXT record GSC provides: add it at the DNS host, wait for propagation, click Verify.
3. Audit users: owner's account holds Owner; operators added as Full users; ex-webmasters and unknown accounts removed.
4. Submit the XML sitemap (from the sitemap skill) and confirm Success status.
5. Link to GA4: in GA4 Admin → Product links → Search Console links, connect the GSC property to the GA4 property and select the web data stream.
6. In GA4, confirm the Search Console reports appear (publish the Search Console collection from the Library if hidden) and queries begin flowing — allow up to 48 hours for first data.
7. Record the verification method and property details in the client record so access never gets lost again.

## Definition of done (QA checklist)
- [ ] Domain property verified in GSC via DNS TXT, owned by the client's account
- [ ] User list audited — no stale or unknown accounts with access
- [ ] Sitemap submitted with Success status
- [ ] GSC↔GA4 link live; Search Console reports visible in GA4 with query data (within 48h)
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
DNS propagation and the up-to-48-hour wait for first query data make this a long-horizon task: a persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) verifies, links, then returns to confirm data actually flows, looping until the entire Definition of done passes, not 90%.
It self-verifies each item — TXT live, users audited, GSC-GA4 link active — against that checklist, persists the verification method and property details in memory so access never gets lost between runs, and logs a meta-article example each run so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /digital-plumbing
- Related (run order): create-xml-sitemap-and-reference-in-robots-txt → set-up-ga4-with-internal-traffic-filtering → this
- Cross-links: /website-qa-audit · /maa (GSC impressions/clicks are core Metrics) · /seo-tree (rankings prove the tree is working)
