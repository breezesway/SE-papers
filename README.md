# SE-papers

软件工程顶会论文整理仓库：收录自2025年起 **ICSE / FSE / ASE / ISSTA** Research Track 全部论文，以及 **ICML / NeurIPS / ICLR / ACL** 中与软件工程（SE）/ Coding 紧密相关的论文。论文按主题分类整理，并附中文总结。

## 亮点

1. **软工顶会按主题分类**：ICSE / FSE / ASE / ISSTA Research Track 全部录用论文按主题归类列出，可按兴趣快速筛选阅读。
2. **AI 会议中的软工相关工作**：从 ICML / NeurIPS / ICLR / ACL 等主会录用论文中筛选与 SE / Coding 紧密相关的工作。

## 仓库内容

| 类型 | 会议 | 说明 |
|------|------|------|
| 软工四大顶会 | ICSE、FSE、ASE、ISSTA | Research Track **全部**录用论文，按分类列出 |
| AI / ML / NLP 顶会 | ICML、NeurIPS、ICLR、ACL | 从主会录用论文中**筛选**与 SE / Coding 相关的工作，按分类列出 |

每个软工会议目录通常包含：

- `{VENUE}_{YEAR}_Research_Track.md`：总览（分类统计、来源链接）
- `category_*.md`：各类别论文详情（作者、摘要、中文总结等）
- `awarded_papers.md`：获奖论文
- `papers.json`：结构化备份

AI 会议则为单份 digest：`{VENUE}{YEAR}_SE_Coding_Papers.md`。

## Skills

本仓库提供两个 Skill，用于自动获取与整理论文：

| Skill | 路径 | 用途 |
|-------|------|------|
| `researchr-rt-paper-digest` | [`.cursor/skills/researchr-rt-paper-digest/`](.cursor/skills/researchr-rt-paper-digest/) | 获取软工会议（ICSE / FSE / ASE / ISSTA）某年 Research Track **全部**论文，分类、中文总结、获奖列表、`papers.json` |
| `ai-conf-se-papers` | [`.cursor/skills/ai-conf-se-papers/`](.cursor/skills/ai-conf-se-papers/) | 从 AI 会议（ICLR / ICML / NeurIPS / ACL 等）录用列表中**筛选**与软工 / Coding 相关的论文，输出分类 digest |

可直接说例如：「整理 ASE 2026 Research Track」或「获取 NeurIPS 2026 软工相关文章」。

---

## 2026

### 软工四个会议（Research Track）

| 会议 | 论文数 | Digest |
|------|------:|--------|
| ICSE'26 | 321 | [ICSE_2026_Research_Track.md](2026/icse2026_research_track/ICSE_2026_Research_Track.md) |
| FSE'26 | 211 | [FSE_2026_Research_Track.md](2026/fse2026_research_track/FSE_2026_Research_Track.md) |
| ASE'26 | 181 | [ASE_2026_Research_Track.md](2026/ase2026_research_track/ASE_2026_Research_Track.md) |
| ISSTA'26 | 210 | [ISSTA_2026_Research_Track.md](2026/issta2026_research_track/ISSTA_2026_Research_Track.md) |

### AI 会议中的软工 / Coding 相关论文

| 会议 | 筛选篇数 | Digest |
|------|------:|--------|
| ICML'26 | 51 | [ICML2026_SE_Coding_Papers.md](2026/icml2026_se_coding/ICML2026_SE_Coding_Papers.md) |
| ICLR'26 | 28 | [ICLR2026_SE_Coding_Papers.md](2026/iclr2026_se_coding/ICLR2026_SE_Coding_Papers.md) |
| ACL'26 | 30 | [ACL2026_SE_Coding_Papers.md](2026/acl2026_se_coding/ACL2026_SE_Coding_Papers.md) |
| NeurIPS'26 | — | 待整理 |

---

## 2025

### 软工四个会议（Research Track）

| 会议 | 论文数 | Digest |
|------|------:|--------|
| ICSE'25 | 245 | [ICSE_2025_Research_Track.md](2025/icse2025_research_track/ICSE_2025_Research_Track.md) |
| FSE'25 | 135 | [FSE_2025_Research_Track.md](2025/fse2025_research_track/FSE_2025_Research_Track.md) |
| ASE'25 | 246 | [ASE_2025_Research_Track.md](2025/ase2025_research_track/ASE_2025_Research_Track.md) |
| ISSTA'25 | 107 | [ISSTA_2025_Research_Track.md](2025/issta2025_research_track/ISSTA_2025_Research_Track.md) |

### AI 会议中的软工 / Coding 相关论文

| 会议 | 筛选篇数 | Digest |
|------|------:|--------|
| ICML'25 | 26 | [ICML2025_SE_Coding_Papers.md](2025/icml2025_se_coding/ICML2025_SE_Coding_Papers.md) |
| NeurIPS'25 | 30 | [NeurIPS2025_SE_Coding_Papers.md](2025/neurips2025_se_coding/NeurIPS2025_SE_Coding_Papers.md) |
| ICLR'25 | 21 | [ICLR2025_SE_Coding_Papers.md](2025/iclr2025_se_coding/ICLR2025_SE_Coding_Papers.md) |
| ACL'25 | 25 | [ACL2025_SE_Coding_Papers.md](2025/acl2025_se_coding/ACL2025_SE_Coding_Papers.md) |

---

## 待更新（截止 2026.7.29）

以下信息尚未补全，后续会陆续更新：

- **ICSE'26**：每篇论文的 PDF 链接
- **ISSTA'26**：每篇论文的 PDF 链接；awarded papers 信息
- **ASE'26**：全部论文的 PDF 链接；awarded papers 信息；部分论文尚缺 abstract，对应中文总结亦待补全（目前约 146/181 篇无摘要）
- **NeurIPS'26**：软工 / Coding 相关论文 digest 尚未整理

> 暂无 PDF 链接的论文，绝大多数可在 [Google Scholar](https://scholar.google.com/) 上通过标题检索到。
