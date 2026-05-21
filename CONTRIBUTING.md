# Contributing / 贡献指南

RealCanvas 目前处于早期阶段。第一优先级是正确性、稳定性，以及能支撑长期演进的文档模型。

RealCanvas is early-stage. The first priority is correctness, stability, and a
document model that can survive long-term development.

## 开发原则 / Development Principles

- 保持本地优先。
- 能局部加载时，不加载整张画布。
- 优先使用公开、文档化的文件格式。
- 把大画布性能当作产品能力，而不是后期优化项。
- 设备特定代码必须隔离在能力检测和适配层之后。

- Keep the canvas local-first.
- Avoid loading the whole board when a region is enough.
- Prefer documented file formats over hidden app state.
- Treat large-board performance as a product feature, not an optimization pass.
- Keep device-specific code isolated behind capability checks.

## 首个目标平台 / First Target Platform

第一阶段目标是 Android 平板。OPPO Pad 4 Pro 是手写行为、延迟和大画布测试的初始参考设备。

The first app target is Android tablet. OPPO Pad 4 Pro is the initial reference
device for stylus behavior, latency, and large-canvas testing.

未来平台应该复用同一套文档模型，不应产生彼此不兼容的文件格式。

Future platforms should reuse the same document model instead of creating
incompatible file formats.

## 代码风格 / Code Style

Android 工程脚手架完成后会补充具体代码风格。

Detailed style rules will be added after the Android project is scaffolded.

## 许可证 / License

提交贡献即表示你同意贡献内容使用本仓库相同许可证发布。

By contributing, you agree that your contribution will be licensed under the
same license as this repository.

