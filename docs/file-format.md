# File Format / 文件格式

文件格式尚未最终定稿。本文记录第一阶段方向。

The file format is not final. This document records the initial direction.

## 项目包 / Project Package

首选本地项目布局是目录包：

The preferred local project layout is a directory package:

```text
Example.realcanvas/
  manifest.sqlite
  chunks/
  assets/
  thumbnails/
  strokes/
  backups/
```

Android 端也可以把这个目录包导出为压缩归档，用于分享和备份。

Android may also export this directory package as a compressed archive for
sharing and backup.

## 清单 / Manifest

`manifest.sqlite` 应存储：

`manifest.sqlite` should store:

- 项目元数据。
- 对象 ID。
- 对象类型。
- 包围盒。
- 所属分块。
- 资产引用。
- 缩略图引用。
- 更新时间。
- 删除标记。
- 基础关系。

- Project metadata.
- Object ids.
- Object types.
- Bounding boxes.
- Chunk membership.
- Asset references.
- Thumbnail references.
- Update timestamps.
- Deletion markers.
- Basic relationships.

## 资产 / Assets

原始文件应存放在清单之外：

Original files should live outside the manifest:

```text
assets/
  <asset-id>.<extension>
```

缩略图和派生预览应当可以丢弃并重新生成。

Thumbnails and derived previews should be disposable and rebuildable.

## 版本 / Versioning

每个项目都应记录文件格式版本。未来迁移必须显式、可测试。

Every project should store a file-format version. Future migrations must be
explicit and testable.

