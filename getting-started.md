---
layout: default
title: Getting Started
nav_order: 2
---

# Getting Started

This guide walks you through watermarking your first batch of images.

---

## 1. Install the app

Download and install **BatchWatermark Image** from the Microsoft Store. Once installed, launch it from the Start menu.

---

## 2. Select your input folder

Click **Browse** next to **Input Folder** and pick a folder containing your images.

Supported formats: **JPG, PNG, WebP, TIFF**

The app immediately counts how many supported images it found and will save results to a `watermarked` subfolder inside your input folder. You can change the subfolder name in the Output section.

---

## 3. Configure your watermark

You can use an **image watermark**, a **text watermark**, or both at the same time.

### Image watermark

Enable the **Image** toggle, then click **Browse** to select a PNG, JPG, or WebP logo file.

| Setting | What it does |
|---|---|
| **Opacity** | How transparent the watermark is (0% = invisible, 100% = fully opaque) |
| **Scale** | How wide the watermark is, as a percentage of the base image width |

A scale of 20% on a 4000px-wide photo produces an 800px-wide watermark.

### Text watermark

Enable the **Text** toggle, type your text, then choose a font, size, and color.

| Setting | What it does |
|---|---|
| **Font** | Any font installed on your Windows system |
| **Size** | Font size in points (8–600) |
| **Color** | Pick any color using the color swatch |
| **Opacity** | How transparent the text is |

---

## 4. Set the position

Use the **3×3 position grid** to place your watermark — corners, edges, or center.

Enable **Repeat / Tile** to tile the watermark across the entire image instead of placing it once.

Adjust **Margin** (pixels from the edge) and **Rotation** (degrees, -180° to 180°) as needed.

---

## 5. Preview before processing

The **Preview** panel on the right shows a live preview using one image from your folder.

Switch between **Watermarked**, **Original**, and **Split** views to compare. Use **Previous** and **Next** to cycle through sample images in the folder.

The preview refreshes automatically as you adjust settings.

---

## 6. Choose your output settings

In the **Output** card:

| Setting | What it does |
|---|---|
| **Format** | Same as Input, JPG, PNG, or WebP |
| **Folder** | Subfolder name created inside your input folder (default: `watermarked`) |
| **Suffix** | Optional tag appended to the filename before the extension (e.g. `_wm`) |
| **Skip existing** | Skip files that were already watermarked in a previous run |

See [Output Formats](output-formats) for details on each format.

---

## 7. Add EXIF metadata (optional)

In the **EXIF Metadata** card, enter a **Copyright** notice and **Author** name. These are embedded into the output file's metadata — they don't appear on the image itself but show up in Properties > Details and metadata-aware apps.

---

## 8. Watermark

Click **Watermark N Images**. The button shows the exact count of images that will be processed.

While running:
- A progress bar shows overall completion
- The current filename scrolls through below the bar
- Click **Cancel** at any time to stop mid-batch

When done, an **Open Output Folder** button appears. Click it to see the results in Windows Explorer.

---

## Tips

- **Both watermarks at once** — enable both the Image and Text toggles to composite them in a single pass.
- **Skip existing** is on by default — safe to re-run with adjusted settings without reprocessing everything. Turn it off to overwrite previous outputs.
- Check the **Activity Logs** (clipboard icon in the header) for error details if any files failed.
- Use **Repeat / Tile** with a diagonal rotation (e.g. -30°) to create a full-coverage watermark pattern.
