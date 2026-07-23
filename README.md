# Belitz Global Change Entomology Lab — Website

Source for the lab website, built with [Hugo](https://gohugo.io/) and the [Hugo Blox Research Group](https://github.com/HugoBlox/theme-research-group) theme (free, open source, MIT/CC-BY licensed).

## What's in here

- `content/_index.md` — homepage
- `content/research/` — research themes page
- `content/people/` + `content/authors/*` — team page and individual profiles (Michael Belitz, Isadora Fluck, Yi Liu)
- `content/publication/` — publications, one folder per paper (`index.md` + `cite.bib`)
- `content/post/` — lab news
- `content/join/` — "Join Us" / how to apply page for prospective students & postdocs
- `content/resources/` — Code of Conduct, How to Apply, and AI Use Policy (**currently placeholder text — read and edit before publishing**)
- `content/contact/` — contact form and info
- `config/_default/` — site title, menu, and theme settings

## Before you publish, please:

1. **Add real photos.** Drop headshots into `content/authors/admin/avatar.jpg` (Michael), `content/authors/isadora-fluck/avatar.jpg`, and `content/authors/yi-liu/avatar.jpg`. Replace the stock placeholder images in `assets/media/` (`welcome.jpg`, `coders.jpg`, `contact.jpg`) with your own lab/field/insect photos.
2. **Fill in Isadora's and Yi's bios**, education years, and interests in their `_index.md` files — I only had names, roles, and degree institutions to go on.
3. **Read and edit the Resources pages** (`content/resources/code-of-conduct/index.md`, `how-to-apply/index.md`, `ai-policy/index.md`) — I drafted starting language, but these should reflect your actual policies before they go live.
4. **Confirm your UW-Madison email** in `content/contact/index.md` and `content/authors/admin/_index.md` (currently set to `mbelitz@wisc.edu` as a placeholder).
5. **Update the `repository` URL** in `config/_default/params.yaml` once you've created the GitHub repo.

## How publications work

Each publication is a folder in `content/publication/` with an `index.md` (metadata + abstract) and a `cite.bib` (BibTeX citation, powers the "Cite" button). I added 8 representative papers from your CV — to add the rest, either:
- Duplicate a publication folder and edit it by hand, or
- Add entries to a `publications.bib` file at the repo root and push — a GitHub Action (`.github/workflows/import-publications.yml`) will automatically open a pull request importing them as new pages.

## Deploying (free, via GitHub Pages)

This repo already includes `.github/workflows/publish.yaml`, which builds the site with Hugo and deploys it automatically on every push to `main` — you don't need to install Hugo locally.

1. Create a new GitHub repository (e.g. `mbelitz/belitzlab`) and push this folder to it.
2. In the repo's Settings → Pages, set **Source** to **GitHub Actions**.
3. Push to `main` — the site will build and deploy automatically. Check the Actions tab for build status.
4. To use **belitzlab.org**: buy the domain from any registrar (Namecheap, Google Domains successor Squarespace Domains, Porkbun, etc. — roughly $12–15/year for `.org`), then in the repo's Settings → Pages, add `belitzlab.org` as a custom domain. GitHub will show you the DNS records (an `ALIAS`/`ANAME` or `A` records) to add at your registrar. This can take up to 24 hours to propagate.
5. Update `baseURL` in `config/_default/hugo.yaml` to match your final domain (already set to `https://belitzlab.org/`).

## Previewing locally (optional)

If you want to preview changes before pushing, install the [extended version of Hugo](https://gohugo.io/installation/) (v0.135.0 or newer, to match the GitHub Action) and run:

```
hugo server
```

Then open http://localhost:1313.

## Editing without touching code

This theme ships with [Decap CMS](https://decapcms.org/), a free browser-based editor — once deployed, you can edit pages at `yoursite.com/admin/` without writing Markdown by hand. See the [Hugo Blox docs](https://docs.hugoblox.com/) for setup.

---

*Original theme by Hugo Blox / Wowchemy, MIT licensed. Customized for the Belitz Global Change Entomology Lab, July 2026.*
