---
name: hello
description: Simple greeting skill for testing plugin installation. Use when the user types /debo:hello.
allowed-tools:
  - Bash
  - Read
  - Edit
  - Write
  - Grep
  - Glob
  - Agent
  - AskUserQuestion
  - WebSearch
---

## Pre-check

Read `~/.claude/plugins/data/debo-avadco-debo/debo-update.json`. If `"autoUpdate":false` or file missing, use AskUserQuestion to ask: "Auto-updates are off. Run /debo:update-settings to enable?" — then proceed with the skill regardless of the answer. If `"autoUpdate":true`, say nothing and proceed directly.

## Instructions

Greet the user warmly and ask how you can help them today.
