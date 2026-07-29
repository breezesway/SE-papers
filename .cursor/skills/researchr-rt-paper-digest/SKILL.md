---
name: researchr-rt-paper-digest
description: >-
  Digests Research Track accepted papers from conf.researchr.org for ICSE, FSE,
  ASE, and ISSTA into categorized Markdown notes with Chinese summaries, awards
  export, and papers.json. Classifies uncategorized papers from title+abstract
  and consolidates categories to 10–15 when too fine-grained. Use when the user
  provides an Accepted papers / Research Track URL, or asks to organize, export,
  summarize, re-categorize, or merge categories for ICSE/FSE/ASE/ISSTA Research
  Track papers.
---

# Researchr Research Track Paper Digest

Organize **Research Track only** accepted papers from `conf.researchr.org` into Markdown digests.

Supported venues: **ICSE, FSE, ASE, ISSTA**.

## When to use

- User names a venue + year and wants Research Track papers organized
- User pastes an Accepted papers / Research Track track URL on researchr
- User asks for category files, Chinese summaries, awarded-paper export, or **category consolidation / re-categorization** for those venues

## Required inputs

Collect if missing:

1. **Venue**: ICSE | FSE | ASE | ISSTA
2. **Year**: e.g. 2025
3. **Accepted papers / Research Track URL** (user usually pastes this)

Scope is fixed: **Research Track only** — do not include SEIP, NIER, Journal-First, etc.

## Output layout

Write under project root (or user-specified path):

```text
{venue_lower}{YEAR}_research_track/
├── {VENUE}_{YEAR}_Research_Track.md   # overview only
├── category_*.md                      # one file per final category
├── awarded_papers.md                  # Award Winner / Best Artifact
└── papers.json                        # structured backup + summary_zh
```

Example: `icse2025_research_track/`.

## Workflow

Copy and track:

```text
Progress:
- [ ] 1. Fetch Accepted papers / Research Track page
- [ ] 2. Fetch Program page (affiliations + awards)
- [ ] 3. Parse & merge fields
- [ ] 4. Resolve categories (Tags → session fallback → title/abstract)
- [ ] 5. Consolidate categories to 10–15 if needed
- [ ] 6. Write overview + category_*.md + papers.json
- [ ] 7. Write Chinese summaries for ALL papers (no sample gate)
- [ ] 8. Insert summaries; fix blank lines between metadata fields
- [ ] 9. Write awarded_papers.md
- [ ] 10. Quality check
```

### 1. Fetch pages

Primary: user-provided Accepted papers / Research Track URL.

Also fetch the conference **Program** page when available:

`https://conf.researchr.org/program/{conf-id}/program-{conf-id}/`

Use short-timeout `curl` (researchr HTML is large). Prefer parsing saved HTML over browser automation.

Parsing details: [reference.md](reference.md).

### 2. Extract & merge

From **Accepted papers** tab/section:

- title, author names, abstract, **Tags** (categories)
- If abstracts/Tags are not inline (e.g. ICSE 2026), fetch abstracts via the event-details AJAX modal and clean carefully — see [reference.md](reference.md)

From **Program** Research Track rows:

- author **affiliations** (`prog-aff`), awards, artifact badges
- If Tags are missing on Accepted papers, use session area names as categories (document this in the overview)

Merge by normalized title. Prefer official **Tags** when present (not CFP Research Areas). A paper may have multiple tags when the source is multi-label.

Also check **Awards** tabs on the track page when Program badges are incomplete.

### 3. Resolve categories (including uncategorized)

Assign categories in this order — **never leave a paper without a category** in the final output:

1. **Official Tags** from Accepted papers (preferred)
2. Else **Program session area** names for Research Track / Research Papers sessions (strip trailing session index, e.g. `Testing 1` → `Testing`)
3. Else **title + abstract classification** (papers with no Tags and not placed in the Program schedule, or modal has no session name)

For step 3 (uncategorized / unscheduled):

- Read the paper’s **title and abstract**
- Assign **one** category that best matches its problem/method contribution
- Prefer an **existing category already used for other papers** in this digest when it fits; only introduce a new label when necessary
- Do **not** invent a leftover bucket like `Uncategorized` / `Unscheduled` / `Other` in the final digest
- Document in the overview note how many papers were classified from title+abstract

See [reference.md](reference.md) for heuristics and examples.

### 4. Consolidate categories (target 10–15)

After initial assignment, count distinct categories.

- If **≤ 15**: keep them (minor rename/normalize for casing duplicates is fine)
- If **> 15**: **merge** into a coarser taxonomy of **10–15** categories before writing final files

Consolidation rules:

- Merge by topical similarity (session/Tag names first; for borderline papers, skim title/abstract)
- Align with a stable SE taxonomy when helpful (AI for SE, SE for AI, Testing, Security, Analysis/Verification, Debugging, Human aspects, MSR, Evolution/Maintenance, Systems/Mobile/UI, Requirements/Design) — **adapt to the venue year**; do not force identical names across years
- Prefer **one primary category per paper** when categories came from Program sessions (usually single-label)
- When source Tags were **official multi-label**, map each fine tag → coarse tag and **dedupe**; multi-label may remain, and overview must note that category sums can exceed total
- Remove obsolete fine-grained `category_*.md` files after rewrite
- State the consolidation in the overview note

Do **not** ask the user for merge approval unless they explicitly want to choose the taxonomy.

### 5. Overview file

`{VENUE}_{YEAR}_Research_Track.md` must contain **only**:

- Title: `{VENUE} {YEAR} Research Track`
- Source: Accepted papers URL
- Total paper count
- Category count table (final categories only)
- Note on category source / consolidation / multi-tag sums if applicable
- Awarded paper count
- Affiliation coverage count if useful

**Do not** append the full paper list to the overview.

### 6. Per-paper Markdown fields

Exact order; **blank line between every `**Field:**` block**:

```markdown
## N. {Title}

**Authors:** Name (Affiliation), Name2 (Affiliation2)

**Categories:** Tag1, Tag2

**Awards:** Award Winner

**Artifact badges:** Artifact-Available

**中文总结:** …

**Abstract:** …
```

Omit `Awards` / `Artifact badges` when absent. Authors without listed affiliation: name only.

### 7. Chinese summaries (full batch)

For **every** paper, write `中文总结` from title + abstract:

- 1–2 sentences preferred; **at most 3**
- Method/problem + key result/contribution
- Do not copy the English abstract
- Keep necessary proper nouns / tool names in English

Style examples:

- 提出 CONI，面向数据库连接器做状态感知测试生成，并通过与参考连接器对比结果找逻辑缺陷；在 5 个主流 JDBC 驱动上发现 44 个未知缺陷（34 个已确认）。
- 提出 Puppy，通过对比「全优化」与「受限优化」执行计划来发现 DBMS 性能退化缺陷（PDB）；在多个数据库上检出 62 个 PDB，其中 54 个为未知缺陷。

Insert after Categories / Awards / Artifact badges and **immediately before** Abstract, with a blank line before Abstract.

Also store as `summary_zh` in `papers.json`.

Large batches: generate in parallel chunks, then merge — still cover 100% of papers.

### 8. Category files

For each distinct **final** category, write `category_{slug}.md`:

- Header: `{VENUE} {YEAR} Research Track — {Tag}`
- Source, count in this category
- All papers that include this Tag (same field blocks as above)

Slug: non-alphanumeric → `_` (e.g. `AI for Software Engineering` → `category_AI_for_Software_Engineering.md`).

### 9. Awarded papers file

`awarded_papers.md`: papers with Award Winner and/or Best Artifact (and equivalent award badges on the page / Awards tab).

Same per-paper fields as category files. Include a short award breakdown table at the top.

### 10. Quality checklist

- [ ] Paper count matches Research Track accepted list
- [ ] **Every paper has ≥ 1 final category** (no Uncategorized / Unscheduled leftovers)
- [ ] Final distinct category count is **10–15** (or naturally fewer if the venue has < 10)
- [ ] Every paper has `中文总结`
- [ ] Every category file paper count matches Tag membership
- [ ] Blank line between `中文总结` and `Abstract` (and between all metadata fields)
- [ ] Overview has **no** full paper dump
- [ ] `papers.json` round-trips key fields

## Do not

- Include non–Research Track papers
- Use CFP Research Areas instead of page Tags
- Leave final papers labeled `Uncategorized` / `Unscheduled` / empty tags
- Keep > 15 fine session/Tag categories without consolidating
- Wait for sample-summary approval before full-batch summaries
- Put the entire paper corpus into the overview Markdown
- Ask the user for permission on routine fetch/classify/merge steps unless they requested to choose the taxonomy
