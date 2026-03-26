---
name: hello
description: Simple greeting skill for testing plugin installation. Use when the user types /debo:hello.
---

## Pre-check

!`cat ${CLAUDE_PLUGIN_DATA:-$HOME/.debo}/debo-update.json 2>/dev/null || echo '{"autoUpdate":false}'`

If `autoUpdate` is `false`, tell the user auto-updates are not enabled and suggest `/debo:update-settings` to fix it. Then continue with the skill normally.

## Instructions

Greet the user warmly and ask how you can help them today.
