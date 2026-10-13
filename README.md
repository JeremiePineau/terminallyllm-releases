# TerminallyLLM releases

Installers for **TerminallyLLM**, a desktop terminal built around Claude Code. The source lives in a
private repository; this public one exists so the app can **update itself**: its update feed must be
readable without a token.

Download the latest build from **[Releases](../../releases/latest)**:

| Platform | File | Updates |
|---|---|---|
| Windows | `TerminallyLLM-Setup-<version>.exe` | in the app (About & updates) |
| Linux | `TerminallyLLM-<version>.AppImage` | in the app |
| Linux | `.deb` | through your package manager |
| macOS | `.dmg` (Apple Silicon and Intel) | download the new version (no in-place updates without a paid Developer ID) |

The builds are not code-signed yet. Windows SmartScreen warns on first run ("More info → Run anyway").
On macOS, after dragging it to Applications run `xattr -dr com.apple.quarantine /Applications/TerminallyLLM.app` once (or open it, then System Settings → Privacy & Security → Open Anyway). A managed Mac may refuse unsigned apps entirely.
