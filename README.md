# portfolio

Source for my engineering portfolio. Plain static HTML/CSS, no build step.

- `index.html` — all content (title, Engineering, Leadership, Journey)
- `styles.css` — design tokens and layout (light/dark)
- `strategy.html` — one-page SUSF projects summary, linked from Head of Projects; prints on one A4 sheet

**Content source:** `portfolio-content-map.md` (kept outside the repo) is the source of truth; the site follows it.

**Add a piece:** copy an existing `<details class="row">` (or a journey `<li>`) in `index.html` and edit it. The `<summary>` is the ledger row (when, title, a one-line layman's summary, status: `Done`/`ok` or `In progress`/`warn`). The `row-body` is a `<dl class="sections">` whose parts follow what the content map gives that item; nothing is invented to fill a fixed template. Mark unfinished text with `<span class="todo">` and missing media with `<div class="asset-todo">`; both show in brick on purpose, so fill them before publishing.

**Assets:** `assets/headshot.webp` (portrait), `assets/thesis/67p.jpg` (thesis figure, cropped from the project-plan slides), `assets/mmat/*.jpg` and `assets/mmat/mmat-poster.pdf` (MMAT screenshots cropped from the UKEO poster, and the poster itself), `assets/vtvl/*.jpg` (Starworks lander-trajectory tool screenshots), `assets/starworks/meeting-*.jpg` (Starworks team-meeting photos), `assets/starworks/banshee-cad.jpg` and `spitfire-pid.webp` (Banshee CAD and test stand P&ID), `assets/scorpio/engine-section.webp`, `injector-fea.jpg` and `hot-fire.mp4` (Scorpio 3 engine CAD, injector FEA and the Comet-1 hot-fire clip, with `hot-fire-poster.jpg` as its still), `assets/sverd/*.jpg` (Sverd engine and Race 2 Space hot-fire photos), `assets/rion/` (finals and prep photos, GMAT trade-study plots from the finals deck, the deck itself, and the February technical report, appendix and business report), `assets/cv.pdf` (Download CV button; the button stays hidden until this file exists), `assets/journey/airbus-finals.jpg` and `assets/journey/esgw-london.jpg` (timeline photos; a missing file hides its slot), `assets/quadcopter/` (CAD, assembly and pre-flight photos, and the muted flight video with its poster still), `assets/elset/decay-*.jpg` (decay plots cropped from a screenshot; originals lost). After changing `styles.css`, bump the `?v=` on its `<link>` in `index.html` and `strategy.html` so browsers fetch the new version.

**Preview:** open `index.html` in a browser, or `python3 -m http.server`.

**Deploy:** GitHub Pages → Settings → Pages → Source: *Deploy from a branch* → `main` / root.
