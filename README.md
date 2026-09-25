# Lucidum

*New research, brought to light.*

This is the site for Lucidum's long-form articles: the longer read behind each Instagram post, with every source linked. It's live at **https://sadiqebrahim.github.io/lucidum/**.

GitHub Pages builds it with Jekyll from the root of `main` on every push. The content pipeline, which lives in a separate private repo, adds each article to `_posts/`.

- `_posts/`: one article per post, `<YYYY-MM-DD>-<slug>.md`, with any diagrams under `assets/posts/<YYYY-MM-DD>-<slug>/`.
- `_layouts/`, `_includes/`, `assets/css/style.css`: the Lucidum look.
- `_data/brand.json`: a copy of the pipeline's brand file (verdicts, series), which the pipeline keeps in sync.
- `assets/img/`: the eyes mark, favicon and social card.

To preview it locally with Docker:

```bash
docker run --rm -p 4000:4000 -v "$PWD":/site -w /site ruby:3.3 sh -c 'gem install jekyll jekyll-feed jekyll-seo-tag kramdown-parser-gfm && jekyll serve --host 0.0.0.0'
```
