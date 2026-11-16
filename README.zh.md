# 飞书合集技能

[English](README.md)

本合集将 28 个上游飞书 `lark-*` 技能合并为一个 [`agent-lark-skill` 入口](agent-lark-skill/SKILL.md)。

## 合并与加载

原入口统一迁入 `agent-lark-skill/references/lark-*/GUIDE.md`。参考文档、脚本和素材一并迁移，并更新了内部路径。4 个会议旧名称仍可路由到会议指南。

按需加载时，先读 `SKILL.md`，再打开对应业务指南，最后读取当前操作所需的参考文档。

## 版本

本地适配基线为 `lark-cli 1.0.100`。各子指南保留了上游声明的版本号。

## 上游与版权

本合集基于官方 Lark CLI 发布的飞书技能独立整理。[上游仓库](https://github.com/larksuite/cli)

再分发受 MIT 许可覆盖的上游内容时，须随附原版权声明（© 2026 Lark Technologies Pte. Ltd.）和完整许可文本。[上游 MIT 许可](https://raw.githubusercontent.com/larksuite/cli/v1.0.100/LICENSE) · [随附 MIT 许可](LICENSES/Lark-MIT.txt)

幻灯片图标索引使用了字节跳动 IconPark 的数据，相关上游数据采用 Apache-2.0 许可。[IconPark 许可](https://github.com/bytedance/IconPark/blob/master/LICENSE) · [随附 IconPark 许可](LICENSES/IconPark-Apache-2.0.txt)
