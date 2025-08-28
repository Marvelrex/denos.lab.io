# Repository Guidelines

## Project Structure & Module Organization
- `index.html`: Site entry point.
- `_config.yml`: Jekyll configuration (site, collections, plugins).
- `_layouts/` and `_includes/`: HTML/Liquid templates and partials.
- `_team/`: Team member Markdown files with front matter (collection).
- `images/`, `css/`, `js/`: Static assets.
- `_site/`: Generated output. Do not edit by hand.

## Build, Test, and Development Commands
- `bundle install`: Install Ruby gems per `Gemfile`.
- `bundle exec jekyll serve --livereload`: Run local dev server at `http://127.0.0.1:4000`.
- `bundle exec jekyll build`: Build the site into `_site/`.
- `JEKYLL_ENV=production bundle exec jekyll build`: Production build.
- `bundle exec jekyll doctor`: Check for common configuration issues.

## Coding Style & Naming Conventions
- Indentation: 2 spaces for HTML/Liquid, YAML, CSS, and JS.
- Filenames: kebab-case (e.g., `team-member.html`, `jiayu-zhou.md`).
- Liquid: Keep logic in layouts/includes; keep pages mostly declarative.
- Assets: Place images under `images/` and reference with absolute paths (e.g., `/images/...`).
- Team entries: `_team/*.md` with front matter:
  ```yaml
  ---
  layout: team-member
  name: Full Name
  title: Role
  picture: /images/profile/name.jpg
  email: user@example.com
  category: 0
  ---
  Brief bio or links.
  ```

## Testing Guidelines
- Local verification: Build and browse key pages; check nav, links, and images.
- Link/config checks: Run `bundle exec jekyll doctor`.
- Optional: Open dev tools console to catch JS/CSS errors.

## Commit & Pull Request Guidelines
- Commits: Present tense, concise summary (e.g., "Update news", "Fix typo"). Group related changes.
- Do not edit `_site/` directly; changes should originate from sources.
- PRs: Include a clear description, before/after screenshots for visual changes, and reference related issues.
- Verify locally (`jekyll serve`) and ensure no broken links/images before requesting review.

## Security & Configuration Tips
- Review `_config.yml` changes carefully; they affect site-wide behavior.
- Avoid committing secrets or API keys; this site is static and should not require them.
