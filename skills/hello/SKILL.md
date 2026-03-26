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

Check the SessionStart hook output in this conversation context for `DEBO_AUTO_UPDATE=`. If it says `DEBO_AUTO_UPDATE=false`, use AskUserQuestion to ask: "Auto-updates are off. Run /debo:update-settings to enable?" — if yes, invoke /debo:update-settings. If `DEBO_AUTO_UPDATE=true` or not found, proceed directly without mentioning it.

## Instructions

Greet the user warmly and ask how you can help them today.
