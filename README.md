# TerminallyLLM releases

Installers for **TerminallyLLM**, a desktop terminal built around Claude Code. The source is in a private repository. This public one holds the installers and the update feed the app checks, which must be readable without a token.

## Download
Get the newest build from **[Releases](../../releases/latest)**:

| Platform | File |
|---|---|
| macOS (Apple Silicon) | `TerminallyLLM-<version>-arm64.dmg` |
| macOS (Intel) | `TerminallyLLM-<version>.dmg` |
| Windows | `TerminallyLLM-Setup-<version>.exe` |
| Linux | `TerminallyLLM-<version>.AppImage`, or `terminallyllm_<version>_amd64.deb` |

**Updates:**
- **macOS, Windows, Linux AppImage:** from inside the app (Settings › Updates & about). Nothing downloads or installs without your click.
- **`.deb`:** install each new version with your package manager.

**Signing:**
- **macOS:** builds are signed with a Developer ID and notarized by Apple.
- **Windows:** builds aren't code-signed, so SmartScreen warns the first time ("More info → Run anyway").

## Requirements
- **Claude Code** (the `claude` CLI), installed and signed in. TerminallyLLM runs it; it doesn't replace it.
- **Windows:** WSL, with Claude Code installed inside it.

## The other files on the release
- **`latest.yml`, `latest-mac.yml`, `latest-linux.yml`:** the update feeds the app reads.
- **`.zip` and `.blockmap` files:** the files those updates download.
- **`TerminallyLLM-provenance-<platform>.sigstore.json`:** signed build provenance for every file.

## More
- **Verifying a download:** see [VERIFY.md](VERIFY.md).
- **Security issues:** report them privately, as described in [SECURITY.md](SECURITY.md).
- **Licence:** proprietary; see [LICENSE](LICENSE).
