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

If the film cannot play, the cover falls back to a real photographed envelope: `assets/env-*.png`
are layers cut out of a photograph — body, flap, inside, ribbon band and bow — so the bow loosens,
the ribbon slides off and falls, the flap lifts and the camera flies into the opening. Those layers
are only fetched when they are needed, and if they are missing too the page draws its own envelope.
See `assets/README.md`.

Once the hero has finished writing itself, a scroll cue fades in at the foot of the screen and
retires as soon as the guest scrolls.

Edit all details in the `CONFIG` object near the bottom of `index.html`.

Live site: enable GitHub Pages (Settings → Pages → Deploy from branch → `main` / root).
