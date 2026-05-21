# Roadmap / 路线图

## Phase 0: 技术原型 / Technical Prototype

目标：证明 Android 画布路线可行。

Target: prove that the core Android canvas approach is viable.

- 无限平移和缩放。
- 基础手写笔迹。
- 文本节点。
- 图片节点。
- SQLite 项目清单。
- 基于视口的对象加载。
- 缩略图生成。
- 至少 10,000 个轻量对象的大画布压力测试。

- Infinite pan and zoom.
- Basic stylus strokes.
- Text nodes.
- Image nodes.
- SQLite manifest.
- Viewport-based object loading.
- Thumbnail generation.
- Large-board stress test with at least 10,000 lightweight objects.

## Phase 1: Android MVP

目标：做出一个能真实记录笔记和混合资料的 Android 平板本地应用。

Target: a local Android tablet app that can be used for real notes and mixed
content boards.

- OPPO Pad 4 Pro 首台设备适配。
- 手写笔、橡皮、压感和基础掌拒。
- 文本、图片、文件和网址节点。
- 选择、移动、缩放、删除、分组。
- 本地项目保存和打开。
- 项目导入和导出。
- 撤销和重做。
- 自动保存。
- 崩溃恢复。
- 局部渲染和局部激活。

- OPPO Pad 4 Pro first-device adaptation.
- Stylus pen, eraser, pressure, and palm rejection baseline.
- Text, image, file, and URL nodes.
- Selection, move, resize, delete, and group.
- Local project save and open.
- Project import and export.
- Undo and redo.
- Autosave.
- Crash recovery.
- Partial rendering and partial activation.

## Phase 2: Android Alpha

目标：提升可靠性和完成度，让早期用户可以试用。

Target: reliability and enough polish for early testers.

- 优化手写延迟和笔迹平滑。
- PDF 作为文件节点预览。
- 音频和视频作为懒加载媒体节点。
- 按节点标题和文本搜索。
- 标签和区域。
- 大画布性能面板。
- 备份和恢复。
- 导出图片和 Markdown。

- Improved handwriting latency and stroke smoothing.
- PDF preview as file node.
- Audio and video as lazy-loaded media nodes.
- Search by node title and text.
- Tags and regions.
- Performance dashboard for large boards.
- Backup and restore.
- Export to image and Markdown.

## Phase 3: 共享核心 / Shared Core

目标：为跨平台开发做准备。

Target: prepare for cross-platform development.

- 抽离共享文档模型。
- 文档化文件格式版本。
- 定义平台无关的画布操作。
- 建立项目文件一致性测试。
- 准备桌面端和 iPad 端规划。

- Extract shared document model.
- Document file format versioning.
- Define platform-neutral canvas operations.
- Build conformance tests for project files.
- Prepare desktop and iPad client planning.

## Later / 后续

- 桌面客户端。
- iPad 客户端。
- 云同步。
- 协作。
- AI 辅助搜索和整理。
- 插件系统。

- Desktop clients.
- iPad client.
- Cloud sync.
- Collaboration.
- AI-assisted search and organization.
- Plugin system.

