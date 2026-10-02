# Copy-paste snippets

This folder is **not published**. Copy the block you need into a page under `docs/`.

## Community tip

Goes at the top of `docs/community-tips/index.md` (newest first).
Screenshot goes in `docs/assets/screenshots/`, named `YYYY-MM-DD-author.png`.

```markdown
!!! quote "@author · YYYY-MM-DD"
    The tip, summarized in our own words.

    ![Screenshot of the post](../assets/screenshots/YYYY-MM-DD-author.png){ loading=lazy }

    [:material-link: Original post](https://x.com/author/status/123)
```

## Video

Goes at the top of `docs/videos/index.md` (newest first). `VIDEO_ID` is the part
after `v=` in the YouTube URL.

```markdown
## Video title

**By:** [Creator](https://www.youtube.com/@creator) · **Topic:** guide

<iframe class="video" src="https://www.youtube-nocookie.com/embed/VIDEO_ID" title="Video title" loading="lazy" allowfullscreen></iframe>

Why it's worth watching, in one or two sentences.
```

## Hall of fame entry

Goes at the top of `docs/hall-of-fame/index.md` (newest first). Give each popup
a **unique id** (e.g. `hof-author-floor1000`) and use it in all three places.
The build part is optional: drop the buttons and the `<div>` if there's none.

```markdown
## Player: achievement

!!! quote "@author · YYYY-MM-DD"
    The achievement, summarized in our own words.

    ![Screenshot of the post](../assets/screenshots/YYYY-MM-DD-author.png){ loading=lazy }

    [:material-link: Original post](https://x.com/author/status/123)

<button class="md-button md-button--primary" popovertarget="hof-UNIQUE-ID">:material-eye: Reveal the build</button>

<div id="hof-UNIQUE-ID" class="build-popup" popover="auto" markdown>

### Build used by @author

| Slot     | Pick                                                   |
| -------- | ------------------------------------------------------ |
| Weapon   | [Weapon name](https://splatoonwiki.org/wiki/Page_Name) |
| Ink tank | [Ink tank name](https://splatoonwiki.org/wiki/Page_Name) |
| Gadgets  | [Gadget name](https://splatoonwiki.org/wiki/Page_Name) |

<button class="md-button" popovertarget="hof-UNIQUE-ID" popovertargetaction="hide">Close</button>

</div>
```

## Inkipedia reference

Inline, the first time a weapon, gadget, enemy or mechanic is mentioned on a page:

```markdown
[Weapon name](https://splatoonwiki.org/wiki/Page_Name)
```

At the top of a strategy or build page:

```markdown
!!! abstract "Game data"
    Stats and details: [Page name on Inkipedia](https://splatoonwiki.org/wiki/Page_Name)
```

## Tags

At the very top of a page:

```markdown
---
tags:
  - Boss
  - Co-op
---
```

## Collapsible block

```markdown
??? note "Click to expand"
    Hidden content.
```
