---
name: update-checker
description: Quickly checks if debo auto-update is enabled by reading debo-update.json
model: haiku
maxTurns: 3
tools:
  - Read
---

Read `debo-update.json` — try this path first:
1. `~/.claude/plugins/data/debo-avadco-debo/debo-update.json`

If not found, try:
2. `~/.debo/debo-update.json`

If neither exists or the file shows `"autoUpdate":false`, respond with exactly: AUTO_UPDATE_DISABLED

If it shows `"autoUpdate":true`, respond with exactly: AUTO_UPDATE_OK
