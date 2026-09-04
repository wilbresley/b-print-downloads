# Quick manual and commands

[Português (Brasil)](USAGE.md)

Short **b-print 1.0.1** manual for Windows. Full Help lives inside the app
(tray → **Help…**). This English page is informational.

---

## After installation

b-print stays in the Windows tray (near the clock; on Windows 11 it may be
behind the **^** arrow).

| Action | Result |
|--------|--------|
| Left-click the icon | Region capture |
| Right-click the icon | Full menu |
| Print Screen | Capture with b-print (can be returned to Windows) |
| Windows+Shift+S | Capture with b-print (can be returned to Windows) |
| Windows+Shift+D | Default extra shortcut (configurable) |
| Esc | Closes a menu/item first; then cancels capture |

Right-click menu: region, timer, all monitors, window under the cursor,
recents, canvas, pin, Settings, Help, and Exit.

Exiting the app always returns Print Screen and Windows+Shift+S to Windows.

---

## Capture

- Drag a rectangle, or click an entire monitor.
- A hint appears at the bottom of the monitor where the mouse is.
- **Left + right** while dragging: current monitor edges become barriers.
  Release the right button to cross monitors.
- **Alt**: 5 px grid only for the area or item being moved.
- With **Rotate** active, the Alt grid is hidden; use **Shift + wheel** for
  5° steps.

Save (`Ctrl+S`) opens the scale menu. Copy (`Ctrl+C`) is immediate.

---

## Settings

Open with a right-click on the tray → **Settings…**.

- **Save** applies changes and **does not close** the window. Use X (or Esc)
  to close.
- After saving, **Settings saved** appears for about one second.
- **Language** (Portuguese / English) takes effect only after Save. The app
  restarts in the tray after 3 seconds. An open capture, editor, or pinned
  image postpones the restart.
- **Fixed shortcuts**: Print Screen and Windows+Shift+S start enabled. Clear
  one to return it to Windows immediately.
- **Extra shortcut**: combinations with Windows, Ctrl, Alt, or Shift, or
  F1–F24 alone. Esc, Print Screen, and Windows+Shift+S are reserved.
- **Uninstall b-print**: asks for confirmation. Close any capture, editor, or
  pin first. Captures in other folders remain.

---

## Text and date/time

On the **Text** button:

- **Text…** opens typing.
- **Date and time** inserts the stamp in the saved format.
- The **clock** opens the format editor. Brazil 24h / US 12h / ISO 24h
  presets change only order and clock; code names stay in the interface
  language. **Save** also inserts the stamp.

---

## Silent installation

```powershell
.\b-print-1.0.1-windows-x64.exe /S /LANG=en
```

With options:

```powershell
.\b-print-1.0.1-windows-x64.exe /S `
  /LANG=en `
  /DIR="$env:LOCALAPPDATA\Programs\b-print" `
  /AUTOSTART=0 `
  /DESKTOP=1 `
  /LAUNCH=0
```

| Option | Purpose |
|--------|---------|
| `/S` | No UI |
| `/LANG=pt-BR\|en` | Installer and first-run language |
| `/DIR=` | Installation folder |
| `/AUTOSTART=0\|1` | Start with Windows |
| `/DESKTOP=0\|1` | Desktop shortcut |
| `/LAUNCH=0\|1` | Launch after install |

---

## Silent uninstall

From the installer:

```powershell
.\b-print-1.0.1-windows-x64.exe /uninstall /S
```

From the installed copy:

```powershell
& "$env:LOCALAPPDATA\Programs\b-print\b-print-desinstalador.exe" --uninstall /S
```

---

## Application commands

```powershell
$app = "$env:LOCALAPPDATA\Programs\b-print\b-print.exe"

& $app --tray
& $app --region
& $app --active-screen
& $app --screen 0
& $app --all-screens
& $app --window-under-cursor
```

Configuration:

```powershell
& $app --configure --desktop-shortcut --autostart
& $app --configure --no-desktop-shortcut --no-autostart
& $app --configure-defaults
& $app --set-save-dir "D:\Captures"
& $app --set-copy-dir "D:\Captures\copies"
& $app --factory-reset
& $app --help
& $app --version
```

---

## Verify SHA-256

```powershell
Get-FileHash .\b-print-1.0.1-windows-x64.exe -Algorithm SHA256
```

Compare with [SHA256SUMS.txt](https://github.com/wilbresley/b-print-downloads/releases/download/v1.0.1/SHA256SUMS.txt)
from the same Release.

---

## If something goes wrong

Installer: `b-print-installer-error.log` next to the exe, with a button to
open that folder.

Application:

```text
%LOCALAPPDATA%\Programs\b-print\data\logs
%LOCALAPPDATA%\Programs\b-print\data\memory-stat.txt
```

[Issues](https://github.com/wilbresley/b-print-downloads/issues) ·
**b-print@bresley.win**
