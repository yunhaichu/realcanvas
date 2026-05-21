# Product Scope / 产品范围

## 一句话定义 / One-Sentence Definition

RealCanvas 是一个本地优先的无限画布，用于手写笔记、文件、媒体和大画布资料整理。

RealCanvas is a local-first infinite canvas for stylus notes, files, media, and
large boards.

## 第一版 / First Version

第一版是 Android 平板应用。它应该先在 OPPO Pad 4 Pro 上真正好用，然后再承诺更广泛设备支持。

The first version is an Android tablet app. It should be useful on OPPO Pad 4
Pro before broader device support is promised.

## 核心问题 / Core Problem

很多可视化白板在内容变多后会变得不稳定。RealCanvas 要解决的不只是“能画无限画布”，而是大画布在长期使用中仍然响应、可恢复、不会轻易崩溃。

Existing visual boards often become unreliable when the canvas grows large. The
core product challenge is not only drawing on an infinite board, but keeping a
large board responsive and recoverable.

## 第一批内容类型 / First-Class Content Types

- 手写笔迹。
- 文本节点。
- 图片节点。
- 文件节点。
- 网址节点。

- Handwriting strokes.
- Text nodes.
- Image nodes.
- File nodes.
- URL nodes.

后续版本可以深化 PDF、音频、视频和网页捕获能力。

Later versions can deepen support for PDF, audio, video, and web captures.

## 关键产品原则 / Key Product Principles

- 画布可以视觉无限，但运行时激活必须局部化。
- 文件应当可迁移、可检查、可备份。
- 手写必须足够即时。
- 大画布必须优雅降级。
- 未来 AI 能力必须建立在同一文档模型之上，而不是替代它。

- The canvas can be visually infinite, but runtime activation must be local.
- Files should remain portable and inspectable.
- Handwriting must feel immediate.
- Large boards must degrade gracefully.
- Future AI features must build on the same document model, not replace it.

