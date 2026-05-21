# Architecture / 架构

## 核心思路 / Core Idea

RealCanvas 应该把画布当作空间文档。打开项目时应先加载清单和索引，而不是一次性加载所有节点、图片、文件和笔迹。

RealCanvas should treat a board as a spatial document. Opening a project should
load a manifest and indexes first, not every node, image, file, and stroke.

## 分层 / Layers

```text
Android UI / Android 界面
  Compose shell, menus, panels, project navigation
  Compose 外壳、菜单、面板、项目导航

Canvas View / 画布视图
  Pan, zoom, stylus input, selection, rendering, invalidation
  平移、缩放、手写输入、选择、渲染、局部刷新

Scene Model / 场景模型
  Nodes, strokes, groups, links, bounding boxes, layers
  节点、笔迹、分组、连接、包围盒、图层

Storage Engine / 存储引擎
  SQLite manifest, chunk files, assets, thumbnails, backups
  SQLite 清单、分块文件、资产、缩略图、备份

Future Extensions / 未来扩展
  Shared core, sync, collaboration, AI, desktop clients
  共享核心、同步、协作、AI、桌面客户端
```

## 对象生命周期 / Object Lifecycle

画布对象应该有明确的激活状态：

Canvas objects should move through explicit activation states:

```text
indexed       只加载 id、类型、边界和元数据
              only id, type, bounds, and metadata are loaded

preview       加载缩略图或简化几何
              thumbnail or simplified geometry is loaded

interactive   可以选择、移动和连接
              object can be selected, moved, and linked

editing       加载完整数据用于编辑
              full object data is loaded for editing

active        媒体或重内容正在播放、解码或完整激活
              media or heavy content is playing or fully decoded
```

这个生命周期是大画布稳定性的基础，尤其是在存在大量图片、文件、媒体和手写笔迹时。

This lifecycle is required for large boards with many images, files, media
objects, and handwriting strokes.

## 渲染原则 / Rendering Principles

- 按视口查询可见对象。
- 谨慎预加载视口附近内容。
- 低缩放级别使用简化几何。
- 优先渲染缩略图，再加载完整资产。
- 尽可能使用脏区刷新。
- 局部编辑不应触发全画布重建。

- Query visible objects by viewport.
- Keep near-viewport prefetch conservative.
- Use simplified geometry at low zoom.
- Render thumbnails before full assets.
- Invalidate dirty regions when possible.
- Avoid global canvas rebuilds for local edits.

