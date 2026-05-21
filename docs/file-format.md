# File Format

The file format is not final. This document records the initial direction.

## Project Package

The preferred local project layout is a directory package:

```text
Example.realcanvas/
  manifest.sqlite
  chunks/
  assets/
  thumbnails/
  strokes/
  backups/
```

Android may also export this directory package as a compressed archive for
sharing and backup.

## Manifest

`manifest.sqlite` should store:

- Project metadata.
- Object ids.
- Object types.
- Bounding boxes.
- Chunk membership.
- Asset references.
- Thumbnail references.
- Update timestamps.
- Deletion markers.
- Basic relationships.

## Assets

Original files should live outside the manifest:

```text
assets/
  <asset-id>.<extension>
```

Thumbnails and derived previews should be disposable and rebuildable.

## Versioning

Every project should store a file-format version. Future migrations must be
explicit and testable.

