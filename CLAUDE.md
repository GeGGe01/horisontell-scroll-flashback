# CLAUDE.md

Status: active

Guidance for Claude Code (claude.ai/code) when working in this repository.

## Repository purpose

A static page that recreates the Flashback forum post "Pi-dagen idag!"
(sp95149773). It shows a device toggle (mobile/desktop web) and several
modes demonstrating how forum code boxes behave with long, horizontally
overflowing code. No build step.

## Structure

```
index.html      Entry point — markup + the component logic (x-dc template)
support.js       Runtime that index.html loads; renders the x-dc component
assets/          Images referenced relatively (avatar-thecrash.jpg)
README.md        Index / overview (Status line + < 40 lines)
LICENSE          CC0 1.0 Universal
.editorconfig    Shared editor settings (LF, UTF-8, 2-space indent)
```

## How it renders

`index.html` holds an `<x-dc>` template plus a `<script type="text/x-dc">`
component (a `DCLogic` subclass). `support.js` boots that component. The
runtime pulls React, ReactDOM and Babel from the unpkg CDN at load time, so
rendering needs network access — this is not a self-contained offline bundle.

## Conventions

- **kebab-case filenames**, descriptive nouns, no dates in names.
- Every Markdown doc opens with an h1 followed by a `Status:` line
  (`draft | active | superseded | archived`).
- Index files are named canonically (`README.md`, web entry point `index.html`).

## Working on the page

- Edit markup/logic directly in `index.html` (the visible `<title>`, the
  `<x-dc>` markup, and the `Component` class with `CODE1`/`CODE2`).
- `support.js` is generated runtime ("do not edit" header) — leave it as is.
- Verify with `npx serve .` (or any static server) and open `/index.html`.

## Operator context

Solo operator, EU/Sweden (GDPR applies). Preference order: operational
simplicity → least-privilege security → conventions → low recurring cost.
