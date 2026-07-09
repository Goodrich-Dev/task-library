---
name: build-personal-brand-website
description: Build the entity-home website on yourname.com that answers who this person is, what they do, and why to trust them.
category: Personal Branding
stage: —
definitive_article: /personal-brand
status: needs-work
---

# Build personal brand website

**Use this when** yourname.com is registered and the person needs their entity home — Phase 1 (Digital Plumbing) of the personal brand build.

## Inputs
- Registered personal name domain with hosting (WordPress preferred — agents can read and update it)
- Professional headshots and real photos (no stock, ever)
- Short and long bios in first person, plus proof assets: testimonials with names and headshots, media mentions, talks
- List of live social profile URLs

## Steps
1. Frame the build correctly: this is a facts page, not a sales page. Its one job is to answer — who is this person, what do they do, why should anyone trust them.
2. Put a real photo of the person in the hero and answer all three questions above the fold, in first person.
3. Build the core sections: About (story plus credentials with evidence, never bare claims), what they do and who they serve, and proof — testimonials with full attribution, media and speaking mentions, results.
4. Embed at least one video of the person (a one-minute video or WHY video) on the homepage.
5. Link every social profile from the site (header, footer, or About) so Person schema can close the entity loop in a later skill.
6. Run the Digital Plumbing basics before calling it live: HTTPS with no mixed content, sub-3-second mobile load, favicon set, indexing not blocked, working contact path.
7. Hand off to implement-person-schema-with-sameas-links to wire the entity together.

## Definition of done (QA checklist)
- [ ] Site live on yourname.com and answers who / what / why-trust without scrolling
- [ ] All copy first person; all images real; testimonials carry names, titles, headshots
- [ ] At least one video embedded; social profiles linked; contact path works
- [ ] Reads as a facts page — no hard-sell landing-page patterns
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Cam Hazzard — camhazzard.com: the entity-home model — a facts page that establishes who/what/why-trust and anchors every other profile.
- Harry Gold — harryjgold.com: a complete entity home produced from a single Zoom call, proof the build does not require months of asset production.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or a comparable OpenAI/Google model) builds the entity home in one long-horizon session: it pulls the canonical name and domain saved by the registration run from memory, drafts and publishes every section, and loops until the full Definition-of-done passes — who/what/why-trust above the fold, video embedded, contact path tested — not 90%.
It self-verifies by loading the live site as a stranger would and checking HTTPS, mobile load speed, and every link.
It stores the page inventory and proof assets in memory for the profile and Person-schema skills that follow, and logs a meta-article example each run so the brand compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /personal-brand
- Related: /digital-plumbing · /one-minute-video-guide · previous: register-personal-name-domain · next: set-up-professional-social-profiles → implement-person-schema-with-sameas-links
