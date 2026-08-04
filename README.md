# DROIDEX Releases

This public repository hosts official DROIDEX macOS downloads. The current
developer preview is **ad-hoc signed and not notarized**. It has no trusted
Developer ID, so it can be distributed without a paid Apple Developer
membership.

Download the latest DMG for
[Apple silicon](https://github.com/anasibnanwar1-droid/droidex-releases/releases/latest/download/droidex-arm64.dmg)
or
[Intel](https://github.com/anasibnanwar1-droid/droidex-releases/releases/latest/download/droidex-x64.dmg).
Published releases are immutable and include `SHA256SUMS` so you can verify the
download.

## Install the unsigned preview

1. Download the DMG matching your Mac and drag DROIDEX to Applications.
2. Try to open DROIDEX once. macOS will warn that Apple cannot verify the
   developer.
3. Use the DMG's **Open Privacy & Security** shortcut, scroll to Security,
   choose **Open Anyway**, then confirm **Open**.

This creates an exception for that copy of DROIDEX. These steps follow
[Apple's documented override](https://support.apple.com/en-us/102445). Only
override Gatekeeper after downloading from this repository and checking the
published SHA-256 digest. We do not recommend disabling Gatekeeper or broadly
removing quarantine attributes.

After this first-launch approval, DROIDEX uses Sparkle to check for future
updates. Every architecture has its own HTTPS update feed and ZIP. Both the feed
and ZIP are verified with DROIDEX's embedded EdDSA public key. DROIDEX does not
download or install an update until you explicitly choose the update action.
Keep DROIDEX in Applications so Sparkle can replace it after your approval. If
an update cannot be installed, download the latest matching DMG above.

## Privacy and support

The application source repository remains private during the closed-source
release period. GitHub's automatic source archives for this repository contain
only these public download documents, not the application source. Electron code
inside a shipped application remains technically inspectable; the client
contains no privileged server credentials or source maps.

Never put prompts, project files, logs, tokens, or personal data in a public
report. The in-app `/bug` and `/feedback` commands and automatic crash
collection deliver minimal diagnostics privately. A successfully delivered
report returns a copyable `RPT-…` ID that can be shared with support without
publishing application source or user project data.
