# Cover artwork

Everything here is optional. The invitation draws its own envelope and ribbon, and only
swaps in real artwork when the matching file is present.

## `cover.jpg` — the backdrop behind the envelope

Any size, portrait (9:16 works best). Used full-bleed behind the envelope; the page's own
floral sheet is used when this file is missing.

## `env-body.png`, `env-flap.png`, `env-band.png`, `env-bow.png` — the envelope

All four must be present, or the drawn envelope is used instead. They are stacked on top of
each other, so they only line up if they are exported from **one** Canva design:

1. Build the whole closed envelope — body, flap, ribbon band, bow — in a single design,
   canvas **1080 × 780 px**, background transparent.
2. Export it four times as **PNG with a transparent background**, each time with only one
   piece visible:

   | File | Contains | Sits at |
   |---|---|---|
   | `env-body.png` | envelope front only (no flap, no ribbon) | the whole canvas |
   | `env-flap.png` | the closed flap triangle + wax seal | must touch the **top edge** — it hinges there |
   | `env-band.png` | the ribbon band only | roughly 81–93% down the canvas |
   | `env-bow.png` | the bow and its tails only | centred on the band, tails may hang past the bottom |

3. Keep the middle of the envelope clear: the couple's names, "the wedding of" and the date
   are drawn by the page over the artwork, between about **45% and 79%** of the canvas height.
   The flap tip should sit above that, around 38%.

Do not crop the four exports differently — every file needs the same 1080 × 780 canvas with
its piece in its final position, transparent everywhere else.
