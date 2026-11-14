# Pika Assets

Consolidated region-map artwork for the Pika Pokémon Telegram bot.

All nine mainline regions in one place, so the bot can pull every region map from a single
raw base URL instead of stitching together one repository per region.

## Layout

```
assets/
  region/
    kanto-map.jpg
    johto-map.png
    hoenn-map.jpg
    sinnoh-map.jpg
    unova-map.jpg
    kalos-map.jpg
    alola-map.jpg
    galar-map.jpg
    paldea-map.png
```

## Region maps

| Region | Path | Dimensions | Size | Source |
|---|---|---|---|---|
| Kanto | `assets/region/kanto-map.jpg` | 2400 × 1792 | 2.1 MB | `TheSunphis/Pika` |
| Johto | `assets/region/johto-map.png` | 2528 × 1696 | 6.7 MB | `TheSunphis/johto-assets` |
| Hoenn | `assets/region/hoenn-map.jpg` | 531 × 376 | 75 KB | `TheSunphis/hoenn-assets` |
| Sinnoh | `assets/region/sinnoh-map.jpg` | 531 × 376 | 63 KB | `TheSunphis/sinnoh-assets` |
| Unova | `assets/region/unova-map.jpg` | 553 × 361 | 57 KB | `TheSunphis/unova-assets` |
| Kalos | `assets/region/kalos-map.jpg` | 1600 × 1048 | 377 KB | `TheSunphis/kalos-assets` |
| Alola | `assets/region/alola-map.jpg` | 739 × 519 | 120 KB | `TheSunphis/alola-assets` |
| Galar | `assets/region/galar-map.jpg` | 725 × 423 | 58 KB | `TheSunphis/galar-assets` |
| Paldea | `assets/region/paldea-map.png` | 1200 × 896 | 2.0 MB | `TheSunphis/paldea-assets` |

### Sourcing notes

- **Kanto** comes from `TheSunphis/Pika`, not `kanto-assets`. The `kanto-assets` repository was
  reset on 2026-11-14 and its `main` branch is currently empty; it never held a whole-region Kanto
  map (only per-town and per-route maps, still readable in its history at `87e8892`).
- Everything else is the byte-identical file currently served from each region's own `-assets`
  repository. Files are copied as-is — same filename, same format — so the copies can be verified
  against their sources with a checksum.
- Formats and resolutions are mixed, intentionally unmodified. Two are PNG (Johto, Paldea); the rest
  are JPEG. If the bot needs a uniform set, they should be re-encoded to a single format and width.

## Raw URL base

```
https://raw.githubusercontent.com/TheSunphis/pika-assets/main/assets
```

So the Kanto map, for example, is:

```
https://raw.githubusercontent.com/TheSunphis/pika-assets/main/assets/region/kanto-map.jpg
```

## Not included

Only the whole-region overview maps live here. Per-town and per-route art (`assets/region-maps/`,
`assets/<location>/region/`) still belongs to the regional repositories.
