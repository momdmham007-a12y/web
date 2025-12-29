# Copilot / AI agent instructions for this repository

This repo is a minimal static site consisting of top-level HTML files. The guidance below is focused on being immediately practical when editing, testing, or extending this codebase.

**Big picture**
- **Repo type:** Static HTML pages (examples: `0001.html`, `0002.html`, `0003.html`) — there is no build tool, framework, or package manifest detected.
- **Primary flow:** Each top-level HTML file is a standalone page. Changes are verified by opening the file in a browser or serving the folder locally.

**How to run locally**
- **Quick view:** Open a file directly in Finder or browser, e.g. open `0001.html`.
- **Serve for multi-page testing:** Run `python3 -m http.server 8000` from the repo root and visit `http://localhost:8000/`.

**What to edit and conventions**
- **File naming:** Pages use numeric names (e.g. `0001.html`); keep numeric ordering when adding new pages to preserve intended sequence.
- **Assets:** There is no assets folder yet — add `assets/` or `static/` alongside the HTML files for images/CSS/JS and update HTML paths accordingly.
- **Encoding / language:** The repository root folder name contains non-ASCII characters; preserve UTF-8 filenames and avoid renaming files to ASCII-only unless required by tooling.

**Testing, CI, and workflows (discoverable state)**
- **No CI/config detected:** No `.github/workflows` or other CI manifests were found. Expect no automated tests or builds unless added.

**Patterns and examples**
- **Standalone pages:** Treat `0001.html` as a complete document — scripts and styles should be either inline or referenced via relative paths.
- **Additive changes:** When adding features, create an `assets/` subfolder and reference it from pages using relative paths like `assets/styles.css`.

**Suggestions for PRs and agent behaviors**
- **Small diffs:** Keep changes contained to a few files per PR because reviewers will likely inspect rendered HTML.
- **Include manual verification steps:** When modifying pages, include a short test note in the PR describing which URL (file) to open and what to verify.

**When you cannot discover something**
- If asked about build/test/CI commands and none are present, state: “No build or CI detected; serve via `python3 -m http.server` or open the HTML directly.”

If any of this is unclear or you'd like the file adapted for a different workflow (add a build step, introduce npm tooling, or add CI pipelines), tell me which direction to take and I will update this guidance.
