# note +delete（删除笔记）

> **前置条件：** 先阅读 [`../zsxq-shared/SKILL.md`](../../zsxq-shared/SKILL.md) 了解认证和安全规则。

本 skill 对应 shortcut：`zsxq-cli note +delete`。

删除指定笔记。删除后**不可恢复**。

> [!CAUTION]
> 这是**不可逆的破坏性操作** —— 删除后笔记将永久消失，无法恢复。执行前必须向用户确认：
> 1. 目标笔记（note_id）及其内容
> 2. 明确用户确实要删除

## 命令

```bash
# 删除笔记
zsxq-cli note +delete --note-id 444555666777
```

## 参数

| 参数 | 必填 | 说明 |
|------|------|------|
| `--note-id <id>` | **是** | 笔记 ID（从 `note +list` 获取） |

## 推荐工作流

```bash
# 第一步：确认笔记内容
zsxq-cli note +detail --note-id 444555666777

# 第二步：向用户确认后执行删除
zsxq-cli note +delete --note-id 444555666777
```

## 参考

- [zsxq-note-detail](zsxq-note-detail.md) — 删除前确认笔记内容
- [zsxq-note-list](zsxq-note-list.md) — 查看笔记列表获取 note_id
- [zsxq-shared](../../zsxq-shared/SKILL.md)