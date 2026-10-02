# Contributing

Thanks for helping! You don't need to know Git to contribute.

## Rule #1: check Inkipedia first

[Inkipedia](https://splatoonwiki.org) is the reference wiki for Splatoon game
data. This wiki only covers **Splatoon Raiders Strategies**.

| Belongs on **Inkipedia**, not here          | Belongs **here**                        |
| ------------------------------------------- | --------------------------------------- |
| Weapon and gadget stats                     | Builds and loadouts, and why they work  |
| Enemy and boss descriptions                 | Boss and raid strategies                |
| Item and loot lists                         | Movement and combat tech                |
| Story, lore, characters                     | Co-op team setups, farming routes       |
| Patch notes                                 | Beginner guides, videos, community tips |

If what you want to add is game data, contribute it to Inkipedia and link to it
from here. Whenever a page mentions a weapon, gadget, enemy or mechanic, link
its name to its Inkipedia page instead of restating its stats:

```markdown
[Weapon name](https://splatoonwiki.org/wiki/Page_Name)
```

## Two ways to contribute

### 1. Submit a form (no Git needed)

[Open a new issue](https://github.com/AtomHare/splatoon-raiders-wiki/issues/new/choose)
and pick a form: **Build or strategy**, **Video** or **Community tip**. A
maintainer turns it into a page.

### 2. Edit a page directly

1. On the wiki, click the ✏️ edit button at the top of any page.
2. GitHub opens the file in its web editor (it asks you to fork the repo the
   first time: just accept).
3. Make your change, then click **Commit changes** → **Propose changes**.
4. Open the pull request. A check builds the site to make sure nothing is
   broken, then a maintainer reviews and merges it.

## What goes where

| Folder                     | Content                                                 |
| -------------------------- | ------------------------------------------------------- |
| `docs/basics/`             | Mechanics, controls, game modes, for new players        |
| `docs/builds/`             | One page per build (weapon + ink tank + gadgets)        |
| `docs/strategies/`         | One page per strategy (boss, raid, team setup, route…)  |
| `docs/videos/index.md`     | One block per video, newest first                       |
| `docs/community-tips/index.md` | One block per tip, newest first                     |
| `docs/hall-of-fame/index.md` | Standout player achievements, newest first           |
| `docs/resources/index.md`  | Community-made websites and tools, credited             |
| `docs/assets/screenshots/` | All images, named `YYYY-MM-DD-author.png`               |
| `templates/`               | Page template and copy-paste snippets (not published)   |

## Adding a page

1. Copy [`templates/strategy.md`](templates/strategy.md) into `docs/strategies/`
   or `docs/builds/`.
2. Give it a short lowercase name with dashes: `boss-name-solo.md`.
3. Set the title on the first line (`# My title`): that's what the menu shows.
4. Add a few `tags:` at the top so it shows up on the tags page.

That's it: the menu is generated from the folders, no config to edit.

Formats for tips, videos and Inkipedia links are in
[`templates/snippets.md`](templates/snippets.md).

## Sourcing rules

- **Always credit and link.** Every tip, video or idea from someone else names
  its author and links to the original.
- **Summarize, don't copy.** Write tips in your own words. Don't paste whole
  posts or articles.
- **Add a screenshot** when the post might disappear (deleted posts, private
  accounts). Save it in `docs/assets/screenshots/` as `YYYY-MM-DD-author.png`.
- **No datamined files or ripped game assets.** Your own gameplay screenshots
  are fine.
- **Don't invent facts.** If you're not sure, say so or leave it out.

## Previewing locally (optional)

```sh
uv venv && uv pip install -r requirements.txt
uv run zensical serve
```

Then open <http://localhost:8000>.
