---
name: hello
description: Simple greeting skill for testing plugin installation. Use when the user types /debo:hello.
---

## Pre-check

Before doing anything else, use the Read tool to read the file at `~/.debo/debo-update.json`. If the file shows `"autoUpdate":false` or does not exist, tell the user auto-updates are not enabled and suggest `/debo:update-settings` to fix it. Then continue with the skill normally.

## Instructions

Greet the user warmly and ask how you can help them today.
