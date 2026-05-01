# BurgundyTable Brand Assets

Canonical asset folder for the BurgundyTable brand. The BurgundyTable brand skill references files here by name.

## Quick reference

- **Brand color (burgundy):** `#7B1822`
- **Last updated:** 2026-05-01
- **Owner:** Brandon Chon (burgundytable@gmail.com)
- **Canonical source:** `01-master/0902_burgundytable_master.ai` — re-export from there if updates are needed.

## Folder structure

```
BurgundyTable Brand Assets/
├── 01-master/        Adobe Illustrator master (2 artboards: wordmark, square icon)
├── 02-logos-icon/    Square icon variants (PNG 128/256/512 + SVG)
├── 03-logos-wordmark/Wordmark variants (burgundy 600/1200 + paper 1200 + SVGs)
├── 04-logos-lockup/  Composed lockups (stacked + horizontal, PNG + SVG)
├── 05-favicon/       Favicons (16, 32 PNG)
└── 06-print/         Korean business card PDFs (legacy 2019, untouched)
```

## Notes for skill consumers

- All PNGs are **transparent background** unless otherwise noted.
- All burgundy fills are exactly `#7B1822` (verified pixel-level).
- The icon's source artwork has a slight non-square aspect ratio (~1.19:1, the white "T" + brackets fill a horizontally wider rectangle than tall). Square PNGs center the icon on a transparent square canvas without distortion.
- **No circle-icon variant exists.** The 2019 master only contains the burgundy *square* icon. Producing a circle version would be a redesign and is intentionally out of scope.
- Lockups (`04-logos-lockup/`) were **composed programmatically** from the two master artboards — they are not native Illustrator artboards. If a designer wants pixel-perfect kerning between icon and wordmark, regenerate from a properly-laid-out Illustrator artboard.
- The wordmark in the master file has the registered-trademark mark (®) attached. It carries through into all wordmark and lockup exports.

## Regeneration

The asset build pipeline lives in `outputs/build_assets.py` (the session that produced these files). To regenerate:

1. Drop a new master AI/PDF into `01-master/`.
2. Run the script.
3. Color, sizing, and lockup composition are deterministic.
