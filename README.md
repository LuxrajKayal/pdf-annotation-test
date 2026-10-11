# Luxraj Editor

**Luxraj Editor** is a browser-based PDF annotation and page-management tool. It runs in your browser, and the app does not upload your PDF files to a server.

## Features

**Annotation Tools**
- Shapes: rectangle, ellipse, line, arrow
- Freehand pen drawing
- Text with font family/size controls (Helvetica, Times New Roman, Courier)
- Highlighter with multiple colors
- Eraser
- Sticky notes
- Signature pad (draw and save for reuse)
- Stamps (DRAFT, CONFIDENTIAL, APPROVED, REVIEWED, FINAL, or custom text)

**Editing Tools**
- Redact sensitive content
- Crop pages
- Select, move, and resize annotations
- Adjustable thickness, opacity, color (presets + hex picker)
- Fill/stroke toggle

**Document Management**
- Merge multiple PDFs (resizable pane)
- Split PDF by page ranges
- Page thumbnails with drag-to-reorder
- Find text in document
- Zoom in/out (0.5x–3x)

**UX**
- Undo and redo
- Keyboard shortcuts for every tool
- Dark mode
- Drag-and-drop file upload
- Download annotated PDF
- Fully accessible (ARIA labels, screen reader announcements)

## Getting Started

No build step required. Serve the files with any static HTTP server:

```bash
# Python
python3 -m http.server 8000

# Node.js (npx)
npx serve .

# PHP
php -S localhost:8000
```

Then open `http://localhost:8000` in your browser.

> **Note:** Opening `index.html` directly via `file://` won't work due to ES module imports.

## Project Structure

```
index.html          — Main HTML shell
pdf-editor-v3.js   — Current application module (~3,800 lines)
pdf-editor.js       — Source copy of the application module
pdf-editor.css      — Styles and design tokens
vendor/
  pdf-lib.esm.js    — small CDN shim for pdf-lib
  pdf.min.mjs       — small CDN shim for PDF.js
```

The PDF libraries are loaded from jsDelivr, so an internet connection is required.

## Libraries

- [pdf-lib](https://pdf-lib.js.org/) — Create and modify PDFs
- [PDF.js](https://mozilla.github.io/pdf.js/) — Render PDFs in the browser

## License

[MIT License](LICENSE) — see [third-party notices](THIRD-PARTY-LICENSES.md) for upstream and library acknowledgements.


## GitHub Pages deployment

This repository uses a GitHub Actions workflow at `.github/workflows/pages.yml`. If the site does not deploy automatically, open **Settings → Pages** and choose **GitHub Actions** as the deployment source. Then open **Actions → Deploy Luxraj Editor to GitHub Pages → Run workflow**, selecting the `main` branch.
