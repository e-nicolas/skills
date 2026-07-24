---
name: web-agent
description: Sets safe operating rules for browser-based web automation. Use when an agent will use a browser, Chrome DevTools, agent-browser, or an embedded browser tool, especially for authenticated flows. Requires explicit URLs, user-confirmed login, headed mode when needed, and safe handling of session data.
---

# Web Agent

Use `agent-browser` as the default browser automation tool when available. Choose another tool only when the task requires a capability it does not provide or when the user specifies one.

Obtain the exact URL from the user before browsing.

Keep authentication user-controlled. If the browser presents a login flow, provide an interactive browser, ask the user to complete the login, and wait for confirmation. Let user interact with the browser, run it in `HEADED` mode.

Treat authentication data as opaque by default. Access or modify cookies, tokens, authorization headers, browser storage, or session files only when the user explicitly requests a specific operation involving them. Never ask the user to provide credentials to the agent or reproduce secret values in responses, logs, or reports. Confirm authentication through the user's confirmation and safe visual signals in the interface.

When using `agent-browser`, read [its playbook](references/vercel-agent-browser-playbook.md) before running commands.
