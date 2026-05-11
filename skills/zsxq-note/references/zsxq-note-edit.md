# note +edit（编辑笔记）

> **前置条件：** 先阅读 [`../zsxq-shared/SKILL.md`](../../zsxq-shared/SKILL.md) 了解认证和安全规则。

本 skill 对应 shortcut：`zsxq-cli note +edit`。

编辑已有笔记的内容。未修改的字段自动保留。

> [!CAUTION]
> 这是**写入操作** —— 执行前确认修改内容无误。

## 命令

```bash
# 修改笔记内容
zsxq-cli note +edit --note-id 444555666777 --text "新的笔记内容"

# JSON 格式输出
zsxq-cli note +edit --note-id 444555666777 --text "新的笔记内容" --json
```

## 参数

| 参数 | 必填 | 说明 |
|------|------|------|
| `--note-id <id>` | **是** | 笔记 ID（从 `note +list` 获取） |
| `--text <text>` | 否 | 新内容（不传则保留原内容） |
| `--files <paths>` | 否 | 新附件，多个用逗号分隔（仅图片，替换原有附件） |
| `--clear-files` | 否 | 清除所有附件 |
| `--json` | 否 | 输出原始 JSON |

## 推荐工作流

```bash
# 第一步：确认当前笔记内容
zsxq-cli note +detail --note-id 444555666777

# 第二步：确认无误后执行编辑
zsxq-cli note +edit --note-id 444555666777 --text "新的笔记内容"
```

## 参考

- [zsxq-note-detail](zsxq-note-detail.md) — 编辑前查看笔记内容
- [zsxq-note-create](zsxq-note-create.md) — 创建笔记
- [zsxq-shared](../../zsxq-shared/SKILL.md)