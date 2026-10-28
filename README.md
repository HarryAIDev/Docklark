<p align="center"><strong>English</strong> · <a href="README.zh-CN.md">简体中文</a></p>
<p align="center"><a href="https://docklark.com/"><img src="assets/docklark-mark.svg" width="80" height="80" alt="Docklark logo"></a></p>
<h1 align="center">Docklark — SSH & operations workspace for Mac</h1>
<p align="center">Connections, terminals, files and host tools in one native workspace.<br>Built for Apple Silicon. Completely free, with no purchase or subscription.</p>
<p align="center"><a href="https://github.com/HarryAIDev/Docklark/releases/latest"><strong>Download for Mac</strong></a> · <a href="https://docklark.com/features/">All features</a> · <a href="https://docklark.com/docs/">Documentation</a> · <a href="https://docklark.com/roadmap/">Development progress</a></p>

<p align="center"><picture><source media="(prefers-color-scheme: dark)" srcset="https://docklark.com/assets/product/native-en-workspace-dark.webp"><img src="https://docklark.com/assets/product/native-en-workspace-light.webp" width="100%" alt="Docklark operations workspace: terminal, connections, remote files and resource history"></picture></p>

Docklark grew out of moving from Windows to macOS and wanting the organized remote-work experience Harry enjoyed in Xshell. It brings saved connections, flexible sessions, file transfers and routine host operations into one Mac application.

> The website's October 27, 2026 review covers the installed v0.2.96 app (build 106). Screenshots are actual English/Chinese, light/dark app captures using public demo data, not production sessions. Interface review and a local sample upload do not certify every authentication method, remote write, container action, forwarding rule or server environment. The [feature page](https://docklark.com/features/#review-scope) explains the review scope; the roadmap records development history, not an installer acceptance checklist.

## What you can do

### Organize connections and return to your workspace

- **Connection library:** nested folders with inherited colors, search, favorites, duplication, batch moves and property editing, plus non-sensitive connection templates.
- **SSH access:** password or private-key authentication, JumpServer entry, managed SSH jump chains, keep-alive, compression and forwarding options. Passwords use macOS Keychain; host fingerprints and authentication prompts still need confirmation.
- **Flexible sessions:** tabs, resizable nested splits and multiple windows. Move connected sessions between panes and windows, switch terminal/operations layouts, and dock favorites or quick commands to any edge.
- **Saved workspaces:** save named multi-window layouts and restore them after restart as pending sessions, then connect manually. Snapshots exclude terminal output, drafts and passwords.
- **Portable configuration:** Docklark JSON import/export and local SSH-key management. Ordinary exports omit passwords; optional passphrase-protected backups can include saved passwords, but not private-key contents or one-time codes. This is not cloud sync or Xshell-format import.

### Work with commands and terminal output

- **Shared command bar:** choose the active session or explicit SSH recipients, review their window origins and availability, then send. Enter sends; Shift+Enter adds a line. Local shells are excluded from whole-window SSH scopes.
- **Quick commands:** groups, ordering, `{{name}}` parameters and drag-to-terminal actions. Reuse this app run's history with Ctrl+R; Tab fills command or confirmed remote-path candidates without executing them. Marked dangerous commands ask for confirmation.
- **Terminal find:** search the current tab or the window's tabs and split panes, with regex, case matching and wrap-around navigation. Switch between inline and detached find without losing search state.
- **Persistent highlights and output alerts:** ordered text/regex rules, foreground/background previews and global, connection or session scopes. Optional notifications show session/rule names rather than matched terminal text; alerts do not execute commands.
- **Shell integration:** navigate command prompts, select the latest command output and inspect exit codes, with configurable key behavior and scrollback. Remote Bash/Zsh integration requires setup; it does not infer a changed target host.
- **Local-shell continuity:** keep the tab and retained output when SSH ends, then continue in a local shell.

Search covers retained output, not unlimited history. Review command recipients before sending: multi-session delivery is not an atomic server transaction. Explicit sensitive snippets use Keychain and send to one terminal only, without Return or broadcast.

### Transfer files and edit remote text

<p align="center"><picture><source media="(prefers-color-scheme: dark)" srcset="https://docklark.com/assets/product/native-en-sftp-dark.webp"><img src="https://docklark.com/assets/product/native-en-sftp-light.webp" width="100%" alt="Docklark native dual-pane SFTP window and transfer queue with demo files"></picture></p>

- **Embedded or separate SFTP:** local/remote browsing, file and directory transfers, hidden files and empty folders, rename, new folders and path copying.
- **Transfer queue:** 1–5 concurrent files (3 by default), task cancellation, retry, reveal-file and result-copy actions. Overlapping paths run in order; conflicting names are saved under new names rather than overwritten or merged.
- **Shell directory following:** after shell integration and same-host confirmation, follow terminal directory changes in the file panel.
- **Remote text editor:** line numbers, find/replace, go-to-line, a diff before saving, remote-change conflict checks and supported encoding preservation. Text is limited to 2 MiB; servers without atomic replacement offer Save As. Unsaved drafts remain available read-only after disconnection.
- **Terminal `rz` / `sz`:** ZMODEM uploads/downloads with a separate progress window, where the target provides compatible tools and allows the protocol. Each file must be smaller than 4 GiB.

SFTP requires an allowed SFTP v3 subsystem. It does not follow symbolic links or device files, delete non-empty directories, or resume transfers across connections.

### Observe hosts and use the tool center

<p align="center"><picture><source media="(prefers-color-scheme: dark)" srcset="https://docklark.com/assets/product/native-en-tools-dark.webp"><img src="https://docklark.com/assets/product/native-en-tools-light.webp" width="100%" alt="Docklark tool center with a multi-host overview and session tools"></picture></p>

- **Resource monitoring:** CPU, memory, swap, network rates and disk space, Top 5 processes and 1/5/15-minute history charts. Linux/macOS collectors use an independent SSH command channel without a remote agent or sudo; macOS memory is an estimate. Refresh defaults to 5 seconds and can be paused or set from 1–3600 seconds.
- **Multi-host overview:** table/card views with shortcuts to the selected host's terminal, resources, files and tools.
- **Process management:** search and inspect remote processes, with confirmation before requesting termination.
- **Docker tools:** container status, images, ports, supported metrics, recent logs, start/stop/restart controls and separate container-terminal tabs, subject to the remote Docker environment and permissions.
- **Forwarding:** named local, remote and dynamic SOCKS rules that can start with a session or be controlled independently without disconnecting SSH.

**Know which host you are operating on.** SFTP, monitoring and host tools use the SSH entry host, or the final authenticated host of a managed jump chain. They do not follow nested `ssh` commands or assets selected from a JumpServer menu. Remote exec/SFTP/Docker permissions and workflow-specific validation still apply; real remote macOS metrics remain under validation.

### Repeat steps, keep records and customize the interface

- **Step workflows:** manually run or single-step commands, text/regex output waits, sensitive-input prompts and pauses, with step timeouts and confirmation for marked dangerous steps. Workflows bind to one session; disconnecting, reconnecting or starting a transfer stops them. They are not unattended schedulers or multi-server transactions.
- **Session output logs:** off by default; start, pause, resume or stop UTF-8 recording, add optional timestamps, then search/copy/export. A connection can opt into recording after authentication. Ordinary remote output may contain secrets: pause before sensitive work and review exports.
- **Diagnostics:** separate local INFO/DEBUG logs, changeable without restart and exportable for troubleshooting. These exclude terminal text, commands, passwords, private keys and file contents, and are not uploaded automatically. Review runtime metadata before sharing.
- **Appearance:** English and Simplified Chinese; system, light or dark interface; 13 terminal palettes, theme previews/search/favorites, JSON and `.itermcolors` import, JSON export, custom colors, global or per-session fonts and appearance. Background opacity and frosted glass are independently adjustable.

<p align="center"><picture><source media="(prefers-color-scheme: dark)" srcset="https://docklark.com/assets/product/native-en-themes-dark.webp"><img src="https://docklark.com/assets/product/native-en-themes-light.webp" width="100%" alt="Docklark native theme center with terminal palette previews"></picture></p>

## Download and get started

**[v0.2.96](https://github.com/HarryAIDev/Docklark/releases/tag/v0.2.96) · Published October 27, 2026 · Apple Silicon (arm64)**

[DMG installer](https://github.com/HarryAIDev/Docklark/releases/download/v0.2.96/Docklark_0.2.96_2026.10.27_arm64.dmg) · [SHA-256 checksum](https://github.com/HarryAIDev/Docklark/releases/download/v0.2.96/Docklark_0.2.96_2026.10.27_arm64.dmg.sha256) · [Latest release](https://github.com/HarryAIDev/Docklark/releases/latest)

1. Download the DMG and matching checksum into the same folder. In Terminal, change to that folder and verify:

   ```sh
   shasum -a 256 -c Docklark_0.2.96_2026.10.27_arm64.dmg.sha256
   ```

2. Open the DMG and copy Docklark into Applications following its installer layout. Keep macOS security protections enabled.
3. Prepare an authorized SSH account and confirm the host-key fingerprint through a trusted channel.
4. Add a connection and begin with one session before trying multi-session commands or management actions.

The developer reports testing on **macOS 27**; earlier versions have not been tested. This release provides no Intel installer. Developer ID signing and notarization have not been independently verified; a matching checksum verifies file integrity, not publisher identity. See the [download and installation guide](https://docklark.com/download/) for current information.

## Documentation and project status

- [Getting started and settings](https://docklark.com/docs/) · [SSH connection guide](https://docklark.com/docs/ssh/) · [JumpServer guide](https://docklark.com/docs/jumpserver/)
- [Complete features and workflow limits](https://docklark.com/features/) · [Daily feature progress](https://docklark.com/roadmap/)
- [SSH client for Mac](https://docklark.com/ssh-client-for-mac/) · [SFTP client for Mac](https://docklark.com/sftp-client-for-mac/) · [Practical articles](https://docklark.com/blog/) · [About Docklark](https://docklark.com/about/)

Docklark is in active early development, with frequent updates initially and stage-based releases as it matures. Use the official website for detailed guidance and Releases for available installers.

**This is the public release, documentation and feedback repository, not the application source repository.** GitHub's automatically generated source archives contain this repository's documentation and assets, not the application source code.

## Feedback

[Open an issue](https://github.com/HarryAIDev/Docklark/issues) or contact [Harry on X](https://x.com/HarryAIDev). Include the app version, macOS version, reproduction steps and expected result. Remove passwords, private keys, tokens, sensitive host details and personal file paths from screenshots and logs.

Docklark is an independent project. Xshell is a trademark of NetSarang Computer, Inc.; Docklark is not affiliated with, sponsored by or endorsed by NetSarang.

<p align="center">Built by Harry for everyday remote work.<br><a href="https://docklark.com/">docklark.com</a></p>
