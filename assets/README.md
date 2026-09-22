# Cover artwork

Everything here is optional. The invitation draws its own envelope and ribbon, and only
swaps in real artwork when the matching file is present.

## `cover.mp4` — a real film of the envelope (takes over everything)

Drop a video in and the cover becomes that film: the guest sees its first frame with
**Tap to open** under it, taps, the film plays full screen, and the invitation dissolves in as
it ends. Nothing else is drawn over it. If the file is missing or cannot play, the envelope
below is used instead — nothing breaks.

- **`cover.mp4`** — H.264, portrait **1080 × 1920**, **4–8 seconds**, **no audio track**,
  ideally under ~6 MB (it is downloaded before the guest taps). Encode with
  `-pix_fmt yuv420p -movflags +faststart` so phones can play it inline.
- **`cover.webm`** *(optional)* — VP9 version; browsers that support it use it first.
- **`cover-poster.jpg`** *(optional)* — the first frame, shown while the video loads.

Two things make the join invisible:

1. **Start** on the closed envelope, held still for a moment — that frame is the cover.
2. **End** light and close-up: the last half second should be nearly filled with cream paper,
   because the invitation (also cream) fades in from it.

Phones only autoplay muted video, so the film plays silently — put nothing in it that depends
on sound.

Where to get one: film it on a phone (a real envelope and ribbon, plain surface, shot from
straight above, steady, untie slowly and lift the flap), or build it in Canva from a stock
clip — Elements → Videos → "envelope opening" / "ribbon untie" — in a 1080 × 1920 design, then
Share → Download → MP4.

## `cover.jpg` — the backdrop behind the envelope

Any size, portrait (9:16 works best). Used full-bleed behind the envelope; the page's own
floral sheet is used when this file is missing.

## `env-body.png`, `env-flap.png`, `env-band.png`, `env-bow.png` — the envelope

All four must be present, or the drawn envelope is used instead. They are stacked on top of
each other at the same size, so they only line up if every file is the same **1080 × 780**
canvas with its piece in its final position and transparent everywhere else.

A ready-made Canva design with one page per layer:
**https://www.canva.com/d/dr-FJluE_2WrDZH**

| Canva page | Export as | Contains |
|---|---|---|
| 1 | — | reference image only, ignore it (or delete it) |
| 2 `Preview (all layers)` | — | all four layers together, to check the look |
| 3 `env-body` | `env-body.png` | envelope front and fold lines |
| 4 `env-flap` | `env-flap.png` | the closed flap and the wax seal |
| 5 `env-band` | `env-band.png` | the ribbon band |
| 6 `env-bow` | `env-bow.png` | the bow, its knot and tails |

Export: Share → Download → **PNG**, tick **Transparent background**, select pages 3–6, then
rename each file to the name in the table.

`env-preview.png` and `envelope-reference.png` are kept here for reference only — the page
never loads them.

Where things sit on the canvas, if you restyle or redraw it:

- the flap folds along the **very top edge** of the canvas — the page hinges it there, so the
  flap must start at y = 0
- the names, "the wedding of" and the date are drawn by the page over the artwork, between
  **45% and 79%** of the canvas height — keep that band of the envelope empty
- the flap tip sits at about 35%, the ribbon band between 81% and 90%, and the bow's tails may
  run to the bottom edge but not past it
