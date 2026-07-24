# Vercel Agent Browser Playbook

Before the first command, load the current guide and list the available Chrome profiles:

```bash
agent-browser skills get core --full
agent-browser profiles
```

If has more than one profile, ask the user which one to use.

Open the URL in a new named session:
```bash
agent-browser --session <task-session> \
  --profile "<chrome-profile>" \
  --headed open "<url>"

agent-browser --session <task-session> snapshot -i
```

and use the same --session for every subsequent command.
