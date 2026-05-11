# note +create（创建笔记）

> **前置条件：** 先阅读 [`../zsxq-shared/SKILL.md`](../../zsxq-shared/SKILL.md) 了解认证和安全规则。

本 skill 对应 shortcut：`zsxq-cli note +create`。

在知识星球创建一条个人笔记，支持文本和图片附件。

> [!CAUTION]
> 这是**写入操作** —— 执行前确认笔记内容无误。

## 命令

```bash
# 创建一条笔记
zsxq-cli note +create --text "示例笔记内容"

# 多行内容（使用 \n 换行）
zsxq-cli note +create --text "示例笔记第一行\n示例笔记第二行"

# JSON 格式输出（含新建 note_id）
zsxq-cli note +create --text "示例笔记内容" --json

# 带图片的笔记
zsxq-cli note +create --text "记录" --files idea.jpg
```

## 参数

| 参数 | 必填 | 说明 |
|------|------|------|
| `--text <text>` | **是** | 笔记内容 |
| `--files <paths>` | 否 | 附件路径，多个用逗号分隔（仅图片） |
| `--json` | 否 | 输出原始 JSON（含 note_id、create_time） |

## 输出

```
✓ Note created
{
  "note_id": "444555666777",
  "create_time": "2026-04-01T15:45:31.007+0800",
  "text": "示例笔记内容"
}
```

## 说明

- 笔记与主题（Topic）是两类不同内容，笔记不属于任何星球

## 参考

- [zsxq-note-edit](zsxq-note-edit.md) — 编辑笔记
- [zsxq-note-delete](zsxq-note-delete.md) — 删除笔记
- [zsxq-topic-create](../../zsxq-topic/references/zsxq-topic-create.md) — 在星球内发布主题（帖子）
- [zsxq-shared](../../zsxq-shared/SKILL.md)
