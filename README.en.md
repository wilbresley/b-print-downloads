# b-print

[Português (Brasil)](README.md)

A lightweight Windows screenshot tool with arrows, shapes, text, highlighting,
redaction, magnification, and an image editor.

## Download

Public downloads are temporarily unavailable while the first release is being
tested.

Internal test version: **1.0.0**

Planned installer name:

```text
b-print-1.0.0-windows-x64.exe
```

The installer is free, installs only for the current Windows user, and does not
require administrator privileges.

> The executable does not have a paid digital signature. Windows may therefore
> show an “Unknown publisher” or SmartScreen warning.

## Installation

When a public Release is authorized:

1. Download the installer from Releases.
2. Verify its SHA-256 against `SHA256SUMS.txt`.
3. Run the installer. It opens in Brazilian Portuguese by default; choose
   English on the first screen.
4. b-print will remain available in the system tray.

Default installation path:

```text
%LOCALAPPDATA%\Programs\b-print
```

## Quick use

- **Print Screen** and **Windows+Shift+S**: open b-print by default; each can
  be returned to Windows independently in Settings.
- **Windows+Shift+D**: configurable default secondary shortcut.
- **Left-click the tray icon**: capture a region.
- **Right-click the tray icon**: access all modes, Settings, Help, and Exit.
- **Esc**: closes menus or unconfirmed items first, then cancels capture.
- **Settings → Uninstall**: removes the app after confirmation; captures
  saved in other folders remain.

See [USAGE.en.md](USAGE.en.md) for the manual and command-line options.

## Privacy

b-print works locally. It does not upload screenshots, telemetry, or logs.
See [PRIVACY.en.md](PRIVACY.en.md).

## Development transparency

b-print is developed and maintained by **Wilian Bresley da Costa** with
assistance from **Cursor** and AI models for implementation, review, and
documentation. Product decisions, testing, distribution, and responsibility
remain with the author.

The running application does not use AI and does not send screenshots or user
data to AI services. Cursor, Anysphere, and model providers do not sponsor,
endorse, or have any affiliation with b-print. Their trademarks belong to
their respective owners.

## Support logs

If the installer fails, it creates `b-print-installer-error.log` beside the
executable and offers an **Open log location** button.

If you encounter a problem, close b-print and collect:

```text
%LOCALAPPDATA%\Programs\b-print\data\logs
%LOCALAPPDATA%\Programs\b-print\data\memory-stat.txt
```

Open an [Issue](https://github.com/wilbresley/b-print-downloads/issues) and
include the approximate time of the problem. Review logs before sharing them,
as they may contain file and folder paths.

Private support, licensing, acquisition of rights, or business partnerships:
**b-print@bresley.win**

## License

b-print's own code is **proprietary freeware**; it is not open source. See
[TERMS.en.md](TERMS.en.md). This English translation is informational. The
Brazilian Portuguese terms control if the versions differ.

Third-party libraries and resources remain under their own licenses. Each
Release includes `LICENSES.zip`, the four corresponding Qt 6.8.2 source
archives, and SBOM documents.

Copyright © 2026 Wilian Bresley da Costa.
