---
name: verify-wordpress-author-set-to-site-owner-name
description: Confirms every post is attributed to the site owner's author account — not admin, VA, or agency logins — so authorship signals accrue to the person's entity.
category: Website QA Audit
stage: —
definitive_article: /website-qa-audit
status: complete
---

# Verify WordPress author set to site owner name

**Use this when** running Layer 2 (Content Architecture Checks) of the Website QA Audit — bylines like "admin" leak that a VA runs the site and waste E-E-A-T signals.

## Inputs
- WordPress admin access (Posts list and Users screen)
- The owner's correct display name as it should appear publicly
- The audit report/spreadsheet for logging results

## Steps
1. In WordPress → Users, confirm an author account exists for the owner with the correct display name, a real bio, and a real profile photo.
2. In Posts → All Posts, add the Author column view and scan every post; flag any authored by "admin", a VA, an agency account, or a misspelled variant.
3. Spot-check the live site: open several posts and confirm the visible byline and author archive page show the owner's name.
4. Cross-check via the REST API (`/wp-json/wp/v2/posts?_fields=author,title`) for a complete machine-readable pass if the post count is large.
5. Reassign any flagged posts to the owner's account using Quick Edit (or bulk edit for many).
6. Log the count of posts checked and reassigned in the audit report.

## Definition of done (QA checklist)
- [ ] 100% of published posts attributed to the owner's author account — zero "admin"/VA bylines
- [ ] Owner's author profile has correct display name, bio, and photo, and the author archive renders
- [ ] Counts logged in the audit report, linked back to /website-qa-audit

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
Run on a persistent agent (Fable 5 or comparable OpenAI/Google models), this check is fully mechanical: pull every post via the REST API, flag any author that isn't the owner's account, reassign, and re-pull until the API returns zero non-owner bylines across all published posts — no sampling.
Memory stores the last-checked post count and verdicts, so each re-run only inspects posts published or edited since, and catches a VA login quietly taking over new bylines.
Each run logs one worked example to ## Example(s) so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /website-qa-audit
- Related: /blog-posting-guidelines · previous: verify-all-pages-written-in-first-person · next check: check-seo-title-under-60-chars-with-focus-keyword
