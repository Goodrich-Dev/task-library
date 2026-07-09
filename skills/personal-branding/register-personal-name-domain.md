---
name: register-personal-name-domain
description: Secure yourname.com as the permanent entity anchor every other personal-brand asset points back to.
category: Personal Branding
stage: —
definitive_article: /personal-brand
status: needs-work
---

# Register personal name domain

**Use this when** starting Phase 1 (Digital Plumbing) of a personal brand build — before the website, profiles, or any content exist.

## Inputs
- The exact professional name the person will use everywhere (bylines, bios, headshots)
- A registrar account owned by the person (not an agency), with a payment method
- Acceptable fallbacks if the exact .com is taken (middle initial, full middle name)

## Steps
1. Lock the canonical name string first — this exact spelling becomes the entity name Google reconciles across the web, so decide it before buying anything.
2. Check availability of yourname.com; the exact-match .com is the strongest entity anchor.
3. If taken, fall back to a variant that is still the person's real name — middle initial or full middle name (the harryjgold.com pattern). Never substitute a slogan or keyword domain; the domain must BE the person.
4. Register the domain in an account the person owns and controls. Ownership of the anchor is non-negotiable — agencies and VAs get delegated access, not ownership.
5. Turn on auto-renew and WHOIS privacy; confirm the renewal date is years out, not months.
6. Document registrar URL, account email, and access in the person's credentials vault, then verify by logging in fresh.
7. Point DNS at the hosting where the entity home will be built (next skill), and reserve matching professional email on the domain.

## Definition of done (QA checklist)
- [ ] yourname.com (or real-name variant) registered, resolving, auto-renew on
- [ ] Registrar account owned by the person; credentials documented and verified by a fresh login
- [ ] Domain spelling exactly matches the canonical professional name used in bios and schema
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Harry Gold — harryjgold.com: exact-name anchor using the middle initial, the foundation an entire brand was built on from one Zoom call.
- Cam Hazzard — camhazzard.com: exact-name domain serving as the entity home everything else links back to.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) runs this as the opening Phase 1 move: lock the canonical name, walk the real-name fallback chain, and loop until every Definition-of-done box passes — registered, resolving, auto-renew on, fresh-login verified — not 90%.
It self-verifies by resolving the live domain and re-authenticating into the registrar before reporting done.
It writes the canonical name string, domain, and registrar record to memory as the anchor every later Plumbing → Content → Authority → Knowledge Panel skill builds on, and logs a meta-article example each run so the brand compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /personal-brand
- Related: /digital-plumbing · next: build-personal-brand-website → set-up-professional-social-profiles → implement-person-schema-with-sameas-links
