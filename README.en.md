# b-print

[Português (Brasil)](README.md)

**Screenshot tool for Windows**, with immediate annotations: arrows, shapes,
text, highlighter, redaction, magnifier, and an image editor.

Current version: **1.0.1** (4 September 2026)

The app lives in the system tray, installs only for the current user, and
does not ask for administrator privileges.

---

## Download

| File | Contents |
|------|----------|
| [b-print-1.0.1-windows-x64.exe](https://github.com/wilbresley/b-print-downloads/releases/download/v1.0.1/b-print-1.0.1-windows-x64.exe) | Windows 64-bit installer |
| [SHA256SUMS.txt](https://github.com/wilbresley/b-print-downloads/releases/download/v1.0.1/SHA256SUMS.txt) | SHA-256 checksums |
| [LICENSES.zip](https://github.com/wilbresley/b-print-downloads/releases/download/v1.0.1/LICENSES.zip) | Terms, LGPL/Qt, SBOMs, and attributions |
| [Releases](https://github.com/wilbresley/b-print-downloads/releases/tag/v1.0.1) | Full release page, including Qt 6.8.2 sources |

The installer is **free**.

> The executable **does not have a paid digital signature**. Windows may show
> “Unknown publisher” or a SmartScreen warning. That is expected. Verify the
> SHA-256 in `SHA256SUMS.txt` before running it.

This English page is informational. Brazilian Portuguese terms control if the
versions differ.

---

## Installation

1. Download `b-print-1.0.1-windows-x64.exe`.
2. Verify the SHA-256 against the matching Release file.
3. Run the installer. It opens in **Brazilian Portuguese** by default;
   choose **English** on the first screen.
4. b-print stays in the system tray, near the clock.

Default folder:

```text
%LOCALAPPDATA%\Programs\b-print
```

Silent install, uninstall, and command line: [USAGE.en.md](USAGE.en.md)

---

## Quick use

- **Print Screen** and **Windows+Shift+S** open b-print by default. Each can
  be returned to Windows under Settings → Capture.
- **Windows+Shift+D** is the extra shortcut (configurable; F1–F24 also work).
- **Left-click** the tray icon: capture a region.
- **Right-click**: all modes, Settings, Help, and Exit.
- **Esc** closes menus and unconfirmed items first, then cancels capture.
- **Alt** shows a 5 px grid for the active gesture only.
- Left + right buttons while dragging lock the area to the current monitor
  edges.
- **Settings → Uninstall** removes the program after confirmation. Captures
  saved elsewhere remain.

The full Help manual is included in the application.

---

## What is included

- Region, monitor, all-monitors, window-under-cursor, and timer capture
- Annotations: arrows, shapes, text, date/time stamp, highlighter, pencil,
  and redaction
- Full-screen magnifier and a windowed editor with zoom
- Dark and Light themes, Portuguese (Brazil) / English
- Immediate clipboard copy and save as PNG, JPEG, or WebP
- Recents, solid canvas, and always-on-top pinned images

---

## Privacy

b-print works **only on this computer**. It does not send screenshots,
telemetry, or logs to a server. It does not use AI at runtime.

Details: [PRIVACY.en.md](PRIVACY.en.md)

---

## Development transparency

b-print is developed and maintained by **Wilian Bresley da Costa** with
assistance from **Cursor** and AI models for implementation, review, and
documentation. Product decisions, testing, distribution, and responsibility
remain with the author.

Cursor, Anysphere, and model providers do not sponsor, endorse, or have any
affiliation with b-print.

---

## Support logs

If the installer fails, it writes `b-print-installer-error.log` beside the
executable and offers **Open log location**.

If the app itself misbehaves, close b-print and copy:

```text
%LOCALAPPDATA%\Programs\b-print\data\logs
%LOCALAPPDATA%\Programs\b-print\data\memory-stat.txt
```

Open an [Issue](https://github.com/wilbresley/b-print-downloads/issues) and
include the approximate time. Review the files first; they may contain paths.

Private support, licensing, or partnership: **b-print@bresley.win**

---

## License

b-print’s own code is **proprietary freeware**. It is not open source. See
[TERMS.en.md](TERMS.en.md). The Brazilian Portuguese terms control.

Qt and other third-party libraries remain under their original licenses. Each
Release includes `LICENSES.zip` and the four corresponding Qt 6.8.2 source
archives.

Copyright © 2026 Wilian Bresley da Costa.
