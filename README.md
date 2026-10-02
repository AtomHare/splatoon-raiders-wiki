# Splatoon Raiders Community Wiki

A community-curated wiki of **strategies, builds, videos and player tips** for
Splatoon Raiders, built with [Zensical](https://zensical.org) and hosted on
GitHub Pages.

**Site:** <https://atomhare.github.io/splatoon-raiders-wiki/>

Game data (stats, enemies, items, story) lives on
[Inkipedia](https://splatoonwiki.org). This wiki complements it and links to it
instead of copying it.

Want to help? See [CONTRIBUTING.md](CONTRIBUTING.md).

## Layout

```text
docs/                  the site (menu is generated from the folders)
templates/             page template + copy-paste snippets (not published)
zensical.toml          site configuration
.github/workflows/     build on every PR, deploy on push to main
.github/ISSUE_TEMPLATE forms for builds/strategies, videos and tips
```

## Maintainer setup (one time)

1. If you fork or rename the repo, replace `AtomHare` / `splatoon-raiders-wiki`
   everywhere:
   `grep -rIl "AtomHare\|atomhare" --exclude-dir=.git .`
   (in `zensical.toml`, `docs/`, `CONTRIBUTING.md`, `README.md`,
   `.github/ISSUE_TEMPLATE/config.yml`).
2. Push to GitHub, then go to **Settings → Pages → Build and deployment →
   Source: GitHub Actions**.
3. Optional: create the labels `content`, `strategy`, `video`, `tip` so issue
   forms label new submissions automatically.

Every push to `main` then rebuilds and deploys the site. Pull requests are
built as a check but never deployed.

## Local preview

```sh
uv venv && uv pip install -r requirements.txt
uv run zensical serve        # http://localhost:8000
uv run zensical build --clean
```
