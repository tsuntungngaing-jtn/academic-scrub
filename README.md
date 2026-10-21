# academic-scrub

Cursor / Codex Agent Skill：从学术稿中去掉 **过程污染** 与 **AIGC 期刊语言包装**——作业/评分/提示词/用户-代理对话/装配元话语、免责声明式自我辩护、实验日志式第一人称堆叠、审稿回复腔、图注/图内防御性文字——而不是把文字改得“更学术”“更像人”或“更不像 AI”。

中英均适用。保留研究逻辑、数字、公式、引用键与有用的图表章节指引。科学边界保留；防御语气改写为模型定义、证据状态与范围陈述。

领域示例仅作功能示意；通用于任意学科。

## Install

```bash
git clone https://github.com/tsuntungngaing-jtn/academic-scrub.git ~/.cursor/skills/academic-scrub
```

Or point your agent at `SKILL.md`.

## Use

```
/academic-scrub
# or: 去AI腔 / 去免责条款 / 去过程污染 / 图注语言审校 / 再次检查修改终版论文
```

Full-manuscript scrub delivers **Parts A–D** (diagnosis table, revised body, figures/tables language audit, defensive-lexicon recount). See `SKILL.md`.

## Layout

| File | Role |
|------|------|
| [`SKILL.md`](SKILL.md) | Trigger, constraints, pass workflow, output contract |
| [`semantic-rules.md`](semantic-rules.md) | Function-based L0–L4 rules (authority) |
| [`reference-patterns.md`](reference-patterns.md) | Search hints, not a blacklist |
| [`examples.md`](examples.md) | Before / after |

## Related

- Upstream AI-tell / grant layers: [AIScientists-Dev/academic-humanizer](https://github.com/AIScientists-Dev/academic-humanizer) — different job
- This skill: process contamination + AIGC defensive/disclaimer/lab-notebook packaging (EN/CN), judged by **function**

## License

MIT
