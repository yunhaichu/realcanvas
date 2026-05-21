# RealCanvas

RealCanvas is an open-source, local-first infinite canvas for tablets and
desktop devices.

The first implementation target is Android tablets, with OPPO Pad 4 Pro as the
reference device. The long-term goal is a cross-platform canvas engine that can
handle handwriting, files, images, audio, video, links, and very large boards
without loading the whole document into memory.

## Goals

- Build a stable infinite canvas for large local boards.
- Support stylus-first note taking and freehand drawing.
- Store mixed content: text, handwriting, images, files, media, and links.
- Use partial rendering and partial activation from the beginning.
- Keep the file format open and documented.
- Start with Android tablets, then expand to other platforms.

## Non-Goals For The First Version

- Cloud sync.
- Multi-user collaboration.
- AI canvas editing.
- Full PDF, audio, and video editing.
- Desktop and iPad clients.

These are future extension areas. The first version focuses on the local canvas
engine, storage model, stylus input, and large-board stability.

## Repository Layout

```text
realcanvas/
  apps/
    android/        Android tablet app, first target implementation
  core/             Future shared canvas model and algorithms
  docs/             Product, storage, rendering, and device adaptation docs
  tools/            Developer and test utilities
```

## Current Target

The first development device is:

- OPPO Pad 4 Pro
- OPPO Pencil / compatible stylus
- Android tablet form factor

The Android app should remain device-aware but not device-locked. OPPO Pad 4 Pro
is the first performance and stylus baseline, not the only supported device.

## Architecture Direction

RealCanvas treats a canvas as a spatial document, not a single giant scene.

```text
UI shell
  Toolbar / panels / project navigation
Canvas engine
  Viewport culling / level of detail / dirty regions / stylus input
Object model
  Nodes / strokes / groups / links / bounds / layers
Storage
  SQLite manifest / chunks / assets / thumbnails / backups
Extensions
  Sync / collaboration / AI / import-export
```

Large boards must be opened by loading the project manifest first, then loading
only the visible or near-visible content.

## License

This repository is licensed under the GNU Affero General Public License v3.0.

