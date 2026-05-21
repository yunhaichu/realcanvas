# RealCanvas Android

这是 RealCanvas 的第一阶段目标应用。

This is the first target application for RealCanvas.

## 初始目标 / Initial Target

- Android 平板优先。
- OPPO Pad 4 Pro 作为参考设备。
- 手写笔优先的画布交互。
- 本地项目存储。

- Android tablet first.
- OPPO Pad 4 Pro as the reference device.
- Stylus-first canvas interaction.
- Local project storage.

## 计划技术栈 / Planned Stack

- Kotlin。
- 主画布使用 Android 原生自定义 View。
- 周边界面使用 Jetpack Compose。
- SQLite 存储项目清单和空间索引。
- 文件系统存储资产、缩略图、笔迹和备份。

- Kotlin.
- Native Android custom canvas view for the main board.
- Jetpack Compose for surrounding UI.
- SQLite for project manifest and spatial indexes.
- File storage for assets, thumbnails, strokes, and backups.

核心画布不应完全依赖 Compose 渲染。主画布需要直接控制手写事件、局部刷新、视口裁剪和大对象渲染。

The core canvas should not depend entirely on Compose rendering. The main board
needs direct control over stylus events, invalidation, viewport culling, and
large-object rendering.

