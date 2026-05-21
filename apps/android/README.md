# RealCanvas Android

This is the first target application for RealCanvas.

## Initial Target

- Android tablet first.
- OPPO Pad 4 Pro as the reference device.
- Stylus-first canvas interaction.
- Local project storage.

## Planned Stack

- Kotlin.
- Native Android custom canvas view for the main board.
- Jetpack Compose for surrounding UI.
- SQLite for project manifest and spatial indexes.
- File storage for assets, thumbnails, strokes, and backups.

The core canvas should not depend entirely on Compose rendering. The main board
needs direct control over stylus events, invalidation, viewport culling, and
large-object rendering.

