# CLAUDE.md

## Git workflow

- Push changes directly to `main` unless the user explicitly asks not to. The live site (GitHub Pages) builds from `main`.

## Writing workflow

New posts ("Thoughts") go through these steps, in order:

1. **Idea.** Bert brings an idea for a post.
2. **Debate (when needed).** If the topic is debatable (psychology, opinions, claims about how people or the brain work), talk it through first: push back, point out weak spots, and check claims against real sources before anything gets written.
3. **Polish.** Bert hands over a raw draft. Polish the vocabulary and formatting, but keep it his post: his voice, his ideas, his stories. Follow the `humanizer` skill so it doesn't read as AI-written.
4. **Review loop.** Bert reads the polished version and makes changes, then Claude checks those changes. Repeat until Bert says he's happy. Only publish (commit and push) after he approves the final version.

### Voice and formatting (match the existing posts)

- Casual, first person, honest. It's fine to admit he doesn't have a clean answer. Keep Ghanaian slang and phrasing like *chale*.
- No em dashes, no hype words, no neat AI-style summaries. Short paragraphs.
- `##` section headings for longer posts; **bold** for the key line of a section; *italics* for inner thoughts and quoted lines.
- Cite research inline with links: `<a href="..." target="_blank" rel="noopener">`.
- Front matter: `layout: post`, `title`, `date`, and a one-sentence `excerpt` (shown on the homepage).
- A closing line can use the pull-quote style: a `>` blockquote followed by `{: .pull-quote}`.

## Project notes

- Jekyll blog hosted on GitHub Pages at https://bertqrt.github.io/bertrandbosu-blog1/ (note the `baseurl`, so always use `relative_url` for links and assets).
- Posts live in `_posts/` and need `layout: post` in their front matter.
- All styling is in `assets/css/style.css`. Colors are CSS variables on `:root` with dark mode overrides under `[data-theme="dark"]`; reuse them so new UI matches both themes.
- Fonts: Source Serif 4 (headings), Inter (body), Space Mono (small uppercase labels and code).
- Only use plugins GitHub Pages supports (currently `jekyll-seo-tag`, `jekyll-feed`, `jekyll-sitemap`).
