---
name: ai-conf-se-papers
description: >-
  Filters software-engineering / coding-related papers from AI/ML/NLP conference
  accepted lists (ICLR, ICML, NeurIPS/NIPS, ACL, EMNLP, etc.), then writes one
  categorized Markdown digest with Chinese summaries. Use when the user asks to
  get SE/coding papers from an AI conference (e.g. "获取 NIPS26 软工相关文章"),
  filter SoftEng papers from ICLR/ICML/NeurIPS/ACL, or produce an
  ICLR*_SE_Coding_Papers.md-style digest.
---

# AI Conference → SE / Coding Papers

从 **AI / ML / NLP 顶会录用论文**中筛选与软件工程 / Coding 紧密相关的工作，输出 **一份** Markdown 文档。

与 `researchr-rt-paper-digest` 的区别：后者整理 **ICSE/FSE/ASE/ISSTA** Research Track；本 skill 面向 **ICLR/ICML/NeurIPS/ACL/EMNLP** 等，做 SE 相关性过滤。

## Required inputs

若缺失则向用户确认：

1. **Venue**：ICLR | ICML | NeurIPS (NIPS) | ACL | EMNLP | 其他（需用户给数据源）
2. **Year**：如 2026（用户说 NIPS26 / NeurIPS'26 即 2026）
3. **可选偏好**：只要 agent；不要 benchmark；灰区是否放宽等（默认按严标准）

## Output

写入项目根目录（或用户指定路径）：

```text
{venue_lower}{YEAR}_se_coding/
└── {VENUE}{YEAR}_SE_Coding_Papers.md
```

示例：`neurips2026_se_coding/NeurIPS2026_SE_Coding_Papers.md`

**只保留这一份 MD**（不要留下 checklist / raw json / 多份中间稿，除非用户明确要求保留）。

文档结构必须对齐已有范例 `iclr2025_se_coding/ICLR2025_SE_Coding_Papers.md`。详见 [output-template.md](output-template.md)。

## Workflow

复制并跟踪：

```text
Progress:
- [ ] 1. 解析 venue/year/偏好
- [ ] 2. 获取主会录用论文元数据（title/authors+affil/abstract/level/link）
- [ ] 3. 去重；排除 workshop / blog / journal track / demo
- [ ] 4. 关键词召回候选池
- [ ] 5. 按筛选标准精筛 + 分类
- [ ] 6. 为每篇写 1–3 句中文总结
- [ ] 7. 写入唯一 MD；删掉中间文件
- [ ] 8. 向用户汇报：保留数、分类表、输出路径
```

### 1. 解析输入

- `NIPS` / `NeurIPS` → 统一目录与文件名用 `NeurIPS`（或用户指定）
- 两位数年份：`26` → `2026`

### 2. 获取论文列表

优先官方/结构化源，避免依赖易失效的手工复制：

| Venue | 常见数据源 |
|-------|------------|
| ICLR | `https://iclr.cc/static/virtual/data/iclr-{YEAR}-orals-posters.json`；摘要可能在 `iclr-{YEAR}-abstracts.json`（按 `id` 关联） |
| ICML / NeurIPS | OpenReview venue（如 `ICML.cc/{YEAR}/Conference`、`NeurIPS.cc/{YEAR}/Conference`）；或官网 virtual/proceedings JSON/HTML |
| ACL / EMNLP | ACL Anthology 会议页 / anthology 元数据；或 OpenReview（若该年使用） |

字段尽量补全：`title`, `authors`（含 institution）, `abstract`, `level`（oral/spotlight/poster）, `url`。

同一论文 oral+poster 只保留一条；`level` 取最高展示档（oral > spotlight > poster）。

若 API 有 challenge/登录墙：改用官网 virtual JSON、proceedings 页面，或请用户提供导出文件。

### 3–5. 筛选与分类

**完整标准**见 [filter-criteria.md](filter-criteria.md)（与项目根目录 `se_paper_filter_prompt.md` 一致）。

要点：

- 宁缺毋滥；Coding Agent / SWE 优先
- 排除：纯预训练、泛 agent、speech/channel coding、ML jailbreak「vulnerability」、数学奥赛写代码等
- 灰区默认 drop
- 分类用建议类别；无论文的类别不要空开一节

推荐类别顺序：

1. Coding Agent / SWE  
2. Testing / Analysis / Security  
3. Program Repair / Debugging  
4. Code Editing / IDE Assist（及相近编辑类）  
5. Verification / Program Analysis  
6. Code Retrieval / Maintenance、Security / Binary Analysis（若有）  
7. Code Benchmark (practical)  
8. Code Generation / SE-related（仅强相关）

### 6. 中文总结

每篇 **1–3 句**，说明：做了什么、面向什么 SE 问题、价值/设定。基于摘要，勿编造未提及的数字或结论。

### 7. 写 MD 并清理

严格按 [output-template.md](output-template.md)：

1. 标题 + 总篇数  
2. `## 各类数量` 表格 + 合计  
3. 展示类型一行（Oral / Spotlight / Poster 计数；无则写「无」）  
4. 按类别 `## {类别}（{n}）`，每篇：

```markdown
### {i}. [{oral|spotlight|poster}] {Title}

- **作者（单位）**：Name（Affiliation）；...
- **中文总结**：...
- **Link**：https://...
- **Abstract**：...
```

level 标签小写：`[oral]` / `[spotlight]` / `[poster]`。

完成后删除该目录下临时文件，只留最终 MD。

### 8. 回复用户

简短汇报：venue/year、保留篇数、分类数量、文件路径。可选列 3–5 篇代表性标题。

## Quality checks

- [ ] 仅主会；无 workshop/blog/journal 混入  
- [ ] 无预训练主线、无 ML-jailbreak 误当软件漏洞  
- [ ] 作者尽量带单位；摘要与 link 非空（实在缺失写「（暂缺）」）  
- [ ] 中文总结覆盖全部保留论文  
- [ ] 目录内只有一份最终 MD  

## Examples

**用户**：请使用这个 skill 获取 NIPS26 软工相关的文章  

**执行**：NeurIPS 2026 → 拉录用列表 → 按 filter-criteria 精筛 → 写入 `neurips2026_se_coding/NeurIPS2026_SE_Coding_Papers.md`

**用户**：帮我筛 ICLR 2025 里和 coding agent / 软工相关的论文  

**执行**：可对照已有 `iclr2025_se_coding/ICLR2025_SE_Coding_Papers.md` 的格式与尺度；若用户只要重跑，覆盖写回同路径。
