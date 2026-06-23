# SC Quick Actions – Update Repo

This repo hosts the version manifest for the SC Quick Actions browser extension. It is checked automatically by the extension on startup to notify users when an update is available.

## File: `version.json`

```json
{
  "version": "2.6.0",
  "notes": "One-line summary of what changed.",
  "url": "https://teams.microsoft.com/..."
}
```

- `version` — must match the version in the extension's `manifest.json` exactly
- `notes` — shown to the user in the update banner
- `url` — link to where the new version can be downloaded (constant, does not change)

## When to update

Update `version.json` each time a new version of the extension is released. The extension checks this file on every popup open (cached for 5 minutes) and shows a banner if the version here is newer than the one installed.
