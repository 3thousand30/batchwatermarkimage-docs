---
layout: default
title: Troubleshooting
nav_order: 5
---

# Troubleshooting

---

## "No supported images found"

The app only processes **JPG, PNG, WebP, and TIFF** files. Other formats (BMP, GIF, HEIC, RAW) are skipped.

HEIC (iPhone photos) must be converted before watermarking. Use the built-in Windows **Photos** app to export as JPG, or a free tool like [CopyTrans HEIC for Windows](https://www.copytrans.net/copytransheic/).

---

## The Watermark button stays disabled

The button is disabled until:

- An input folder with at least one supported image is selected
- At least one watermark is configured (Image or Text toggle enabled with valid content)

For the image watermark, a file must be selected. For the text watermark, the text field must not be empty.

---

## Nothing happened — the progress bar showed 0 processed

This usually means the output folder could not be created. Common causes:

- **OneDrive or network folders** — watermarked images are saved locally first. If the output path is on a synced drive with access issues, folder creation can fail silently.
- **Read-only or permission-restricted folders** — try changing the output subfolder, or move your images to a local path like `C:\Users\YourName\Pictures\`.

Check the **Activity Logs** panel (clipboard icon in the header) for a "Failed —" entry with the exact error.

---

## Some images failed, others succeeded

Partial failures are shown in the Activity Logs with the filename and error message. Common causes:

| Error | Fix |
|---|---|
| `Input file is missing` | The source file was moved or deleted while the batch was running |
| `Input buffer contains unsupported image format` | The file has a supported extension but is corrupt or not a real image |
| `Unable to write to output` | Output folder became unavailable mid-run (synced drive disconnected, full disk) |

---

## The preview doesn't update

The preview refreshes automatically after a short delay when you change settings. If it stops updating:

- Click **Refresh** in the preview panel to force a new render
- Make sure at least one watermark type is enabled and configured
- If the folder was changed outside the app, re-select the input folder to reload the sample list

---

## The watermark position looks different in the output than in the preview

The preview uses a reduced-resolution version (max 1200px wide) for performance. The watermark scale and position are calculated relative to the preview image size, so small rounding differences can occur at very high resolutions. If placement precision matters, use a test run on a single image and open the output to verify.

---

## The watermark image has a white or black rectangle around it

Your watermark file is likely a JPG with no transparency. JPG does not support alpha channels — the background of the watermark will be filled with a solid color.

Use a **PNG with a transparent background** as your watermark file for a clean overlay with no rectangular border.

---

## The font I selected looks different in the output

The text watermark uses the system font name exactly as listed in the font dropdown. The same font must be present on the machine where the images are processed. If the font renders differently, check that the correct font variant (Regular vs Bold vs Italic) is selected.

---

## The app won't start or crashes on launch

- Ensure you're running Windows 10 or later
- Try reinstalling from the Microsoft Store
- Check for a pending Windows update

If the issue persists, [open an issue](https://github.com/3thousand30/batchwatermarkimage-docs/issues) with a description of what happens.

---

## Output folder won't open

The **Open Output Folder** button uses Windows Explorer. If it doesn't open, navigate manually to the subfolder inside your input folder (default name: `watermarked`).

---

## Still stuck?

Email [hello@3thousand30.com](mailto:hello@3thousand30.com) or [open an issue](https://github.com/3thousand30/batchwatermarkimage-docs/issues) on GitHub.
