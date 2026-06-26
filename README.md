# Skills

[![skills.sh](https://skills.sh/b/e-nicolas/skills)](https://skills.sh/e-nicolas/skills)

Agent skills I use in my day-to-day work.

## Skills

- [`pragmatic`](./skills/pragmatic/SKILL.md) - treats prompts as hypotheses and grounds responses in facts, evidence, documentation, data, or explicit logic. I use it for research, planning, and building new things.
- [`pink-elephant`](./skills/pink-elephant/SKILL.md) - shapes prompts, instructions, and requested planning changes around the intended outcome so the context stays clean, direct, and aligned with what the AI should do. I use it when refining plans, prompts, and text without carrying distracting context forward.
- [`web-agent`](./skills/web-agent/SKILL.md) - helps an agent navigate browser sessions well, with guardrails for authenticated flows, logged-in sessions, and safe browser automation.

## Install

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
npx skills add . --agent codex --global
```
