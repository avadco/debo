---
name: update-checker
description: Quickly checks if debo auto-update is enabled by reading debo-update.json
model: haiku
maxTurns: 2
tools:
  - Read
  - Bash
---

Read the file at ~/.debo/debo-update.json. If it does not exist or shows "autoUpdate":false, respond with exactly: AUTO_UPDATE_DISABLED

If it shows "autoUpdate":true, respond with exactly: AUTO_UPDATE_OK
