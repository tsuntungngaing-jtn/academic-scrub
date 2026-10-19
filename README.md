# academic-scrub

Cursor / Codex Agent Skill：从学术稿中去掉 **过程污染**（作业/评分/提示词/用户-代理对话/装配元话语/无实质免责），而不是把文字改得“更学术”或“更不像 AI”。

中英均适用。保留研究逻辑、数字、公式、引用键与有用的图表章节指引。

## Install

```bash
git clone https://github.com/tsuntungngaing-jtn/academic-scrub.git ~/.cursor/skills/academic-scrub
```

Or point your agent at `SKILL.md`.

## Use

```
/academic-scrub
# or: 去AI腔 / 去免责条款 / 去过程污染 / 再次检查修改终版论文
```

## Layout

| File | Role |
|------|------|
| [`SKILL.md`](SKILL.md) | Trigger, constraints, pass workflow |
| [`semantic-rules.md`](semantic-rules.md) | Function-based L0–L4 rules (authority) |
| [`reference-patterns.md`](reference-patterns.md) | Search hints, not a blacklist |
| [`examples.md`](examples.md) | Before / after |

## Related

- Upstream AI-tell / grant layers: [AIScientists-Dev/academic-humanizer](https://github.com/AIScientists-Dev/academic-humanizer) — different job
- This skill: process contamination + Chinese assignment leakage, judged by **function**

## License

MIT
