# Rendering Model

## Requirement

RealCanvas must not render or activate the full board at once.

## Viewport Query

Each frame should begin with the current viewport:

```text
screen viewport
  -> world bounds
  -> spatial query
  -> visible object list
  -> level-of-detail selection
  -> render pass
```

## Level Of Detail

Objects should have multiple representations:

- Far zoom: bounds, icons, or aggregated previews.
- Mid zoom: thumbnails and simplified strokes.
- Near zoom: full node surfaces and editable strokes.

## Dirty Regions

Local edits should invalidate only the affected board region when possible.
Global redraws are acceptable for early prototypes, but should not become the
permanent architecture.

## Stress Targets

Early benchmarks should include:

- 10,000 lightweight nodes.
- 1,000 image nodes using thumbnails.
- Large stroke sets split by region.
- Fast pan and zoom across populated areas.

