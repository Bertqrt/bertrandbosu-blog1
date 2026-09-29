# CLAUDE.md

## Git workflow

- Push changes directly to `main` unless the user explicitly asks not to. The live site (GitHub Pages) builds from `main`.

## Project notes

- Jekyll blog hosted on GitHub Pages at https://bertqrt.github.io/bertrandbosu-blog1/ (note the `baseurl`, so always use `relative_url` for links and assets).
- Posts live in `_posts/` and need `layout: post` in their front matter.
- All styling is in `assets/css/style.css`. Colors are CSS variables on `:root` with dark mode overrides under `[data-theme="dark"]`; reuse them so new UI matches both themes.
- Fonts: Source Serif 4 (headings), Inter (body), Space Mono (small uppercase labels and code).
- Only use plugins GitHub Pages supports (currently `jekyll-seo-tag`, `jekyll-feed`).
