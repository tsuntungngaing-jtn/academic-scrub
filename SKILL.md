---
name: academic-scrub
description: >-
  Scrub AI fluff and assignment/disclaimer meta-discourse from academic drafts
  (EN/CN): remove "这份作业重点讨论…对此本文…", this report/assignment framing, roadmap
  fillers, and Layer-1/2 AI tells; then revise while preserving numbers, equations,
  and citations. Use when the user asks to 去AI腔, 去免责条款, 去元话语, humanize,
  scrub coursework leakage, polish a final paper, 再次检查修改终版论文, or invokes
  /academic-scrub.
disable-model-invocation: true
---

# Academic Scrub（去 AI 腔 + 去免责/元话语）

把个人项目里纠缠过的两类问题揉成一次终稿 pass：

1. **AI 屁话 / AI tells**（空泛开场、连接词堆砌、over-claim、破折号等）
2. **免责条款 / 作业元话语**（“这份作业重点讨论…对此本文…”、this report/assignment、roadmap 式段落）

默认任务：**先审计，再改稿**（不是只点评）。

## Hard constraints

- 不发明数据、机理、结果或参考文献。
- 不改 **数字、公式符号、单位、引用键**（除非已证实的笔误）。
- 不为规避 AI 披露而改写；封面/声明区要求的 AI declaration **保留**。
- 作业 brief / marking scheme **只作静默合规清单**，其措辞不得进入正文。
- 默认去掉 em dash `—`；数字范围可用 en dash `–`（如 `1.4–2`）。
- 正文读起来应像投期刊的研究者手稿，不是交作业的学生报告。

## Inputs

1. 目标稿（用户路径，或工作区最新 `*Revised*` / `*final*` / `*Comments*`）。
2. 可选：作业 brief —— 仅 Yes/No 合规，不写进稿。
3. 可选深化：项目内 `_tools/academic-humanizer/SKILL.md`（上游 Layers 1–6）；本 skill 的 `reference-patterns.md`（本仓库实战词表）。

## Workflow

```
Academic scrub pass:
- [ ] 1 Backup
- [ ] 2 Audit（quote → 问题类型 → 拟改一句；先不改）
- [ ] 3 Revise（按层顺序）
- [ ] 4 Residual scan（必须干净）
- [ ] 5 短 changelog 回复用户
```

### 1. Backup

`TARGET` → `TARGET_backup_before_scrub_YYYYMMDD_HHMMSS.ext`（同目录）。

### 2. Audit — 四层扫描

对全文（含表内单元格、图注；**排除**参考文献书名里的 Handbook、以及要求保留的 AI 声明区）扫描：

| 层 | 名称 | 做什么 |
|----|------|--------|
| **L0** | 免责 / 作业泄漏 | 见下表 A；中英都要扫 |
| **L1** | 元话语 / 路线图 | 见下表 B |
| **L2** | AI tells | 见下表 C；细则见 `reference-patterns.md` 或上游 skill |
| **L3** | 证据纪律 | 动词强度 ≤ 证据；悬空交叉引用 |

每条审计记：**原句摘录 → 类型 → 拟改写（一行）**。

#### A. 免责条款 / 作业泄漏（必须删或改成技术表述）

中文典型（含同义改写）：

- 这份作业 / 本作业 / 课程作业 **重点讨论 / 要求** …
- **对此本文 / 因此本文 / 本文据此** …
- 根据作业要求 / 评分标准 / marking criteria / 为满足要求
- 本文旨在完成 / 回应 / 覆盖 作业要点
- 与 team project / 团队项目 / 小组课题 的关系说明（除非真是期刊合作声明）

英文典型：

- this assignment / coursework / module / marking / rubric / as required by / to satisfy
- this report (正文；封面声明可保留)
- team project / preparation for prototyping / selected for the prototype
- required by the assignment / instructions / Learning Mall / Student ID（正文）
- 教学套件品牌泄漏：Arduino Uno 作为作业套件口吻 → 改为 microcontroller ADC（保留技术含义）

**原则：** Instructions are constraints, not content. 作业要求是隐形约束，不是正文叙事。

#### B. 元话语 / 空路线图（低信息量 → 改成科学内容句）

- The subsequent sections… / This section examines/will discuss…
- The following … one paper at a time / The survey focuses on…
- rather than an exhaustive list…
- why this structure was chosen / how this report satisfies…
- It should be noted that / It is worth noting that / Notably, / Importantly,（无实质信息时删）

保留：**有技术必要的**限定（如 “analogy, not direct evidence…”、指标不可直接横向排名且已说明原因）。

#### C. AI tells（去腔，不口语化）

- 空开场：In recent years… / With the rapid development… / 近年来…受到广泛关注
- 词库：delve, underscore, intricate, tapestry, pivotal, seamless, leverage（废话用法）, foster, realm, showcase…
- 连接词连开：Moreover / Furthermore / Additionally 连续句首
- not only X but also Y；rule-of-three 注水
- over-claim：prove / demonstrate / significantly（无数字）/ paves the way / sheds light / paramount
- 过长从句堆叠（约 30+ 词或 3+ 从句）→ 拆句
- em dash `—` → 逗号 / 括号 / 分句

### 3. Revise（顺序固定）

1. **L0** 免责/作业泄漏 → 技术等价表述（见 `examples.md`）。
2. **L1** 元话语 → 直接写科学内容，不要 TOC 散文。
3. **L2** AI tells → 收紧；拆长句；去 `—`。
4. **L3** 证据 → 仅在错误明确时改；不擅自重排整份参考文献。
5. 结构（章节/图序）不动，除非标题/图注本身含泄漏词。

`.docx`：段落 run 碎裂时，整段写入首 run 并清空其余 runs。跳过 AI declaration 区与参考文献里合法的 “Handbook …” 书名。

交付：

- `*_scrubbed.docx`（或用户说终版/直接改时覆盖工作稿）
- 旁路 `ACADEMIC_SCRUB_LOG.md`：计数 + 关键替换 + residual

### 4. Residual scan（不过则继续改）

正文+表格（声明区/参考文献除外）不得残留（大小写不敏感）：

**EN:** `this report`, `this assignment`, `coursework`, `team project`, `this module`, `marking criteria`, `as required by`, `preparation for prototyping`, `required by assignment`, `this paper will discuss`, `subsequent sections`, `this section examines`, `one paper at a time`

**CN:** `这份作业`, `本作业`, `作业要求`, `评分标准`, `对此本文`, `本文旨在满足`, `课程作业重点`

并抽查：散文中是否仍有 `—`。

### 5. 回复用户（短）

1. 清了什么（分 L0/L1/L2 要点）
2. 输出路径
3. 若有 brief：一行合规 Yes/No 表（不写分析长文）
4. 仍需人工的风险（页数、`[AI-SUGGESTED]` 须本人重写等）

## Do not

- 把作业目标句粘进稿件冒充引言。
- 写 “this revision addresses…”（除非真是期刊 rebuttal）。
- 把合理 hedging 改成假确定性。
- 整篇无差别同义改写；只改审计命中 + 轻度 tell 清理。
- 与上游 `nature-polishing` 混用目标：那个偏 Nature 润色；本 skill 偏 **去作业腔 + 去 AI 腔**。

## Progressive detail

- 词表与替换范例：同目录 [`reference-patterns.md`](reference-patterns.md)、[`examples.md`](examples.md)
- 上游完整 AI-tell / 基金申请 Layer 6：项目 `_tools/academic-humanizer/SKILL.md` 或个人目录 `academic-humanizer`（**不同 skill，不同职责**）
