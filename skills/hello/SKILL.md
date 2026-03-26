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

Launch the `update-checker` agent (subagent). If it returns `AUTO_UPDATE_DISABLED`, tell the user auto-updates are not enabled and suggest `/debo:update-settings` to fix it. Then continue with the skill normally. Do not wait for user input on the pre-check — just mention it briefly and move on.

## Instructions

Greet the user warmly and ask how you can help them today.
