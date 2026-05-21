# Contributing

RealCanvas is early-stage. The first priority is correctness, stability, and a
document model that can survive long-term development.

## Development Principles

- Keep the canvas local-first.
- Avoid loading the whole board when a region is enough.
- Prefer documented file formats over hidden app state.
- Treat large-board performance as a product feature, not an optimization pass.
- Keep device-specific code isolated behind capability checks.

## First Target Platform

The first app target is Android tablet. OPPO Pad 4 Pro is the initial reference
device for stylus behavior, latency, and large-canvas testing.

Future platforms should reuse the same document model instead of creating
incompatible file formats.

## Code Style

Detailed style rules will be added after the Android project is scaffolded.

## License

By contributing, you agree that your contribution will be licensed under the
same license as this repository.

