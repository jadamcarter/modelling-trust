# Modelling Trust — website

The website of **Modelling Trust**, a research network at the University of Glasgow funded by the Glasgow Changing Futures (GCF) Collaborative Seed Fund (2026–27).

Built with [Hugo](https://gohugo.io/) and the [Blowfish](https://blowfish.page/) theme, and published by GitHub Pages: every push to `main` rebuilds the site (see `.github/workflows/hugo.yml`).

## Editing

All the words are plain Markdown in `content/`:

| Page | File |
|---|---|
| Home page introduction | `content/_index.md` |
| The three strand cards on the home page | `data/strands.yaml` |
| About | `content/about.md` |
| Programme (add dates, speakers, registration links here) | `content/programme.md` |
| People | `content/people.md` |
| Research (working papers, recordings) | `content/research.md` |
| Join / contact | `content/join.md` |
| Accessibility | `content/accessibility.md` |
| News | one file per item in `content/news/` (copy `launch.md`, change the title, date and text) |

You can edit any of these directly on github.com (open the file, click the pencil, commit); the site updates a minute or two later.

The funding acknowledgement and GCF strapline in the footer are in `layouts/partials/extend-footer.html`. Colours and the home-page layout are in `assets/css/custom.css` and `layouts/partials/home/custom.html`.

## Previewing locally

```sh
brew install hugo          # once
git submodule update --init
hugo server                # then open http://localhost:1313
```

## Domain

The site is meant to live at `modellingtrust.uk`. At the registrar, add these DNS records:

| Type | Name | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| AAAA | @ | 2606:50c0:8000::153 |
| AAAA | @ | 2606:50c0:8001::153 |
| AAAA | @ | 2606:50c0:8002::153 |
| AAAA | @ | 2606:50c0:8003::153 |
| CNAME | www | jadamcarter.github.io |

Then, in the repository's Settings › Pages, set the custom domain to `modellingtrust.uk` and tick "Enforce HTTPS" once the certificate has been issued.
