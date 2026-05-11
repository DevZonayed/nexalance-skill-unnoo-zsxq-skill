---
name: zsxq-note
version: 1.1.0
description: "知识星球笔记管理：创建笔记、编辑笔记、查看笔记详情、查看笔记列表、删除笔记。当用户需要在知识星球记录个人笔记、编辑笔记、查看笔记详情、删除笔记、或查看历史笔记时使用。"
metadata:
  requires:
    bins: ["zsxq-cli"]
  cliHelp: "zsxq-cli note --help"
---

# note (v1)

**CRITICAL — 开始前 MUST 先用 Read 工具读取 [`../zsxq-shared/SKILL.md`](../zsxq-shared/SKILL.md)，其中包含认证、错误处理规则。**

## Core Concepts

- **笔记（Note）**：个人私密（或特定权限）的记录，支持文本和图片。与主题（Topic）不同，笔记是个人维度的内容。

## Shortcuts（推荐优先使用）

| Shortcut | 说明 |
|----------|------|
| [`+create`](references/zsxq-note-create.md) | 创建一条个人笔记，支持文本和图片附件 |
| [`+list`](references/zsxq-note-list.md) | 查看自己的笔记列表，支持分页 |
| [`+detail`](references/zsxq-note-detail.md) | 查看单条笔记的完整详情 |
| [`+edit`](references/zsxq-note-edit.md) | 编辑笔记内容，需确认后执行 |
| [`+delete`](references/zsxq-note-delete.md) | 删除笔记（不可恢复），需确认后执行 |
