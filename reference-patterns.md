# Academic Scrub — pattern catalog

Sourced from MFE209TC personal-homework cleanup (meta clean, Ctrl+F leakage, leakage audit, academic-humanizer audits) plus the Sep 2026 writing-rules prompt.

## L0 — Assignment / disclaimer leakage

### Chinese

| Cue | Action |
|-----|--------|
| 这份作业重点讨论… | Delete; open with scientific gap/motivation |
| 对此本文… / 因此本文将… | Delete or → direct claim about the topic |
| 根据作业要求 / 评分标准 / 为满足…要求 | Never in body |
| 本文旨在完成课程… | → research objective in technical terms |
| 与团队项目 / team project 的关系是… | Remove from individual paper body |
| 本报告 / 本次作业 | → 本文 / 本综述 / 本分析（或直接删主语） |

### English

| Cue | Action |
|-----|--------|
| this assignment / coursework / marking / rubric | Remove |
| as required by / to satisfy the requirement / according to the instructions | Remove |
| this report (body) | → this review / the present analysis / drop subject |
| this module / in this module | → considered here / under review |
| team project / preparation for prototyping | Technical scope only |
| selected for the prototype / present prototype / prototype system | → sensing implementation / bending-mode sensing |
| required by assignment (tables) | → under review |
| Role in this report | → Role in the present review |
| Arduino Uno / Arduino ADC (lab-kit voice) | → 10-bit microcontroller ADC / microcontroller ADC |
| Student ID / Learning Mall / module handbook (body) | Cover/declaration only |

### Keep on purpose

- Required **AI Usage Declaration** cover bullets (coursework rule).
- Bibliographic titles containing “Handbook”.
- Necessary scientific limits (“should not be ranked directly” when metrics differ; “analogy, not direct evidence”).

## L1 — Meta-discourse / roadmap filler

| Cue | Prefer |
|-----|--------|
| The subsequent sections compare… | One content sentence naming the topics without TOC voice |
| This section examines… | Lead with the governing parameters / mechanism |
| The following five … one paper at a time; The survey focuses on… | “Five studies are examined through structures, experiments, and claimed metrics…” |
| rather than an exhaustive list | Drop defensive clause; name what Fig. shows |
| why this structure was chosen / how the report satisfies | Delete |
| It should be noted / It is worth noting / Notably, / Importantly, | Delete opener; keep payload if any |
| Defensive duplicates of the same “rather than…” across sections | Keep **one** strong instance |

## L2 — AI tells (condensed)

### Vocabulary / rhetoric

delve, underscore, intricate, tapestry, testament, landscape (abstract), pivotal, showcase, foster, leverage (filler), realm, seamless, groundbreaking, cutting-edge, transformative, rich/vibrant (figurative)

### Structures

- In recent years… / With the rapid development… / Despite recent advances…
- Moreover / Furthermore / Additionally / In particular as consecutive openers
- not only X but also Y; rule-of-three padding
- serves as → is
- Em dash `—` → commas, parentheses, or split sentences
- Sentences ≳30 words or 3+ stacked subordinates → split

### Over-claim / hype

prove, demonstrate (universal), establish/confirm/guarantee (overstrong), significantly (no test/number), paves the way, sheds light, paramount, bridges the gap, extensive/comprehensive experiments, a wide range of, to the best of our knowledge, for the first time, novel (more than once per section)

### Soften examples

| Bad | Better |
|-----|--------|
| We prove … significantly outperforms | … improves X by a–b over strongest baseline (Table N) |
| paves the way for a new paradigm | addresses failure mode Y (Section N) |
| extensive experiments on a wide range | evaluate on three datasets (named) |

## L3 — Claim ↔ evidence

- Unbacked comparative adjective → add Fig/Table/cite or soften.
- Verb stronger than evidence → downgrade.
- Keep calibrated hedging: suggests, may, consistent with, appears to.

## Silent compliance (brief only)

If an assignment brief is supplied, check pillars Yes/No only. Never narrate compliance in the manuscript.

## Ctrl+F residual needles (body + tables)

```
assignment|coursework|module|marking|rubric|this report|required by|as requested|
team project|subsequent sections|this section examines|this section will|
one paper at a time|exhaustive list|preparation for prototyping|
这份作业|本作业|作业要求|评分标准|对此本文|本文旨在满足
```

Exclude: AI cover zone; reference entries with Handbook; intentional “reported” in results language.
