# Parsing reference (conf.researchr.org)

## Typical URLs

- Research Track / Accepted papers:  
  `https://conf.researchr.org/track/{conf-id}/{conf-id}-research-track`  
  (user may paste this or a close variant)
- Program:  
  `https://conf.researchr.org/program/{conf-id}/program-{conf-id}/`

`{conf-id}` examples: `icse-2025`, `fse-2025`, `ase-2025`, `issta-2025` (confirm from the user URL).

## Fetch tips

- Pages are often 2–3MB HTML; use `curl --max-time 20~30` and save to disk, then parse locally.
- Accepted content may live in tab panes (`Accepted papers` / `event-overview`), not above the fold.
- Prefer HTML parse over waiting on JS-rendered views.
- Some tracks also have an **Awards** tab listing Distinguished Paper titles — use it when Program badges are missing.

## Accepted papers section

### Pattern A (e.g. ICSE 2025): inline abstract + Tags

```html
<h5> Author1, Author2, "Paper Title" </h5>
<p><b>Abstract:</b> ...</p>&nbsp;Tags: "Tag A", "Tag B" &nbsp;<br>
```

Extract: authors (names), title (quoted), abstract, Tags list.

### Pattern B (e.g. ICSE 2026 / FSE 2026): overview list + AJAX modal abstract

Accepted list may only show titles/authors in `#event-overview` **without** per-paper `Tags:` / `Abstract:`.

Abstracts load via WebDSL modal POST:

- URL: `https://conf.researchr.org/eventDetailsModalByAjaxConferenceEdition`
- Copy hidden inputs from the page form whose `action` is that URL
- Set the form’s `event-id-input` field to the paper event id
- Set the long `eventDetailsModalByAjaxConferenceEdition_ia0_…` action key to `1`
- Also send `__ajax_runtime_request__=event-modal-loader` and `context={conf-id}` (e.g. `icse-2026`)
- Response JSON: concatenate `append` action `value` HTML fragments

**Abstract cleaning (critical):** `event-description` often contains `<p>` abstract paragraphs **plus** preprint links and author profile cards. Do **not** `clean()` the whole div. Take only non-empty `<p>...</p>` text **before** the first `publication-link` / `class="media"` / `profile/{conf-id}/` marker.

### Categories when Tags are missing

If Accepted papers has no `Tags:`, fall back to **Program session area** names for Research Track / Research Papers sessions (e.g. session title `AI for Software Engineering 12` → category `AI for Software Engineering`, strip trailing session index). State this fallback in the overview note. Prefer one session area per paper when that is how the program is structured.

## Uncategorized / unscheduled papers (title + abstract)

Some accepted papers never appear in the Program schedule (or their modal header has no session link). Treat them as **uncategorized until classified** — not as a final category.

### Procedure

1. Collect all papers lacking Tags and lacking a Program session area
2. For each, read **title + abstract** (already fetched)
3. Assign **exactly one** category:
   - Prefer an existing category used by other papers in this digest
   - Otherwise choose a clear SE topic label consistent with the venue’s emerging taxonomy
4. Optionally keep an internal note (`category_source: title_abstract`) in working data; do not surface `Uncategorized` in final Markdown
5. Overview should report how many papers used this fallback

### Classification heuristics (guidance, not hard rules)

| Signal in title/abstract | Likely category family |
| --- | --- |
| LLM/code generation/repair/agents for SE tasks | AI for Software Engineering |
| Fairness/robustness/energy of ML models; SE for ML systems | Software Engineering for AI |
| Fuzzing, test generation, GUI/unit testing, oracles | Testing and Fuzzing / Testing and Quality |
| Vulnerability, exploit, malware, smart-contract security, TEE | Security and Vulnerability |
| Static/dynamic analysis, verification, formal methods, SMT | Program Analysis and Verification |
| Debugging, root-cause, fault localization, incident diagnosis | Debugging and Fault Diagnosis |
| Developers, OSS communities, code review as human process | Human and Social Aspects |
| Mining repos, ecosystem empirical mining | Mining Software Repositories |
| Dependencies, migration, release engineering, maintenance | Evolution and Maintenance |
| Mobile, UI, cloud/microservices, performance/energy systems | Systems, Mobile, and UI |
| Requirements, specifications, API specs, design models | Requirements and Specifications |

When unsure between two labels, pick the one matching the **primary contribution** (problem solved), not every technique mentioned.

### Examples (style)

- Title about ransomware I/O correlation → Security and Vulnerability  
- Title about microservice multi-root-cause localization → Debugging and Fault Diagnosis  
- Title about LLM code editing / repo-level repair → AI for Software Engineering  
- Title about ML fairness / bias mitigation trade-offs → Software Engineering for AI  

## Category consolidation (10–15)

### When

After initial category assignment, if distinct labels **> 15** (common when Program sessions are fine-grained: Fuzzing, GUI Testing, Test Generation, …), merge before writing final files.

If the venue naturally has **fewer than 10**, do **not** invent empty categories to pad.

### How

1. List categories with counts and 2–4 sample titles each
2. Draft a merge map: fine label → coarse label (about 10–15 coarse labels)
3. For borderline fine categories (e.g. `SE and AI`, `Performance`, `Logging`), skim titles/abstracts and split or override per paper when needed
4. Apply map; rewrite `papers.json` tags, overview, `category_*.md`, `awarded_papers.md`
5. Delete obsolete fine `category_*.md` files
6. QC: every paper categorized; category file counts match; final distinct count ∈ [1, 15] and ideally ≥ 10 when enough topical diversity exists

### Suggested coarse taxonomy (adapt per venue)

Use as a starting palette, rename to match venue wording:

1. AI for Software Engineering  
2. Software Engineering for AI  
3. Testing and Fuzzing *(or Testing and Quality)*  
4. Program Analysis and Verification  
5. Security and Vulnerability  
6. Debugging and Fault Diagnosis  
7. Human and Social Aspects  
8. Mining Software Repositories  
9. Evolution and Maintenance  
10. Systems, Mobile, and UI *(or + Autonomy)*  
11. Requirements and Specifications  
12. Architecture and Design *(optional if volume warrants)*  

### Multi-label vs single-label

| Source | After consolidation |
| --- | --- |
| Program session areas (usually one session/paper) | Prefer **one** coarse category per paper; counts sum to total |
| Official Accepted Tags (often multi-label, e.g. ICSE 2025) | Map each fine tag → coarse; **dedupe**; multi-label OK; note sums may exceed total |

### Overview wording examples

- Session fallback + consolidation:  
  *Original program sessions were fine-grained and were consolidated into the coarser categories above; N papers without a schedule slot were classified from title/abstract.*
- Official Tags + consolidation:  
  *Original Accepted Papers Tags (~K labels) were consolidated into the coarser categories above; a paper may still have multiple categories.*

## Program page (affiliations & awards)

Split on Research Track markers, e.g.:

```html
<div class="prog-track">Research Track</div>
<div class="performers">
  <a ...>Name</a><span class="prog-aff"> Affiliation</span>, ...
</div>
```

Track names vary (`Research Track`, `Research Papers`). Avoid catastrophic regexes that span huge gaps with `[\s\S]*?` across the whole Program HTML — use marker splits + local windows.

Awards / artifacts often appear as:

```html
data-facet-badge="Award Winner"
data-facet-badge="Award Winner Best Artifact"
data-facet-badge="Artifact-Available"
data-facet-badge="ACM SIGSOFT Distinguished Paper Award"
```

Map (names vary by year; keep the page’s wording when clearer):

- `Award Winner` / `Distinguished Paper Award` / `ACM SIGSOFT Distinguished Paper Award` → Awards
- badges containing `Best Artifact` / `Artifact Award Winner` → artifact award (and Award Winner if combined)
- `Artifact-*` → Artifact badges

## Title merge

Normalize before join:

- lowercase
- unify quotes/dashes
- strip non-alphanumeric to spaces
- collapse whitespace

If exact match fails, use high-threshold token Jaccard / containment; fall back to author-name set match for affiliations.

## Markdown formatting pitfall

Never glue metadata lines:

```markdown
**中文总结:** …
**Abstract:** …
```

Always:

```markdown
**中文总结:** …

**Abstract:** …
```

Same rule between Categories / Awards / Artifact badges / 中文总结 / Abstract.

## papers.json shape (suggested)

```json
{
  "title": "...",
  "authors": [{"name": "...", "affiliation": "..."}],
  "tags": ["..."],
  "abstract": "...",
  "awards": ["Award Winner"],
  "artifact_badges": ["Artifact-Available"],
  "summary_zh": "..."
}
```
