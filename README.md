# Floral — Wedding Invitation

Garden-rose digital wedding invitation for Rashad & Zahra.

Single self-contained page (`index.html`): a sealed "tap to open" cover, hero artwork,
handwritten names, parents, countdown, location map, curved programme timeline, dua with
WhatsApp wish button.

The cover holds the page until the guest taps it: a closed envelope tied with a gold ribbon.
On tap the bow unravels loop by loop, the ribbon slips off and falls, the flap lifts, and the
camera flies into the envelope's mouth and dissolves into the invitation. The hero handwriting
and reveal animations only start once that flight ends, so nothing plays behind the cover.
A film of the envelope takes over the whole cover when `assets/cover.mp4` is present: it plays
full screen on tap and the invitation dissolves in as it ends.

Without it, the envelope and the ribbon are drawn by the page, and are replaced by real artwork as soon as
`assets/env-body.png`, `env-flap.png`, `env-band.png` and `env-bow.png` are all present — see
`assets/README.md` for how to export those four layers. The backdrop behind the envelope works the
same way with `assets/cover.jpg`. No code change is needed for either swap. Reduced-motion visitors
get the invitation immediately on tap.

Edit all details in the `CONFIG` object near the bottom of `index.html`.

Live site: enable GitHub Pages (Settings → Pages → Deploy from branch → `main` / root).
