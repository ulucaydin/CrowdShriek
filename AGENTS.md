# Repository Guidelines

## Project Structure & Module Organization
- `crowdshriek-architecture.html` is the single source of truth, containing the HTML, inline `<style>`, and inline `<script>` for canvas rendering and interactivity.
- `design-pdf.pdf` is a reference export of the design; treat it as read-only unless explicitly updating the visual spec.
- There are no separate `src/`, `tests/`, or `assets/` directories in this repository.

## Build, Test, and Development Commands
There is no build system or package manager. To preview changes locally:
```sh
python3 -m http.server
```
Open `http://localhost:8000/crowdshriek-architecture.html` in a browser. You can also open the file directly if a local server is unnecessary.

## Coding Style & Naming Conventions
- Use 2-space indentation in HTML, CSS, and JS to match the existing formatting.
- CSS class names are kebab-case (e.g., `latency-panel`), JS functions and variables are camelCase (e.g., `switchView`), and shared constants are uppercase (e.g., `COLORS`, `DETAIL`).
- Keep color tokens in `:root` and the `COLORS` object in sync when adding or modifying hues.
- Preserve the existing section banner comments (`/* ─── */` and `// ═══`) for readability.
- No formatting or linting tools are configured; keep edits consistent with the surrounding style.

## Testing Guidelines
- No automated test framework or coverage requirements are configured.
- Manual checks: load the page, toggle between Data Flow and System Design, click nodes to open/close the modal, and resize below 900px to confirm responsive layout and canvas scaling.

## Commit & Pull Request Guidelines
- This directory is not currently a git repository, so there is no commit history to infer conventions.
- Use clear, imperative commit subjects (e.g., "Update threat tier labels") and add a short body when data or visuals change.
- For PRs, include a concise summary, rationale, and a screenshot or GIF for any visual, typography, or layout changes. Call out updates to `DETAIL` or node labels explicitly.

## External Dependencies
- Fonts are loaded from Google Fonts via a `<link>` tag. If you introduce new fonts or external assets, document them here and ensure they are publicly accessible.
