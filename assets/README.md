# Assets needed

Drop these files into this `assets/` folder. The page already has working
fallbacks (hand-drawn SVG gopuram + thali, and a dashed placeholder box for
the couple art), so nothing breaks if a file is missing, but the page looks
best once these are in place.

| File | Purpose | Recommended spec |
|---|---|---|
| `temple-dim.png` | Thiruvannamalai Annamalaiyar gopuram, **unlit / dusk** look, used before the user taps "Tap to Seek Blessings" | Transparent or dark-background PNG/WebP, portrait-ish crop of the gopuram, ~800–1200px tall, compressed (<300KB) |
| `temple-lit.png` | The same gopuram, **illuminated at night** (gold lighting, like the reference temple photo), revealed bottom-to-top on tap | Same crop/framing as `temple-dim.png` so the reveal animation lines up, transparent or matching background, compressed (<400KB) |
| `thali.png` | South Indian thali / mangalsutra graphic (gold pendant on a beaded chain), hero image | Transparent PNG or WebP, ~800–1200px wide, compressed (<300KB) |
| `couple.png` | Studio Ghibli-style illustration of Deepak & Nivi | Transparent background PNG/WebP, ~1000px wide, compressed (<400KB) |
| `music.mp3` | Background music, starts after splash tap | MP3 or AAC, short loop, <2MB, normalize volume |

Important: `temple-dim.png` and `temple-lit.png` must be the **same framing/
crop** of the gopuram (just unlit vs. lit), since the splash screen animates
a clip-path mask over the lit image to reveal it bottom-to-top over the dim
one. Mismatched framing will look like the temple "jumps" when lit.

Tips:
- Export artwork as WebP where possible (smaller, broad support) and keep a
  PNG fallback only if you need older browser support.
- Run images through an optimizer (e.g. `squoosh.app`, `cwebp`) before
  committing, large uncompressed PNGs will slow down first paint on mobile.
- Keep transparent backgrounds so the art blends into the maroon page
  background instead of showing a white/black box.
- The maroon background already has a gold kolam-pattern overlay built in
  with CSS (no separate asset needed for that).

