# Beaches that need their own photo

These beaches are live in the app and on beach-report.com, but their photo is a
stand-in (a nearby beach) because no usable photo of the beach itself could be
found. Replace them when a real photo turns up: a photo you took or have rights
to, or a public-domain / CC0 / CC BY / CC BY-SA photo (never NC or ND).

| Beach (app id) | Current photo | What it actually shows | Added |
|---|---|---|---|
| Dune Allen (`dune-allen`) | `238-dune-allen.jpg` | Topsail Hill Preserve State Park, ~1.4 mi west | 2026-10-10 |
| Inlet Beach (`inlet-beach`) | `247-inlet-beach.jpg` | Camp Helen State Park, next door (marsh view to the Gulf) | 2026-10-10 |
| WaterSound (`watersound`) | `242-rosemary-beach.jpg` (shared) | Rosemary Beach, ~1.5 mi east | 2026-10-10 |

## Could be better (real photo of the beach, but not ideal)

| Beach | Current photo | Why |
|---|---|---|
| Indialantic | `213-indialantic.jpg` | Night / moonlight shot |
| Melbourne Beach | `214-melbourne-beach.jpg` | Sunrise shot (dark foreground) |
| Delray Beach | `225-delray-beach.jpg` | Overcast day |

## How to swap one in

New photo -> next free number (e.g. `250-dune-allen.jpg`), add its row to
CREDITS.md if it needs credit, then point the beach at it: the app's
`IMAGE_MAPPING` / `PHOTO_CREDITS` in `expo/constants/beaches.ts` and the site's
`image` / `imageCredit` in `src/data/beaches.core.json`. Remove the row above.
