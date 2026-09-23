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

## The envelope layers — cut from the photograph

`envelope-reference.png` is the photograph everything else here comes from: an ivory envelope
tied with a gold satin ribbon. It is not loaded by the page; it is the source the five layers
were cut out of, so the cover animates a real envelope rather than a drawing.

| File | What it holds |
|---|---|
| `env-body.png` | the envelope with the ribbon painted out |
| `env-flap.png` | the top flap, cut along its own fold lines — it hinges on the canvas's top edge |
| `env-mouth.png` | the inside, shaded from the fold down; revealed as the flap lifts |
| `env-band.png` | the ribbon band, its stripe carried across where the bow sat |
| `env-bow.png` | the bow, its knot, the wax seal and the tails |

All five share one **812 × 586** canvas (a 1082 × 781 crop of the photograph, scaled down) with
the envelope's top edge at y = 0, so they stack into the original picture exactly. The band sits
at 45–57% of the canvas height and the flap's tip at 69%, which is why the couple's names sit
below the envelope rather than on it.

Replacing them: keep one shared canvas, the same 1.385 : 1 shape, the fold along the very top
edge, and transparency everywhere else. Any layer missing and the page falls back to the
envelope it draws itself; `cover.mp4` still overrides all of it when present.
