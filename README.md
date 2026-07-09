# BlitzMetrics Task Library

Hub-and-spoke skill library. This repo is the **hub**: the registry, the dashboard, and the default home for skill files. Skills can also live in their owner's own repo (the **spokes**) — the build pulls them in at build time.

## Layout

```
skills/<category-folder>/<slug>.md   skill files that live in this repo ("local")
build/registry.json                  slug -> source; THE index of the library
build/categories.json                the 13 categories (order, icons, colors)
build/site-meta.json                 bundle URL, meta-article URL, updated label
build/build.py                       resolve -> validate -> compose dashboard/data.json
dashboard/                           index.html + app.js + generated data.json
Task-Library-Standard.md             the spec every skill.md must meet
.github/workflows/build.yml          CI: build + deploy to GitHub Pages
```

> **Bringing your own skill repo?** See [CONTRIBUTING-SKILLS.md](CONTRIBUTING-SKILLS.md) — the full guide to formatting and registering an external skill (spoiler: if it's a normal Claude skill, it already qualifies).

## Owning a skill in your own repo

1. Put your `SKILL.md` (Task-Library-Standard format, frontmatter `name` = the slug) in your repo.
2. Change your skill's entry in `build/registry.json`:

```json
"google-ads-maa-report": {
  "source": "github:danielgoodrich/google-ads-analyzer@main:SKILL.md",
  "category": "Strategy & Measurement"
}
```

3. That one-line PR is the last time you touch this repo. Push to *your* repo; the daily build (or any manual run) picks it up.

Pin to a commit SHA instead of `@main` to freeze a version. Fetch failures fall back to the last good cached copy, so a deleted repo never blanks the dashboard. Private repos need `SKILLS_READ_TOKEN` set in Actions secrets.

## Validation

`build/build.py` rejects skills that: lack frontmatter or any required field, have `name` ≠ slug, use an unknown category/stage/status, or miss required sections (Inputs, Steps, Definition of done, Examples, Definitive article & links). It warns (build passes) on: stub language in a `complete` skill, <3 numbered steps, frontmatter/registry category mismatch.

## Asset Tracker

The Asset Tracker's *Task Library* tab stays the ops-facing index (status, owner, flags). Publish it to web as CSV and set `TRACKER_CSV_URL` repo variable — the build then overrides `status`/`owner`/`article` per slug from the sheet. Content always comes from git; workflow state comes from the sheet.

The sheet is also the **onboarding path**: a row whose Slug isn't in the registry but has a Source Repo link becomes a new external skill on the next build — no PR to this repo needed. See CONTRIBUTING-SKILLS.md.

## SEO

The dashboard itself is `noindex` (it's a utility, not the ranking surface — and it must never compete with the hub articles from a github.io origin). The build also emits **`dashboard/library-index.html`**: a plain semantic HTML fragment — category H2s, every task with its description, links to the definitive articles. Paste it into the WordPress task-library page *below* the iframe (or template it in) so blitzmetrics.com serves an indexable representation of the library with internal links to the hubs. Refresh the paste when categories/articles change materially; the fragment is deterministic, so a diff shows when.

## Local build

```
python3 build/build.py          # writes dashboard/data.json + library-index.html, exit 1 on validation errors
```
