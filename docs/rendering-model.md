# Rendering Model / 渲染模型

## 要求 / Requirement

RealCanvas 不能一次性渲染或激活整张画布。

RealCanvas must not render or activate the full board at once.

## 视口查询 / Viewport Query

每帧应从当前视口开始：

Each frame should begin with the current viewport:

```text
screen viewport / 屏幕视口
  -> world bounds / 世界坐标范围
  -> spatial query / 空间查询
  -> visible object list / 可见对象列表
  -> level-of-detail selection / 分级细节选择
  -> render pass / 渲染
```

## 分级细节 / Level Of Detail

对象应有多种表现形式：

Objects should have multiple representations:

- 远距离缩放：边界、图标或聚合预览。
- 中等缩放：缩略图和简化笔迹。
- 近距离缩放：完整节点表面和可编辑笔迹。

- Far zoom: bounds, icons, or aggregated previews.
- Mid zoom: thumbnails and simplified strokes.
- Near zoom: full node surfaces and editable strokes.

## 脏区 / Dirty Regions

局部编辑应尽可能只刷新受影响区域。早期原型可以接受全局重绘，但不能把全局重绘变成永久架构。

Local edits should invalidate only the affected board region when possible.
Global redraws are acceptable for early prototypes, but should not become the
permanent architecture.

## 压测目标 / Stress Targets

早期基准测试应包括：

Early benchmarks should include:

- 10,000 个轻量节点。
- 1,000 个使用缩略图的图片节点。
- 按区域切分的大量笔迹。
- 在高密度区域快速平移和缩放。

- 10,000 lightweight nodes.
- 1,000 image nodes using thumbnails.
- Large stroke sets split by region.
- Fast pan and zoom across populated areas.

