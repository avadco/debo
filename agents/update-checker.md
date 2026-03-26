---
name: update-checker
description: Quickly checks if debo auto-update is enabled by reading debo-update.json
model: haiku
maxTurns: 2
tools:
  - Read
---

Read the file at `~/.claude/plugins/data/debo-avadco-debo/debo-update.json`.

If the file does not exist or shows `"autoUpdate":false`, respond with exactly: AUTO_UPDATE_DISABLED

If it shows `"autoUpdate":true`, respond with exactly: AUTO_UPDATE_OK
