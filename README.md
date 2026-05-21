# Agency Brain — Downloads

Public installers for the Agency Brain desktop app.

**Download page:** https://ads2ai.com/downloads

The newest release is always the top one. The download links on ads2ai.com point
at `releases/latest/download/<stable-name>`, so they auto-resolve to the latest
release and never need editing.

## Stable filenames (do NOT version-pin — the latest-download URLs depend on these)

| Platform | File |
|---|---|
| Windows | `Agency-Brain-Setup.exe` |
| macOS (Apple Silicon) | `Agency-Brain-mac-arm64.dmg` |
| macOS (Intel / x64) | `Agency-Brain-mac-intel.dmg` |

Always-latest direct link (Windows):
`https://github.com/8020brain/agency-brain-downloads/releases/latest/download/Agency-Brain-Setup.exe`

## How a new build lands here

This repo is the **public mirror** of the private `8020brain/agency-brain-sync`
build. On every new tagged build, mirror it with:

```bash
node tools/mirror-agency-release.cjs vX.Y.Z   # run from the brain repo
```

That downloads the source release, renames to the stable filenames above, and
publishes a matching release here marked **Latest**. Full process + the
code-signing fix for the install warnings:
`projects/agencybrain/downloads-and-releases.md` in the brain.

Why public: the app is inert without an OTP login, so an open download is safe.
