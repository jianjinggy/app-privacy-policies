# Repository Guidelines

## Project Structure & Module Organization

This repository is a static GitHub Pages site for privacy and support pages. `index.html` lists existing policies; new app pages do not need to be added there. Each app gets a directory whose name exactly matches its GitHub project name. Do not add, remove, translate, or reformat parts of the name; a date is included only when it is part of that GitHub name. Example: project `2026-08-13-ball-run-4` uses `2026-08-13-ball-run-4/`. Keep platform pages as sibling files:

```text
appstore-privacy-policy.html
googleplay-privacy-policy.html
```

Use only applicable files, keep platform names consistent, and do not nest pages. Each page is self-contained HTML with inline CSS; there is no source tree, asset pipeline, or generated output. Keep `.nojekyll` in place so GitHub Pages serves files directly.

## Build, Test, and Development Commands

There is no dependency install or production build. Preview the site locally with:

```sh
python3 -m http.server 8000
```

Open `http://localhost:8000/` to preview the site. Before committing, run `git diff --check` and check `git status --short`.

## Coding Style & Naming Conventions

Use valid HTML5 with two-space indentation, lowercase semantic elements, a UTF-8 charset, responsive viewport metadata, and an informative `<title>`. Keep page-specific styles in the existing inline `<style>` block unless a shared stylesheet is introduced deliberately. Use the exact GitHub project name for the app directory and the exact platform filenames above. Preserve existing public paths; links and canonical URLs must match the project directory and filename.

## Testing Guidelines

Testing is manual; no framework or coverage requirement is configured. For each changed page, check the local URL in desktop and narrow/mobile viewports, follow all navigation and external links, and verify that the app name, platform, contact address, effective date, and last-updated date are accurate. For privacy-content changes, confirm disclosures match the app’s actual ads, analytics, identifiers, purchases, permissions, and storage behavior.

## Commit & Pull Request Guidelines

Use a short imperative commit subject, such as `Add Ball Run 4 privacy policy` or `docs: update Apple privacy policy`. Pull requests should state the affected app/platform and public URLs, summarize content or layout changes, mention local verification, and include screenshots when visual presentation changes. Link a related issue when one exists.

## Security & Configuration Tips

Treat every HTML file as public. Do not commit passwords, API keys, private logs, or unpublished user data. Recheck third-party policy links and legal/privacy claims before publishing changes.
