# CTRL Browser releases

Compiled Windows builds of CTRL Browser. This repository does not contain the application source.

CTRL Browser is a local-first desktop browser. Bookmarks, history, notes, and preferences stay on the device. There is no account and no cloud sync.

## Supported platform

| Item | Value |
| --- | --- |
| Version | 0.1.0 |
| Platform | Windows 10 or later, 64-bit |
| Installer | `CTRLBrowser-setup.exe` |
| Full application archive | `CTRL Browser-win32-x64-0.1.0.zip` |
| Signature | Not Authenticode signed |

Windows SmartScreen can warn before an unsigned installer runs. That warning is expected for this build.

## Download

Latest installer:

[CTRLBrowser-setup.exe](https://github.com/shahil5z/ctrl-browser-releases/releases/latest/download/CTRLBrowser-setup.exe)

All versions are listed on the [releases page](https://github.com/shahil5z/ctrl-browser-releases/releases).

SHA-256 for the 0.1.0 files:

```
7164AB4303BC7787D53D55DC3A8D220CE15D15D35F8E454140D23D88DDCB955E  CTRLBrowser-setup.exe
C251354574DF18B831740E52BDF74B03E2F379AF8C14E122E687852081B1249E  CTRL Browser-win32-x64-0.1.0.zip
```

## Install

1. Download `CTRLBrowser-setup.exe`.
2. Run it. The installer is per-user and does not ask for administrator rights.
3. Open CTRL Browser from the Start menu.

The zip is the full packaged application folder, not a single-file portable program. Extract the whole archive and run `CTRL Browser.exe` from inside that folder. Copying only the executable will not start the browser.

## First launch

The browser opens on its New Tab page. You can type an address or a search. Settings, bookmarks, history, and downloads are stored in the Windows profile for this app. Uninstalling the program does not delete that profile.

## Release history

| Version | Date | Notes |
| --- | --- | --- |
| [0.1.0](https://github.com/shahil5z/ctrl-browser-releases/releases/tag/v0.1.0) | 2026-10-15 | First public Windows x64 build. Unsigned. |

## Limitations

- This build is not code-signed.
- Install, upgrade, and uninstall were not tested on a clean Windows machine.
- Automated tests are not all green. The 15 October 2026 run was 1016 passed, 10 failed, 7 skipped.
- There is no automatic update feed in this public repository.
- Private browsing is not anonymity. Custom DNS does not hide your IP address.

## Security

The installer and zip were produced with Electron Forge on Windows x64. Authenticode status of `CTRLBrowser-setup.exe` was `NotSigned`. No certificate is included in this repository.

Report a problem by opening an issue on this repository. Do not send passwords, browsing history, or profile databases.

## License

No license has been selected for the source code. These files are published builds only.
