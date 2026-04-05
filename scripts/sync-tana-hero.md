# Sync Hero Content from Tana

The hero text on the homepage is driven by `src/content/hero.json`.
This file maps to two Tana nodes tagged with `#Website Content`:

- **EN**: Node ID `QLgjkcwEKsL1` ("Hero Text (EN)") in Kaja Website workspace
- **DE**: Node ID `qCTs6H5auSZR` ("Hero Text (DE)") in Kaja Website workspace

## How to update hero text

1. Edit the hero node in Tana (in the "Kaja Website" workspace)
2. Ask Claude Code: "sync hero text from Tana and rebuild"
3. Claude will read the Tana nodes, update `hero.json`, build, and push

## Manual sync

Edit `src/content/hero.json` directly. The structure is:

```json
{
  "en": {
    "tanaNodeId": "QLgjkcwEKsL1",
    "intro": "I'm inviting you...",
    "lines": [
      { "emphasis": "to align", "text": "with the free-flowing rhythm of your essence" }
    ]
  }
}
```

Then run `npx astro build` and push to deploy.
