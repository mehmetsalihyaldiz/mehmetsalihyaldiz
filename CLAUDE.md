# CLAUDE.md

Guidance for AI assistants (Claude Code and others) working in this repository.

## What this repository is

This is a **GitHub special profile repository**. Because the repository name
(`mehmetsalihyaldiz`) matches the owner's GitHub username, the contents of
`README.md` are rendered on the user's GitHub profile page at
`https://github.com/mehmetsalihyaldiz`.

This is **not** an application. There is no source code, build system, package
manager, test suite, or CI pipeline. The "product" is the rendered Markdown of
the profile page itself.

## Repository structure

```
.
├── README.md      # The profile page content (rendered on github.com/mehmetsalihyaldiz)
└── download.svg   # LinkedIn brand icon (SVG), kept as a local asset
```

That is the entire repository. Keep it minimal — do not add tooling,
dependencies, or scaffolding unless the user explicitly asks for it.

## Content conventions

The README is the only meaningful file. When editing it, preserve these
existing conventions:

- **Language:** Body copy and section headings are written in **Turkish**
  (e.g. `## Teknolojiler`, `## İletişim`, `## Şu an üzerinde çalıştıklarım`).
  Keep new prose in Turkish unless the user asks otherwise. Technology names
  (TypeScript, Docker, etc.) stay in their original form.
- **Layout:** The header block is centered using `<div align="center">`. The
  GitHub stats block is also centered. Sections are separated by `---`
  horizontal rules.
- **Badges:** Technology and metadata badges use
  [shields.io](https://shields.io). Two badge styles are in use:
  - `style=for-the-badge` with the GitHub-dark palette
    (`labelColor=0d1117`) for the header info chips (location, status, focus).
  - `style=flat-square` with each technology's brand color and logo for the
    tech-stack and contact sections.
  Match the surrounding style when adding a badge rather than mixing styles
  within a section.
- **Stats widgets:** GitHub stats use
  `github-readme-stats.vercel.app` with `theme=github_dark` and
  `hide_border=true`. The `username` parameter must remain
  `mehmetsalihyaldiz`.
- **Tone:** The profile presents Mehmet Salih Yaldız as a Full Stack
  Developer (Konya, Türkiye). Recent commit history shows a deliberate move
  toward a **clean, professional layout** — earlier flashy animations and
  excess badges were intentionally removed. Favor restraint; do not
  reintroduce animated GIFs, typing SVGs, or decorative clutter unless asked.

## Development workflow

There is nothing to build or run. To preview changes, render the Markdown
(any Markdown previewer, or push to a branch and view it on GitHub). Badge and
stats images load from external services, so a network connection is needed to
see them.

### Git conventions

- The default branch is `main`.
- Profile updates are typically small, single-purpose commits. Use clear,
  descriptive messages in the imperative mood (the history mixes
  `Update README.md` with more descriptive messages like
  `Revamp profile README with a clean, professional layout` — prefer the
  descriptive style).
- Do not create a pull request unless the user explicitly asks for one.

## Things to watch out for

- **Username consistency:** The username `mehmetsalihyaldiz` appears in badge
  links, stats widget URLs, and contact links. If it ever changes, update
  every occurrence — and note that renaming the repo would break the special
  profile-page behavior.
- **External dependencies:** All images (shields.io badges, stats widgets) are
  fetched from third-party services at render time. There are no pinned
  versions; a service outage shows broken images on the live profile.
- **`download.svg`** is an unused-in-README LinkedIn glyph kept as an asset.
  Leave it unless asked to remove or wire it in.
