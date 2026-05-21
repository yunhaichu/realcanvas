# Roadmap

## Phase 0: Technical Prototype

Target: prove that the core Android canvas approach is viable.

- Infinite pan and zoom.
- Basic stylus strokes.
- Text nodes.
- Image nodes.
- SQLite manifest.
- Viewport-based object loading.
- Thumbnail generation.
- Large-board stress test with at least 10,000 lightweight objects.

## Phase 1: Android MVP

Target: a local Android tablet app that can be used for real notes and mixed
content boards.

- OPPO Pad 4 Pro first-device adaptation.
- Stylus pen, eraser, pressure, and palm rejection baseline.
- Text, image, file, and URL nodes.
- Selection, move, resize, delete, group.
- Local project save and open.
- Project import and export.
- Undo and redo.
- Autosave.
- Crash recovery.
- Partial rendering and partial activation.

## Phase 2: Android Alpha

Target: reliability and enough polish for early testers.

- Improved handwriting latency and stroke smoothing.
- PDF preview as file node.
- Audio and video as lazy-loaded media nodes.
- Search by node title and text.
- Tags and regions.
- Performance dashboard for large boards.
- Backup and restore.
- Export to image and markdown.

## Phase 3: Shared Core

Target: prepare for cross-platform development.

- Extract shared document model.
- Document file format versioning.
- Define platform-neutral canvas operations.
- Build conformance tests for project files.
- Prepare desktop and iPad client planning.

## Later

- Desktop clients.
- iPad client.
- Cloud sync.
- Collaboration.
- AI-assisted search and organization.
- Plugin system.

