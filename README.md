<p align="center">
  <strong>English</strong> · <a href="README.zh-CN.md">简体中文</a>
</p>

<p align="center">
  <a href="https://docklark.com/">
    <img src="assets/docklark-mark.svg" width="88" height="88" alt="Docklark logo">
  </a>
</p>

<h1 align="center">Docklark</h1>

<h3 align="center">Connect far. Stay focused.</h3>

<p align="center">
  A native SSH workspace for Apple Silicon Mac.<br>
  Your servers, sessions, and files, together in one calm place.
</p>

<p align="center">
  <a href="https://docklark.com/download/"><img src="https://img.shields.io/badge/macOS-Apple%20Silicon-20312a?style=flat-square&amp;logo=apple&amp;logoColor=white" alt="Target platform: macOS on Apple Silicon"></a>
  <a href="https://docklark.com/features/"><img src="https://img.shields.io/badge/SSH-%2B%20JumpServer-52723a?style=flat-square" alt="SSH and JumpServer"></a>
  <a href="https://github.com/HarryAIDev/Docklark/releases"><img src="https://img.shields.io/badge/status-in%20development-b78b35?style=flat-square" alt="In development; no public release yet"></a>
</p>

<p align="center">
  <a href="https://docklark.com/"><strong>Website</strong></a> ·
  <a href="https://docklark.com/docs/"><strong>Documentation</strong></a> ·
  <a href="https://github.com/HarryAIDev/Docklark/releases"><strong>Releases</strong></a> ·
  <a href="https://github.com/HarryAIDev/Docklark/issues"><strong>Feedback</strong></a>
</p>

<p align="center">
  <a href="#inside-docklark">Features</a> ·
  <a href="#download--installation">Download &amp; installation</a> ·
  <a href="#getting-ready">Getting ready</a>
</p>

<br>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/en-workspace-dark.webp">
    <source media="(prefers-color-scheme: light)" srcset="assets/en-workspace-light.webp">
    <img src="assets/en-workspace-light.webp" alt="Docklark workspace preview reconstructed with fictional hosts, sessions, and terminal output" width="100%">
  </picture>
</p>

<p align="center">
  <sub>Development preview · Reconstructed with fictional demo data.<br>Light shows a sample terminal; dark shows Quick Start. This is not a completed-session or performance test.</sub>
</p>

## Inside Docklark

Keep remote work close at hand, from a saved connection to the command you run next. The capabilities below are in development builds; complete workflows are still undergoing real-world validation.

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>⌘ &nbsp; Connections, organized</h3>
      <p>Direct SSH and JumpServer access, with saved hosts, nested folders, favorites, and search.</p>
    </td>
    <td width="50%" valign="top">
      <h3>▥ &nbsp; Space for every session</h3>
      <p>Tabs, nested splits, and separate windows keep related tasks together without losing your place.</p>
    </td>
  </tr>
  <tr>
    <td valign="top">
      <h3>⇄ &nbsp; Files beside your terminal</h3>
      <p>A dual-pane SFTP browser for local and remote folders, with a transfer queue, progress, and cancellation.</p>
    </td>
    <td valign="top">
      <h3>›_ &nbsp; Commands within reach</h3>
      <p>Save reusable commands and choose the active session or selected sessions from a shared command bar.</p>
    </td>
  </tr>
  <tr>
    <td valign="top">
      <h3>◉ &nbsp; Context at a glance</h3>
      <p>CPU and memory for the SSH entry host, plus search across retained terminal output.</p>
    </td>
    <td valign="top">
      <h3>◐ &nbsp; Make it feel like home</h3>
      <p>Light and dark appearances, terminal palettes, and English and Simplified Chinese interfaces.</p>
    </td>
  </tr>
</table>

SFTP and host monitoring address the SSH entry host; they do not follow a nested SSH connection or a selected JumpServer asset. See the [feature overview](https://docklark.com/features/) for details and boundaries.

## Download & installation

**The first public release is still being prepared. No public installer is available yet.**

- **Target platform:** macOS on Apple Silicon
- **System requirements:** the minimum macOS version will be confirmed with the public release; Intel support has not been announced
- **Release information:** check [GitHub Releases](https://github.com/HarryAIDev/Docklark/releases) and the [official release-status page](https://docklark.com/download/) for availability and installation instructions

## Getting ready

While the first release is being prepared, explore the connection guides:

1. [Prepare a direct SSH connection](https://docklark.com/docs/ssh/): host, port, account, network access, and host-key checks.
2. [Connect through JumpServer](https://docklark.com/docs/jumpserver/): the bastion entry point, authentication requirements, and authorized assets.
3. [Follow the roadmap](https://docklark.com/roadmap/): development progress and what still needs validation.

## Feedback

Found a rough edge or have an idea? [Open an issue](https://github.com/HarryAIDev/Docklark/issues) or reach [Harry on X](https://x.com/HarryAIDev).

For bug reports, include the app version, macOS version, reproduction steps, and the expected result. Remove passwords, private keys, tokens, and sensitive host details from screenshots and logs before sharing.

---

<p align="center">
  Built by <a href="https://x.com/HarryAIDev">Harry</a>, for everyday remote work.<br>
  <sub>This repository is Docklark's public home for releases, documentation, and feedback. Application source code is not published here.</sub>
</p>
