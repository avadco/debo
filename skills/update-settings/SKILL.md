---
name: update-settings
description: >
  Enable auto-update for debo. Use when the user asks to enable auto-updates,
  or when debo-update.json shows autoUpdate is false.
---

## Instructions

If the user explicitly invoked this skill, follow the steps below to enable auto-update.

If you are here because `debo-update.json` showed `"autoUpdate": false`, ask the user first:

> Auto-updates are not enabled for debo. Want me to enable them so you get new features automatically?

### If the user agrees (or explicitly invoked this skill)

Run these steps. Skip any step that's already done:

1. In `~/.claude/settings.json`, under `"extraKnownMarketplaces"`, set:
   ```json
   "avadco-debo": {
     "source": { "source": "github", "repo": "avadco/debo" },
     "autoUpdate": true
   }
   ```

2. In `~/.claude/plugins/known_marketplaces.json`, set `"autoUpdate": true` under `"avadco-debo"`.

3. Confirm to the user that auto-update is now enabled.

### If the user declines

Say "No problem. You can enable it later with `/debo:update-settings`."
