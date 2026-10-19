---
name: academic-scrub
description: >-
  Use when the user asks to academic-scrub, /academic-scrub, 去AI腔, 去免责条款,
  去元话语, 去作业腔, 去过程污染, 去 rubric 味, scrub assignment/course/prompt/user/agent
  leakage, or re-check a final academic draft (EN/CN) for process contamination.
disable-model-invocation: true
---

# Academic Scrub — Semantic Academic Scrubber

Remove **process contamination** from academic prose. Do **not** make the text sound more academic, more human, or less AI-generated.

> Preserve content; remove provenance.

The reader should meet the research, not the assignment, prompt, agent, drafting process, or an author explaining every possible misunderstanding.

**Authority for classification and examples:** read [`semantic-rules.md`](semantic-rules.md) before revising. Cues: [`reference-patterns.md`](reference-patterns.md). Before/after: [`examples.md`](examples.md).

## Hard constraints

- Judge **function**, not vocabulary. No forbidden-word model. `report` / `section` / `requirement` / `following` / `limitation` are not automatically bad.
- Do not invent literature, evidence, causal claims, limitations, or terminology.
- Do not change numbers, equations, units, citation keys/numbers, figure/table numbers, or technical terms (except proven typos).
- Preserve research logic, specificity, disciplinary voice, and evidence-matched hedging.
- Keep useful section/figure/table/equation navigation. Keep required AI-declaration cover text.
- Course brief / rubric is a silent compliance list only; its wording must not enter the body.
- Default: drop prose em dash `—`; numeric ranges may use en dash `–`.
- Mechanical swaps are forbidden (`this report`→`this review`, `assignment`→`study`) unless the sentence’s meaning actually improves.
- Intervention order: delete → rewrite framing → lexical swap last. Smallest change that removes contamination. Stop polishing.

## Contamination layers (function)

| Layer | What to remove | Keep |
|---|---|---|
| **L0** | User/prompt/agent/feedback/draft/revision narration | Research itself |
| **L1** | Assignment, course, rubric, marking as **authority** | Methods that happen to have been taught |
| **L2** | Document-assembly narration (“what comes next because the task needs it”) | Locating Table/Fig/Eq/Section for substance |
| **L3** | Rhetorical self-defence, empty “not intended to…” | Scientific uncertainty, limits, necessary negation |
| **L4** | Unnecessary, repetitive, generic, inflated filler | Polished technical prose that already does work |

Old “evidence discipline” is a **constraint**, not a contamination class: verb strength ≤ evidence; do not weaken mechanisms into generic “better performance”.

## Workflow

```
Academic scrub pass:
- [ ] 1 Backup
- [ ] 2 Audit (quote → function class → keep/delete/rewrite; do not edit yet)
- [ ] 3 Revise by layer L0→L4 using the five-step procedure
- [ ] 4 Semantic residual scan (not a word blacklist)
- [ ] 5 Five quality questions; then a short changelog
```

### 1. Backup

`TARGET` → `TARGET_backup_before_scrub_YYYYMMDD_HHMMSS.ext` (same folder).

### 2. Audit

Scan body, table cells, captions. Skip bibliographic titles (e.g. Handbook) and required AI-declaration blocks.

For each candidate: **excerpt → function (research / method / evidence / interpretation / limit / scope / navigation / assignment / interaction / defence / filler) → if deleted, is a scientific fact lost?**

### 3. Revise (per suspicious passage)

1. Identify function.
2. If no scientific fact/inference/assumption/limit/relationship would be lost → delete.
3. If content is needed but framing is contaminated → drop provenance/process/defence; keep the proposition. Convert requirement language into research language.
4. Re-read the **paragraph** (not only the sentence): continuity, variables, uncertainty, references.
5. Stop. Do not keep rewriting “to sound more academic”.

`.docx`: if runs are fragmented, write the whole paragraph into the first run and clear the rest.

Deliver: `*_scrubbed.docx` (or overwrite if the user asked for a final in-place edit) plus `ACADEMIC_SCRUB_LOG.md`.

### 4. Residual scan (semantic)

Ask whether the text still shows: the user/prompt/instructions/feedback/previous drafts; coursework/rubric/marking as task provenance; how the document was assembled or why a section exists to satisfy a brief; repeated empty disclaimers; formulaic closures with no new inference.

Do **not** require disappearance of `this study`, `this section`, `this report`, hedging, `however`/`therefore`, or scientific negation.

### 5. Quality test then reply

**A Provenance** — could a reader tell this answered a prompt/assignment/conversation?  
**B Integrity** — did science disappear? Restore it.  
**C Defence** — repeated “does not mean…” without interpretive work?  
**D Rubric smell** — checklist voice? Rewrite as research.  
**E Over-edit** — changed only because it “sounded AI”? Restore.

Reply short: what was removed (by layer), output paths, brief Yes/No if a brief was given, leftover human risks.

## Do not

Rewrite every sentence; strip all meta-language; auto-replace report/assignment/course; remove legitimate hedging, limits, or technical negatives; add transitions or conclusions; turn numbers into “better performance”; mix this job with `nature-polishing` (style/venue) or `academic-humanizer` (voice/grant layers).
