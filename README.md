# GSS Executives and Staff Guide

A GitHub Pages site providing a practical reference for executives and staff
of the Graduate Student Society of UBC Vancouver.

Live site: https://ubcgss.github.io/executives_staff_guide

Built with Jekyll and the [Just the Docs](https://just-the-docs.com) theme.

## Current Scope

The guide is organized around executive roles and shared facilities operations:

- President
- VP University & Academic Affairs
- VP External Relations
- VP Students
- Financial Officer
- Facilities

The Financial Officer section contains the detailed reference material from the
original FO-focused guide. The non-FO executive sections are source-aware
skeletons and should be expanded only with verified role documents. The
Facilities section provides the structure for spaces, active projects, contacts,
agreements, leases, and recurring obligations.

## Local Development

Run commands from the repository root.

```bash
bundle install
bundle exec jekyll serve
bundle exec jekyll build
```

The local dev server runs at:

```text
http://localhost:4000/executives_staff_guide/
```

## Content Rules

Edit Markdown source files, `_config.yml`, Sass, images, and workflow files
directly. Do not edit `_site/`, which is generated output.

Do not publish credentials, account numbers, private access links, personal
contact details, draft agreements, negotiation folders, or other sensitive
operational details. Facilities agreement links should point only to final or
executed documents approved for this guide.
