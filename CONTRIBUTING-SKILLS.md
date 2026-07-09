# Listing Your Skill Repo in the Task Library

How to format a GitHub repo so your skill shows up on the Task Library dashboard with a working "download everything" link — while you keep full ownership of the code in your own repo.

The short version: **you don't reformat your skill, you register it.** If your repo is a normal Claude skill or plugin, it already qualifies. The library just needs to know where your SKILL.md lives and where people download the full package.

---

## What your repo needs (the checklist)

1. **A public GitHub repo** (private works too, but requires the library's read token — ask the maintainer).
2. **One folder per skill** containing a `SKILL.md`, with any supporting files in `references/` next to it. This is the standard Claude skill layout:

```
your-repo/
├── skills/
│   ├── your-main-skill/
│   │   ├── SKILL.md
│   │   └── references/
│   └── your-helper-skill/
│       ├── SKILL.md
│       └── references/
├── README.md
└── (optional) .claude-plugin/ files if you also ship it as a plugin
```

3. **SKILL.md frontmatter with `name` and `description`.** That's all the library reads from the file:

```markdown
---
name: your-main-skill
description: One clear first sentence saying what the skill does and for whom.
  Trigger phrases and details can follow — only the first sentence shows
  on the dashboard card.
---
```

The first sentence of your description becomes your dashboard card text. Write it for a human deciding whether to click.

4. **A download URL that serves the whole package.** You get one for free — every GitHub repo has a permanent archive link:

```
https://github.com/<you>/<your-repo>/archive/refs/heads/main.zip
```

Better: cut a **Release** (GitHub → Releases → "Draft a new release", attach a zip or let it auto-package). Then use:

```
https://github.com/<you>/<your-repo>/releases/latest/download/<your-asset>.zip
```

The difference matters: `main.zip` is whatever your repo looks like right now, mid-edit and all. A release is a version you deliberately shipped. The library convention is *releases for anything marked ready*.

---

## Registering it — the easy way (no repo access needed)

Add a row to the **Task Library tab of the Asset Tracker sheet**. Fill in:

| Column | What to put |
|---|---|
| Slug | your skill's name (must match `name` in your SKILL.md frontmatter) |
| Category | one of the 13 library categories |
| Status | `ready`, `wip`, or `gap` |
| Owner | you |
| Source Repo | your repo URL — `https://github.com/you/your-repo` |
| Download URL | optional; defaults to your repo's zip archive |

That's it. The build assumes your SKILL.md is at `skills/<slug>/SKILL.md` in your repo. If it lives elsewhere, paste the deeper link instead — a folder link (`.../tree/main/path/to/skill-folder`) or a direct file link (`.../blob/main/path/to/SKILL.md`) both work. The next build (daily, or on request) fetches, validates, and publishes your skill. Errors show in the build log with your slug on them.

Registering a suite: one row per skill, same Source Repo on each.

## Registering it — the registry way (for pinning and local skills)

The sheet path tracks your `main` branch. If you want to pin a specific commit, use a release download asset, or add a skill that lives *in* the central repo, add an entry to `build/registry.json` instead:

```json
"your-main-skill": {
  "source": "github:<you>/<your-repo>@main:skills/your-main-skill/SKILL.md",
  "format": "claude-skill",
  "category": "Strategy & Measurement",
  "status": "needs-work",
  "article": "/your-definitive-article",
  "download": "https://github.com/<you>/<your-repo>/releases/latest/download/<asset>.zip",
  "flag": "optional note reviewers should see"
}
```

Field by field:

- **source** — where the build fetches your SKILL.md. `@main` tracks your latest; pin a commit SHA (`@a1b2c3d`) to freeze a version.
- **format: "claude-skill"** — tells the validator this is a standard Claude skill (name + description frontmatter only). Without this, the file is validated against the full Task-Library-Standard format instead.
- **category** — one of the 13 library categories. Required.
- **status** — `complete`, `needs-work`, or `gap`. Defaults to `needs-work`; `complete` should mean you, the owner, stand behind it. The Asset Tracker sheet can override this later without touching the registry.
- **article** — your skill's definitive article (short URL like `/dad`, or omit if it doesn't exist yet — that's your gap to close).
- **download** — the full-package link described above. This renders as "Download full skill suite ⬇" on your dashboard card.

**Multi-skill suites** (a quarterback that dispatches helpers): register each skill as its own entry, all pointing at the same repo and the **same download URL**. Whichever piece someone finds, the download gives them the complete system. Worked example: the `google-ads-analyzer` entry in the registry.

---

## What happens after you register

The build robot runs daily (and on every change to the central repo). Each run it:

1. Fetches your SKILL.md from your repo.
2. Validates it: frontmatter has `name` + `description`, and your registry entry has a valid category/status. Failures are reported in the build log and the skill keeps its last good version — a broken push to your repo never blanks the dashboard.
3. Publishes it to the dashboard: your description's first sentence on the card, your full SKILL.md in the detail view, your download link on both.

From then on, updating your skill = pushing to your own repo. You never touch the central repo again unless you're changing your registry entry (new category, new download URL, status change).

## Ownership expectations

Registering a skill makes you its **owner** in the Asset Tracker sense: your name goes in the Owner column, you keep the skill current with how the task is actually done, you close its definitive-article gap, and status `complete` is your signature. The registry's git history is the provenance trail — commits to your repo are your LDT/CCS documentation happening automatically.

## Common rejections

The build log will tell you, but these are the usual ones: missing or empty `name`/`description` in frontmatter; frontmatter `name` doesn't match the registry slug (warning — registry wins); registry entry missing `category` or using a status/stage outside the allowed values; the source path 404s (typo in the path, renamed folder, or the repo went private without a token).
