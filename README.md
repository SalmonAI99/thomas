# Juntao Wu — Personal Website

Personal site and portfolio for Juntao Wu, built with [al-folio](https://github.com/alshedivat/al-folio), Jekyll, and GitHub Pages.

## Live site

Once GitHub Pages finishes its first deployment, the site will be available at:

<https://salmonai99.github.io/thomas/>

## Run locally

This project is built with Jekyll and Ruby. Install the dependencies, then build and serve the site:

```bash
bundle install
npm ci
bundle exec jekyll serve
```

Open <http://localhost:4000/thomas/>.

## Updating the site

- `_pages/about.md` — homepage biography.
- `_projects/` — research, product, and systems projects.
- `_bibliography/papers.bib` — publications.
- `_data/cv.yml` and `assets/json/resume.json` — CV page data.
- `assets/pdf/Juntao_Wu_CV.pdf` — downloadable PDF CV.
- `_config.yml` — site identity and GitHub Pages URL/base path.

The `Deploy site` workflow in `.github/workflows/deploy.yml` builds the site and publishes it with GitHub's Pages artifact deployment on pushes to `main`.

Before the first successful deploy, enable Pages in **Settings → Pages** and set **Source** to **GitHub Actions**. Do not select a branch as the source.
