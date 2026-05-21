# Architecture

## Core Idea

RealCanvas should treat a board as a spatial document. Opening a project should
load a manifest and indexes first, not every node, image, file, and stroke.

## Layers

```text
Android UI
  Compose shell, menus, panels, project navigation

Canvas View
  Pan, zoom, stylus input, selection, rendering, invalidation

Scene Model
  Nodes, strokes, groups, links, bounding boxes, layers

Storage Engine
  SQLite manifest, chunk files, assets, thumbnails, backups

Future Extensions
  Shared core, sync, collaboration, AI, desktop clients
```

## Object Lifecycle

Canvas objects should move through explicit activation states:

```text
indexed       only id, type, bounds, and metadata are loaded
preview       thumbnail or simplified geometry is loaded
interactive   object can be selected, moved, and linked
editing       full object data is loaded for editing
active        media or heavy content is playing or fully decoded
```

This lifecycle is required for large boards with many images, files, media
objects, and handwriting strokes.

## Rendering Principles

- Query visible objects by viewport.
- Keep near-viewport prefetch conservative.
- Use simplified geometry at low zoom.
- Render thumbnails before full assets.
- Invalidate dirty regions when possible.
- Avoid global canvas rebuilds for local edits.

