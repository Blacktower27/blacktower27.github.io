# Repository Guidelines

## Project Structure & Module Organization

This repository is a Jekyll academic portfolio. Site-wide settings live in `_config.yml`; navigation and author metadata are in `_data/`. Edit primary content in `_pages/` and publication entries in `_publications/`. Reusable HTML belongs in `_includes/`, page shells in `_layouts/`, and Sass partials in `_sass/`. Browser assets are under `assets/`, while downloadable papers, slides, and media belong in `files/` or `assets/`. The `markdown_generator/` scripts and notebooks generate publication Markdown from TSV data; `talkmap.py`, `talkmap.ipynb`, and `talkmap/` support the map feature.

## Build, Test, and Development Commands

- `bundle install` installs Ruby and Jekyll dependencies.
- `bundle exec jekyll serve -l -H localhost` serves the site at `http://localhost:4000` with live reload.
- `bundle exec jekyll build` renders the production site into `_site/` and catches Liquid, YAML, and plugin errors. Docker preview output is isolated in `_site_local/`, so builds do not overwrite the running preview.
- `npm install && npm run build:js` installs front-end dependencies and rebuilds `assets/js/main.min.js`.
- `npm run watch:js` rebuilds JavaScript when source files change.
- `docker compose up --build` runs the same site in a container.

## Coding Style & Naming Conventions

Use two-space indentation in YAML, HTML, JavaScript, and Sass; follow PEP 8 for Python. Keep Markdown front matter bounded by `---`, quote text values when punctuation could confuse YAML, and use lowercase kebab-case for new page or publication filenames. Add styles to the appropriate `_sass/` partial and JavaScript to `assets/js/_main.js` or `assets/js/plugins/`; do not hand-edit generated `main.min.js`. Preserve existing Liquid and Academic Pages conventions.

## Testing Guidelines

There is no dedicated automated test suite or coverage target. Before submitting, run `bundle exec jekyll build`, rebuild JavaScript when applicable, and inspect affected pages locally at desktop and mobile widths. Check navigation, external links, images, PDFs, color contrast, and keyboard focus states. If changing generators, run the relevant script or notebook and review the generated Markdown diff.

## Commit & Pull Request Guidelines

History uses short imperative summaries such as `add publication` and `fix github and linkedin url`. Keep commits focused and use a specific present-tense subject. Pull requests should explain the user-visible change, list validation performed, link related issues, and include screenshots for layout or theme changes. Do not commit `_site/`, `node_modules/`, local Bundler output, or secrets; review generated files before staging.
