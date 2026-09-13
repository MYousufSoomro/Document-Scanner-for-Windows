# Changelog

All notable changes to Document Scanner are documented here.
Format loosely follows [Keep a Changelog](https://keepachangelog.com/).

## [1.0.0] - 2026-09-13

Initial public release.

### Added
- Import single or multiple images (JPG, PNG, BMP, TIFF) or an existing PDF
- Automatic document boundary detection with a confidence check (falls
  back to manual crop rather than guessing)
- **Magic Filter**: one-click auto-detect + auto-crop + auto-deskew +
  auto-enhance pass, applied automatically on import
- Interactive four-corner crop / perspective-correction editor
- Rotation (90°/180°/270°) and one-click auto-straighten (deskew)
- 8 enhancement presets: Original, Auto, Document (default), Color
  Document, Grayscale, Black & White, ID/Receipt, Photo
- "Apply to All Pages" button for presets, once changed on one page
- Manual brightness, contrast, sharpening and noise-reduction controls
- Shadow removal and background whitening
- Non-destructive editing with full undo/redo, per page
- Page thumbnails with drag-and-drop reordering, duplicate, delete
- Batch processing with a progress indicator; the UI never freezes
- Export to JPG/PNG (auto-numbered for multi-page) or a combined,
  multi-page PDF (A4 / Letter / Original / Auto page sizing)
- Drag-and-drop import directly into the window
- Windows installer via Inno Setup (`installer/DocumentScanner.iss`)

### Changed
- Default enhancement preset changed from Auto to **Document**
- Skew correction rewritten to use a line/edge-based (Hough transform)
  estimator instead of a text-density guess, for more accurate
  auto-straightening on real photographed documents

### Notes
- Closed-source freeware release - see [LICENSE](LICENSE)
- No OCR / searchable PDF export yet
- No project save/reopen (`.dscan`) yet
- Installer is not yet code-signed
