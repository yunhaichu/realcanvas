# Performance Targets

These targets are early engineering goals, not final guarantees.

## Prototype Targets

- Open a large project by loading only metadata first.
- Keep pan and zoom responsive with 10,000 lightweight objects.
- Load image thumbnails lazily.
- Avoid decoding off-screen media.
- Keep stylus ink latency low enough for real note taking.

## MVP Targets

- 10,000 objects remain navigable.
- 1,000 image nodes do not exhaust memory.
- Large boards recover after app restart.
- Autosave does not block drawing.
- Project files can be backed up and restored.

## Instrumentation

The Android app should eventually expose internal diagnostics:

- Visible object count.
- Loaded object count.
- Active asset count.
- Image cache size.
- Frame timing.
- Stroke latency.
- Storage write latency.

