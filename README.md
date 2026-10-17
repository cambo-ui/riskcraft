# RiskCraft

A personal blog about **IT risk management** — a practical, zero-to-hero path from
risk vocabulary to running an enterprise GRC programme.

Static [Hugo](https://gohugo.io/) site deployed on [Vercel](https://vercel.com/).
Push to `main` and Vercel builds and deploys automatically.

> **Tagline:** *From risk fundamentals to enterprise GRC.*

## Information architecture

Two organising axes plus a learning path.

```
Learning path (the `level` field, 0–5)
  0 Ground Zero   → risk vocabulary
  1 Foundations   → lifecycle, register, appetite
  2 Practitioner  → assessment & treatment
  3 Specialist    → frameworks & compliance
  4 Enterprise    → governance & GRC at scale
  5 Hero          → culture, metrics, leadership

Topics (the `categories` taxonomy) — 10 domains
  Foundations · Risk Assessment · Frameworks & Standards · Treatment & Controls
  Governance & Oversight · Third-Party Risk · Cloud & Cyber Risk
  Compliance & Audit · Metrics & Reporting · Culture & Career

Tags (the `tags` taxonomy) — free-form keywords
```

### Pages

| URL | File | Purpose |
| --- | --- | --- |
| `/` | `layouts/index.html` + `content/_index.md` | Hero, path preview, topic grid, latest posts |
| `/start-here/` | `content/start-here.md` | How to use the blog, what to read first |
| `/learning-path/` | `content/learning-path.md` (`layout: learning-path`) | The full zero→hero roadmap |
| `/categories/` | `content/categories/_index.md` | Browse by topic |
| `/categories/<topic>/` | `content/categories/<topic>/_index.md` | Topic landing + posts |
| `/tags/` | auto-generated | Browse by tag |
| `/resources/` | `content/resources.md` | Glossary, framework cheat sheet, templates |
| `/about/` | `content/about.md` | Bio — **edit this** |
| `/archive/` | `content/archive.md` (`layout: archive`) | All posts by year |
| `/index.xml` | auto-generated | RSS |

### Layout of the project

```
content/posts/        Markdown posts
content/categories/   One _index.md per topic (title + description)
data/learning_path.yaml  Drives the learning path (levels, outcomes, planned posts)
data/topics.yaml      Drives the topic grid (names + descriptions)
layouts/              Custom templates (no theme)
static/css/style.css  Styling
scripts/              new-post.sh, publish.sh
archetypes/           Front-matter templates for new posts
.pages.yml            Pages CMS (browser editing) config
hugo.toml             Site config, menus, taxonomies
vercel.json           Vercel build settings
```

## Writing a post

Every post sets two coordinates plus a spot on the path:

```yaml
---
title: "My post"
date: 2026-10-20
description: "One-line summary for previews and SEO."
categories: ["Risk Assessment"]   # one or more topic domains
tags: ["fair", "scoring"]          # free-form keywords
level: 2                           # 0–5, positions it on the learning path
weight: 10                         # order within the level
---
```

If a category is new, add it to `data/topics.yaml` and create
`content/categories/<slug>/_index.md` so it gets a landing page.

## Local preview

```sh
hugo server -D     # http://localhost:1313
```

## Publish from the command line

```sh
printf '# Hello\n\nBody here.\n' | ./scripts/new-post.sh \
  --title "My Post" --tags "fair,scoring" --description "Short summary"

./scripts/publish.sh -m "Fix typo"   # commit + push pending edits
```

## Publish from a browser (Pages CMS)

`.pages.yml` provides a WordPress-like editor at <https://app.pagescms.org>.
Sign in with GitHub, open the repo, and you get title, date, draft, description,
**level** and **topic** dropdowns, tags, and a rich-text body. Saving commits to
`main`, which triggers a Vercel rebuild.

## Deploy (one-time)

1. Create an empty GitHub repo (no README/.gitignore).
2. `git remote add origin git@github.com:USER/REPO.git && git push -u origin main`
3. In Vercel: **Add New → Project → Import** the repo. The **Hugo** preset is
   detected; build/output come from `vercel.json`.
4. Set `baseURL` in `hugo.toml` to the live URL and commit.

## Editing the learning path

`data/learning_path.yaml` is the single source of truth for the roadmap: level
names, taglines, outcomes, and the **planned** posts shown as "coming soon". A
post joins a level by setting `level: <id>`; it then appears under that level
automatically. Edit the YAML to reshape the curriculum — no template changes.

See [CONTENT-PLAN.md](CONTENT-PLAN.md) for the full editorial roadmap.
