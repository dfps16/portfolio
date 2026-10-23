# portfolio

Source for my engineering portfolio. Plain static HTML/CSS, no build step.

- `index.html` — all content (title, Engineering, Leadership, Journey)
- `styles.css` — design tokens and layout (light/dark)

**Content source:** `portfolio-content-map.md` (kept outside the repo) is the source of truth; the site follows it.

**Add a piece:** copy an existing `<details class="row">` (or a journey `<li>`) in `index.html` and edit it. The `<summary>` is the ledger row (when, title, a one-line layman's summary, status: `Done`/`ok` or `In progress`/`warn`). The `row-body` is a `<dl class="sections">` whose parts follow what the content map gives that item; nothing is invented to fill a fixed template. Mark unfinished text with `<span class="todo">` and missing media with `<div class="asset-todo">`; both show in brick on purpose, so fill them before publishing.

**Assets:** `assets/headshot.webp` (portrait), `assets/cv.pdf` (Download CV button), `assets/journey/airbus-finals.jpg` and `assets/journey/esgw-london.jpg` (timeline photos; a missing file hides its slot). After changing `styles.css`, bump the `?v=` on its `<link>` in `index.html` so browsers fetch the new version.

**Preview:** open `index.html` in a browser, or `python3 -m http.server`.

**Deploy:** GitHub Pages → Settings → Pages → Source: *Deploy from a branch* → `main` / root.
