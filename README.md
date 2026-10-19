<p align="center">
  <img src="assets/ctrl-browser-logo.png" alt="CTRL Browser" width="320">
</p>

<h1 align="center">CTRL Browser</h1>

<p align="center">
  A local-first, privacy-focused desktop browser for Windows.<br>
  Your bookmarks, history, notes, search index and settings stay on your own computer.
</p>

<p align="center">
  <a href="https://github.com/shahil5z/ctrl-browser-releases/releases/latest"><img src="https://img.shields.io/github/v/release/shahil5z/ctrl-browser-releases" alt="Latest release"></a>
  <a href="https://github.com/shahil5z/ctrl-browser-releases/releases/latest"><img src="https://img.shields.io/github/release-date/shahil5z/ctrl-browser-releases" alt="Release date"></a>
  <a href="https://github.com/shahil5z/ctrl-browser-releases/releases/latest"><img src="https://img.shields.io/badge/platform-Windows%2010%2B%20x64-0078D4" alt="Platform"></a>
  <a href="https://ctrl-browser.vercel.app"><img src="https://img.shields.io/badge/website-ctrl--browser.vercel.app-111111" alt="Website"></a>
</p>

<p align="center">
  <b><a href="https://github.com/shahil5z/ctrl-browser-releases/releases/latest/download/CTRLBrowser-setup.exe">Download for Windows</a></b>
  &nbsp;|&nbsp;
  <a href="https://github.com/shahil5z/ctrl-browser-releases/releases">All releases</a>
  &nbsp;|&nbsp;
  <a href="https://ctrl-browser.vercel.app">Website</a>
</p>

---

## About this repository

This repository contains the official Windows builds of CTRL Browser: the installer, release notes and checksums.

The source code lives in a separate private repository and is not included here.

## Download

| File | What it is |
|---|---|
| `CTRLBrowser-setup.exe` | Installer (recommended). Installs for the current user only. |
| `CTRL.Browser-win32-x64-[version].zip` | Portable version. Extract the folder and run `CTRL Browser.exe`. |
| `updates.json` | Version and SHA-256 checksum of the installer. CTRL Browser reads this when you check for updates. |

Both files are attached to every release on the [Releases](https://github.com/shahil5z/ctrl-browser-releases/releases) page, along with their SHA-256 checksums.

## Installation

1. Download `CTRLBrowser-setup.exe` from the [latest release](https://github.com/shahil5z/ctrl-browser-releases/releases/latest).
2. Run the installer. You do not need administrator rights.
3. Open CTRL Browser from the Start menu.

**Requirements:** Windows 10 or later, 64-bit.

**About the SmartScreen warning:** the current builds are not code-signed yet, so Windows SmartScreen may warn you the first time you run the installer. Check the file hash (see below), then click "More info" and "Run anyway".

## Checking your download

Run this in PowerShell and compare the result with the SHA-256 value in the release notes:

```powershell
Get-FileHash .\CTRLBrowser-setup.exe -Algorithm SHA256
```

The installer checksum for 0.1.11 is `EBCE885185875C04602D8D0D6A27A5A33DD3447EE7CC5D7A91863B39A135BDED`.

## Updates

[updates.json](https://github.com/shahil5z/ctrl-browser-releases/releases/latest/download/updates.json) is published with every release. Check for updates in CTRL Browser reads that file, then downloads `CTRLBrowser-setup.exe` only when the checksum matches.

## Features

**Tabs and workspaces**
- Tab groups with names and colours, workspaces, vertical tabs
- Pinned tabs, tab hibernation, split view, session restore

**Local-first tools**
- Search index stored on your device, covering your bookmarks, history and pages you choose to index
- Notes linked to pages, Reader Mode, command palette
- Bookmarks with folders, browsing history, download manager

**Appearance**
- Custom New Tab page with wallpaper, skins, clock, weather and shortcut styles
- Light, dark and system themes, accent colours and per-tab colours

## Privacy

- Tracker blocking using a local rule list, with a per-site counter
- Unknown third-party cookies are blocked
- Site permissions can be set to Ask, Allow or Deny for each site
- USB, Bluetooth, Serial and sensor APIs are turned off
- Fingerprint surfaces are standardized, not randomized
- Optional DNS-over-HTTPS
- Private tabs are kept in memory only and are gone when closed
- No accounts, no cloud sync, no telemetry

Please note: private tabs and tracker blocking do not make you anonymous. CTRL Browser does not hide your IP address and is not a VPN or Tor replacement.

## Technology

| Area | Details |
|---|---|
| Runtime | Electron (Chromium and Node.js), Windows x64 |
| Language and UI | TypeScript, React |
| Storage | SQLite running in its own utility process, saved in the per-user profile folder |
| Security | Sandboxed renderer, context isolation, strict Content Security Policy, every IPC message validated at runtime with Zod |
| Testing | Vitest unit and integration tests, packaged smoke tests, type checking and linting before each release |
| Packaging | Electron Forge, Squirrel.Windows installer, release files published with checksums |

## Release notes

Every release lists what changed, which platform was tested, the test results for that build and the SHA-256 checksums of the attached files.
See the [Releases](https://github.com/shahil5z/ctrl-browser-releases/releases) page.

## Feedback

Found a bug or have an idea? Open an issue on [GitHub Issues](https://github.com/shahil5z/ctrl-browser-releases/issues).

## Author

Designed and developed by **Shohrab Haque Shahil**

[GitHub](https://github.com/shahil5z) | [LinkedIn](https://www.linkedin.com/in/shohrab-haque) | [Website](https://shahil-personal.vercel.app)

## License

CTRL Browser is proprietary software for personal use. See the [LICENSE](LICENSE) file for details.
