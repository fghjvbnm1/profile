# Profile

This repository is an [al-folio](https://github.com/alshedivat/al-folio) starter site configured for GitHub Pages.

## GitHub Pages

The current configuration assumes this repository is published as a project site:

- Source repository: `fghjvbnm1/profile`
- Site URL: `https://fghjvbnm1.github.io/profile/`
- `_config.yml`:
  - `url: https://fghjvbnm1.github.io`
  - `baseurl: /profile`

If this repository is renamed to `fghjvbnm1.github.io`, change `_config.yml` to:

```yml
url: https://fghjvbnm1.github.io
baseurl:
```

## Deploy

1. Push this repository to GitHub.
2. In GitHub, open `Settings -> Actions -> General -> Workflow permissions`.
3. Select `Read and write permissions`.
4. Push to `main` or run the `Deploy site` workflow manually from the Actions tab.
5. In `Settings -> Pages`, set the publishing source to `Deploy from a branch` and select the `gh-pages` branch.

The included workflow builds the Jekyll site and publishes `_site` to `gh-pages`.

## Customize

- Main site metadata: `_config.yml`
- Home page: `_pages/about.md`
- Social links: `_data/socials.yml`
- CV data: `_data/cv.yml`
- Publications: `_bibliography/papers.bib`
- Projects: `_projects/`
- Blog posts: `_posts/`

Most optional pages are currently hidden from the navbar with `nav: false`. Set `nav: true` in the relevant file under `_pages/` when you are ready to publish that section.

## Local preview

Using Docker:

```bash
docker compose pull
docker compose up
```

Then open `http://localhost:8080/profile/`.

Using local Ruby tooling:

```bash
bundle install
bundle exec jekyll serve --baseurl /profile
```

Then open `http://localhost:4000/profile/`.
