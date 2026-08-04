# DROIDEX Releases

This public repository hosts official DROIDEX macOS downloads. The current
`v0.1.0` developer preview is **unsigned and not notarized** so it can be
distributed without a paid Apple Developer membership.

Download the latest DMG from
[Releases](https://github.com/anasibnanwar1-droid/droidex-releases/releases).
Choose `arm64` for Apple silicon Macs or `x64` for Intel Macs. Published
releases are immutable and include `SHA256SUMS` so you can verify the download.

## Install the unsigned preview

1. Download the DMG matching your Mac and drag DROIDEX to Applications.
2. Try to open DROIDEX once. macOS will warn that Apple cannot verify the
   developer.
3. Open **System Settings → Privacy & Security**, scroll to Security, choose
   **Open Anyway**, then confirm **Open**.

This creates an exception for that copy of DROIDEX. These steps follow
[Apple's documented override](https://support.apple.com/en-us/102445). Only
override Gatekeeper after downloading from this repository and checking the
published SHA-256 digest. We do not recommend disabling Gatekeeper or broadly
removing quarantine attributes.

After this first-launch approval, DROIDEX uses Sparkle to check for and install
future updates. Every architecture has its own HTTPS update feed and ZIP. Both
the feed and the ZIP are verified with DROIDEX's embedded EdDSA public key
before Sparkle replaces the app. You do not need to repeat the DMG install for
normal updates.

Keep DROIDEX in Applications and leave **Keep DROIDEX up to date** enabled in
Settings. If an update cannot be installed, download the latest matching DMG
from this repository and repeat the documented Apple approval flow.

## Privacy and support

The application source repository remains private during the closed-source
release period. GitHub's automatic source archives for this repository contain
only these public download documents, not the application source. Electron code
inside a shipped application remains technically inspectable; the client
contains no privileged server credentials or source maps.

Never put prompts, project files, logs, tokens, or personal data in a public
report. The in-app `/bug` command and automatic crash collection deliver
minimal diagnostics privately. `/bug` returns a `BUG-…` report ID and a
pseudonymous `USR-…` support ID that can be shared with support without
publishing application source or user project data.
