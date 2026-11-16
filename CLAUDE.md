# Agentic Robotics website

Static, single-page research article for the Agentic Robotics project (UC Berkeley AUTOLAB + NVIDIA).
No build step: `index.html`, `css/style.css`, and media in `assets/`. Served by GitHub Pages from the
`gh-pages` branch, which `deploy.yml` fills from `main`. Every PR gets a preview at
`https://berkeleyautomation.github.io/agentic-robotics/pr-preview/pr-N/`.

## Rules for edits

- **Edit only what was asked.** Don't reword, reorder, reformat, or "improve" anything else. No drive-by
  refactors, renamed classes, or whitespace churn. Keep diffs as small as possible.
- **Keep the existing look.** It reads as a Distill-style research article, not a product page:
  880px serif text column, IBM Plex Sans for headings/captions/figures, numbered sections, numbered
  figures and tables, bracketed citations like `[7]`, single light theme.
- Use the CSS custom properties in `:root` of `css/style.css` (`--ink`, `--accent`, `--gold`, `--serif`,
  `--sans`, etc.). Don't add new colors, fonts, frameworks, or JavaScript libraries unless asked.
- Reuse existing classes and markup patterns (look at a neighboring section/figure first) rather than
  inventing new ones. New styles go in `css/style.css`, not inline, except the existing positional
  `style="left:..;top:.."` on hero tags.
- Keep section numbering, figure numbering, nav links (`#s1`…), and reference numbers consistent. If you
  add or remove a citation, section, or figure, renumber everything that refers to it.
- Don't change author names, affiliations, citations, or scientific claims unless explicitly asked.
- Media: add videos as `.mp4` with a matching `.jpg` poster in the same folder, and keep files small (the
  whole site is a few MB). Videos stay `muted autoplay loop playsinline`. Every image/video needs alt text
  or an `aria-label`.
- Use relative paths (`assets/...`, `css/...`) so PR previews under `/pr-preview/pr-N/` work.
- It must still work at phone width with no horizontal scroll.
- Don't touch `.github/workflows/` or this file unless asked.

## Workflow

- Work on a branch and open a PR. Never push directly to `main`; merging to `main` publishes the live site.
- In the PR description, list what changed and link the preview URL.
