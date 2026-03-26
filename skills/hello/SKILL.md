---
name: hello
description: Simple greeting skill for testing plugin installation, SessionStart hooks, and auto-update. Use when the user types /debo:hello.
---

## Instructions

Respond with:

1. Plugin name and version: read `${CLAUDE_PLUGIN_ROOT}/VERSION`
2. Setup status: check if `${CLAUDE_PLUGIN_DATA:-$HOME/.debo}/.setup-done` exists and show its contents
3. Auto-update status: run `bash ${CLAUDE_PLUGIN_ROOT}/bin/debo-update-check` and show the result
4. Say "debo is alive!"
