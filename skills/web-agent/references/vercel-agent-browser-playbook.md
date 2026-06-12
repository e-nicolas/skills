# Vercel Agent Browser Playbook

Before the first command, load the current tool guide:

```bash
agent-browser skills get core
```

Always use agent-browser with CDP.

# CDP 
If there is no Chrome instance with CDP available yet, open a headed instance with remote debugging. Use a dedicated profile to prevent Chrome from reusing an existing window without applying the debug port:

```bash
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --remote-debugging-port=9222 --user-data-dir=/tmp/web-agent-profile
```

Validate CDP without inspecting session data:

```bash
curl -sf http://localhost:9222/json/version
lsof -nP -iTCP:9222 -sTCP:LISTEN
```

When listing tabs, use the result only for URL and title.

```bash
curl -sf http://localhost:9222/json/list
```

Connect `agent-browser` to the user's Chrome with a new named session. This prevents reusing an old daemon stuck at `/login`:

```bash
agent-browser --session <safe-session-name> --cdp 9222 get url
agent-browser --session <safe-session-name> --cdp 9222 snapshot -i
```

After confirming that the session is correct, save the local state if that helps run the task without another login:

```bash
agent-browser --session <safe-session-name> state save ./.agent-browser-auth.local.json
```

Prefer using the saved state for the task, but validate it before trusting it:

```bash
agent-browser --session <task-session-name> --state ./.agent-browser-auth.local.json open <front-url>
agent-browser --session <task-session-name> get url
agent-browser --session <task-session-name> snapshot -i
```

If the saved-state session opens at `/login`, continue through the already validated CDP session:

```bash
agent-browser --session <safe-session-name> --cdp 9222 open <front-url>
agent-browser --session <safe-session-name> --cdp 9222 snapshot -i
```

This fallback is expected in apps whose authentication cannot be reproduced with `agent-browser state save` alone. Report that validation worked through direct CDP and that state restoration did not work, without exposing any secret.

In final reports, include only safe evidence: whether CDP was reachable at `localhost:9222`, and whether the URL landed on login or in the authenticated app.
