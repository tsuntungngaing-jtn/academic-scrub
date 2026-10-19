# Semantic rules (authority)

Loaded from SKILL.md during a scrub pass. Judge **function**, not vocabulary.

## Purpose

Remove process contamination while preserving research content, reasoning, evidence, terminology, uncertainty, and disciplinary voice.

The goal is **not** to sound more academic, more human, or less AI-generated.

Remove references to the assignment, course, rubric, user, agent, prompt, drafting process, document-production process, and unnecessary defensive framing **when those elements do not belong to the scholarly content itself**.

The result should read as though the author is directly presenting the research.

## 1. Core principle

**Preserve content; remove provenance.**

Legitimate (keep): research claims, methodological decisions, evidence, limitations, uncertainty, interpretation, definitions, comparisons, figure/table explanations, scope statements.

Contamination (remove or rewrite when not part of the research): assignment requirements, course terminology as authority, rubric logic, user/agent instructions, prompts, previous drafts/revisions, explanations of what the writer was asked to do, explanations of what the document will contain, defensive statements added only to prevent hypothetical criticism.

Never confuse the two. Do not use a forbidden-word model. Words such as report, section, requirement, analysis, review, method, limitation, instruction, comparison, discussion, requested, following, therefore, note, important can be legitimate or contaminated depending on function.

## 2. L0 — Interaction / provenance leakage (highest priority)

Remove the interaction that produced the text: as requested/instructed; based on your instructions; the user asked/requested; according to / following the prompt; the prompt requires; the instructions above; as specified in the task; in response to / following the feedback; the previous/revised version; I have revised; I was asked to; the requested structure/comparison; the analysis below (when it only narrates generation); I/we will now; the following response; the answer below.

Do not keep interaction context merely because it explains why a sentence exists. The document should contain the research, not the conversation.

## 3. L1 — Assignment / course / rubric leakage

Remove educational-task provenance that is not research: assignment, coursework, course examples/chain, module requirements, rubric, marking criteria/scheme, assessment, learning outcomes, grading, submission, task instructions, project brief, “for this assignment”, “to satisfy the requirement”.

A method taught in a course may still be valid science. Do not remove the method. Remove the **course as source of authority** if it is irrelevant.

**Bad:** The measurement principle used here is the course chain for a resistive gauge.  
**Better:** The measurement principle is based on a resistive gauge: deformation changes the film strain, which changes its resistance and is converted to a voltage by the readout circuit.

**Bad:** A voltage divider is the front end written in the course examples.  
**Better:** The voltage-divider configuration is described in Section II, whereas the reported voltages are calculated using the constant-current configuration.

## 4. L2 — Document-production meta-discourse

Legitimate navigation (keep): “Table II summarizes the material systems considered.” “Equation (3) defines the voltage used in the comparison.” “Figure 1(b) shows the application categories.”

Unnecessary assembly narration (delete or simplify): “A named product is given in Section IV.” “The remaining checks follow in the next sections.” “The table below addresses the requirements…”

A section/figure/table reference is acceptable when it helps the reader locate or interpret substance. It is unnecessary when it only previews what the author will discuss later.

**“The calculations that follow use a constant-current amplifier.”** → **“The calculations use a constant-current amplifier.”**

## 5. L3 — Defensive / self-protective prose

Preserve epistemic qualification (uncertainty, error, model limits, scope, evidence strength). Compress or remove rhetorical self-defence whose main job is to prevent hypothetical criticism: “It should be noted/emphasised that…”, “It is important to acknowledge…”, “This should not be interpreted as…”, “This is not intended/meant to…”, “The authors do not claim…”, “This does not necessarily imply…”, especially when there is no extra scientific payload.

**Defensive:** It should be noted that the following comparison should not be interpreted as an exhaustive ranking of all possible approaches.  
**Better:** The comparison covers the approaches evaluated in this study. (Or delete if scope is already obvious.)

**Negative-definition:** do not define an object mainly by what it is not, unless the negation is scientifically necessary.

Leakage: “They are not a SolidWorks drawing set, and they are not three CAD projects named P, F, and R16.”  
Prefer: “The geometry inputs are the imported flexible-ink mesh and the R12 composite-trace mesh.”

Keep: “The signal is not a direct measurement of strain; it is derived from the resistance change.”

## 6. L4 — AI-style surface patterns

After removing contamination, inspect formulaic prose. Do not rewrite merely because prose is polished. Do not add artificial variation, force every sentence shorter, or make prose informal.

Suspect only when unnecessary, repetitive, generic, inflated, or filler: “It is important/worth noting…”, “In conclusion…”, stacked Furthermore/Moreover/Additionally, “highlights the importance / underscores the significance”, “plays a crucial role”, “comprehensive/multifaceted/nuanced understanding”, “the findings suggest that…” when the evidence already states the claim, repeated therefore/however/thus, rule-of-three padding, generic intros, inflated verbs, unnecessary nominalisation, repeated closures.

These phrases are **not** automatically forbidden.

## 7. Do not mechanically replace academic meta-language

Never auto-map: this report→this review; this assignment→this study; this section→the present section; the following analysis→the present analysis; course examples→established methods — unless the sentence’s academic meaning genuinely improves. Mechanical replacement creates fake academic prose and keeps the contamination.

Preferred order: (1) delete, (2) rewrite directly, (3) lexical substitution last.

## 8. Do not over-scrub legitimate academic language

Preserve when useful: this study/work/analysis/paper/review; the present study/analysis; Section II; Table II; Figure 1; Equation (3); the literature; the proposed method; the experimental setup; the model; the simulation; the results; the comparison.

“this report”, “this section”, and “the following” are not automatically bad.

## 9. Research logic must survive

Never remove or weaken substantive reasoning because it is tightly structured. Keep causal relations, assumptions, design criteria, equations, ranges, numbers, comparisons, constraints, objectives, method choices, evidence chains, literature gaps, limitations, interpretations.

Do not turn “R0 rises by more than q falls, so ΔV rises.” into “The thinner layer therefore improves performance.”

## 10. Avoid rubric-driven writing

Watch: “The requirement is…”; “The table addresses…”; “The analysis evaluates X, Y, and Z to satisfy…”; “The calculation therefore keeps X, keeps Y, and accepts Z…”; “The survey selects these metrics.” Rewrite around the research problem.

**Rubric-like:** The calculation therefore keeps the bending-face strain near 1%, keeps one layout from Fig. 1(a), and accepts a design only when the voltage rises and the local peak falls inside the force limit.  
**Better:** The analysis evaluates a fixed conductor geometry at approximately 1% tensile strain and selects designs that increase voltage output while reducing local strain concentration within the force limit.

## 11. Convert requirement language into research language

If a requirement is substantive, translate function; do not delete the science.

- “The design must consider both voltage output and local strain.” → “The design is evaluated using both voltage output and local strain concentration.”
- “The report needs to compare the two approaches.” → “The two approaches are compared in terms of sensitivity and mechanical demand.”
- “The following section discusses the limitations.” → “The main limitations are…”
- “The analysis needs to remain within the force limit.” → “The reaction force is constrained to 54.72 N.”

## 12. Scientific negation vs defensive negation

Keep essential distinctions (“Reaction force is not the measurand.”) or recast positively if clearer. Remove interactional negation (“These files are not SolidWorks drawings.”) unless the distinction is part of the method; if the fact matters, state the actual inputs.

## 13. Do not explain every potential misunderstanding

Avoid the AI stack: define X, explain X, explain what X is not, explain why X is not Y, warn the reader not to confuse them. Prefer definition → relevant implication → move on. Add contrast only when it changes interpretation.

## 14. Closure sentences

Do not auto-delete “This distinction is important / provides a basis / highlights / demonstrates / confirms / establishes / therefore shows…”. Ask whether the sentence adds an inference not already obvious. If no, delete or merge.

## 15. Preserve appropriate hedging

Do not make prose unnaturally certain. Keep may/might/can/could/suggests/indicates/is consistent with/appears to/likely/approximately/near/about/within the tested range when evidence supports them. Match confidence to evidence.

## 16. Do not add claims

The scrubber is not a co-author. No new literature, evidence, causal claims, interpretations, limitations, terminology, or methodological justification unless asked. Do not invent a rationale to “improve” an argument.

## 17. Do not remove specificity

Never replace precise numbers/mechanisms with generic “better performance”. Keep materials, software versions, parameters, equations, units, model names, algorithms, scientifically necessary file/geometry IDs, citation numbers, figure/table references.

## 18. Figures and tables

Keep structural language that locates content (“Fig. 1(a) shows eight conductor geometries.”). Remove assignment-style reasons for including them (“Table II was included to satisfy the literature-review requirement.”).

## 19. Literature-review language

Do not force “literature shows…” generics. Keep concrete paper–claim links (“Jiang et al. show that section and modulus move the local strain…”).

## 20. Technical clarification vs conversation leakage

Keep: “The voltage is calculated from the constant-current configuration rather than the voltage-divider configuration.”  
Drop course provenance: “The voltage is not the value from the course example.”  
If files matter, state inputs: “The simulation uses the imported 3MF meshes.” not “does not use the SolidWorks files mentioned previously.”

## 21. Paragraph-level reasoning

Do not scrub sentences in isolation. Before deleting, ask whether the sentence introduces evidence, defines a variable, constrains interpretation, explains a methodological choice, establishes a literature gap, or connects scientific reasoning. Only process/assignment/conversation narration should normally go.

## 22. Five-step rewrite

1. Classify function.  
2. Necessity: would a scientifically relevant fact be lost? If no, delete.  
3. Rewrite only if needed: drop assignment/user/agent/process/defence; keep the proposition.  
4. Re-read the paragraph.  
5. Stop. Do not polish for “more academic”.

## 23. Minimal intervention

1. Delete pure contamination.  
2. Compress redundant defence.  
3. Rewrite contaminated framing.  
4. Fix grammar created by deletion.  
5. Stop. Editor, not ghostwriter.

## 24. Residual scan (semantic, not blacklist)

Do not require disappearance of report/section/analysis/review/assignment/requirement/following/limitation as words.

Check residuals of: user, prompt, instructions, feedback, previous drafts, revisions, what the agent was asked to do; coursework/assessment/rubric/marking/course or assignment requirements when not research; how the document was generated; why a section exists; what appears later only because the assignment requires it; empty “not intended / it should be noted / not exhaustive / should not be interpreted as / does not necessarily imply”; formulaic transitions and generic closures.

If none remain at a meaningful level, stop.

## 25. Anti-overcorrection

A clean document is **not** zero meta-language, zero “this study/section”, zero hedging, zero however/therefore, zero negation, zero document references. Optimize **functional relevance**, not lexical purity.

## 26–30. Worked examples

See [`examples.md`](examples.md).

## 31. Must not

Rewrite every sentence; replace every “this”; remove every section/report; auto-replace report→study, assignment→study, course→literature; remove legitimate hedging, limits, or technical negatives; invent academic vocabulary or smoothness transitions; add unsupported conclusions or citations; alter numbers, equations, variable definitions, citation numbering, figure/table numbering, or terminology; turn concrete claims generic; force concision at the expense of reasoning; force sophistication; randomize style to seem human.

## 32–34. Quality test and governing preferences

See SKILL.md quality questions A–E.

When uncertain, prefer: semantic preservation over stylistic improvement; direct scientific statements over explanations of why the statement is being made; necessary qualification over defensive qualification; research logic over rubric logic; minimal intervention over comprehensive rewriting.

Success = the same research, less evidence of the process that produced it.
