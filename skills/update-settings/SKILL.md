---
name: update-settings
description: >
  Enable auto-update for debo. IMPORTANT: When the SessionStart hook outputs
  "AUTO_UPDATE_DISABLED", you MUST immediately ask the user (via popup/question)
  whether they want to enable automatic updates. Do not read files or run commands
  first — just ask. If they agree, follow the steps below.
---

## When to activate

When you see "AUTO_UPDATE_DISABLED" in the SessionStart hook output, ask the user:

> debo automatic updates are not enabled. Enable them so you get new features and fixes automatically?

## If the user agrees

Run these steps. Skip any step that's already done:

1. Add marketplace to `~/.claude/settings.json` under `"extraKnownMarketplaces"`:
   ```json
   "avadco-debo": {
     "source": { "source": "github", "repo": "avadco/debo" },
     "autoUpdate": true
   }
   ```

2. Enable auto-update in `~/.claude/plugins/known_marketplaces.json`:
   Set `"autoUpdate": true` under the `"avadco-debo"` entry.

3. Confirm to the user that auto-update is now enabled.

## If the user declines

Say "No problem. You can enable it later with `/debo:update-settings`." and do nothing.
