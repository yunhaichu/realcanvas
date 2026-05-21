# Stylus Adaptation

## First Reference Device

OPPO Pad 4 Pro is the first hardware baseline for development and testing.

## Input Data To Capture

The Android app should record which stylus capabilities are available on the
current device:

- Tool type.
- Pressure.
- Tilt.
- Orientation.
- Hover.
- Eraser mode.
- Button events.
- Pointer source.

Capabilities should be detected at runtime. Device-specific behavior should be
isolated so additional tablets can be added without changing the canvas model.

## Palm Rejection

Palm rejection should start with a conservative rule set:

- Prefer stylus input when stylus is active.
- Ignore broad touch contacts during active stylus strokes.
- Allow explicit touch gestures when no stylus stroke is active.
- Keep a short timeout after stylus hover or stylus down events.

The exact thresholds should be tuned on the reference device.

## Stroke Storage

Strokes should be stored as vector data, not flattened into images.

Each point may include:

- x and y.
- timestamp.
- pressure.
- tilt.
- orientation.
- tool type.

Simplified stroke geometry can be generated for low-zoom rendering.

