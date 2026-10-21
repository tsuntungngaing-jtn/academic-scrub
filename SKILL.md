---
name: academic-scrub
description: >-
  Use when the user asks to academic-scrub, /academic-scrub, 去AI腔, 去免责条款,
  去元话语, 去作业腔, 去过程污染, 去 rubric 味, scrub assignment/course/prompt/user/agent
  leakage, journal-language audit, defensive-disclaimer scrub, figure/caption language
  scrub, or re-check a final academic draft (EN/CN) for process contamination or
  AIGC defensive / lab-notebook / reviewer-response tone.
disable-model-invocation: true
---

# Academic Scrub — Semantic Academic Scrubber

Remove **process contamination** and **AIGC journal-language artefacts** from academic prose. Do **not** invent sophistication, inflate claims, or rewrite for “less AI detection.”

> Preserve content; remove provenance and defensive packaging.

The reader should meet the research—definitions, evidence status, scope—not the assignment, prompt, drafting chat, or an author repeatedly explaining what the work is *not*.

**Authority:** [`semantic-rules.md`](semantic-rules.md). **Search cues:** [`reference-patterns.md`](reference-patterns.md). **Before/after:** [`examples.md`](examples.md).

Domain examples in those files are illustrative only. Apply the **functions** to any field (CS, bio, materials, social science, etc.).

## Hard constraints

- Judge **function**, not vocabulary. No forbidden-word model.
- Do not invent literature, evidence, causal claims, limitations, or terminology.
- Do not change numbers, equations, units, citation keys/numbers, figure/table numbers, or technical terms (except proven typos).
- Preserve research logic, specificity, disciplinary voice, and evidence-matched hedging.
- Keep useful section/figure/table/equation navigation. Keep required AI-declaration cover text.
- Course brief / rubric is a silent compliance list only; its wording must not enter the body.
- Default: drop prose em dash `—`; numeric ranges may use en dash `–`.
- Mechanical swaps forbidden (`this report`→`this review`, blanket active→passive) unless meaning improves.
- Intervention order: delete → rewrite framing → lexical swap last. Smallest change that removes contamination. Stop polishing.
- Missing symbols / broken placeholders (`image`, empty equation objects): mark `[AUTHOR CHECK: …]`; never guess.

## Contamination layers (function)

| Layer | What to remove | Keep |
|---|---|---|
| **L0** | User/prompt/agent/feedback/draft/revision narration | Research itself |
| **L1** | Assignment, course, rubric, marking as **authority** | Methods that happen to have been taught |
| **L2** | Document-assembly narration (“what comes next because the task needs it”) | Locating Table/Fig/Eq/Section for substance |
| **L3** | Rhetorical self-defence, empty “not intended / no claim / does not establish…”, reviewer-response tone, command-like instructions to the reader | Scientific uncertainty, limits, necessary negation, positive model definition |
| **L4** | Unnecessary, repetitive, generic, inflated filler; lab-notebook “we” stacks; abrupt topic dumps; caption/figure defensive essays | Polished technical prose that already does work |

**Evidence discipline** (constraint, not a layer): verb strength ≤ evidence (`calibrate` / `validate` / `verify` / `establish` only when earned). Do not weaken mechanisms into generic “better performance”.

### Target register (L3–L4)

Shift dense stacks of:

- “explaining what was *not* done / preventing misunderstanding / enumerating exclusions”

toward:

- scientific definition · evidence status · methodological scope · controlled comparison · physical/logical interpretation · concise limitation

Prefer: definition, `X denotes…`, `X is evaluated by…`, `Y remains to be established`, `The analysis considers…`  
Reduce: defensive disclaimer, reviewer-response tone, first-person laboratory narration, AI-style caveats, command-like methodological instructions.

**Three post-edit questions (every revised paragraph):**

1. Does this mainly say what the research *is*, or what it *is not*? Prefer the former.
2. Is this scientific logic, or a reply to an imagined reviewer? Prefer the former.
3. If this limitation sentence were deleted, would the reader’s sense of scope change? If not, delete or move to Discussion/Limitations.

## Workflow

```
Academic scrub pass:
- [ ] 1 Backup
- [ ] 2 Audit (quote → function → keep/delete/rewrite; do not edit yet)
- [ ] 3 Revise L0→L4 (five-step procedure + conversion patterns in semantic-rules)
- [ ] 4 Residual scan (semantic; high-frequency defensive lexicon density)
- [ ] 5 Quality questions; deliver Parts A–D (or short log if user asked quick-only)
```

### 1. Backup

`TARGET` → `TARGET_backup_before_scrub_YYYYMMDD_HHMMSS.ext` (same folder).

### 2. Audit

Scan body, captions, **in-figure text** (axes, legends, annotations), table titles/heads/cells/notes. Skip bibliographic titles and required AI-declaration blocks.

For each candidate: **excerpt → function → if deleted, is a scientific fact lost?**

Also flag: undefined first-use symbols; paragraphs that open on a local gadget without a topic sentence; Methods cluttered with “does not include…”; captions carrying methodology defence.

### 3. Revise

1. Identify function.
2. If no scientific fact/inference/assumption/limit/relationship would be lost → delete.
3. If content is needed but framing is contaminated → drop provenance/process/defence; keep the proposition. Convert requirement/command language into research consequence. Prefer **positive definition** over negative exclusion stacks (see semantic-rules §5).
4. Re-read the **paragraph** (not only the sentence): continuity, variables, uncertainty, references.
5. Stop. Do not keep rewriting “to sound more academic.”

`.docx`: if runs are fragmented, write the whole paragraph into the first run and clear the rest.

### 4. Residual scan

Still showing: user/prompt/feedback/drafts; coursework/rubric as provenance; assembly narration; repeated empty disclaimers; formulaic closures; dense `does not` / `cannot` / `no claim` / `we use|define|select` / `Importantly|Notably|Critically` without scientific need?

Do **not** require disappearance of `this study`, hedging, `however`/`therefore`, or scientific negation.

### 5. Quality test

**A Provenance** — could a reader tell this answered a prompt/assignment/conversation?  
**B Integrity** — did science disappear? Restore it.  
**C Defence** — repeated “does not mean…” without interpretive work?  
**D Rubric smell** — checklist / command voice? Rewrite as research.  
**E Over-edit** — changed only because it “sounded AI”? Restore.  
**F Scope placement** — exclusions restated every Results paragraph that belong once in Methods scope or Limitations?

## Output contract

Default for a full manuscript / “审校” / “去AI腔终版” request — **four parts**:

**Part A — Diagnosis** (only real issues; no padded rows)

| Location | Original | Problem | Revision principle |

**Part B — Revised body**  
Full revised text: keep section structure, citation numbers, equation numbers, Fig/Table refs; no new numbers/results/conclusions. Unrecoverable placeholders → `[AUTHOR CHECK: …]`.

**Part C — Figures / Tables language audit**  
Per figure: Caption; X/Y axes; Legend; Panel headings; Annotations. If already fine: `No language revision required.`  
Per table: title, column heads, footnotes, cell wording.

**Part D — High-frequency defensive / AIGC lexicon audit**  
Recount and justify each *retained* hit among cues in [`reference-patterns.md`](reference-patterns.md) (L3–L4 density section). Goal: lower repetitive density, not zero.

If the user asks only for a quick scrub of a short excerpt: deliver revised text + short layer changelog; Parts A–D optional.

Also write `*_scrubbed` artifact and `ACADEMIC_SCRUB_LOG.md` when editing files on disk.

## Do not

Rewrite every sentence; strip all meta-language; auto-replace report/assignment/course; remove legitimate hedging, limits, or technical negatives; add transitions or conclusions; turn numbers into “better performance”; blanket-passivize every `we`; mix this job with `nature-polishing` (venue style) or `academic-humanizer` (grant/voice layers) unless the user explicitly requests both.
