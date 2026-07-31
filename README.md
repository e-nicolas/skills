# Emmanouil Nicolas' Agent Skills

[![skills.sh](https://skills.sh/b/e-nicolas/skills)](https://skills.sh/e-nicolas/skills)

Agent skills by [Emmanouil Nicolas](https://github.com/e-nicolas), used in my day-to-day work.

## Skills

- [`pragmatic`](./skills/pragmatic/SKILL.md) - treats prompts as hypotheses and grounds responses in facts, evidence, documentation, data, or explicit logic. I use it for research, planning, and building new things.
- [`pink-elephant`](./skills/pink-elephant/SKILL.md) - shapes prompts, instructions, and requested planning changes around the intended outcome so the context stays clean, direct, and aligned with what the AI should do. I use it when refining plans, prompts, and text without carrying distracting context forward.
- [`research`](./skills/research/SKILL.md) - researches a topic across different sources. I use it to explore subjects in depth and compare what the sources say.
- [`task-breakdown`](./skills/task-breakdown/SKILL.md) - breaks large, complex things into a clear sequence of practical tasks. I use it to turn broad ideas, plans, or initiatives into focused work I can execute step by step.
- [`web-agent`](./skills/web-agent/SKILL.md) - helps an agent navigate browser sessions well, with guardrails for authenticated flows, logged-in sessions, and safe browser automation.

## Install in Claude

No terminal or `npx` required:

1. Open **Customize → Plugins** in Claude.
2. Select **Add marketplace**.
3. Select **Add from a repository**.
4. Enter `e-nicolas/skills`.
5. Install **Agent Skills**.

Claude Code users can alternatively run:

```text
/plugin marketplace add e-nicolas/skills
/plugin install agent-skills@e-nicolas-skills
```

## Install with skills.sh

Install these skills with `skills`:

```bash
npx skills add e-nicolas/skills
```

Install a specific skill:

```bash
npx skills add e-nicolas/skills --skill pragmatic
```

## Local Development

From this repository, install the local skills globally for Codex:

```bash
npx skills add . --global
```
