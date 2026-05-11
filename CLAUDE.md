# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

Keep `AGENTS.md` and `CLAUDE.md` synchronized for project conventions, commands, deployment notes, and content rules.

## Project type

**Development** — Jekyll / Just the Docs static documentation site deployed through GitHub Pages.

The UBC Graduate Student Society (GSS) uses this site as a practical reference for executives and staff. The current content focuses on the Financial Officer (FO) role, its recurring responsibilities, systems, governance work, and transition tasks.

## Working rules

- Run commands from the repo root.
- Edit Markdown source files, `_config.yml`, images, and workflow files directly; do not edit `_site/`, which is generated output.
- Preserve existing Just the Docs front matter conventions: `layout`, `title`, `nav_order`, `parent`, `has_children`, and `permalink`.
- Prefer existing page structure and terminology over introducing new navigation patterns.
- Do not store credentials, account numbers, passwords, private access links, or other sensitive operational details in the guide.
- Verify policy-sensitive content against current GSS source documents or flag it as needing confirmation.
- Do not revert unrelated local changes.
- After any major change, explicitly suggest the git sync flow: `git add`, `git commit`, `git pull --rebase`, `git push`.

## Git workflow

Before changing tracked files:
- Run `git status --short --branch`.
- Verify `origin` points to `https://github.com/ubcgss/executives_staff_guide.git`.
- Run `git fetch`, then make sure the local branch is not behind `origin/main`.
- If the working tree is otherwise clean, fast-forward with `git pull --ff-only` before editing.
- If unrelated tracked changes are already present, do not mix them into the task; stop and ask how to proceed. Untracked files that are clearly unrelated can be left alone.

Every substantive implementation plan must include the relevant git sync steps: pre-work fetch/pull checks, post-work validation, commit, push, and PR steps when a review flow is needed.

Use a short feature branch for substantive structure, workflow, dependency, or deployment changes. Lightweight documentation edits, typo fixes, and small housekeeping changes can be made on the current branch unless the user asks for a branch. Still report the remaining `git status` and suggest the exact files to commit.

Hard stops:
- Do not use `git push --force`.
- Do not push directly to `main` unless the user explicitly asks.
- Do not merge PRs or delete branches without explicit user approval.
- Do not use destructive git commands such as `git reset --hard` or `git checkout --` unless explicitly approved.

## Commands

**Install dependencies:**
```bash
bundle install
```

**Serve locally with live reload:**
```bash
bundle exec jekyll serve
```

**Build to `_site/`:**
```bash
bundle exec jekyll build
```

The local dev server runs at `http://localhost:4000/executives_staff_guide/`. The `_site/` directory is the build output; do not edit files there directly.

## Site structure

```
index.md                    # Home page (layout: home)
docs/
  01-introduction/index.md  # FO role overview
  02-regular-tasks/         # biweekly.md, monthly.md, quarterly.md, annual.md
  03-systems/               # zoho.md, banking.md, investment.md
  04-governance/            # council-reporting.md, hfc.md, budget-process.md
  05-transition/            # accounts-access.md, files-records.md, checklist.md
_config.yml                 # Jekyll + Just the Docs config
```

## Front matter conventions

Every page requires front matter. Section index pages use `has_children: true` and a `permalink`; leaf pages use `parent:` to nest under the section:

```yaml
---
layout: default
title: Banking
nav_order: 2
parent: Systems
permalink: /docs/03-systems/banking/
---
```

The `nav_order` within a section controls sidebar ordering. `nav_sort: case_insensitive` is set globally.

## Content standards

- Write for GSS officers and staff who need procedural clarity.
- Keep pages task-oriented: responsibilities, deadlines, systems, contacts, and verification steps.
- Use Just the Docs callouts for cautions or policy-verification notes.
- Avoid embedding sensitive operational details such as credentials, exact banking identifiers, private staff-only links, or personal contact details.
- When referencing another GSS guide, use the live GitHub Pages URL unless a local relative link is clearly intended.

## Callouts and Mermaid

Just the Docs callouts are configured for `note` (blue) and `warning` (yellow):

```markdown
{: .note }
Text here.

{: .warning }
Text here.
```

Mermaid diagrams (version 10) are enabled via `_config.yml`.

## Deployment

Pushing to `main` triggers the GitHub Actions workflow (`.github/workflows/pages.yml`), which builds and deploys automatically. No manual deploy step is needed. After deployment-related changes, verify that the workflow completes and the live site responds at `https://ubcgss.github.io/executives_staff_guide`.

## Completion criteria

For content-only edits:
- Check front matter, sidebar ordering, internal links, and image paths.
- Run `bundle exec jekyll build` when navigation, config, links, or includes change.

For config, dependency, or deployment workflow edits:
- Run `bundle exec jekyll build`.
- Report changed files, validation run, and any known gaps.
