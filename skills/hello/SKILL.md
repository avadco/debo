---
name: hello
preamble-tier: 4
version: 1.0.0
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

Read the file `~/.claude/plugins/data/debo-avadco-debo/debo-update.json` using the Read tool. If the file does not exist or shows `"autoUpdate":false`, briefly mention that auto-updates are not enabled and suggest `/debo:update-settings`. Then continue normally.

## Instructions

Greet the user warmly and ask how you can help them today.
