# Floral — Wedding Invitation

Garden-rose digital wedding invitation for Rashad & Zahra.

Single self-contained page (`index.html`): a sealed "tap to open" cover, hero artwork,
handwritten names, parents, countdown, location map, curved programme timeline, dua with
WhatsApp wish button.

The cover holds the page until the guest taps it; the hero handwriting and reveal animations
only start once it opens. Its background is `assets/cover.jpg` when that file exists, and falls
back to the invitation's own floral sheet when it does not — drop a new cover image at that path
to swap the artwork, no code change needed.

Edit all details in the `CONFIG` object near the bottom of `index.html`.

Live site: enable GitHub Pages (Settings → Pages → Deploy from branch → `main` / root).
