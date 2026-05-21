# RealCanvas

RealCanvas 是一个开源、本地优先的无限画布项目。第一阶段专注 Android
平板，首台参考设备为 OPPO Pad 4 Pro；长期目标是发展为跨平台画布系统。

RealCanvas is an open-source, local-first infinite canvas project. The first
implementation focuses on Android tablets, with OPPO Pad 4 Pro as the reference
device. The long-term goal is a cross-platform canvas system.

## 项目目标 / Goals

- 构建一个能承载大画布的稳定无限画布。
- 支持手写笔优先的笔记、批注和自由绘制。
- 支持混合内容：文本、手写、图片、文件、音频、视频和网址。
- 从第一天开始采用局部渲染和局部激活，避免大文件崩溃。
- 保持文件格式开放、可迁移、可文档化。
- 先做 Android 平板，再扩展到其他平台。

- Build a stable infinite canvas for large local boards.
- Support stylus-first note taking, annotation, and freehand drawing.
- Store mixed content: text, handwriting, images, files, audio, video, and URLs.
- Use partial rendering and partial activation from day one.
- Keep the file format open, portable, and documented.
- Start with Android tablets, then expand to other platforms.

## 第一版暂不做 / Non-Goals For The First Version

- 云同步。
- 多人协作。
- AI 画布编辑。
- 完整 PDF、音频、视频编辑。
- 桌面端和 iPad 端。

- Cloud sync.
- Multi-user collaboration.
- AI canvas editing.
- Full PDF, audio, and video editing.
- Desktop and iPad clients.

这些是未来扩展方向。第一版重点解决本地画布引擎、存储模型、手写输入和大画布稳定性。

These are future extension areas. The first version focuses on the local canvas
engine, storage model, stylus input, and large-board stability.

## 仓库结构 / Repository Layout

```text
realcanvas/
  apps/
    android/        Android 平板 App，第一阶段实现目标
                    Android tablet app, first target implementation
  core/             未来共享画布模型和算法
                    Future shared canvas model and algorithms
  docs/             产品、存储、渲染和设备适配文档
                    Product, storage, rendering, and device adaptation docs
  tools/            开发、压测和项目文件检查工具
                    Developer, benchmark, and project-file utilities
```

## 当前目标 / Current Target

第一台开发和测试设备：

First development and test device:

- OPPO Pad 4 Pro
- OPPO Pencil / compatible stylus
- Android tablet form factor

Android 版本会优先适配 OPPO Pad 4 Pro，但不会锁死在单一设备。它是第一台性能、
手写和大画布稳定性基准设备，不是唯一支持设备。

The Android app should remain device-aware but not device-locked. OPPO Pad 4 Pro
is the first performance, stylus, and large-board stability baseline, not the
only supported device.

## 架构方向 / Architecture Direction

RealCanvas 把画布当作“空间文档”，而不是一张必须整体加载的巨大场景。

RealCanvas treats a canvas as a spatial document, not a single giant scene that
must be loaded all at once.

```text
UI shell / 界面外壳
  Toolbar / panels / project navigation
  工具栏 / 面板 / 项目导航

Canvas engine / 画布引擎
  Viewport culling / level of detail / dirty regions / stylus input
  视口裁剪 / 分级细节 / 脏区刷新 / 手写输入

Object model / 对象模型
  Nodes / strokes / groups / links / bounds / layers
  节点 / 笔迹 / 分组 / 连接 / 边界 / 图层

Storage / 存储
  SQLite manifest / chunks / assets / thumbnails / backups
  SQLite 清单 / 分块 / 资产 / 缩略图 / 备份

Extensions / 扩展层
  Sync / collaboration / AI / import-export
  同步 / 协作 / AI / 导入导出
```

大画布打开时只应先加载项目清单，再按视口加载可见或临近可见内容。

Large boards should load the project manifest first, then load only visible or
near-visible content.

## 许可证 / License

本仓库使用 GNU Affero General Public License v3.0。

This repository is licensed under the GNU Affero General Public License v3.0.

