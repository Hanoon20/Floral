# Floral — wedding invitation site

One self-contained page. No build step, no framework, no npm install.
Open `index.html` in a browser to see it.

## Files
- `index.html` — everything: HTML, CSS, JS, the floral artwork (base64 JPEG),
  the Great Vibes font (base64 WOFF) and opentype.js (inlined, minified).
- `intro.mp4` + `poster.jpg` — tap-to-open intro video.
- Artifact/single-file version: the video and poster are base64 inside the HTML instead.

## How it is put together
- All wedding details live in the `CONFIG` object near the bottom of `index.html`
  (names, date, venue, map query, programme, parents, dua, WhatsApp number).
  Everything on the page is rendered from it — change data there, not in the markup.
- Sections: intro overlay → hero → parents → invitation + countdown → location
  (Google Maps iframe with a drawn SVG fallback) → programme (curved SVG timeline
  drawn on scroll) → dua with WhatsApp wish button → closing.
- Hero background, the canopy above the dua section and the closing strip are the
  same artwork reused with `background-position`, via the `.art` class.
- Bride and groom names are drawn as SVG paths from the embedded font with opentype.js
  and written stroke by stroke. Falls back to a clip-path wipe if that fails.
- `onStart()` / `startShow()` gate every hero animation until the intro video ends
  or is skipped.
- Section entrances: each section's children are wrapped in a `.stage` div and
  transformed in 3D on scroll (rAF loop with lerp smoothing).
- Text intros: headings split into characters, prose into words (Arabic and Tamil
  are always split by word, never by character), revealed by IntersectionObserver.
- Everything respects `prefers-reduced-motion`.

## House rules
- Keep it a single page with no dependencies fetched at runtime, except Google Fonts.
- Do not break the `CONFIG`-drives-everything rule.
- Test at 390px width first; the layout is a centred 520px column.

## Deploy
GitHub Pages from `main` / root → https://hanoon20.github.io/Floral/
