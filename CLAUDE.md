# CLAUDE.md

Status: active

Guidance for Claude Code (claude.ai/code) when working in this repository.

## Repository purpose

A single, self-contained `index.html` that renders a Flashback-style forum
post about Pi-dagen ("Pi day"). The page demonstrates horizontal-scroll
behaviour in code boxes. No build system, no external dependencies — every
asset is embedded and unpacked in the browser at load time.

## Structure

```
index.html      The whole site — markup, styles, embedded base64 resources
README.md        Index / overview (Status line + < 40 lines)
LICENSE          CC0 1.0 Universal
.editorconfig    Shared editor settings (LF, UTF-8, 2-space indent)
```

## Conventions

- **kebab-case filenames**, descriptive nouns, no dates in names.
- Every Markdown doc opens with an h1 followed by a `Status:` line
  (`draft | active | superseded | archived`).
- Index files are named canonically (`README.md`, web entry point `index.html`).

## Working on the page

- `index.html` is a bundled artifact: a `__bundler/manifest` (base64 assets)
  plus a `__bundler/template` (the real HTML). Edit the visible `<title>` and
  outer shell directly; the post content lives inside the template JSON.
- Verify by opening the file in a browser, or `python3 -m http.server 8000`.

## Operator context

Solo operator, EU/Sweden (GDPR applies). Preference order: operational
simplicity → least-privilege security → conventions → low recurring cost.
