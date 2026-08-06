# Changelog

## Unreleased

### Added
- Smart Undo dispatcher on Ctrl+Shift+Z for plugin-title-based routing.
- ShaperBox 3 Smart Undo provider using window-bounded image matching.
- Multi-permutation image search support for undo references via undo*.png.
- Debug overlay and detailed match/failure diagnostics for Smart Undo.

### Changed
- Redo route standardized to Ctrl+Y.
- Redo delegates to plugin-specific redo when VST shortcuts are enabled.
- Smart Undo click anchor now uses bias values tuned for cropped references.
