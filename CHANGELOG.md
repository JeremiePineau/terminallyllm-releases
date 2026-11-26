# Release notes

Every TerminallyLLM release, newest first. Only the newest installers are kept on the [Releases](../../releases/latest) page; these notes stay.

## 0.22.3 — 2026-11-26
- **Readable text on coloured buttons in every theme:** buttons and badges on the theme's accent (Update, Download, Restart and install, each window's main button), a person's colour or a context-bar segment now pick dark or light text to match, in the theme's own colours. White on Zellij's yellow-green is gone.
- **Style picker:** three large cards in Settings › Appearance, each a miniature of its window, with a ring around the one in use.
- **Today** is a clear button at the top of Projects, with a summary of what's waiting ("2 waiting on you · 1 follow-up due") and a count; it turns amber when something needs you.

## 0.22.2 — 2026-11-26
- The release's software bill of materials now covers every platform: it lists the terminal module's native add-on for Windows and macOS too, not only Linux's.

## 0.22.1 — 2026-11-26
- Each release now includes its software bill of materials (`TerminallyLLM-<version>-sbom.cdx.json`), covered by the same signed build provenance as the installers.
- Build tooling: a known denial-of-service issue in a dependency of the installer builder is patched (it was never part of the app).

## 0.22.0 — 2026-11-26
- **Three styles** (Settings › Appearance › Style): **Workspace**, the new default (big labelled icons down the left, search in the title bar, every tool listed beside the one you opened), **Command deck** (terminal-native: your terminal's font, thin lines, a status bar, tools in a side panel) and **Refined** (the classic layout). Colours still come from your theme.
- The logo shows in the title bar again.
- The Library window no longer runs past the bottom of a short window.

## 0.21.7 — 2026-11-26
- New toolbar: **Palette, Tools, Glossary, Settings**, each with its name. Tools groups History, Changes, Context hygiene, RAM, Spend, Library and Alerts, with a dot when a repo has changes.
- **Interface size** (Settings › Appearance): Auto fits the window to the screen (smaller on a 1080p laptop, 100% on a large monitor), or pick a fixed size; Ctrl+Alt+= / − / 0 (Ctrl+Cmd on a Mac).

## 0.21.6 — 2026-11-25
- Releases page: one release per version, published only once every platform built and passed.

## 0.21.5 — 2026-11-25
- Squad store sync: each computer's last change is found by history, not by clock.

## 0.21.4 — 2026-11-25
- Security review: the approval broker lets through only plain reads (stricter parsing of curl, wget, httpie and `gh api`), checks a URL's real host before treating it as local, and resolves git and gh aliases. A PM's squad proposal shows its full prompt text before you save it.

## 0.21.3 — 2026-11-25
- Signed build provenance attached to every release; licence and security policy included.

## 0.21.2 — 2026-11-23
- Windows: the app's helper scripts in WSL install and update again (broken since 0.15.0).

## 0.21.1 — 2026-11-23
- Squad seats that went to sleep before their first message wake up working instead of failing to resume.
- Order drafts survive switching tabs; nothing switches tabs on its own.

## 0.21.0 — 2026-11-23
- Tabs reorder by drag and can be minimized (their sessions sleep); a tab with a permission waiting turns red.
- Squad workers say they need you only for a permission or a question, and are told when their next task can start.

## 0.20.0 — 2026-11-23
- Squads and projects: knowledge scoped to a project, named instances, pinning an instance to a project, the order card, and a PM that can propose a new squad.

## 0.19.0 — 2026-11-23
- Old Workforce names removed (renamed Squads in 0.16); hardened Electron settings.

## 0.18.0 – 0.18.1 — 2026-11-22
- macOS builds are signed and notarized, and update from inside the app.
- + Project next to + Claude, + Squad and + Shell.

## 0.17.0 — 2026-11-22
- The app no longer shows web pages itself: artifacts, pages and links open in your default browser. The app page loads from its own protected scheme.

## 0.16.0 – 0.16.1 — 2026-11-22
- Workforces are now **Squads**; a glossary of every term in the app; resizable project panel.

## 0.15.0 – 0.15.6 — 2026-11-21 to 2026-11-22
- **Projects:** a PM per project that keeps its memory, a board of open loops, Today and the sweep, open PRs with triage and nudges, weekly updates and a daily brief.
- **Approval broker:** outward actions from sessions are held for your OK in the app.
- **Resources:** memory per session; idle sessions sleep and wake where they left off.
- Feature usage view (counted on this computer only); a security review of the whole app.

## 0.14.0 – 0.14.4 — 2026-11-17 to 2026-11-18
- Squad roles with playbooks, a lead that interviews you, a researcher, and a steward that keeps the knowledge base healthy.
- Saved teams run as several instances sharing one knowledge base; a Needs-you strip for seats waiting on you.
- Terminals no longer flash white or go blank when switching tabs.

## 0.13.0 — 2026-11-17
- The team learns: the lead curates the knowledge base when an order is archived.

## 0.12.0 — 2026-11-16
- A knowledge base per team, used by every seat.

## 0.11.0 — 2026-11-16
- A notebook per team and a report card per order.

## 0.10.0 — 2026-11-16
- Orders you archive and reopen; teams versioned in a local store you can back up to GitHub.

## 0.9.0 – 0.9.3 — 2026-11-10
- Workforces v2: an ops panel and command center, team map, plan board, outputs viewer; Mac fixes.

## 0.8.0 — 2026-11-10
- **Workforces:** a team of Claude sessions in a tab of its own, with a lead, roles and a shared task list.

## 0.7.0 – 0.7.5 — 2026-10-20 to 2026-10-30
- Tabs (F1–F8) and tabs in their own windows; a bigger tab bar.
- Fork a session, optionally into its own git worktree.
- Links Claude or its tools open follow your browser setting; copying from Claude's output works again.

## 0.6.0 – 0.6.4 — 2026-10-14 to 2026-10-19
- Changes: who changed what, with diffs. Comments on local pages.
- Option/Alt+arrows move by word; Ctrl+V / Ctrl+C paste and copy on Windows and Linux; links open in your default browser.

## 0.5.0 – 0.5.4 — 2026-10-13
- Library of skills, agents and MCP servers; live subagents; notes shared with Claude; distribute panes evenly.

## 0.4.0 – 0.4.1 — 2026-10-12
- New logo and title bar; a Markdown note per session.

## 0.3.0 – 0.3.6 — 2026-10-11 to 2026-10-12
- First release: multiplexer, context gauge, skills timeline, spend, plugins, resume after restart.
- Needs-you queue and permission banner, session history, paste images, rebindable shortcuts, themes.
