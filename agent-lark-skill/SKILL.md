---
name: agent-lark-skill
description: "处理飞书、Lark、lark-cli 和妙搭（Spark/Miaoda）任务时使用，涵盖消息与群聊、邮箱、通讯录、云文档、电子表格、多维表格、幻灯片、画板、Markdown、云空间和知识库，以及日历、视频会议与妙记、任务、审批、考勤、OKR、事件订阅、认证授权和原生 OpenAPI。也适用于飞书资源 URL、token 或旧 lark-* 技能名。"
metadata:
  requires:
    bins: ["lark-cli"]
---

# 飞书技能路由

1. 按用户要做的操作从下表选择子指南。一次任务涉及多个域时，在进入各域时依次加载对应指南。
2. 在子指南中找到具体操作，每次只打开当前步骤需要的参考和前置资料。已经读过的文件在同一任务中可复用。
3. Markdown 链接相对于当前文档解析。命令示例中的子指南自带脚本和素材从该指南目录定位。用户文件及 CLI 的路径参数仍按具体指南和命令的工作目录规则处理。

## 业务入口

| 用户意图 | 读取 |
| --- | --- |
| 收发消息、搜索聊天、管理群聊、下载聊天附件、交互卡片及其回调 | [即时通讯](references/lark-im/GUIDE.md) |
| 草拟、收发或搜索飞书邮件，管理邮箱标签、联系人和收信规则 | [邮箱](references/lark-mail/GUIDE.md) |
| 按姓名或邮箱查联系人、解析 open_id、搜索机器人或智能体 | [通讯录](references/lark-contact/GUIDE.md) |
| 读写文档正文、操作思维笔记、处理文档附件、在文档中插入画板 | [云文档](references/lark-doc/GUIDE.md) |
| 操作电子表格单元格、公式、样式、筛选、图表或透视表 | [电子表格](references/lark-sheets/GUIDE.md) |
| 操作 Base、数据表、记录、视图、表单、BaseApp/AppMode、模板或自动化 | [多维表格](references/lark-base/GUIDE.md) |
| 新建演示文稿、读取或编辑幻灯片页面 | [幻灯片](references/lark-slides/GUIDE.md) |
| 查看、导出或编辑已有画板 | [画板](references/lark-whiteboard/GUIDE.md) |
| 创建、读写、局部更新或比较原生 Markdown 文件 | [Markdown](references/lark-markdown/GUIDE.md) |
| 按名称搜索文件，管理云盘文件、目录、权限、评论、版本、导入或导出 | [云空间](references/lark-drive/GUIDE.md) |
| 管理知识空间、成员、Wiki 节点、层级和快捷方式 | [知识库](references/lark-wiki/GUIDE.md) |
| 查询或安排日程、添加参会人、查忙闲、预订会议室 | [日历](references/lark-calendar/GUIDE.md) |
| 查询历史或进行中的视频会议、逐字稿、智能纪要、妙记和妙记待办；机器人入会或会中互动 | [视频会议](references/lark-meeting/GUIDE.md) |
| 汇总指定日期范围内的会议纪要、生成会议周报 | [会议纪要汇总](references/lark-workflow-meeting-summary/GUIDE.md) |
| 汇总今天、明天或本周的日程和未完成待办 | [日程待办摘要](references/lark-workflow-standup-report/GUIDE.md) |
| 管理普通待办、任务清单、子任务或任务智能体 | [任务](references/lark-task/GUIDE.md) |
| 查询和处理审批待办、查看审批实例或发起审批 | [审批](references/lark-approval/GUIDE.md) |
| 查询自己的打卡记录 | [考勤](references/lark-attendance/GUIDE.md) |
| 管理 OKR 周期、目标、关键结果、对齐和进展 | [OKR](references/lark-okr/GUIDE.md) |
| 创建、设计、开发或部署妙搭应用，管理其数据、角色、环境、监控或触发器 | [妙搭](references/lark-apps/GUIDE.md) |
| 订阅或持续消费飞书事件流 | [事件订阅](references/lark-event/GUIDE.md) |
| 配置 CLI、登录或授权、选择用户或机器人身份、处理 scope、退出码 10 或 `_notice` | [共享规则与认证](references/lark-shared/GUIDE.md) |
| 已有业务指南和 CLI 已注册命令无法覆盖，需要查询并调用原生飞书 API | [OpenAPI 探索](references/lark-openapi-explorer/GUIDE.md) |
| 将飞书 API 或多步流程封装成可复用技能 | [技能制作](references/lark-skill-maker/GUIDE.md) |

## 链接和跨域操作

- 按资源 URL 的路径、对象类型和操作意图分流，同样适用于 `doubao.com`。`/docx/`、`/sheets/`、`/base/`、`/slides/`、`/minutes/` 分别进入对应业务指南。`/app/app_…`、`/page/<token>` 或妙搭运行域名进入妙搭，一般的 BaseApp `/app/<token>` 进入多维表格。
- `/wiki/<token>` 表示 Wiki 节点。管理空间或节点结构时读取知识库指南。操作节点底层对象时，按 [Wiki token 解析](references/lark-shared/references/lark-wiki-token-routing.md) 识别对象类型并进入对应指南。
- 对文件做搜索、权限、独立评论、格式导入或导出时进入云空间。随文档正文读取评论用云文档。编辑在线原生 `.md` 用 Markdown，把本地 Markdown 导入为在线 Docx 用云空间。
- 查会议产物或处理妙记中的待办用视频会议。管理未来安排和会议室用日历。按主题收集或整理知识库资料时，从知识库指南进入其中链接的云空间工作流。

## 旧名称

提到某个旧 `lark-*` 名称时，从本入口打开同名目录的 `GUIDE.md`。[lark-minutes](references/lark-minutes/GUIDE.md)、[lark-note](references/lark-note/GUIDE.md)、[lark-vc](references/lark-vc/GUIDE.md) 和 [lark-vc-agent](references/lark-vc-agent/GUIDE.md) 都转入视频会议指南，可直接读取视频会议。
