# All-in-One Lark Skill

[简体中文](README.zh.md)

This collection merges 28 upstream Feishu/Lark skills into a single [`agent-lark-skill` entry](agent-lark-skill/SKILL.md).

## Merge and loading

The original entries are now guides under `agent-lark-skill/references/lark-*/GUIDE.md`. Their references, scripts, and assets moved with them, and internal paths were updated. The four legacy meeting names still route to the meeting guide.

Start with `SKILL.md`, open the guide for the relevant domain, then load the references needed for the current operation.

## Version

The local adaptation baseline is `lark-cli 1.0.100`. Individual guides retain any version declared by the upstream skill.

## Upstream and licensing

This collection independently repackages skills distributed by the official Lark CLI project. [Upstream repository](https://github.com/larksuite/cli)

For upstream material covered by MIT, redistribution must include the original copyright notice (© 2026 Lark Technologies Pte. Ltd.) and the full license text. [Upstream MIT license](https://raw.githubusercontent.com/larksuite/cli/v1.0.100/LICENSE) · [Included MIT license](LICENSES/Lark-MIT.txt)

The slide icon index uses data from ByteDance's IconPark, whose upstream data is licensed under Apache-2.0. [IconPark license](https://github.com/bytedance/IconPark/blob/master/LICENSE) · [Included IconPark license](LICENSES/IconPark-Apache-2.0.txt)
