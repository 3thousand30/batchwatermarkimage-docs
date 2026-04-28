---
layout: default
title: Watermark Options
nav_order: 3
---

# Watermark Options

BatchWatermark Image supports two watermark types — image and text — that can be used independently or together.

---

## Image watermark

An image watermark overlays a logo, stamp, or signature graphic on top of each photo.

**Best formats for your watermark file:**
- **PNG with transparency** — the most common choice; the transparent areas are preserved so only the logo shows
- **JPG** — works, but has no transparency; the watermark will have a rectangular background
- **WebP** — supported, with or without transparency

### Opacity

Controls how transparent the watermark appears over the image.

- **0%** — fully invisible
- **50%** — semi-transparent (default)
- **100%** — fully opaque, no bleed-through from the base image

For a subtle watermark that doesn't distract from the subject, 30–50% is a common range.

### Scale

Controls how wide the watermark is, expressed as a percentage of the base image's width.

- **10%** — small logo in a corner
- **20%** — moderate size (default)
- **50%** — dominant watermark
- **100%** — watermark as wide as the entire image

Scale is proportional — the watermark's aspect ratio is preserved. A 10% scale on a 4000px image produces a 400px-wide watermark.

---

## Text watermark

A text watermark stamps any text string onto the image using a font installed on your Windows system.

### Font

Any font installed on Windows is available in the font dropdown. The font is rendered server-side using the same font name — what you see in the preview is what you get in the output.

### Size

Font size in points, from 8 to 600. For a typical 3000px-wide photo:
- **72 pt** (default) — subtle one-line text
- **150–200 pt** — clearly visible signature or copyright
- **400+ pt** — large statement watermark

### Color

Pick any color using the color swatch. White (`#ffffff`) with some transparency is a classic choice for photos. Dark colors work better on light backgrounds.

### Opacity

Same behavior as image watermark opacity — 0% invisible to 100% fully opaque.

---

## Using both at once

Enable both the Image and Text toggles to composite them in a single pass. Both watermarks share the same position, margin, and rotation settings. They are layered on top of each other — image first, then text — so the text appears above the image watermark if they overlap.

---

## Positioning

### 9-position grid

The grid places your watermark at one of nine anchor points on the image:

```
↖  ↑  ↗
←  ⊙  →
↙  ↓  ↘
```

The **Margin** value controls the distance in pixels between the watermark and the nearest edge. A margin of 20px keeps a small gap between the logo and the image border.

When **Repeat / Tile** is enabled, the position grid is disabled — the watermark tiles across the entire image instead.

### Repeat / Tile

Tiles the watermark continuously across the full image area. Useful for:
- Full-coverage copyright protection
- Diagonal pattern watermarks (combine with rotation)
- Preventing cropping out a corner watermark

The tile spacing is determined by the **Margin** value — larger margin means more space between tiles.

### Rotation

Rotates the watermark from -180° to 180°.

- **0°** (default) — no rotation
- **-30° to -45°** — a popular diagonal angle for tiled watermarks
- **180°** — upside down

Rotation applies to both image and text watermarks.

---

## Live preview

The **Preview** panel on the right of the app shows a reduced-resolution preview of your watermark settings applied to a sample image from your folder.

- **Watermarked** — the output with the watermark applied
- **Original** — the unmodified source image
- **Split** — both side by side for direct comparison

Use **Previous** and **Next** to cycle through different images in your folder. The preview refreshes automatically as you change settings (with a short debounce delay).

The preview uses a maximum width of 1200px for performance — it is a visual proof for placement and opacity, not a pixel-accurate rendering of the final output.
