---
name: web-agent
description: Use when an agent will operate on the web through a browser, browser automation, Chrome DevTools, agent-browser, or an embedded browser tool, especially when the flow may require manual user authentication, a headed browser, or safe handling of logged-in sessions.
---

# Web Agent

Whenever you use a browser for any web operation, whether through `agent-browser`, `chrome devtools`, or an embedded agent tool, first check whether the flow requires authentication. If it does, stop the flow immediately, ask me to log in, and wait for my confirmation before continuing. To let me interact with the browser, run it in `HEADED` mode.

Never ask me for credentials, and never read, print, summarize, or manipulate cookies, tokens, authorization headers, `localStorage`, `sessionStorage`, or session files as login evidence. Confirmation must come from me and from safe visual signals in the authenticated interface.

Do not infer any URL. Ask me for the URL we will use.

When the selected tool is Vercel `agent-browser`, read `references/vercel-agent-browser-playbook.md` before running commands specific to that tool.
