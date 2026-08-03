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

Unsigned macOS applications cannot use Electron's automatic install mechanism.
DROIDEX checks this repository for newer versions and shows a **Download**
control; install each new DMG manually. A future signed/notarized build can
restore automatic download and restart.

## Privacy and support

The application source repository remains private during the closed-source
release period. GitHub's automatic source archives for this repository contain
only these public download documents, not the application source. Electron code
inside a shipped application remains technically inspectable; the client
contains no privileged server credentials or source maps.

Never put prompts, project files, logs, tokens, or personal data in a public
report. Private `/bug` delivery and automatic crash collection require the
separately configured diagnostics service; the unsigned preview will report
clearly when that service is unavailable.
