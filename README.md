# Sports Intelligence Lab Website

Static site built with Jekyll and deployed via GitHub Pages.

## Local development

1. Install Ruby (>= 3.0 recommended).
2. Install dependencies:
   ```bash
   bundle install
   ```
3. Run the development server:
   ```bash
   bundle exec jekyll serve --livereload
   ```
4. Open `http://localhost:4000/SIL/` (or `/` if `baseurl` is empty).

## Deployment (GitHub Pages)

- Push the repository to GitHub as `username/SIL` (or your preferred repo name).
- In GitHub Settings → Pages, set Build and deployment to "GitHub Actions" or "Deploy from branch" (main branch, root).
- This site uses the `github-pages` gem for compatible dependency versions.

## Configuration

- `_config.yml` → site metadata, `url` and `baseurl` (update to your GitHub Pages values):
  - `url`: `https://<username>.github.io`
  - `baseurl`: `/<repo>` (empty if using user/organization site)

## Content management

- Data-driven pages via `_data/*.yml`:
  - `team.yml`, `areas.yml`, `publications.yml`, `projects.yml`, `news.yml`, `collaborations.yml`, `resources.yml`
- Pages in root directory: `about.md`, `research-areas.md`, `team.md`, `publications.md`, `projects.md`, `news.md`, `collaborations.md`, `resources.md`, `contact.md`

## SEO

- `jekyll-seo-tag`, `jekyll-sitemap`, and `robots.txt` are enabled.
- Add a logo at `assets/img/logo.png` for richer previews.


