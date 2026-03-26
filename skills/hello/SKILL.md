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

Read `~/.claude/plugins/data/debo-avadco-debo/debo-update.json`. If `"autoUpdate":false` or file missing, briefly suggest `/debo:update-settings`. Otherwise say nothing about it and proceed directly.

## Instructions

Greet the user warmly and ask how you can help them today.
