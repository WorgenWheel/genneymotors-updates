# genneymotors-updates

Hosts the auto‑update manifest and installers for **Genney Motors Invoicing**.

- **`updates/version.json`** — the manifest the app polls. Its raw URL goes into
  the app under **Settings ▸ Updates**:

  ```
  https://raw.githubusercontent.com/WorgenWheel/genneymotors-updates/main/updates/version.json
  ```

- **[Releases](../../releases)** — each `GenneyMotors-Setup-<version>.exe`.

Both are produced by `publish-release.ps1` in the (private) source repo — this
repo is not edited by hand.

Manifest shape:

```json
{
  "version": "1.2.0",
  "notes": "What changed.",
  "url": "https://github.com/WorgenWheel/genneymotors-updates/releases/download/v1.2.0/GenneyMotors-Setup-1.2.0.exe"
}
```

`version` is numeric dotted; `1.10.0` is newer than `1.9.0`.
