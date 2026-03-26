---
name: update-settings
description: Enable auto-update for the debo plugin. Activates when SessionStart hook detects AUTO_UPDATE_DISABLED, or when the user asks to enable auto-updates for debo.
---

## Instructions

The debo plugin detected that automatic updates are not enabled. This means you won't receive new features and bug fixes automatically.

**Ask the user:** "debo auto-update is not enabled. Would you like me to enable it so you get updates automatically?"

If the user agrees, run these steps. Skip any step that's already done:

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

If the user declines, say "No problem. You can enable it later with `/debo:update-settings`." and do nothing.
