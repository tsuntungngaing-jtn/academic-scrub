# academic-scrub

Cursor / Codex Agent Skill：去掉学术稿里的 **AI 腔** 和 **作业/免责元话语**（中英）。

典型目标句：

- 「这份作业重点讨论XXXX，对此本文XXX」
- `this report` / `as required by the assignment` / `The subsequent sections…`

保留数字、公式、引用键；不为规避 AI 披露而改写。

## Install

```bash
git clone https://github.com/tsuntungngaing-jtn/academic-scrub.git ~/.cursor/skills/academic-scrub
```

Or point your agent at `SKILL.md`.

## Use

```
/academic-scrub
# or: 去AI腔 / 去免责条款 / 再次检查修改终版论文
```

## Layout

| File | Role |
|------|------|
| [`SKILL.md`](SKILL.md) | Workflow + hard constraints |
| [`reference-patterns.md`](reference-patterns.md) | L0–L3 pattern catalog |
| [`examples.md`](examples.md) | Before / after |

## Related

- Upstream AI-tell catalog: [AIScientists-Dev/academic-humanizer](https://github.com/AIScientists-Dev/academic-humanizer) (different job: voice/evidence layers + grant mode)
- This skill’s extra job: coursework leakage + Chinese disclaimer scrub

## License

MIT
