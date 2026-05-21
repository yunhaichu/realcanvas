# Performance Targets / 性能目标

这些目标是早期工程目标，不是最终承诺。

These targets are early engineering goals, not final guarantees.

## 原型目标 / Prototype Targets

- 打开大项目时先只加载元数据。
- 10,000 个轻量对象仍能保持平移和缩放响应。
- 图片缩略图懒加载。
- 不解码屏幕外媒体。
- 手写延迟足够低，可以真实记笔记。

- Open a large project by loading only metadata first.
- Keep pan and zoom responsive with 10,000 lightweight objects.
- Load image thumbnails lazily.
- Avoid decoding off-screen media.
- Keep stylus ink latency low enough for real note taking.

## MVP 目标 / MVP Targets

- 10,000 个对象仍可导航。
- 1,000 个图片节点不耗尽内存。
- 大画布重启后可恢复。
- 自动保存不阻塞书写。
- 项目文件可以备份和恢复。

- 10,000 objects remain navigable.
- 1,000 image nodes do not exhaust memory.
- Large boards recover after app restart.
- Autosave does not block drawing.
- Project files can be backed up and restored.

## 观测指标 / Instrumentation

Android 应用后续应暴露内部诊断：

The Android app should eventually expose internal diagnostics:

- 可见对象数量。
- 已加载对象数量。
- 已激活资产数量。
- 图片缓存大小。
- 帧耗时。
- 手写延迟。
- 存储写入延迟。

- Visible object count.
- Loaded object count.
- Active asset count.
- Image cache size.
- Frame timing.
- Stroke latency.
- Storage write latency.

