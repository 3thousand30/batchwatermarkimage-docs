---
layout: default
title: Output Formats
nav_order: 4
---

# Output Formats

BatchWatermark Image can output in four formats. Here's how to choose.

---

## Same as Input (default)

Keeps each image in its original format. A JPG stays JPG, a PNG stays PNG, a WebP stays WebP.

**Use this when:** You don't need to change formats — you just want to apply the watermark and move on. It's the simplest option and avoids any unnecessary re-encoding.

---

## JPG

JPEG compression — high quality (92%) with a small lossy artifact.

**Pros:**
- Smallest file sizes
- Universal compatibility — every app, website, and print lab accepts JPG
- Ideal for photographs (continuous-tone images without hard edges or text)

**Cons:**
- Lossy — each save introduces a small amount of compression artifact
- No transparency support

**Use JPG when:** You're sharing photos online, sending to a print lab, or need the smallest files. The 92% quality setting used by BatchWatermark Image is above the threshold where artifacts are visible under normal viewing.

---

## PNG

Lossless compression — no quality loss, larger files.

**Pros:**
- No compression artifacts — pixel-perfect output
- Supports transparency (alpha channel)
- Ideal for graphics, illustrations, logos, images with text overlays

**Cons:**
- Larger file sizes than JPG (often 3–5× bigger for photographic content)

**Use PNG when:** Your images have hard edges, logos, or transparency — or when you want an archival copy with zero quality degradation.

---

## WebP

A modern format from Google — smaller than JPG at equivalent quality.

**Pros:**
- Excellent compression — smaller than JPG at similar quality
- Supports transparency
- Good for web distribution

**Cons:**
- Not universally supported — some older software, print labs, and stock platforms don't accept WebP
- Not the standard format for traditional photo workflows

**Use WebP when:** You're preparing watermarked images for web publishing and you know your platform supports it.

---

## Format comparison at a glance

| | Same as Input | JPG | PNG | WebP |
|---|---|---|---|---|
| Compression | Original | Lossy | Lossless | Lossy |
| Transparency | Original | No | Yes | Yes |
| File size | Original | Small | Large | Smallest |
| Compatibility | Original | Universal | Good | Limited |
| Best for | General use | Photos, sharing | Graphics, logos | Web |

---

## A note on TIFF

BatchWatermark Image reads TIFF files as input but does not output TIFF. If your workflow requires TIFF output, export as PNG (lossless, same quality) and convert using a free tool like IrfanView or GIMP.
