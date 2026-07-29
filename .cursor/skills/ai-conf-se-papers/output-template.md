# 输出 Markdown 模板

对齐范例：`iclr2025_se_coding/ICLR2025_SE_Coding_Papers.md`。

## 文件路径

```text
{venue_lower}{YEAR}_se_coding/{VENUE}{YEAR}_SE_Coding_Papers.md
```

## 文档骨架

```markdown
# {VENUE} {YEAR} 软工 / Coding 相关论文

> 按统一筛选标准从 {VENUE} {YEAR} 主会录用论文中整理。共 **{N}** 篇。

## 各类数量

| 类别 | 数量 |
|------|------|
| Coding Agent / SWE | {n} |
| Testing / Analysis / Security | {n} |
| ... | ... |
| **合计** | **{N}** |

展示类型：Oral {a}；Spotlight {b}；Poster {c}

## Coding Agent / SWE（{n}）

### 1. [poster] Paper Title Here

- **作者（单位）**：Alice（MIT）；Bob（Stanford University）
- **中文总结**：一两句说明工作内容与软工意义。必要时第三句点出设定或价值。
- **Link**：https://...
- **Abstract**：全文或官方摘要原文（保留英文原文，不要翻译替代）。

### 2. [oral] Another Title

- **作者（单位）**：...
- **中文总结**：...
- **Link**：...
- **Abstract**：...

## Testing / Analysis / Security（{n}）

...
```

## 字段规则

| 字段 | 规则 |
|------|------|
| 标题行 level | 小写：`[oral]` / `[spotlight]` / `[poster]`；无 spotlight 的会议可只有 oral/poster |
| 作者（单位） | `姓名（单位）`，多人用中文分号 `；` 连接；无单位则只写姓名 |
| 中文总结 | 1–3 句中文；基于摘要，不编造 |
| Link | 优先官方 paper/virtual/OpenReview/Anthology 页面 |
| Abstract | 英文原文；清理多余空白与 HTML 实体 |

## 类别节

- 只输出 **有论文的类别**
- 类内排序：oral → spotlight → poster，同类按标题字母序（或保持稳定排序即可）
- 类名与筛选标准中的建议类别一致；可有合理细分（如 `Code Editing / IDE Assist`），但避免过度碎片化

## 清理

写入最终 MD 后，删除同目录临时文件（`_raw*`、`candidates*`、`papers_final*`、`CHECKLIST` 等），**只留这一份 MD**。
