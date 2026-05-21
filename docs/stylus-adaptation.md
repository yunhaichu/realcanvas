# Stylus Adaptation / 手写笔适配

## 首台参考设备 / First Reference Device

OPPO Pad 4 Pro 是第一台开发和测试基准设备。

OPPO Pad 4 Pro is the first hardware baseline for development and testing.

## 需要捕获的输入数据 / Input Data To Capture

Android 应记录当前设备可用的手写笔能力：

The Android app should record which stylus capabilities are available on the
current device:

- 工具类型。
- 压感。
- 倾斜。
- 方向。
- 悬停。
- 橡皮模式。
- 按钮事件。
- 指针来源。

- Tool type.
- Pressure.
- Tilt.
- Orientation.
- Hover.
- Eraser mode.
- Button events.
- Pointer source.

能力应运行时检测。设备特定行为必须隔离，方便后续增加更多平板适配。

Capabilities should be detected at runtime. Device-specific behavior should be
isolated so additional tablets can be added without changing the canvas model.

## 掌拒 / Palm Rejection

掌拒先采用保守规则：

Palm rejection should start with a conservative rule set:

- 手写笔处于活动状态时，优先接收手写笔输入。
- 活动笔迹期间忽略大面积触摸。
- 没有手写笔活动时允许明确的触控手势。
- 手写笔悬停或落笔后保留一个短暂保护窗口。

- Prefer stylus input when stylus is active.
- Ignore broad touch contacts during active stylus strokes.
- Allow explicit touch gestures when no stylus stroke is active.
- Keep a short timeout after stylus hover or stylus down events.

具体阈值应在参考设备上调优。

The exact thresholds should be tuned on the reference device.

## 笔迹存储 / Stroke Storage

笔迹应保存为矢量数据，不应只压平成图片。

Strokes should be stored as vector data, not flattened into images.

每个点可以包含：

Each point may include:

- x 和 y。
- 时间戳。
- 压感。
- 倾斜。
- 方向。
- 工具类型。

- x and y.
- timestamp.
- pressure.
- tilt.
- orientation.
- tool type.

低缩放渲染可以使用简化后的笔迹几何。

Simplified stroke geometry can be generated for low-zoom rendering.

