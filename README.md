# DROIDEX Releases

This repository hosts the official DROIDEX downloads for macOS.

- [Download for Apple silicon](https://github.com/anasibnanwar1-droid/droidex-releases/releases/latest/download/droidex-arm64.dmg)
- [Download for Intel](https://github.com/anasibnanwar1-droid/droidex-releases/releases/latest/download/droidex-x64.dmg)

## Install DROIDEX

1. Download the DMG matching your Mac and drag DROIDEX to Applications.
2. Open DROIDEX once. macOS will show a security warning.
3. In the DMG, double-click **Open Privacy & Security**.
4. Find the DROIDEX notice, click **Open Anyway**, and confirm.

DROIDEX is currently **ad-hoc signed and not notarized**. This keeps distribution
free of a paid Apple Developer membership, but requires manual approval on first
launch. Confirm **Open** and authenticate if macOS asks. Do not disable
Gatekeeper. Published releases are immutable and include `SHA256SUMS` for
download verification.

## Updates

DROIDEX checks its signed Sparkle feed for new versions. A blue download button
appears beside Settings only when a newer version is available. Clicking it
opens Sparkle's native update window; nothing downloads or installs until you
approve it. You can also check manually in **Settings → Setup & updates** or
**DROIDEX → Check for Updates…**. Keep DROIDEX in Applications so an approved
update can be applied cleanly.

## Privacy and support

The application source repository remains private. This public repository's
source archives contain only README and SECURITY documents, not the application
source. Code packaged in the Electron app remains technically inspectable;
releases contain no privileged server credentials or public source maps.

Use `/bug` or `/feedback` inside DROIDEX to send a private report. After a
successful submission, copy the `RPT-…` ID for support. Do not post prompts,
project files, logs, tokens, or personal information in public issues.
