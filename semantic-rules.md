# Semantic rules (authority)

Loaded from SKILL.md during a scrub pass. Judge **function**, not vocabulary. Patterns are **domain-agnostic**; examples may use any field.

## Purpose

Remove process contamination and AIGC packaging (defensive disclaimers, lab-notebook narration, reviewer-response tone, caption essays) while preserving research content, reasoning, evidence, terminology, uncertainty, and disciplinary voice.

The goal is **not** “sound more academic,” “sound more human,” or “evade AI detectors.”

Remove assignment/course/rubric/user/agent/prompt/drafting provenance and unnecessary defensive framing **when those elements do not belong to the scholarly content itself**.

Express caution through **precise model definition, evidence status, and scope**—not through repetitive self-defence.

## 1. Core principle

**Preserve content; remove provenance and defensive packaging.**

Legitimate (keep): research claims, methodological decisions, evidence, limitations, uncertainty, interpretation, definitions, comparisons, figure/table reading aids, scope statements.

Contamination (remove or rewrite): assignment requirements, course terminology as authority, rubric logic, user/agent instructions, prompts, previous drafts, “what I was asked to do,” “what the document will contain,” defensive stacks added only to prevent hypothetical criticism, command-like instructions to the author/reader (unless protocol/standard text).

Never confuse the two. No forbidden-word model. Words such as report, section, requirement, limitation, following, therefore, note, important can be legitimate or contaminated depending on function.

## 2. L0 — Interaction / provenance leakage (highest priority)

Remove: as requested/instructed; based on your instructions; the user asked; according to / following the prompt; the prompt requires; the instructions above; as specified in the task; in response to feedback; the previous/revised version; I have revised; I was asked to; the requested structure; I/we will now; the following response; the answer below.

The document should contain the research, not the conversation.

## 3. L1 — Assignment / course / rubric leakage

Remove educational-task provenance that is not research: assignment, coursework, rubric, marking criteria, assessment, learning outcomes, “for this assignment”, “to satisfy the requirement”.

Keep methods that were taught; remove the **course as source of authority** if irrelevant.

## 4. L2 — Document-production meta-discourse

Legitimate navigation (keep): “Table II summarizes…”, “Equation (3) defines…”, “Figure 1(b) shows…”.

Unnecessary assembly narration (delete/simplify): “The remaining checks follow…”, “The table below addresses the requirements…”, “A named product is given in Section IV” (when only previewing compliance).

## 5. L3 — Defensive / self-protective prose (expanded)

Preserve epistemic qualification (uncertainty, error, model limits, scope, evidence strength). Compress or remove rhetorical self-defence whose main job is to prevent hypothetical criticism.

### 5.1 High-density disclaimer cues (search, then classify)

does not establish / cannot establish / cannot independently establish / is not claimed / no claim is made / is not intended to / should not be interpreted as / is intentionally not / is not part of this model / is outside the scope / rather than retaining / if this cannot… declare… / no particular X is claimed to…

These are **not** banned. Excess density makes prose read like a risk notice, AI safety clause, or reviewer reply.

### 5.2 Conversion patterns (prefer)

| Instead of | Prefer |
|---|---|
| X does not establish Y. | Y requires independent evidence from Z. / Local Y therefore requires information beyond X alone. |
| X is not part of this model. | The present formulation describes Y under Z conditions. Then, if needed: W remains beyond the present constitutive / statistical / experimental formulation. |
| No claim is made that X. | X remains to be established experimentally. / Camera-/device-specific performance against these requirements has not yet been established. |
| This should not be interpreted as X. | The present interpretation is restricted to Y. |
| If X fails, use / declare / recompute Y. | If X is not satisfied, Y would provide the appropriate basis for subsequent analysis. |
| Damage, creep, and piezoresistivity are not part of this model. *(when unused in the argument)* | Delete the exclusion list, or state once what the model *does* describe. |
| A high value alone cannot establish… | Performance is therefore evaluated using both A and B. |
| The simulation does not prove… | Experimental validation remains necessary for… |
| These examples do not establish clinical suitability. *(if clinical is off-topic)* | The examples motivate the sensing / modelling configuration. Or delete. |

**Negative-definition rule:** do not define an object mainly by what it is not, unless the negation is scientifically necessary.

If an excluded mechanism does **not** affect the paper’s conclusions, prefer silence over manufacturing a new reviewer hook.

### 5.3 Methods vs Limitations placement

Methods should answer: what the model/experiment **is**.

Prefer once: “The model combines … Homogeneous isotropic layers and one-way coupling are assumed.”

Do **not** re-insert “does not include damage / creep / …” after every result. Move unused exclusions to Discussion / Limitations / a single model-scope paragraph.

### 5.4 Command-like methodological instructions

Watch: declare, retain, reject, recompute, use X instead, do not interpret, must be treated as — when not a standard/protocol/algorithm step.

Body text states **what follows scientifically**, not what the reader must do.

### 5.5 Self-defence in Results

Prefer controlled-comparison / dual-metric framing over “X alone cannot establish…”. Prefer evidence-status sentences over “does not prove…”.

## 6. L4 — AI-style surface patterns and narrative artefacts

After removing contamination, inspect formulaic and packaging prose. Do not rewrite merely because prose is polished.

### 6.1 Formulaic fillers

Suspect when unnecessary/repetitive: Critically / Importantly / Notably / More importantly / It should be noted that / It is important to note that / In particular (stacked) / Consequently / Accordingly / Therefore (overused).

Often: “Importantly, the 0.60 mm design…” → “The 0.60 mm design…”.

Also: In recent years; delve/underscore/intricate/tapestry/pivotal/seamless; stacked Moreover/Furthermore/Additionally; not only X but also Y; rule-of-three padding; inflated closures.

### 6.2 First-person laboratory narration

`We` is not banned. Continuous stacks in parameter definition / control studies / method recipes are.

| Avoid stacking | Prefer |
|---|---|
| We use \(t\) for thickness. | Conductor thickness is denoted by \(t\). / \(t\) denotes… |
| We change \(t\) while keeping \(E_c\) fixed. | Thickness sensitivity is evaluated by varying \(t\) while holding \(E_c\) constant. |
| We selected 1 GPa. | \(E_c=1\) GPa is selected as the midpoint of the investigated range. |

Do **not** blanket-passivize. Prefer: `X is defined as…` / `X denotes…` / `X is evaluated by…` / `The analysis considers…` / `The comparison isolates…`.

### 6.3 Topic sentences and abrupt detail dumps

Paragraphs must not open on a local gadget (encoder, camera, mesh size, GF, voltage, clinical aside, software field name) without establishing: problem → gap → why this comparison.

Prefer: need → problem → method → metric → bound. First sentence = topic sentence.

Test: if the previous paragraph were deleted, would the opening still make sense? If not, add a short premise—not a transition adverb.

### 6.4 First-use definitions

Every subscript, software field, custom probe, coordinate, material parameter, strain component, sensitivity metric, mesh metric must be defined at first appearance with physical/operational meaning.

Bad: “Green–Lagrange strain \(E_{xx}\)” alone when \(x\) is non-obvious.  
Better: “the axial Green–Lagrange strain \(E_{xx}\), where \(x\) denotes the prescribed loading direction.”

Software builtins: name the field and what it extracts (“…using the solver’s solid.eXX field variable…”). Author-defined probes/operators: say they are defined, and where.

### 6.5 calibrate / validate / verify / establish

Do not interchange.

- **calibration** — reference truth / standard / independent datum used to set parameters  
- **verification** — implementation correctness  
- **validation** — agreement with reality / independent data  
- **mesh independence / convergence** — not “validation” by default  

Otherwise: quantify, evaluate, assess, characterize, compare, isolate, investigate, estimate.

### 6.6 Figures: captions vs body

Caption = how to **read** the figure (what is shown; panels; markers/lines/shading; essential conditions).  
Body = why the figure was built that way; methodology defence; limitations.

Move out of captions: why a point is omitted; why a method is inapplicable; “should not be interpreted as…”; long result discussion.

### 6.7 In-figure text (mandatory audit)

Axes, legends, panel titles, annotations, callouts, colorbars, schematic labels, dashed-line labels.

1. No full sentences in annotations; prefer short labels (“Selected design”, “Design point”).  
2. No defensive tags (“Not validated”, “Not claimed”, “Cannot establish”) unless that taxonomy *is* the object of study; prefer neutral status (“Experimental verification pending”, “Geometry-driven response”).  
3. No insider voice (“our design”, “current best”) → “present design”, “selected configuration”, “baseline”, “optimized configuration”.  
4. Axes = physical quantity + unit.  
5. Abbreviations consistent with body (one working name per quantity).

If wording is already fine: `No language revision required.`

### 6.8 Tables

Titles/heads/cells/notes: avoid sentence-length or command-like cells. Prefer terse heads (“Selection rationale”) and short cells (“Midpoint of investigated range”). Titles must not duplicate a full Methods paragraph.

### 6.9 Placeholders and conversion damage

Search: `image`, `[image]`, empty equation objects, broken subscripts, unresolved symbols (e.g. “reference strain, image at image mm”).

Restore from source when possible. Otherwise `[AUTHOR CHECK: missing equation/symbol in source]` — never invent.

## 7. Do not mechanically replace academic meta-language

Never auto-map: this report→this review; this assignment→this study; active→passive everywhere. Preferred order: (1) delete, (2) rewrite directly, (3) lexical substitution last.

## 8. Do not over-scrub legitimate academic language

Preserve when useful: this study/work/analysis/paper; Section/Table/Figure/Equation pointers; the literature; the proposed method; the model; the results; the comparison.

## 9. Research logic must survive

Never remove or weaken substantive reasoning. Keep causal relations, assumptions, design criteria, equations, ranges, numbers, comparisons, constraints, objectives, evidence chains, literature gaps, limitations.

Do not turn mechanism into “therefore improves performance.”

**Preserve scientific boundaries; delete defensive tone.** Keep: model assumptions, coupling direction, strain definition, sampling location, mesh criteria, calibration definition, uncertainty, parameter ranges, baselines, validation thresholds, why a model cannot emit a quantity it does not contain.

## 10. Avoid rubric-driven writing

Watch: “The requirement is…”; “The table addresses…”; “evaluates X, Y, and Z to satisfy…”. Rewrite around the research problem.

## 11. Convert requirement language into research language

- “must consider both A and B” → “evaluated using both A and B”  
- “The report needs to compare…” → “The two approaches are compared in terms of…”  
- “The following section discusses the limitations.” → “The main limitations are…”

## 12. Scientific negation vs defensive negation

Keep essential distinctions (“Reaction force is not the measurand.”) or recast positively if clearer. Remove interactional negation unless the distinction is part of the method.

## 13. Do not explain every potential misunderstanding

Avoid the AI stack: define X → explain X → explain what X is not → warn not to confuse X with Y. Prefer definition → relevant implication → move on.

## 14. Closure sentences

Ask whether the sentence adds an inference not already obvious. If no, delete or merge.

## 15. Preserve appropriate hedging

Keep may/might/suggests/indicates/consistent with/approximately when evidence supports them. Match confidence to evidence. Do not strip caution that changes scope.

## 16. Do not add claims

No new literature, evidence, causal claims, interpretations, limitations, or terminology unless asked.

## 17. Do not remove specificity

Never replace precise numbers/mechanisms with generic superiority language.

## 18. Figures and tables (structural)

Keep locating language. Remove assignment-style reasons for inclusion.

## 19. Literature-review language

Keep concrete paper–claim links; do not force “literature shows…” generics.

## 20. Technical clarification vs conversation leakage

Keep: “Voltage is calculated from configuration A rather than B.”  
Drop: “not the value from the course example / previous chat.”

## 21. Paragraph-level reasoning

Do not scrub sentences in isolation. Ask whether the sentence introduces evidence, defines a variable, constrains interpretation, explains a methodological choice, or connects reasoning.

## 22. Five-step rewrite

1. Classify function.  
2. Necessity: would a scientifically relevant fact be lost? If no, delete.  
3. Rewrite only if needed: drop assignment/user/agent/process/defence; keep the proposition; prefer positive definition / evidence status.  
4. Re-read the paragraph.  
5. Stop. Do not polish for “more academic”.

## 23. Minimal intervention

Delete → compress defence → rewrite framing → fix grammar from deletion → stop.

## 24. Residual scan (semantic, not blacklist)

Check residuals of L0–L4 and density of disclaimer / we-stack / Importantly-stack cues. Optimize functional relevance, not lexical purity.

## 25. Anti-overcorrection

A clean document is **not** zero meta-language, zero “this study”, zero hedging, zero however/therefore, zero negation, zero “we”, zero “does not”.

Success = the same research, less evidence of the process that produced it, and caution expressed as definition/scope/evidence status rather than repetitive self-defence.

## 26–30. Worked examples

See [`examples.md`](examples.md).

## 31. Must not

Rewrite every sentence; remove every section/report; auto-replace report→study; remove legitimate hedging/limits/technical negatives; invent vocabulary or unsupported conclusions; alter numbers/equations/citations/figure numbers; turn concrete claims generic; force concision at the expense of reasoning; blanket-passivize.

## 32–34. Quality test and governing preferences

See SKILL.md quality questions A–F and Parts A–D output contract.

When uncertain, prefer: semantic preservation over stylistic improvement; direct scientific statements over explanations of why the statement is being made; necessary qualification over defensive qualification; research logic over rubric logic; minimal intervention over comprehensive rewriting.
