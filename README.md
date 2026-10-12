# Behzad Beigzadeh — personal website

Academic and professional website covering cybersecurity research, federated learning, IoT security, cryptography, and secure software development.

Live site: https://behzadbeigzadeh.github.io/

## Content

- `_pages/about.md`: biography and current work.
- `_projects/`: verified open-source projects, with the clinical AI project featured first.
- `_bibliography/papers.bib`: published research and publication identifiers.
- `_pages/publications.md`: published research and clearly identified manuscripts in progress.
- `assets/json/resume.json`: the CV page's primary data source.
- `_data/cv.yml`: matching YAML fallback for the CV page.
- `assets/pdf/CV_Beigzadeh.pdf`: downloadable CV.
- `_news/`: research and project updates.

## Local development

The site uses Jekyll and the al-folio theme. With Ruby, Bundler, and ImageMagick installed:

```sh
bundle install
bundle exec jekyll serve
```

To create a production build:

```sh
JEKYLL_ENV=production bundle exec jekyll build
```

The existing deployment workflow in `.github/workflows/deploy.yml` builds the site on updates to `main` or `master` and deploys the generated `_site` directory. See `INSTALL.md` and `CUSTOMIZE.md` for theme setup details.

## Content sources and status

The October 12, 2026 content refresh uses the owner-provided CV and the owner's public GitHub repositories. The clinical AI project descriptions and benchmark figures come from its README and REPORT.md. Published-paper titles, authors, venues, pages, and DOI identifiers were checked against Crossref records deposited by IEEE.

The Android malware manuscript is listed as submitted to ICCKE 2025 in the supplied CV; acceptance or publication has not been independently confirmed. The IoT power-consumption manuscript is listed as in preparation. These manuscripts are kept separate from published papers, and the clinical AI repository is presented as a project.

## Attribution

Built with [al-folio](https://github.com/alshedivat/al-folio). The theme's MIT license and attribution are retained in `LICENSE`.
