# note +detail（查看笔记详情）

> **前置条件：** 先阅读 [`../zsxq-shared/SKILL.md`](../../zsxq-shared/SKILL.md) 了解认证和安全规则。

本 skill 对应 shortcut：`zsxq-cli note +detail`。

获取单条笔记的完整详情，包括内容正文、创建时间等。

## 命令

```bash
# 查看笔记详情
zsxq-cli note +detail --note-id 444555666777

# JSON 格式输出
zsxq-cli note +detail --note-id 444555666777 --json
```

## 参数

| 参数 | 必填 | 说明 |
|------|------|------|
| `--note-id <id>` | **是** | 笔记 ID（从 `note +list` 获取） |
| `--json` | 否 | 输出原始 JSON |

## 参考

- [zsxq-note-list](zsxq-note-list.md) — 查看笔记列表获取 note_id
- [zsxq-note-edit](zsxq-note-edit.md) — 编辑笔记
- [zsxq-shared](../../zsxq-shared/SKILL.md)
